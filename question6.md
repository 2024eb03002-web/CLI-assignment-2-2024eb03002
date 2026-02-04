Question 6 [6 Points]

Create a shell script metrics.sh that analyzes a text file input.txt.The script should display:
• Longest word

• Shortest word

• Average word length

• Total number of unique wordsUse pipes and commands such as tr, sort, uniq, wc.

Working Principle:- Through the usage of tr and awk commands, i was able to clean and tokenize input and handle numeric computation efficiently respectively. Through the usage of sorting, i was able to simplify finding the longest and shortest words easily. 

created input.txt file
<img width="1901" height="87" alt="Screenshot 2026-02-05 005147" src="https://github.com/user-attachments/assets/c899ce07-31ef-4438-8a61-357d3d466bd3" />

created a metrics.sh file

command 

     tr -cs '[:alpha:]' '\n'
explanation:- It basically splits the input text into individual words by replacing non alphabetic characters with newlines. separating words to reduce partial comparisons. 

command 

     awk '{print length, $0}'
explanation:- It calculates the length of each word and prints them both i.e. the length and the word. 

command 

     sort -nr
explanation:-Sorts the numeric values in reverse order to essentially identify the longest word. 

command 

     wc -l
explanation:-Used to count unique words line by line

command 

     awk '{s+=length} END {print s/NR}'
explanation:-computes the avg word length by summing up character counts and dividing by total words 

complete code:-
<img width="1919" height="256" alt="Screenshot 2026-02-05 005245" src="https://github.com/user-attachments/assets/3d18908b-b383-4340-bbe0-74a6a0c132e5" />

executed the metrics.sh file along with output

the output reflects the longest word along with the avg word and unique words in the input.txt file. 

<img width="1587" height="169" alt="Screenshot 2026-02-05 005343" src="https://github.com/user-attachments/assets/712fbd3c-2f34-43a6-96a6-1516de45852d" />
