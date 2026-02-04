Question 9 [6 Points]

Write a C program to demonstrate zombie process prevention.

• Create multiple child processes

• Ensure terminated child processes do not remain zombies

• Parent process should print the PID of each child it cleans upUse fork(), wait(), or waitpid().


I first created a zombie.c file using nano command. 
i used a for loop to help easily pass through multiple children at the same time. When the children executes, using the exit(0) command makes the child immediately become zombies since they haven't been called out by the parent. 
by calling the sleep() function on the parent, it allows zombies to exist without being cleaned too fast. 
calling wait() later on cleans zombie entries from process table. 

command 

      fork()
explanation:- created child processes. Each child exits immediately, entering the zombie state reaped by the parent.

command 

      _exit(0)
explanation:- Terminates the child process without flushing buffers, ensuring the child exits instantly and becomes a zombie

command 

     sleep(5)
explanation:- in this context used to force the parent process to delay execution. This was used so that the zombie processes exist temporarily

command 

      wait(NULL)
explanation:- Parent process waits for terminated child processes and removes them from the process table. 

complete code:-
<img width="1870" height="631" alt="Screenshot 2026-02-05 011635" src="https://github.com/user-attachments/assets/1f0ae2ca-b45a-4bfe-bb2f-e15b5f29d3da" />

executed the file along with output
command 

      gcc zombie.c -o zombie
compiles the zombie process demonstration program and creates an executable named zombie.

command 

      ./zombie
runs the program. 
<img width="1720" height="139" alt="Screenshot 2026-02-05 011609" src="https://github.com/user-attachments/assets/a05371af-13dd-4939-be67-195f89e6a637" />
