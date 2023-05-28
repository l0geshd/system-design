
# **SYSTEM DESIGN CONCETPS**

# **Key system design concepts**

## Scalability
- Ablity of the system to handle load/large volume of requests
  ### **vertical scaling**
  - adding multiple instace of the compute or storage
  ### **horizontal scaling**
  - adding more memeory or processing power to existing machine
## Reliability
- reliability is the probability a system will fail in a given period
- A reliable distributed system achieves this through redundancy of both the software components and data.
- reliability includes security of the system
## Availability 
- availability is the time a system remains operational to perform its required function in a specific period.
## Efficiency
- Two standard measures of its efficiency are 
  -  **response time (or latency)** that denotes the delay to obtain the first item 
  -  **throughput (or bandwidth)** which denotes the number of items delivered in a given time unit (e.g., a second). 
     ![image](https://github.com/l0geshd/system-design/assets/61483272/6499c92b-ef4c-4f4b-b908-6c02b78838c3)
     ![image](https://github.com/l0geshd/system-design/assets/61483272/b8f5ed51-eb0e-4629-aa5b-50f9768a363e)
## Manageability
-  Serviceability or manageability is the simplicity and speed with which a system can be repaired or maintained; 
-  if the time to fix a failed system increases, then availability will decrease.

# **Load Balancing [LB]**

- LB's helps to improve responsiveness and availability of applications, websites or databases
### Places where LBs can be used
  - Between Client and Web Server
  - Between Webserver and App Server
  - Between App Server to DB

### Different Load blancing algorithms

  ![image](https://substack-post-media.s3.amazonaws.com/public/images/12dffcce-f231-48cc-915f-d53c0f8bce0c_3735x3573.jpeg)

  #### Static Algorithms [TBR]
  - **Round robin** 
    The client requests are sent to different service instances in sequential order. The services are usually required to be stateless.
  - **Sticky round-robin** 
    This is an improvement of the round-robin algorithm. If Alice’s first request goes to service A, the following requests go to service A as well.
  - **Weighted round-robin** 
    The admin can specify the weight for each service. The ones with a higher weight handle more requests than others.
  - **Hash** 
    This algorithm applies a hash function on the incoming requests’ IP or URL. The requests are routed to relevant instances based on the hash function result.
  #### Dynamic Algorithms
  - **Least connections** 
    A new request is sent to the service instance with the least concurrent connections.
  - **Least response time** 
    A new request is sent to the service instance with the fastest response time. 

#### Reducndant Load balancer [TBR]

  The load balancer can be a single point of failure; to overcome this, a second load balancer can be connected to the first to form a cluster. Each LB monitors the health of the other and, since both of them are equally capable of serving traffic and failure detection, in the event the main load balancer fails, the second load balancer takes over.

# **Caching**
  ## CDN
  ## Cache Invalidation
  ## Cache Eviction

# **Sharding or Data Partitioning**

# **Indexes**
- The goal of creating an index on a particular table in a database is to make it **faster to search through the table** and find the row or rows that we want.

# **Proxies**

  Typically, proxies are used to **filter requests, log requests, or sometimes transform requests** (by adding/removing headers, encrypting/decrypting, or compressing a resource). Another advantage of a proxy server is that its cache can serve a lot of requests.

![image](https://substackcdn.com/image/fetch/f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fbucketeer-e05bbc84-baa3-437e-9518-adb32be77984.s3.amazonaws.com%2Fpublic%2Fimages%2F257642d6-9742-432b-9ca8-2a866dea04dd_1445x1536.jpeg)

## Forward Proxy
A forward proxy is a server that sits between user devices and the internet.

A forward proxy is commonly used for: 
- Protect clients
- Avoid browsing restrictions
- Block access to certain content

## Reverse Proxy
A reverse proxy is a server that accepts a request from the client, forwards the request to web servers, and returns the results to the client as if the proxy server had processed the request.

A reverse proxy is good for:
- Protect servers
- Load balancing
- Cache static contents
- Encrypt and decrypt SSL communications

# **Redundancy & Replication**

# **SQL vs. NoSQL**

# **CAP Theorem**

# **Consistent Hashing**

# **Long-Polling vs WebSockets vs Server- Sent Events**







