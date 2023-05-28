
# SYSTEM DESIGN CONCETPS
## **Key system design concepts**
## Scalability
- Ablity of the system to handle load/large volume of requests
  ### vertical scaling
  - adding multiple instace of the compute or storage
  ### horizonatal scaling
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
## **Load Balancing [LB]**
- LB's helps to improve responsiveness and availability of applications, websites or databases
### Places where LBs can be used
  - Between Client and Web Server
  - Between Webserver and App Server
  - Between App Server to DB

### Different Load blancing algorithms

  ![image](https://substack-post-media.s3.amazonaws.com/public/images/12dffcce-f231-48cc-915f-d53c0f8bce0c_3735x3573.jpeg)

  #### Static Algorithms
  - Round robin 
    The client requests are sent to different service instances in sequential order. The services are usually required to be stateless.
  - Sticky round-robin 
    This is an improvement of the round-robin algorithm. If Alice’s first request goes to service A, the following requests go to service A as well.
  - Weighted round-robin 
    The admin can specify the weight for each service. The ones with a higher weight handle more requests than others.
  - Hash 
    This algorithm applies a hash function on the incoming requests’ IP or URL. The requests are routed to relevant instances based on the hash function result.
#### Dynamic Algorithms
  - Least connections 
    A new request is sent to the service instance with the least concurrent connections.
  - Least response time 
    A new request is sent to the service instance with the fastest response time. 


