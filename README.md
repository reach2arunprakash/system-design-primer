# system-design-primer

* [How Web Works](#How Web Works)
     https://github.com/reach2arunprakash/system-design-primer/tree/master/how-web-works

* [System design topics: start here](#system-design-topics-start-here)
    * [Step 1: Review the scalability video lecture](#step-1-review-the-scalability-video-lecture)
* [Performance vs scalability](#performance-vs-scalability)
* [Latency vs throughput](#latency-vs-throughput)
* [Availability vs consistency](#availability-vs-consistency)
    * [CAP theorem](#cap-theorem)
        * [CP - consistency and partition tolerance](#cp---consistency-and-partition-tolerance)
        * [AP - availability and partition tolerance](#ap---availability-and-partition-tolerance)
* [Domain name system](#domain-name-system)
* [Content delivery network](#content-delivery-network)
* [Load balancer](#load-balancer)
    * [Horizontal scaling](#horizontal-scaling)
* [Reverse proxy (web server)](#reverse-proxy-web-server)
    * [Load balancer vs reverse proxy](#load-balancer-vs-reverse-proxy)
* [Application layer](#application-layer)
    * [Microservices](#microservices)
    * [Service discovery](#service-discovery)
* [Database](#database)
    * [SQL or NoSQL](#sql-or-nosql)
    * [Relational database management system (RDBMS)](#relational-database-management-system-rdbms)
        * [Sharding](#sharding)
        * [Denormalization](#denormalization)
    * [NoSQL](#nosql)
        * [Key-value store](#key-value-store)
        * [Document store](#document-store)
        * [Wide column store](#wide-column-store)
        * [Graph Database](#graph-database)
* [Cache](#Cache)
    * [Client caching](#client-caching)
    * [CDN caching](#cdn-caching)
    * [Web server caching](#web-server-caching)
    * [Database caching](#database-caching)
    * [Application caching](#application-caching)
    * [Caching at the database query level](#caching-at-the-database-query-level)
    * [Caching at the object level](#caching-at-the-object-level)
* [Asynchronism](#asynchronism)
    * [Message queues](#message-queues)
    * [Task queues](#task-queues)
    * [Back pressure](#back-pressure)
* [Communication](#communication)
    * [Transmission control protocol (TCP)](#transmission-control-protocol-tcp)
    * [User datagram protocol (UDP)](#user-datagram-protocol-udp)
    * [Remote procedure call (RPC)](#remote-procedure-call-rpc)
    * [Representational state transfer (REST)](#representational-state-transfer-rest)
    * [GraphQL](#graphql)
    
    
    
    
  ![Image of Yaktocat](https://octodex.github.com/images/yaktocat.png)
  
  ## WHAT IS WEB APPLICATION ARCHITECTURE?

  ![Image of Scalable Archi]( https://github.com/reach2arunprakash/system-design-primer/blob/master/images/Web%20Archi.png)
  
  
    ## COMPONENTS OF WEB APPLICATION ARCHITECTURE
  
  ![Image of Scalable Archi](https://github.com/reach2arunprakash/system-design-primer/blob/master/images/intro-scalable-arch.png)
  
  
  Src :  https://www.digitalocean.com/community/tutorials/5-common-server-setups-for-your-web-application
  
  ## Details 
    
    ### 1. Everything On One Server
       
     ![Image of Scalable Archi]( https://github.com/reach2arunprakash/system-design-primer/blob/master/001-Single%20Server.png )
          
    ### 2. Using a CDN
    
     ![Image of Scalable Archi]( https://github.com/reach2arunprakash/system-design-primer/blob/master/002%20-%20using-cdn.png )
      
    ### 3. Separate Database Server
    
     ![Image of Scalable Archi]( https://github.com/reach2arunprakash/system-design-primer/blob/master/003-u-separate_database.png )
      
    ### 4. Load Balancer (Reverse Proxy)
    
     ![Image of Scalable Archi]( https://github.com/reach2arunprakash/system-design-primer/blob/master/004-u-load_balancer.png )
      
    ### 5. Primary-replica Database Replication
    
     ![Image of Scalable Archi]( https://github.com/reach2arunprakash/system-design-primer/blob/master/005-u-primary_replica_database_replication.png )
    ### Cache
    
     ![Cache]( https://github.com/reach2arunprakash/system-design-primer/blob/master/006-cache.jfif )  
     
     ![Image of Scalable Archi](https://github.com/reach2arunprakash/system-design-primer/blob/master/007-redis%20cache.png )  
    
    
   
 ### Step 1: Review the scalability video lecture

[Scalability Lecture at Harvard](https://www.youtube.com/watch?v=-W9F__D3oY4)


## Performance vs scalability

A service is **scalable** if it results in increased **performance** in a manner proportional to resources added. Generally, increasing performance means serving more units of work, but it can also be to handle larger units of work, such as when datasets grow.<sup><a href=http://www.allthingsdistributed.com/2006/03/a_word_on_scalability.html>1</a></sup>

Another way to look at performance vs scalability:

* If you have a **performance** problem, your system is slow for a single user.
* If you have a **scalability** problem, your system is fast for a single user but slow under heavy load.

### Source(s) and further reading

* [A word on scalability](http://www.allthingsdistributed.com/2006/03/a_word_on_scalability.html)
* [Scalability, availability, stability, patterns](http://www.slideshare.net/jboner/scalability-availability-stability-patterns/)

## Latency vs throughput

**Latency** is the time to perform some action or to produce some result.

**Throughput** is the number of such actions or results per unit of time.

Generally, you should aim for **maximal throughput** with **acceptable latency**.

## CAP theorem

   ![CAP](https://github.com/reach2arunprakash/system-design-primer/blob/master/images/001-CAP.png )  
   
   
   ![CAP](https://github.com/reach2arunprakash/system-design-primer/blob/master/images/002-CAP.jfif )  
   

## Database

   ### ACID
   
   ![ACID](https://github.com/reach2arunprakash/system-design-primer/blob/master/images/001%20-ACID.png)  

   ![ACID and CAP](https://github.com/reach2arunprakash/system-design-primer/blob/master/images/ACID%20and%20CAP.jfif)  

   ### NoSQL

![SQL and NOSQL structure](https://github.com/reach2arunprakash/system-design-primer/blob/master/images/002%20-%20Sql%20vs%20NOSql%20Collection.png )  
  
  ![NoSQL](https://github.com/reach2arunprakash/system-design-primer/blob/master/images/001%20-%20Sql%20vs%20NOSql.png )  

  ![Image of Scalable Archi](https://github.com/reach2arunprakash/system-design-primer/blob/master/images/003-%20MySQL%20vs%20MongoDB.png )  
  
  
 ## GraphQL 
  
[GraphQL - arun prakash ](  https://www.youtube.com/watch?v=LO2tQtfGO2s)

## Asynchronism
  ![Message queues](https://github.com/reach2arunprakash/system-design-primer/blob/master/images/message_queue.png )  
  

