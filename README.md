# Dining Philosophers Problem With Resource Hierarchy

The Dining Philosopher problem is a classic scenario that represents synchronization issues in multiprocessor systems. In this problem, a group of 
philosophers sit around a table and attempt to share a spaghetti dinner. However, each philosopher must use the forks shared by the philosophers 
next to them. Deadlock can occur when one philosopher takes a fork and while waiting for the other, other philosophers are interested in the same 
fork.

<hr>

# Solution Strategy: Resource Hierarchy

#### Note:
Sometimes, only one philosopher is able to eat spaghetti due to the randomness of thinking time, waiting time after picking up the fork, and spaghetti 
eating time.

<hr>

For example, philosopher F1 takes the left fork, waits for a random amount of time, and if philosopher F2 to their right is already eating spaghetti, 
philosopher F1 cannot take the fork and start eating. Simultaneously, the philosopher to the left of F1 picks up their left fork, waits for a random 
amount of time, and attempts to pick up the right fork. However, they are unable to do so as it is being held by F1. 

To illustrate this point, let us provide a comprehensive example

F2 takes the left fork and waits for 3 seconds. Meanwhile, F1's thinking time ends, and they take the left fork since it is available, and wait for 3 seconds. 
If the right fork is empty after 3 seconds for F2, he takes it and starts eating spaghetti for 7 seconds. Before the end of 3 seconds for F1, the thinking time 
for philosopher F5 ends. F5 takes the left fork and waits for 1 second. However, since the right fork for F5 is the left fork of F1 and F1 is using it, F5 cannot 
take it and starts thinking. Meanwhile, the 3-second period for F1 ends, but since F2's left fork is not free, F1 cannot take the right fork and starts thinking.   