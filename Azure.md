## Azure
#### Course Reference
- https://www.youtube.com/watch?v=7n38Tha5JIE

#### Azure resources and Azure Resource Manager
### Resource
    A manageable item that's available through Azure. Virtual machines (VMs), storage accounts, web apps, 
    databases, and virtual networks are examples of resources.
### Resource group
    A container that holds related resources for an Azure solution. The resource group includes resources 
    that you want to manage as a group. You decide which resources belong in a resource group based on what
    makes the most sense for your organization
    
    Resource groups are a fundamental element of the Azure platform. A resource group is a logical container for 
    resources deployed on Azure. These resources are  anything you create in an Azure subscription like VMs, Azure Application 
    Gateway instances, and Azure Cosmos DB instances. All resources must be in a resource group, and a resource can only be a member 
    of a single resource group. Many resources can be moved between resource groups with some services having specific limitations or 
    requirements to move. Resource groups can't be nested. Before any resource can be provisioned, you need a 
    resource group for it to be placed in.

## 5 Different Messaging Services
1. Service Bus
2. Event Hub
3. Event Grid
4. Relay Service
5. Storage Queue

## Service Bus Brokered Messaging Features
![image](https://user-images.githubusercontent.com/11143215/159606666-a2b1bb52-15a4-491d-bff8-c05b8aac4dfe.png)


## Receiving and Processing Messages
#### Multi-threaded Message Receiving
1.Receive and Delete
  - Message received and deleted in one operation
  - No option to abandon, defer, or dead-letter message
  - At most once delivery
      - No duplicate Processing
      - Possible message loss
2. Peak Lock
  - Two phase receive
  - Message can be abandoned, deferred or dead-lettered
  - Receiver is responsible for message completion
  - At least once delivery
      - No message loss
      - Possible message duplication

## Publish Subscribe Messaging
### Filter Types
![image](https://user-images.githubusercontent.com/11143215/160364789-9c472b6c-85fd-49fc-a5ae-328665b3177f.png)

### What is Azure Service Bus?
- https://www.youtube.com/watch?v=7n38Tha5JIE
- https://www.youtube.com/watch?v=fERL-FXDEAg

### Azure Service Bus Implementation Example
- https://www.youtube.com/watch?v=bmZQkMJErZM

### Azure Event Hub
- https://www.youtube.com/watch?v=HwZldR8KlKM

# Send Events to Event Hub
![image](https://user-images.githubusercontent.com/11143215/184755780-6f45721a-44ec-40fe-ab98-3e57222ae317.png)

# Read Events from Event Hub
![image](https://user-images.githubusercontent.com/11143215/184759445-11f139fe-da9b-46f4-a539-47fe0670d86e.png)


