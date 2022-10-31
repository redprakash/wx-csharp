# How to Mock Azure Service Bus for Integration Testing
- Mocking the SB to send the message to local list instead of real SB in azure
## Step 1 => Overriding the methods to send messages to list
```
public class ServiceBusSenderMock : ServiceBusSender
{
    public List<ServiceBusMessage> ServiceBusMessagesToPublish = new();
    public List<ServiceBusMessageBatch> ServiceBusMessageBatchesToPublish = new();
    public List<ServiceBusMessageBatch> CustomServiceBusMessageBatchesCreated = new();

    public override Task SendMessagesAsync(
        ServiceBusMessageBatch messageBatch,
        CancellationToken cancellationToken = default)
    {

        ServiceBusMessageBatchesToPublish.Add(messageBatch);
        return Task.CompletedTask;
    }

    public override ValueTask<ServiceBusMessageBatch> CreateMessageBatchAsync(
        CancellationToken cancellationToken = default)
    {
        var batchToReturn = ServiceBusModelFactory.ServiceBusMessageBatch(1000, ServiceBusMessagesToPublish);
        CustomServiceBusMessageBatchesCreated.Add(batchToReturn);
        return ValueTask.FromResult(batchToReturn);

    }
    public override ValueTask DisposeAsync()
    {
        return ValueTask.CompletedTask;
    }

}
```

## Step 2 => Call the service from the test file
```
 public class YourTestName :  IClassFixture<CustomWebApplicationFactory>
    {
      
        private readonly CustomWebApplicationFactory _factory;
        private readonly ServiceBusSenderMock _serviceBusSenderMock;
        public DomainEventIntegrationTests(CustomWebApplicationFactory factory)
        {
            _factory = factory;
            _serviceBusSenderMock = (ServiceBusSenderMock)factory.Services.GetService<ServiceBusSender>();
        }
    }

```
### Now can use the _serviceBusSenderMock to mock 
