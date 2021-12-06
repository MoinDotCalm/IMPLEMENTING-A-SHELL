# IMPLEMENTING-A-SHELL
The Shell is the command interpreter on Linux systems. This document introduces some of the basic features of the Shell and lists many of the commands or programs available on the Linux computers in Cardiff School of Computer Science & Informatics. 
 
Shell is a command interpreter, which interprets the command given by the user to the kernel. It can also be defined as an interface between a user and the operating system. 
Command shells are the most basic tools that facilitate user interaction with the operating system, and one of the oldest. Although modern operating systems with graphical user interfaces no longer require users to work at a command prompt, most OSes still provide a command shell for lower level tasks. 
There are a variety of UNIX command shells, each with its own strengths, but virtually all of them use a very basic syntax for specifying commands. For example:  grep Allow logfile.txt. The command is "grep", and the two arguments are "Allow" and "logfile.txt". The command shell runs the program "grep" (wherever it might appear on the current filesystem path), and passes it an array of 3 arguments: 
char *argv[] = { "grep", "Allow", "logfile.txt", NULL }; 
(The argument list is always terminated with a NULL value. In this case, argc = 3 even though there are four elements in argv.) 
Note that the command is tokenized by whitespace (spaces and tabs). If we want an argument to preserve its whitespace, it must be enclosed in double quotes, like this: 
grep " Allowing access" logfile.txt Now, the argument array is as follows: char *argv[] = { "grep", " Allowing access", "logfile.txt",
NULL };
