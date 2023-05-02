CS 3700 Project 4: Reliable Transport Protocol

APPROACH:
The approach that I had while completing this project was to break the pieces down into separate 
components and to run through the tests one by one. This approach allowed me to complete all of the
tests all the way to the final test. 

CHALLENGES:
A challenge that I faced while completing this project was deciphering exactly which part was failing.
The given log messages were really hard to comprehend and it was harder to find specifically which portion 
of the code that it affected. A particularly bad portion was doing 4-1 because I couldn't figure out why my
packets weren't retransmitting. 

FEATURES:
A particular feature that I was proud of was implementing the sliding window for tests 7. I thought that this
portion was particularly difficult, and I managed to accomplish it without too much difficulty.

TESTING:
I tested the application throughout the process of completing each step by using the log function
to log the outputs of specific things that were breaking. Through this, I can thoroughly check
which parts of the function that is implemented incorrectly. Furthermore, in the end I ran through 
all of the tests using ./test and then if there were some that were breaking, I ran the test individually
to see which parts were breaking. 