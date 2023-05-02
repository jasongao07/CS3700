CS 3700 Project1: Socket Basics

DESCRIPTION:
This project will implement a client program that plays a variant of the recently-popular game Wordle. 
The program will make guesses for the secret word, and the server will give you information about how close your guess is.
Once the client correctly guesses the word, the server will return a secret flag that is unique for each student. 
If you receive the secret flag, then you know that your program has run successfully.
Furthermore the client must support TLS encrypted sockets. 
The server will return different secret flags depending on whether your client communicates with or without TLS.

APPROACH:
My approach to this project was to first test out components such as sending/receiving messages.
I tested to make sure that I got all the right inputs and outputs received from the server.
Afterwards, I ran the wordle solver by sending and receiving inputs from the server.
Once the wordle solver is correct, I implemented the tls and tested to see if the socket wrapped with the tls socket works

CHALLENGES:
A major challenge that I had when doing this project was sending and receiving data. 
Parsing the JSON file kept giving errors, which prevented me from continuing with the project.

STRATEGY:
My strategy for the wordle solver is to first guess the "best" word that will 
reduce the most words in the wordlist: "salet".
After guessing a word, I will then filter out the words in my wordlist according 
to the marks that I receive from the server.
If a 2 is received, I will remove all instances in the wordlist that does not 
contain the same letter in the same position.
If a 1 is received, I will remove all instance in the wordlist that does contains
the word or when the letter is in the same place.
If a 0 is received, I will remove all instances of the word that contains that letter.

TESTING:
I tested the application by first testing to see if the input/output is correct. 
Afterwards, I tested the wordle solver by outputting both the data received from the server and the filtered wordlist
Repeatedly testing filter helped me figure out logical errors that were present in my filter function.
Lastly I tested the tls/tcp connection while running the wordle solver.






