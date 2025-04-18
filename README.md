# `Sung Hwan` (Alex) Cho

Backend & Network Engineer with 3 + years of hands‑on experience designing scalable game servers, real‑time multiplayer networking, and cloud deployments on Azure & AWS. Proficient in C++, C#, .NET, Node.js, Redis, and CosmosDB, with a track record of cutting gameplay latency via snapshot synchronization, securing user data through token‑based throttling, and automating CI/CD pipelines with Docker. Proven collaborator and mentor—guided 70 + students in socket programming and leveraged Navy CERT experience to embed robust security into every layer of the stack. 

# Projects Portfolio

### 1. Real-Time Collaborative Networking Engine

#### Project Overview
This network-based engine is designed for real-time collaborative environments, facilitating real-time data exchange and maintaining synchronized states between clients and servers. It aims to handle data efficiently and reliably, optimized specifically for game development and real-time collaboration software.

#### Key Features

##### 1. Network Communication and Data Management
- Manages stable client-server connections using **TCP-based communication**.
- Efficiently manages and synchronizes user information and states (`UserPresence`).
- Real-time serialization and deserialization of data changes optimized for network transmission.

##### 2. Event-Driven Architecture
- Utilizes separate threads to manage event queues (`EventQueue`), preventing bottlenecks and optimizing performance.
- Ensures system scalability and stability through asynchronous processing.

##### 3. User State Synchronization
- Detects and broadcasts real-time state changes (e.g., user locations, selected objects) to all connected clients.
- Maintains consistent states among clients, enhancing reliability in collaborative environments.

##### 4. Server Management and Scalability
- Systematically manages server states (RUNNING, STOPPED, STOPPING) to support reliable server operations.
- Supports automatic server registration and deregistration, enabling smooth integration with external services.

##### 5. Azure Cloud Infrastructure Integration
- Securely manages sensitive information (e.g., Redis connection strings) using Azure Key Vault.
- Efficiently stores and manages server information using Redis, updating the server list in real-time.
- Builds stable and scalable server infrastructure using Azure Container Apps, maximizing stability in cloud environments.

#### Technology Stack
- **Languages and Libraries**: C++, WebSocket API, cpprestsdk, C#, Azure SDK, StackExchange.Redis
- **Communication Method**: TCP/IP Socket
- **Multithreading**: std::thread, std::mutex, std::condition_variable
- **Cloud Services**: Azure Key Vault, Azure Container Apps, Redis

#### Achievements and Improvements
- Implemented reliable data synchronization and real-time update functionalities.
- Completed high scalability and performance testing in multi-client environments.
- Enhanced code quality and maintainability through modularization and abstraction.

#### Code Structure Examples
```cpp
// UserPresence example
NetworkComponent::UserPresence userPresence(userId, position, currentScene);

// Event Queue usage example
eventQueue_.Push(eventData);
auto eventData = eventQueue_.Pop();

// Server state management
void Server::start(int port, NetworkComponent::ServerInfo serverInfo) {
    // Initialize and run the server
}

// Client state update
void Client::handleReceivedPresence(const std::vector<uint8_t>& data) {
    auto presence = networkInterface_.deserializeUserPresence(data);
    localStateManager_.updateUserPresence(presence);
}
```

#### Future Plans
- Improve accessibility over the internet by integrating NAT and cloud servers.
- Continuously integrate and expand Azure cloud infrastructure to maximize scalability.

This project aims for practical applications in areas such as game servers and real-time collaboration tools, with ongoing improvements and expansions planned for further sophistication.




  Download Project: [Here](https://drive.google.com/file/d/1J7VP7blzivIjM2nEyOoP4NlWd1M3grsv/view?usp=sharing)  
  Download Project Release: [Here](https://drive.google.com/file/d/1v0fi-vvKjAgF02VgeAjJTaMENRhg-O1l/view?usp=sharing)

  <img src="https://largna.github.io/Materials/Engine/Collaboration.gif" style="width:100%; max-width:1000px;" alt="Project Screenshot">


---

### 2. RIZZSIM2077

#### Project Overview
RizzSim2077 is an innovative dating simulation management game utilizing advanced Large Language Model (LLM) technologies. My primary responsibility involved designing and implementing the network and server infrastructure, ensuring efficient management of real-time user data, authentication, and token usage throttling through robust backend and cloud infrastructure.

#### Key Features

##### Scalable User Management System (UMS)
- Implemented user data management with Azure Cosmos DB for secure, reliable, and scalable data storage.
- Tracked token usage on a per-session and daily basis, enforcing limits and additional charges for exceeding usage.
- Enhanced secure access and efficient data synchronization between Cosmos DB and Redis cache.

##### Game Server with Real-Time Data Caching
- Developed a robust GameServer using Redis for caching active user data, providing rapid data retrieval and updates.
- Implemented real-time token-based throttling to optimize API usage and performance.
- Ensured quick response times for authentication and user state management.

##### Secure Information Management
- Integrated Azure Key Vault to securely store and manage sensitive credentials required during development and deployment.
- Restricted sensitive data access exclusively to essential services, enhancing security across the infrastructure.

##### Integration and Optimization of AI Responses
- Collaborated closely with AI programmers to evaluate, integrate, and optimize HTTP communication protocols.
- Significantly reduced latency and improved the response efficiency of the integrated LLM APIs.

#### Technology Stack
- **Programming Languages:** C#, .NET
- **Cloud Infrastructure:** Azure CosmosDB, Redis, Azure Key Vault
- **Tools and Libraries:** Docker, Git, VS Code, Visual Studio
- **OS:** Windows, Linux

#### Achievements
- Successfully built a scalable backend infrastructure capable of handling large-scale user interactions.
- Achieved high efficiency in managing real-time user data and authentication, significantly enhancing user experience.
- Enhanced backend performance by implementing optimized API communication methods, resulting in reduced latency and increased reliability.

#### Code Example
```csharp
// Redis cache example for active user data
var activityData = new ActivityData
{
    UserId = userId,
    LastActivity = DateTime.Now,
    usedTokenPerMin = 0,
    usedTokenPerDay = user.usedTokenPerDay,
    totalTokenUsage = user.totalTokenUsage
};

await db.StringSetAsync($"activity:{userId}", JsonSerializer.Serialize(activityData));
```
#### Future Plans
- Complete implementation of JWT-based authentication for enhanced security.
- Integrate Azure Event Hub for efficient event-driven architecture.
- Further scalability testing and optimization in multi-region deployments.

  Access Server Project: [Here](https://github.com/largna/RizzSim2077Server)  
  Access Server Design Document: [Here](https://github.com/largna/largna.github.io/Materials/sunghwan.cho_RizzSim2077.docx)

  <img src="https://largna.github.io/Materials/RizzSim2077/sunghwan.cho_RizzSim2077_Whiteboard.png" style="width:100%; max-width:1000px;" alt="Project Screenshot">

---

### 3. Megalocheplao

<!--
  My first team game project, where I developed the entire graphics and image engine.  
  A 2D hide-and-seek action game where players complete spy missions in each level by hiding from enemies or eliminating them.  
    
  Download Game: [Here](https://github.com/sangbeom-kim/sangbeom-kim.github.io/raw/main/Files/Spy%20the%20Man.zip)  

  <video style="width:100%; max-width:1000px;" controls>
  <source src="https://sangbeom-kim.github.io/Medias/Spy%20the%20Man%20Trailer.mp4">
  Your browser does not support the video tag.
  </video>
-->