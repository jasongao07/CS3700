High Level Approach

We added to the preexisting code provided.
In the run function, we added functionality to handle the different
types of messages.

We also implemented many helper functions to help convert netmasks to CIDR and IP addresses to 
their binary versions so that we can preform operations on them. We used string versions
of binary numbers because we found them easier to work with.

To create the forwarding table, we made a function that returned a newly generated table each time
based on all the messages that were sent to the router. We found this easier to implement than
trying to change a fixed forwarding table each time there was a new withdraw message. The function
was responsible for handling changes to the table from update and withdraw messages, and was also
responsible for aggregating the entries in the table. We preformed aggregation after processing all
the update and withdraw messages.

In order to debug our code, we ran the config tests on it and looked at the expected input and outputs within the files
and error messages in the terminal.

Challenges We Faced:
For us, this project was the most complicated one to date. There were a lot of different moving parts in
the code, which made it hard to debug. Furthermore, since each item was essentially a dictionary, we had a lot
of nested indexing.

We had the most difficultly in steps 5 and 6.
For step 5, we had a lot of difficulty in translating the IP addresses and netmasks into something we can work with.
We first had to understand the process of subnetting and the decisionmaking behind it before trying to
implement it into our code.

For step 6, it was difficult to determine what could be aggregated because of how many attributes we 
needed to make sure lined up. Furthermore, we had to make sure that we started checking from the beginning
after each aggregate due to the possibility of having multiple aggregates. We needed clarification
about numerical adjacency because we thought the example given was a bit vague.

Properties/Features We Thought Were Good:
By generating a new forwarding table each time, we reduced the complexity of the code drastically.
By writing helper functions that helped us convert between binary, IP addresses, and strings, we 
greatly reduced the amount of repetitive code in our program.

Testing the Code:
In order to test our code, we ran the tests in the config file.