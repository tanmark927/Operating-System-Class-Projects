# Operating-System-Class-Projects
This repository contains all the projects that I have done within my Operating Systems course.

Programming Review:

This C++ project allocates and deallocates a struct that comprises of an integer array and a char pointer array. It allows the user to access a pointer, deallocate memory and list the indices of the char pointer array that have been deallocated. When a user wants to access a pointer, one is allowed to either print the first ten characters in that pointer or delete all the chars associated with it. Memory is allocated based on the size defined in each index of the integer array, and chars are initialized to a random uppercase letter.

Process Termination:

This lab is a hands-on activity that involves using the kill command in Linux, “kill -9 PID”, in which the process ID, also known as PID, represents the task a user intends to terminate. To check if the desired task to eliminate has been removed, a statistic task view is used to identify the tasks that are running, as well as information tied to that task. One can use the command “ps aux” to access this view. To test the kill command, a rogue program will be used in which one of its processes will run out of control.

Interprocess Communication and Synchronization:

This project is an event tracking system in which three senders and two receivers communicate with each other using one message queue. The senders send events in the form of randomly generated integers that are divisible by a marker value such as 251, 997 and 257. The receivers get events from the senders, output the message and send an acknowledgement message back to the original sender. All five components are intended to terminate on a given condition, and execution must begin with the 251 & 997 receiver because that is where the message queue is allocated.

Creation and Inheritance of Child Processses:

This is a string replacement program that finds a word within a string and replaces it with another word. It also keeps a count on the number of times the desired word is replaced. The replacement procedure involves the creation of a child process, and a child will be made for each replacement scenario. If a replacement fails, the child process will do the replacement in an infinite loop meaning that the child can only be terminated using the kill command. To exit the program, type in “!wq” as one of your strings to find and replace.

Interprocess Communication with Semaphores and Shared Memory:

This program spawns four child processes in which each generates a random integer and checks if it is a factor of either a U value or a V value. At most, one process is responsible for comparing the random integer to a reference value, and processes must wait in case both references are used. If the random integer is less than 100 or is a factor of the reference value, it will conclude and allow the next child process to be active. When a process is waiting to use a value, it is added to the waiting queue and will only be removed once it is resumed. By default, the newly resumed process checks the U value first.

This current iteration of the program does not exhibit deadlock because there is always at least one process making progress. Although there is mutual exclusive use of resources due to how I initialize my semaphore variables (both are initialized at 1), there is no scenario where circular wait is apparent. In addition, this solution does not exhibit starvation because all processes are able to make progress at all times, even when some are in the waiting state.
