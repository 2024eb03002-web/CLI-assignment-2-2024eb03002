Create a shell script emailcleaner.sh that processes emails.txt.

• Extract all valid email addresses and store them in valid.txt

• Extract invalid email addresses and store them in invalid.txt

• Remove duplicate entries from valid.txtValid email format:<letters_and_digits>@<letters>.comUse grep, sort, uniq, and redirection.

Working Principle:- Using regex, i am able to ensure correctness with minimal code. Email format validation is pattern based which is perfect for regex. Through the usage of two separate files, we can not only separate but also ensure readability. 


created emails.txt file, displayed below
<img width="1885" height="326" alt="Screenshot 2026-02-05 003349" src="https://github.com/user-attachments/assets/cdbe356c-b806-417e-bfbd-6321c2d5f2b1" />

created .sh file

command 

     grep -E 'regex' emails.txt
explanation:- Uses extended regular expressions to filter valid email addresses based on a set of parameters. 

command 

    sort | uniq
explanation:- used to sort email addresses and remove any possible duplicate entries

command 

     grep -v -E 'regex'
explanation:- selects lines which do not match the email patterns, essentially identifying invalid addresses. 

command 

     >
explanation:- redirects output to files as required 

<img width="900" height="41" alt="Screenshot 2026-02-05 003446" src="https://github.com/user-attachments/assets/4c46cd1e-dd35-48b9-97b3-1314677d24f8" />


complete code:-
<img width="1907" height="177" alt="Screenshot 2026-02-05 003423" src="https://github.com/user-attachments/assets/1aa8542b-7a71-456b-a9f8-30a4535fcc24" />

executed .sh file
<img width="976" height="61" alt="Screenshot 2026-02-05 003458" src="https://github.com/user-attachments/assets/41979771-7346-444b-9d78-3e4c6c804e4e" />

outputs

We receive two files i.e. valid.txt and invalid.txt. I have used nano to open the files for verification purposes in this case. 
valid.txt file
<img width="1910" height="206" alt="Screenshot 2026-02-05 003305" src="https://github.com/user-attachments/assets/7184c25d-9fe5-47b7-a49b-4ad4abc5a4f7" />

invalid.txt file
<img width="1911" height="160" alt="Screenshot 2026-02-05 003323" src="https://github.com/user-attachments/assets/4d52d4be-370f-408d-807e-29b3cbb938df" />

