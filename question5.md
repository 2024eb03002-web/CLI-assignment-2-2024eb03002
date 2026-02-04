Question 5 [6 Points]

Create a shell script sync.sh to compare two directories dirA and dirB.Your script should:

• List files present only in dirA

• List files present only in dirB

• For files with the same name in both directories, check whether their contents matchDo NOT copy or modify files.Use diff, cmp, or checksum techniques.

Working Principle:- Through the usage of sorting, i was able to use the comm command through which we are able to ensure accurate comparison results. Through checking content with cmp, we can ensure logical correctness. Because the files are essentially in two different directories, they need not have the same content. 

creating two new directories along with files.

used the commands mkdir to create new directories. Through the usage of echo along with > symbol, i was effectively able to print a sentence and make a file at the same time.
<img width="1113" height="146" alt="Screenshot 2026-02-05 004351" src="https://github.com/user-attachments/assets/ae140dad-9c2e-4df7-ae65-08944069ee52" />

creating sync.sh file

command 

     ls dirA | sort
explanation:- lists files in a directory. then it sorts them alphabetically for accurate comparison. 

command 

     comm -23 file1 file2
explanation:- It compares and displays lines present only in the first file, i.e. lines unique to dirA

command 

     comm -13 file1 file2
explanation:- It displays lines present only in the second file. 

command 

     cmp file1 file2
explanation:- just compares two files byte-by-byte to detect differences in content

complete code:- 
<img width="1911" height="493" alt="Screenshot 2026-02-05 004332" src="https://github.com/user-attachments/assets/082ef339-b79b-4a4a-81d8-10d38ea1d77f" />


executing sync.sh +output

It presents us with the files exclusive to dirA and dirB while pointing out same files. 
<img width="1727" height="229" alt="Screenshot 2026-02-05 004403" src="https://github.com/user-attachments/assets/b668bbcf-078b-4a91-bb96-2b0f86a8d44e" />
