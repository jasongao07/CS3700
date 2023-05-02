CS 3700 Project 6: Distributed Key Value database

PROJECT DESCIPTION:
In this project, we will be building a (relatively) simple, distributed, replicated key-value datastore. 
A key-value datastore is a very simple type of database that supports two API calls from clients: put(key, value) and get(key). 
The former API allows a client application to store a key-value pair in the database, while the latter API allows a client to retrieve a previously 
stored value by supplying its key. Real-world examples of distributed key-value datastores include memcached, Redis, DynamoDB, etc.

APPROACH:
The approach that we had while completing this project was to implement a modified version of the Raft consensus protocol.
The system will consist of multiple replicas, which will communicate through an unreliable network. We intially started with 
implementing all aspects of the raft protocol. Going through this, we were met with difficulties with the test cases. Therefore we ended up 
changing some aspects of the Raft protocol. Our implementation consisted of several components, including a leader election mechanism and 
handling redirects, heartbeats, get and pull request from replicas. 

CHALLENGES:
The biggest challenge we faced while implementing this project was getting the advanced tests to pass. While debugging this test, wrote log
messages to see where the error lies, and through these messages we were able to get the advanced tests to compile. 

FEATURES: 
Some properties and features that I think was good was the implementation of the leader election protocol in order to ensure that only one 
replica is responsible for proposing updates at any given time. This reduces conflicts and ensures that all replicas converge on the same state. 
Another property of the design that we think was good was the implementation of the Raft protocol because this ensures consistency as all the replicas 
maintain a consistent copy of the log. 

TESTING:
We tested the application by running through through each of the tests individually. By going through each test, and displaying the log messages
of each one, we were ultimately able to understand where the errors lie. Lastly, we used the ./run all to make sure that all of the tests ran correctly.
