# system-design-primer

* [How Web Works!](https://github.com/reach2arunprakash/system-design-primer/tree/master/how-web-works) 
* [How Google works PhD paper - !](http://infolab.stanford.edu/~backrub/google.html)
* [Web Architecture](#Web-Architecture)
* [System design topics: start here](#system-design-topics-start-here)
    * [Scalability video Series](#Scalability-video-Series)  
* [Availability vs consistency](#availability-vs-consistency)
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
 * [Company engineering blog links](#Company-engineering-blog-links)
 * [OO design principles](#OO-design-principles)
 * [Object-Oriented Design](#Object-Oriented-Design)
 * [System Design Interview Questions](#System-Design-Interview-Questions)
 * [Clean Code](https://github.com/reach2arunprakash/system-design-primer/tree/master/cleancode) 

      
   # Welcome
                       
  ![Image of Yaktocat](https://octodex.github.com/images/yaktocat.png)
  
  
  
  
  ## Web Architecture

  ![Web Architecture]( https://github.com/reach2arunprakash/system-design-primer/blob/master/images/3%20tire%20architecture.png )
  
  
    ## COMPONENTS OF WEB APPLICATION ARCHITECTURE
  
  ![Image of Scalable Archi](https://github.com/reach2arunprakash/system-design-primer/blob/master/images/intro-scalable-arch.png)
  
  
  Src :  https://www.digitalocean.com/community/tutorials/5-common-server-setups-for-your-web-application
  
  ## Details 
    
   ### 1. Everything On One Server
       
   ![Image of Scalable Archi]( https://github.com/reach2arunprakash/system-design-primer/blob/master/001-Single%20Server.png )
          
   ### 2. Content delivery network
    
   #### Content delivery network
    
   ![Using a CDN]( https://github.com/reach2arunprakash/system-design-primer/blob/master/002%20-%20using-cdn.png )
    
   ![Using a CDN]( https://github.com/reach2arunprakash/system-design-primer/blob/master/images/OverView%20CDN.png )
      
   ![Using a CDN]( https://github.com/reach2arunprakash/system-design-primer/blob/master/images/cdn.png )
   
   
   ![Using a CDN]( https://github.com/reach2arunprakash/system-design-primer/blob/master/images/Before%20After%20CDN.png )

   
   #### Use Cases:
   
   ![Using a CDN]( https://github.com/reach2arunprakash/system-design-primer/blob/master/images/When%20to%20use%20CDN.jfif )



   ### 3. Separate Database Server
    
   ![Image of Scalable Archi]( https://github.com/reach2arunprakash/system-design-primer/blob/master/003-u-separate_database.png )
      
   ### 4. Load Balancer (Reverse Proxy)
    
   ![Image of Scalable Archi]( https://github.com/reach2arunprakash/system-design-primer/blob/master/004-u-load_balancer.png )
      
   ### 5. Primary-replica Database Replication
    
   ![Image of Scalable Archi]( https://github.com/reach2arunprakash/system-design-primer/blob/master/005-u-primary_replica_database_replication.png )
   ### Cache
    
   ![Cache]( https://github.com/reach2arunprakash/system-design-primer/blob/master/006-cache.jfif )  
     
   ![Image of Scalable Archi](https://github.com/reach2arunprakash/system-design-primer/blob/master/007-redis%20cache.png )  
    
    
 ## System design topics: start here
 
 ### Scalability video Series

[Scalability Lecture at Harvard](https://www.youtube.com/watch?v=-W9F__D3oY4)

[Scalability for first 10M users](https://www.youtube.com/watch?v=w95murBkYmU)



## Performance vs scalability

A service is **scalable** if it results in increased **performance** in a manner proportional to resources added. Generally, increasing performance means serving more units of work, but it can also be to handle larger units of work, such as when datasets grow.<sup><a href=http://www.allthingsdistributed.com/2006/03/a_word_on_scalability.html>1</a></sup>

Another way to look at performance vs scalability:

* If you have a **performance** problem, your system is slow for a single user.
* If you have a **scalability** problem, your system is fast for a single user but slow under heavy load.

### Source(s) and further reading

* [A word on scalability](http://www.allthingsdistributed.com/2006/03/a_word_on_scalability.html)
* [Scalability, availability, stability, patterns](http://www.slideshare.net/jboner/scalability-availability-stability-patterns/)


* [Four Distributed Systems Architectural Patterns by Tim Berglund](https://www.youtube.com/watch?v=tpspO9K28PM)

* [Twitter's GCP Architecture for Its Petabyte-Scale Data Storage in GCS (Cloud Next '19)](https://www.youtube.com/watch?v=rBNFwdVDlyo)

* [Building Software at Google Scale: Bazel](https://www.youtube.com/watch?v=6GCDfoAOKIY)

* [Scaling Slack - The Good, the Unexpected, and the Road Ahead](https://www.youtube.com/watch?v=_M-oHxknfnI)


* [The Evolution of Reddit.com's Architecture](https://www.youtube.com/watch?v=nUcO7n4hek4)

* [Scaling Instagram Infrastructure](https://www.youtube.com/watch?v=hnpzNAPiC0E&t=3s)

* [Scaling Push Messaging for Millions of Devices @Netflix](https://www.youtube.com/watch?v=6w6E_B55p0E)



## Latency vs throughput

**Latency** is the time to perform some action or to produce some result.

**Throughput** is the number of such actions or results per unit of time.

Generally, you should aim for **maximal throughput** with **acceptable latency**.

## CAP theorem

   ![CAP](https://github.com/reach2arunprakash/system-design-primer/blob/master/images/001-CAP.png )  
   
   
   ![CAP](https://github.com/reach2arunprakash/system-design-primer/blob/master/images/002-CAP.jfif )  
   
## Domain name system 

   ![DNS](https://github.com/reach2arunprakash/system-design-primer/blob/master/images/DNS.jfif)  

## Database

   ### ACID
   
   ![ACID](https://github.com/reach2arunprakash/system-design-primer/blob/master/images/001%20-ACID.png)  

   ![ACID and CAP](https://github.com/reach2arunprakash/system-design-primer/blob/master/images/ACID%20and%20CAP.jfif)  

   ### NoSQL

![SQL and NOSQL structure](https://github.com/reach2arunprakash/system-design-primer/blob/master/images/002%20-%20Sql%20vs%20NOSql%20Collection.png )  
  
  ![NoSQL](https://github.com/reach2arunprakash/system-design-primer/blob/master/images/001%20-%20Sql%20vs%20NOSql.png )  

  ![Image of Scalable Archi](https://github.com/reach2arunprakash/system-design-primer/blob/master/images/003-%20MySQL%20vs%20MongoDB.png )  
  
  
## Transmission control protocol (TCP)

  ![Image of Scalable Archi](https://github.com/reach2arunprakash/system-design-primer/blob/master/images/TCP%20vs%20UDP.jfif )  
  
## Representational state transfer (REST)
  
  ![Image of Scalable Archi](https://github.com/reach2arunprakash/system-design-primer/blob/master/images/REST%20Constraits.png )  
  
  
  
    
  ![Image of Scalable Archi](https://github.com/reach2arunprakash/system-design-primer/blob/master/images/REST.jfif )  
  
 ## GraphQL 
  
[GraphQL - arun prakash ](  https://www.youtube.com/watch?v=LO2tQtfGO2s)

## Asynchronism

  ![Message queues](https://github.com/reach2arunprakash/system-design-primer/blob/master/images/message_queue.png )  
  

## Childish Curiosity 

How did FB started at first? How much it costed them?

https://techcrunch.com/2012/10/20/facebooks-first-server-cost-85month/

FB: Breaking Ground on Our First Custom Data Center

https://www.facebook.com/notes/262655797130

What are the minimum hardware requirements to run a server at my home?
How do you calculate server costs per user for a social networking type platform where storage for each user would max out at 2gb a month/500mb a day?
What server size do I need for 30M users?
	How many active users a day you have?
	Are the users are normally active during a certain time of the day or will you have peaks in specific dates?
	How much CPU and RAM each user will be taking?
	And how much growth your current load has?
	Whats the bandwith Cost?
	What are the Activites a normal user will do?
		Are they watching Videos?
		Uploading photos/files?
		Doing computation?
		Just create txt (blog)?
	Where are your users located geographically?
	Where do you log their activity?



## Company engineering blog links

courtesy [checkcheckzz](https://github.com/checkcheckzz/system-design-interview#toc)

Depending on where you are interviewing, go through the company blog. VERY USEFUL IN INTERVIEWS! It really helps if you have an idea of the architecture, as the questions asked will generally be of that domain and your prior knowledge will help out here.

* [Airbnb Engineering](http://nerds.airbnb.com/)
* [Bandcamp Tech](http://bandcamptech.wordpress.com/)
* [BankSimple Simple Blog](https://www.simple.com/engineering/)
* [Bitly Engineering Blog](http://word.bitly.com/)
* [Cloudera Developer Blog](http://blog.cloudera.com/blog/)
* [Dropbox Tech Blog](https://tech.dropbox.com/)
* [Engineering at Quora](http://engineering.quora.com/)
* [Etsy Code as Craft](http://codeascraft.com/)
* [Facebook Engineering](https://www.facebook.com/Engineering)
* [Flickr Code](http://code.flickr.net/)
* [Foursquare Engineering Blog](http://engineering.foursquare.com/)
* [Google Research Blog](http://googleresearch.blogspot.com/)
* [Groupn Engineering Blog](https://engineering.groupon.com/)
* [High Scalability](http://highscalability.com/)
* [Instagram Engineering](http://instagram-engineering.tumblr.com/)
* [LinkedIn Engineering](http://engineering.linkedin.com/blog)
* [Oyster Tech Blog](http://tech.oyster.com/)
* [Pinterest Engineering Blog](http://engineering.pinterest.com/)
* [Songkick Technology Blog](http://devblog.songkick.com/)
* [SoundCloud Backstage Blog](https://developers.soundcloud.com/blog/)
* [Square The Corner](http://corner.squareup.com/)
* [THE REDDIT BLOG](http://www.redditblog.com/)
* [The GitHub Blog](https://github.com/blog/category/engineering)
* [The Netflix Tech Blog](http://techblog.netflix.com/)
* [Twilio Engineering Blog](http://www.twilio.com/engineering)
* [Twitter Engineering](https://engineering.twitter.com/)
* [WebEngage Engineering Blog](http://engineering.webengage.com/)
* [Yammer Engineering](http://eng.yammer.com/blog/)
* [Yelp Engineering Blog](http://engineeringblog.yelp.com/)
* [Smarkets Blog](https://smarketshq.com/)



## OO design principles

  ![SOLID](https://github.com/reach2arunprakash/system-design-primer/blob/master/images/SOLID-PNG.png )  


  ![SOLID](https://github.com/reach2arunprakash/system-design-primer/blob/master/images/SOLID%202.png )  


### SRP: The Single Responsibility Principle  (Just because you can, doesn’t mean you should.)

    Your classes should have one single responsibility and no more.
        Take validation of an e-mail address as an example. If you place your validation logic directly in the code that creates user accounts, you will not be able to reuse it in a different context. Having validation logic separated into a distinct class would let you reuse it in multiple places and have only a single implementation.

### OCP: The Open-Closed Principle

    Create code that does not have to be modified when requirements change or when new use cases arise. "Open for extension but closed for modification"
        Requires you to break the problem into a set of smaller problems. Each of these tasks can then vary independently without affecting the reusability of remaining components.
        MVC frameworks. You have the ability to extend the MVC components by adding new routes, intercepting requests, returning different responses, and overriding default behaviors.

### LSP: The Liskov Substitution Principle
        Functions that use pointers or references to base classes must be able to use objects of derived classes without knowing it.


### ISP: The Interface-Segregation Principle
     No client should be forced to depend on methods it does not use

### DIP: The Dependency-Inversion Principle

    Dependency injection provides references to objects that the class depends on instead of allowing the class to gather the dependencies itself. In practice, dependency injection can be summarized as not using the "new" keyword in your classes and demanding instances of your dependencies to be provided to your class by its clients.
    Dependency injection is an important principle and a subclass of a broader principle called inversion of control. Dependency injection is limited to object creation and assembly of its dependencies. Inversion of control, on the other hand, is a more generic idea and can be applied to different problems on different levels of abstraction.
        IOC is heavily used by several frameworks such as Spring, Rails and even Java EE containers. Instead of you being in control of creating instances of your objects and invoking methods, you become the creator of plugins or extensions to the framework. The IOC framework will look at the web request and figure out which classes should be instantiated and which components should be delegated to. This means your classes do not have to know when their instances are created, who is using them, or how their dependencies are put together.


## DRY: Don't repeat yourself

    There are a number of reasons developers repeated waste time:
        Following an inefficient process
        Lack of automation
        Reinventing the wheel
        Copy/Paste programming
        
# Object-Oriented Design

1. **Deck of Cards**: Design the data structures for a generic deck of cards. Explain how you would subclass the data structures to implement blackjack.
2. **Call Center**: Imagine you have a call center with three levels of employees: respondent, manager, and director. An incoming telephone call must be first allocated to a respondent who is free. If the respondent can't handle the call, he or she must escalate the call to a manager. If the manager is not free or not able to handle it, then the call should be escalated to a director. Design the classes and data structures for this problem. Implement a method dispatchCall() which assigns a call to the first available employee.
3. **Jukebox**: Design a musical jukebox using object-oriented principles.
4. **Parking Lot**: Design a parking lot using object-oriented principles.
5. **Online Book Reader**: Design the data structures for an online book reader system.
6. **Jigsaw**: Implement an NxN jigsaw puzzle. Design the data structures and explain an algorithm to solve the puzzle. You can assume that you have a `fitsWith` method which, when passed two puzzle edges, returns true if the two edges belong together.
7. **Chat Server**: Explain how you would design a chat server. In particular, provide details about the various backend components, classes, and methods. What would be the hardest problems to solve?
8. **Othello**: Othello is played as follows: Each Othello piece is white on one side and black on the other. When a piece is surrounded by its opponents on both the left and right sides, or both the top and bottom, it is said to be captured and its color is flipped. On your turn, you must capture at least one of your opponent's pieces. The game ends when either user has no more valid moves. The win is assigned to the person with the most pieces. Implement the object-oriented design for Othello.
9. **Circular Array**: Implement a CircularArray class that supports an array-like data structure which can be efficiently rotated. If possible, the class should use a generic type (also called a template), and should support iteration via the standard for ( Obj o : circularArray ) notation.
10. **Minesweeper**: Design and implement a text-based Minesweeper game. Minesweeper is the classic single-player computer game where an NxN grid has B mines (or bombs) hidden across the grid. The remaining cells are either blank or have a number behind them. The numbers reflect the number of bombs in the surrounding eight cells. The user then uncovers a cell. If it is a bomb, the player loses. If it is a number, the number is exposed. If it is a blank cell, this cell and all adjacent blank cells (up to and including the surrounding numeric cells) are exposed. The player wins when all non-bomb cells are exposed. The player can also flag certain places as potential bombs. This doesn't affect game play, other than to block the user from accidentally clicking a cell that is thought to have a bomb. (Tip for the reader: if you're not familiar with this game, please playa few rounds online first.)
11. **File System**: Explain the data structures and algorithms that you would use to design an in-memory file system. Illustrate with an example in code where possible.
12. **Hash Table**: Design and implement a hash table which uses chaining (linked lists) to handle collisions.


## System Design Interview Questions

A curated list of System Design interview questions for SDE-1 (Experienced),SDE-2 and above.

Targeted companies: Amazon, Google, Facebook and other biggies.

    Design commenting system
    Design subscription based sports website which can display scores, game status, history for any games.
    Design Netflix => search, video serving, authentication, encryption, dns lookup,caching strategy,serving multi quality video etc
    Design a Latency Management System
    Design a Library Management System
    Design a Notification service
    Design ESPN/Cricinfo/Cricbuzz
    Design Uber
    Design Whatsapp
    Design Quora
    Design Lookahead system
    Design Google Docs/ Collaborative Editing service
    Design URL Shortner service
    Design RedBus
    Design BookMyShow
    Design Domain Backdooring system
    Design Amazon Locker
    Design Movies Review Aggregator System > Data should be fetched from movie rating providers like imdb, rotten tomatoes, etc
    Design offline caching system for Ecommerce platform
    Design Amazon E-commerce
    Design Online chess game/Multiplayer game
    Design gaming platform. A number of games can be hosted on this platform. User can login and select a particular game
    Design a last-mile delivery platform in case of peak seasons
    Design Zomato/Swiggy/Foodpanda
    Design Meeting Calendar system
    Design Spotify
    Design Promo Code API by taking into account Amazon's customer traffic into picture
    Design Vending machine with following functionalities ==> Three types of Users : User, Operator, Admin
        User can select and buy multiple items at a time. Money can be inputted multiple times (you will get the item if there is a time gap > 30 secs). He can also do window shopping (see only the prices of items and buy nothing)
        Operator can load the items and mark the items as expired if needed, gets notified if a product goes out of stock.
        Admin can own multiple vending machines, he should have a analytics report of the items purchased in a month. He can also change the prices directly and it should reflect in all the vending machines which he owns.
        Exception handling in all the edge cases
    Design splitwise
    Design Google pay at scale
    Design a Job schedular => scalability, fault tolerance, high availability, how scheduler picks up job, how will you take care where one job can run for 30 min and one for 30 hour, how will you distribute jobs on servers. Based on frequency & time how will you execute them ? How will you notify back the user about start/stop or completion of a job ? How will your system know if a job is killed / terminated due to unknown reasons ?
    Design Meeting Scheduler
    Design Debugger
    Design Automatic Parking System
    Design a ranking system. We have an infinite supply of words ending with ‘.’ We need to implement a reader program that ranks words on the basis of certain criteria Example: This is my cat. This house belongs to my uncle An amazing country with so many tourist places And so on.. Ranking System criteria : rank the words on the basis of occurrence, for example Output : This:2, is:2, my:2… highest rank (sorted asc or desc based on provided flag) Design it completely and scalable Ranking System
    Design Amazon Cart system
    Design Google Search
    Design Twitter
    Design Facebook
    Design Snapchat
    Design Instagram
    Design App-store
    Design a music player application
    Design a distributed LRU Cache
    Design Gmail
    Design a recommendation system
    Design a food sharing application
    Design payment module for Uber app
    Design Truecaller type of system
    Design performance management system (appraisal workflow system) that can be used across companies.
    Design comment system like disqus
    Design flight system
    Design Tinder
    Design survey site like surveymonkey
    Design a geographically partitioned multi-player card game, that supports multiple players, multiple games at a time. Each game will have one contractor like ones we have in a bar, He can play a game or just watch it. Integrate payment systems
    Design a kind of kindle fire application where we can subscribe news channel and read the news from all publishers as a digital format
    Design a realtime Video chat like Google Duo
    Design News paper & Magazine subscription system
    Design a system like GUVI/Leetcode/Hackerrank/Codechef/Topcoder
    Design a concurrent Hashmap
    Design an ATM Machine system which can support massive amount of transactions
    Design Airport Baggage system
    Design Flight Information Display system
    Design a conference room booking system for a company which can have offices in multiple cities, each city can have multiple buildings, each building can have multiple floors, each floor can have multiple rooms. Each room can have features like capacitiy, video conferencing available, etc.
    Design newsfeed feature of Facebook
    Design an efficient Mail delivery system
    Design like/dislike feature at Youtube scale.
    Design Paypal
    Design Air traffic control system
    Design a realtime service which tells your friends who is online
    Design Google Maps
    Design Grammarly

