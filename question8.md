Question 8 [6 Points]

Create a shell script bg_move.sh that accepts a directory path.

• Move each file in the directory into a subdirectory named backup/

• Perform each move operation in the background

• Display the PID of each background process

• Wait for all background processes to finishUse &, wait, $$, and $! variables.

Working principle:- Moving files in the background demonstrates parallel execution and improves performance. the usage of commands like & sends each mv commmand to the background allowing multiple moves simultaneously. through the usage of $!, we can print PID and confirm background execution. And finally using wait allows the script to completely execute. 

created testdir and some files required 

command 

    mkdir 
was used to make a directory as required for the execution. 
<img width="1913" height="65" alt="Screenshot 2026-02-05 010654" src="https://github.com/user-attachments/assets/b57edce0-02e2-4489-875b-b11cafb75796" />


created a bg_move.sh file 
command 

     ./bg_move.sh testdir
explanation:- It executes the shell script that moves files from a directory into a backup folder using background execution. 

command 

     mkdir -p backup
explanation:- if the backup directory doesn't exist, it creates a new one. the -p option avoids any possible errors if the directory already exists. 

command 

    mv "$f" backup/ &
explanation:- moves a file into a backup directory and runs the command in the background using &

command 

     $!
explanation:- Stores and prints the process id. 

command 

    wait
explanation:- suspends the script, ensuring background processes finish execution. 

complete script:-
<img width="1884" height="314" alt="Screenshot 2026-02-05 010453" src="https://github.com/user-attachments/assets/9f5dbda7-afa6-4ab2-8b16-3ee3839ca54d" />

executed file + output
 I just executed the .sh file and confirmed the results in this part
<img width="1875" height="167" alt="Screenshot 2026-02-05 010644" src="https://github.com/user-attachments/assets/44cc42c1-5338-4e82-8fce-7a6a0fedc0fb" />
<img width="1796" height="117" alt="Screenshot 2026-02-05 010703" src="https://github.com/user-attachments/assets/b4638703-7a42-4366-9658-fbc24278c174" />
