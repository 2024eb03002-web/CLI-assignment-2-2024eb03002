Question 7 [6 Points]

Write a shell script patterns.sh that reads a text file and:

• Writes words containing ONLY vowels into vowels.txt

• Writes words containing ONLY consonants into consonants.txt

• Writes words containing both vowels and consonants but starting with a consonant into mixed.txt, Case should be ignored while checking patterns.

Working principle:- 
I used a regex based logic. The specification that case should be ignored while checking patterns motivated me to use this particular logic. Through conversion to lowercase, we can ensure case insensitive comparison. Through splitting text into words, we can presevent partial matches inside sentences. 

made a input.txt file
used nano command to make an input.txt file.
used a cat command to easily display the txt file. 

<img width="1901" height="87" alt="Screenshot 2026-02-05 005147" src="https://github.com/user-attachments/assets/07449912-0d0a-4f84-9d7f-b616a10d587a" />


made a patterns.sh file\

command 

     tr 'A-Z' 'a-z'
explanation:- converts all uppercase letter to lowercase to make pattern matching case insensitive. 

command 

     tr -cs 'a-z' '\n'
explanation:- Replaces non alphabetic characters with newlines, through which, it divides sentences effectively into individual words. 

command 

     [[ "$word" =~regex ]]
explanation:-Uses Bash's regular expression matching to classify words based on vowel/consonant patterns

command 

     >> file.txt
explanation:- Appends matching words to the respective output file without any overwriting on existing content. 

complete code:-
<img width="1914" height="373" alt="Screenshot 2026-02-05 005831" src="https://github.com/user-attachments/assets/99387014-8c2b-40f4-b2e2-bbec8e3f1797" />

executed the file
<img width="1864" height="52" alt="Screenshot 2026-02-05 010042" src="https://github.com/user-attachments/assets/c4629e79-dded-4dce-b7f1-da6e5274d1a5" />

output

using cat command, basically showed execution of the file. 
<img width="1916" height="729" alt="Screenshot 2026-02-05 010028" src="https://github.com/user-attachments/assets/d28f6c51-5109-49b9-bc50-1f09d4cc2737" />
