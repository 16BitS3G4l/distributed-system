# Distributed System
Our operating systems project (a distributed system) 

Whenever you're checking the instructions for specifics, please [use the link](https://touroc-my.sharepoint.com/:w:/g/personal/yitzchak_novick_touro_edu/EfrWzuAgS5VMjEtyG1PwPXcBR3OAQDWmL4HRUa5tRCTXLg). The professor noted that he'd be making updates throughout the semester over there. 

Overall structure of the project: 
  - Master
     - Slave(s) 
  - 2 Clients (unless we want to make it dynamic, no matter the number)
  <hr>
  
  There is expected to be one master. 
  
  Two types of slaves: A and B. 
  
  There will also be two types of jobs for the master to give to the slaves, a job called A and a job called B. 
  
  Slave A can do Job A better than Slave B can do Job A, and Slave B can do Job B better than Slave A can do Job B. 
  Note that a job is just a period of time sleeping. Once "completed," the slave will notify the master it's done, and the master will let the 
  appropriate client that the job has finished.
 
  We are going to have to have some type of algorithm for "load balancing." 
  This will be a sort of filter for clients when they're talking to the master. The master will use this algorithm for deciding what
  slave should get a job from a client. 
  
  Example: 
    Let's say we have a client connecting to our master, and they have a Job A they need done. Now, in the typical case, we'd give that job to a slave which is optimized for Job A, which would be slave A, right? Now, at some point, giving a job to a slave A for a job A, will actually be slower than giving it to a suboptimized slave, slave B for a job A. 
    These are the sort of things we'll have to implement in this load balancer. 
  
  
  
