# Background tasks with hosted services in ASP.NET Core
    In ASP.NET Core, background tasks can be implemented as hosted services. A hosted service is a class with background task 
    logic that implements the IHostedService interface
- https://docs.microsoft.com/en-us/aspnet/core/fundamentals/host/hosted-services?view=aspnetcore-6.0&tabs=visual-studio
- https://www.youtube.com/watch?v=iaRaYmNz2so

# What problem do background tasks solve?
![image](https://user-images.githubusercontent.com/11143215/176367934-9ec5e0ec-b0c8-4745-a3d3-580a68f96bdb.png)
- Perform some CPU intensive work asynchronously
- Eventual consistency

# Options for Background Tasks
- IHostedService
- BackgroundService
- WorkerService

# What is an IHostedService?
- lets you host a background job inside an ASP.NET Core App
- Interface with StartAsync and StopAsync
- Register via dependency injection and services.AddHostedSerive<T>
