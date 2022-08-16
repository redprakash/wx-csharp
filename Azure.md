## Azure
#### Course Reference
- https://app.pluralsight.com/library/courses/azure-service-bus-in-depth/table-of-contents

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


## Managing Artifact with Code
### Useful Classes
![image](https://user-images.githubusercontent.com/11143215/160317180-85fc1406-df17-4ccf-b96a-2b238d7fec4a.png)

### NamespaceManager Methods
![image](https://user-images.githubusercontent.com/11143215/160317046-f114be8f-949b-4e10-aefb-1cf1b3384dec.png)

### Creating Queues
![image](https://user-images.githubusercontent.com/11143215/160317333-964b1d74-a852-4a14-9f6f-00d896e5b5bf.png)

![image](https://user-images.githubusercontent.com/11143215/160317451-e86276c2-2473-40eb-ad98-b52494950c61.png)

### Creating Topics
![image](https://user-images.githubusercontent.com/11143215/160317529-403bca41-dae1-46a9-98ab-dce048d1adb9.png)

### Adding Subscriptions to Topics
![image](https://user-images.githubusercontent.com/11143215/160317591-d10680e8-fce2-45b6-8bc1-004e0f5a8fa9.png)

## Sending Messages
### Sending Messages Individual
![image](https://user-images.githubusercontent.com/11143215/160321051-6c565c88-b703-4b67-b9ec-7662bba34298.png)

### Sending Messages Batches
![image](https://user-images.githubusercontent.com/11143215/160321104-fa67b3a3-d7d4-4709-b18f-f7665b1d42ce.png)

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

### Creating Topics with Default Subscriptions
![image](https://user-images.githubusercontent.com/11143215/160364958-f070984f-496e-426d-bf38-461f9e5d441b.png)

### Creating Sql Filtered Subscriptions
![image](https://user-images.githubusercontent.com/11143215/160365181-3e2b86ac-3b83-4a6d-a65e-e2b778dd288a.png)

### Using Correlation Filters
![image](https://user-images.githubusercontent.com/11143215/160365715-298b88f9-ccbd-4aac-a72a-8c40bb714414.png)




### What is Azure Service Bus?
- https://www.youtube.com/watch?v=fERL-FXDEAg

### Azure Service Bus Implementation Example
- https://www.youtube.com/watch?v=bmZQkMJErZM

### Azure Event Hub
- https://www.youtube.com/watch?v=HwZldR8KlKM

# Send Events to Event Hub
![image](https://user-images.githubusercontent.com/11143215/184755780-6f45721a-44ec-40fe-ab98-3e57222ae317.png)

# Read Events from Event Hub
![image](https://user-images.githubusercontent.com/11143215/184759445-11f139fe-da9b-46f4-a539-47fe0670d86e.png)


