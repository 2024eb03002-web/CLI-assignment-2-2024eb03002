Question 1

Create a shell script named analyze.sh that accepts exactly ONE command-line argument.

• If the argument is a file: – Display the number of lines, words, and characters in the file.

• If the argument is a directory: – Display the total number of files present. – Display the number of .txt files in the directory.

• If the argument count is invalid or the path does not exist: – Display an appropriate error message.

Working Principle:- The differentiation of a test file vs directory is important because different operations apply to each. This can help prevent invalid command execution. Through the suppression of errors we can ensure clear inputs. 

Created a txt file 
<img width="942" height="42" alt="Screenshot 2026-02-04 233854" src="https://github.com/user-attachments/assets/1ed87b01-d6be-4d74-9163-db58d578f592" />

main .sh file

command 

    -f and -d
explanation:- tests whether the given argument is a file or directory. 

command 

      wc 
explanation:- counts lines, words and characters in a file. 

command 

      ls *.txt
explanation:- Lists all text files within a directory. 

command 

      2>/dev/null
explanation:- suppresses any error messages when no .txt files are present allowing for seamless execution. 

creating a sh file

used nano command
<img width="919" height="41" alt="Screenshot 2026-02-04 233844" src="https://github.com/user-attachments/assets/f8195f9a-2feb-448a-8815-2c233864b282" />

sh file contents

complete code:-
<img width="1079" height="489" alt="Screenshot 2026-02-04 233826" src="https://github.com/user-attachments/assets/1b834d59-c078-4e8d-8732-22dfcde379b4" />

executing the shell file
<img width="963" height="29" alt="Screenshot 2026-02-04 233907" src="https://github.com/user-attachments/assets/561c5b53-0f4b-4962-b46d-16851a608aaa" />

output

output reflects file/ directory check
<img width="921" height="89" alt="Screenshot 2026-02-04 233917" src="https://github.com/user-attachments/assets/5bc7b69c-60f7-4133-87f2-3807b5d10089" />
