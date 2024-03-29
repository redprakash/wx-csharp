# How to Mock Azure Service Bus for Integration Testing
- Mocking the SB to send the message to local list instead of real SB in azure
## Step 1 => Overriding the methods to send messages to list
```
public class ServiceBusSenderMock : ServiceBusSender
{
    public List<ServiceBusMessage> PublishedMessages = new();
    private readonly Dictionary<ServiceBusMessageBatch, List<ServiceBusMessage>> _batchToMessagesMapping = new();

    public override Task SendMessagesAsync(
        ServiceBusMessageBatch messageBatch,
        CancellationToken cancellationToken = default)
    {
        PublishedMessages.AddRange(_batchToMessagesMapping[messageBatch]);
        return Task.CompletedTask;
    }

    public override ValueTask<ServiceBusMessageBatch> CreateMessageBatchAsync(
        CancellationToken cancellationToken = default)
    {
        var batchMessages = new List<ServiceBusMessage>();
        var batch = ServiceBusModelFactory.ServiceBusMessageBatch(1000, batchMessages);
        _batchToMessagesMapping.Add(batch, batchMessages);
        return ValueTask.FromResult(batch);

    }
    public override ValueTask DisposeAsync()
    {
        return ValueTask.CompletedTask;
    }

    public void Reset()
    {
        PublishedMessages.Clear();
        _batchToMessagesMapping.Clear();
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
             _serviceBusSenderMock.Reset();
        }
    }

```
### Now can use the _serviceBusSenderMock to mock 
