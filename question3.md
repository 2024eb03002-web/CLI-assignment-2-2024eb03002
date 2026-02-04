Question 3 [6 Points]

Write a shell script validate_results.sh that reads student data from marks.txt.
Each line contains:RollNo, Name, Marks1,Marks2,Marks3Your script should:

• Print students who failed in exactly ONE subject

• Print students who passed in ALL subjects

• Print the count of students in each categoryPassing marks for each subject is 33.Use loops, conditionals, and arithmetic operations.

please excuse the lack of validate_results.sh file, it has been replaced by question3.sh file, i noticed too late. 

Working principle:- I have decided to count failures instead of passes to simplify the code because it reduces conditional complexity. Through skipping of header, i can prevent invalid numeric comparison since the header is only for our reference pov. 

created marks.txt file

using nano, i created a marks.txt file, giving random values, while ensuring i can have failed in one cases. 
<img width="977" height="40" alt="Screenshot 2026-02-05 001839" src="https://github.com/user-attachments/assets/5c9b71e9-ab42-4414-91de-db3ac0298477" />

<img width="1858" height="219" alt="Screenshot 2026-02-05 001735" src="https://github.com/user-attachments/assets/cdc2f8c2-eb9b-4ff0-8565-6f22e7abcf53" />

main .sh file


command 

    IFS=',' read -r
explanation:- Reads comma separated values safely. It does not interpret escape characters

command 

    [ "$mark" -lt 33 ]
explanation:- Performs integer comparisons to determine pass/fail conditions

command 

     ((count++))
explanation:- just an increment counter used in this context to track student performances in diff categories. 

command 

    continue 
explanation:- used to skip the header line so as to not cause errors and to prevent incorrect numeric comparisons

making of the .sh file:-

using nano i created a .sh file. 

<img width="864" height="38" alt="Screenshot 2026-02-05 001830" src="https://github.com/user-attachments/assets/30b3d063-f997-4065-a4de-9a3eac76bf11" />

complete code:-
<img width="1721" height="815" alt="Screenshot 2026-02-05 001658" src="https://github.com/user-attachments/assets/5e3db912-fb9c-41c7-b484-d538caf1dd9b" />
<img width="1919" height="88" alt="Screenshot 2026-02-05 001714" src="https://github.com/user-attachments/assets/7ac56560-fb00-4d8b-a8ae-6ed594a47993" />

output

the output shows the amount of all passed and one failed, along with the names of the students who have passed in all subjects. 

<img width="1110" height="226" alt="Screenshot 2026-02-05 001816" src="https://github.com/user-attachments/assets/d7ef7a3f-4c64-4d63-b47f-298361b64b6e" />

