Question 2 [6 Points]

You are given a log file containing entries in the format:

YYYY-MM-DD HH:MM:SS LEVEL MESSAGE

Example:

2025-01-12 10:15:22 INFO System started

2025-01-12 10:16:01 ERROR Disk not found

2025-01-12 10:16:45 WARNING High memory usage

2025-01-12 10:17:10 ERROR Network timeout

Requirements:

1. The script must accept the log file name as a command-line argument.

2. Validate that the file exists and is readable.

3. Count and display:

  - Total number of log entries

  - Number of INFO, WARNING, and ERROR messages

4. Display the most recent ERROR message.

5. Generate a report file named logsummary_<date>.txt.

6. Handle errors gracefully with meaningful messages.


Working principle:- Through the use of counting keywords and storing output in dated file, i was essentially able to help identify severity distribution and improve traceability of file. 

created a log.txt file

i used the nano command to create a log.txt file for sample data utilising the one that was given in the question. 

<img width="628" height="27" alt="Screenshot 2026-02-05 002020" src="https://github.com/user-attachments/assets/688c9757-19b5-4602-bc7a-524696122611" />
contents of file
<img width="1919" height="251" alt="Screenshot 2026-02-04 234820" src="https://github.com/user-attachments/assets/c091346b-2e42-48e7-9f9b-528787d20da0" />


Main .sh file

command 

    wc -l < logfile
explanation:- counts total number of log entries efficiently without printing filenames. 

command 

     grep -c "ERROR"
explanation:- counts occurences of a specific keyword in the log file, in this case the word "ERROR"

command 

     tail -1
explanation:- Extracts the most recent matching log entry. 

command 

    date +%Y-%m-%d
explanation:- used to generate the current data used in the output file for the code. 

making of .sh file
<img width="943" height="41" alt="Screenshot 2026-02-05 002004" src="https://github.com/user-attachments/assets/289a7c3f-09c7-4901-8498-4bf1ad80e337" />

complete code:- 
<img width="1609" height="742" alt="Screenshot 2026-02-04 234751" src="https://github.com/user-attachments/assets/f0bd43fc-984a-48fd-b152-001207183306" />


execution of the file, with output
<img width="966" height="173" alt="Screenshot 2026-02-04 234805" src="https://github.com/user-attachments/assets/cf52e16e-978d-44c8-8f4b-22cde68b7d0c" />

visible in log summary also

used the nano command to open and check the output file. confirmed that it was indeed printed. 
<img width="1471" height="197" alt="Screenshot 2026-02-04 234724" src="https://github.com/user-attachments/assets/2e325ffa-cd4b-4190-8f74-c50ac2bbfd17" />



