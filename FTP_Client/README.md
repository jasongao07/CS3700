CS 3700 Project2: FTP Client

DESCRIPTION:
In this project, you will implement a client for a more complex protocol, that has more features,
 and uses two sockets rather than one.

Specifically, in this project you will develop a client for the File Transfer Protocol (FTP) protocol. 
We have setup an FTP server for you to use when developing and debugging your client. 

Your goal to write a basic FTP client application. This client will run on the command line, 
and must support the following six operations: directory listing, making directories, file deletion, 
directory deletion, copying files to and from the FTP server, and moving files to and from the FTP server.

APPROACH:

My approach to this project was to follow the suggested implementation. 
I first learned how to parse the urls using urllib. From then I connected the sockets and 
start sending individual commands such as USER, PASS, TYPE, MODE, STRU, and QUIT. 

After confirming that each command is being interpretted correctly, 
I moved on to the other commands like MKD, RMD, PASV, and LIST
From PASV on, I started to code the second socket. 
After testing that the data socket works correctly through sending some commands, 
I continued until I finished adding all of the Commands.

Lastly from there, I matched the commandline commands to the ftp commands.

CHALLENGES:
A major challenge that I had when doing this project was completing the mv command.
This challenge was due to the fact that there was a bug in my code which caused two different
operations to compile instead of the correct one. This was solved shortly after discovering the mistake.


TESTING:
I tested the application by running each command individually and checking with Filezilla to make
sure that all of the commands were doing what it is supposed to. This ensures that the final 
application will have all the correct outputs. 

