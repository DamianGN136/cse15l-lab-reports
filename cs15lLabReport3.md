Lab Report 3  
---
For this lab report I have chosen to research the `find` command  


1st command line operation: `find -name`  
-
Use: This use of find looks for files or directories with a specific names/patterns. Here are two examples of how you could use the `find -name` command:  

1. You can use `find -name` to find one specific file. For example, in the /technical directory. I want to see if a file called "chapter-1.txt" exists within this repository.
This woud be my input and output:  

```
[cs15lsp23eu@ieng6-202]:technical:643$ find /home/linux/ieng6/cs15lsp23/cs15lsp23eu/docsearch/technical -name "chapter-1.txt"
/home/linux/ieng6/cs15lsp23/cs15lsp23eu/docsearch/technical/911report/chapter-1.txt
```

As you can see, the terminal outputed my file that I was looking more which means that "chapter-1.txt" does exist within the /technical directory. 

2. You can also use this `find -name` to find all files with a specific patter. For example, if I wanted to find all the java files within 
the wavelet repository, this would be my input and output:  

```
[cs15lsp23eu@ieng6-202]:technical:645$ find /home/linux/ieng6/cs15lsp23/cs15lsp23eu/docsearch/technical -name "*.txt"
/home/linux/ieng6/cs15lsp23/cs15lsp23eu/docsearch/technical/biomed/1471-2334-1-13.txt
/home/linux/ieng6/cs15lsp23/cs15lsp23eu/docsearch/technical/biomed/1471-2334-1-17.txt
/home/linux/ieng6/cs15lsp23/cs15lsp23eu/docsearch/technical/biomed/1471-2334-1-21.txt
/home/linux/ieng6/cs15lsp23/cs15lsp23eu/docsearch/technical/biomed/1471-2334-1-24.txt
/home/linux/ieng6/cs15lsp23/cs15lsp23eu/docsearch/technical/biomed/1471-2334-1-9.txt
/home/linux/ieng6/cs15lsp23/cs15lsp23eu/docsearch/technical/biomed/1471-2334-2-1.txt
/home/linux/ieng6/cs15lsp23/cs15lsp23eu/docsearch/technical/biomed/1471-2334-2-24.txt
/home/linux/ieng6/cs15lsp23/cs15lsp23eu/docsearch/technical/biomed/1471-2334-2-26.txt
/home/linux/ieng6/cs15lsp23/cs15lsp23eu/docsearch/technical/biomed/1471-2334-2-27.txt
/home/linux/ieng6/cs15lsp23/cs15lsp23eu/docsearch/technical/biomed/1471-2334-2-29.txt
/home/linux/ieng6/cs15lsp23/cs15lsp23eu/docsearch/technical/biomed/1471-2334-2-5.txt
/home/linux/ieng6/cs15lsp23/cs15lsp23eu/docsearch/technical/biomed/1471-2334-2-6.txt
/home/linux/ieng6/cs15lsp23/cs15lsp23eu/docsearch/technical/biomed/1471-2334-2-7.txt
/home/linux/ieng6/cs15lsp23/cs15lsp23eu/docsearch/technical/biomed/1471-2334-3-10.txt
/home/linux/ieng6/cs15lsp23/cs15lsp23eu/docsearch/technical/biomed/1471-2334-3-11.txt
/home/linux/ieng6/cs15lsp23/cs15lsp23eu/docsearch/technical/biomed/1471-2334-3-12.txt
/home/linux/ieng6/cs15lsp23/cs15lsp23eu/docsearch/technical/biomed/1471-2334-3-13.txt
/home/linux/ieng6/cs15lsp23/cs15lsp23eu/docsearch/technical/biomed/1471-2334-3-15.txt
/home/linux/ieng6/cs15lsp23/cs15lsp23eu/docsearch/technical/biomed/1471-2334-3-9.txt
/home/linux/ieng6/cs15lsp23/cs15lsp23eu/docsearch/technical/biomed/1471-2350-2-11.txt
```
As you can see, the terminal displayed all the .txt files in the wavelet repository. In the argument I used for `find -name`, the asterisk 
before the ".txt" acts as a place holder for any text that might come before the '.txt' signature.  (note: the files above were not the only ones found. There were just too many to paste all in this report.)


2nd command line operations: `find -type`  
-

Use: `find -type`, as you may have guessed, allows you to find specific file types. These are some different example uses of `-type`:  

1. You can use `find -type` to find specifically all the directories in the specified directory. For example, if I wanted to display all 
the directories inside the "government" directory thats within the stringsearch-data/technical/ directory on my ieng6 account, I would use the following
command and get the following output:  


```
[cs15lsp23eu@ieng6-202]:~:548$ find /home/linux/ieng6/cs15lsp23/cs15lsp23eu/stringsearch-data/technical/government -type d 
/home/linux/ieng6/cs15lsp23/cs15lsp23eu/stringsearch-data/technical/government
/home/linux/ieng6/cs15lsp23/cs15lsp23eu/stringsearch-data/technical/government/About_LSC
/home/linux/ieng6/cs15lsp23/cs15lsp23eu/stringsearch-data/technical/government/Alcohol_Problems
/home/linux/ieng6/cs15lsp23/cs15lsp23eu/stringsearch-data/technical/government/Env_Prot_Agen
/home/linux/ieng6/cs15lsp23/cs15lsp23eu/stringsearch-data/technical/government/Gen_Account_Office
/home/linux/ieng6/cs15lsp23/cs15lsp23eu/stringsearch-data/technical/government/Media
/home/linux/ieng6/cs15lsp23/cs15lsp23eu/stringsearch-data/technical/government/Post_Rate_Comm
```

As you can see, after specifying the directory, I used the `-type d` command. The `d` after the `-type` specifies the directory file type.  

2. You can also use the `-type` command to find specifically all the regular files in a directory. For example, if I wanted to find all the regular files inside 
the 911 directory report that is also inside the technical directory, I would use the following command and get the following output:  

```
[cs15lsp23eu@ieng6-202]:911report:556$ find /home/linux/ieng6/cs15lsp23/cs15lsp23eu/stringsearch-data/technical/911report -type f
/home/linux/ieng6/cs15lsp23/cs15lsp23eu/stringsearch-data/technical/911report/chapter-1.txt
/home/linux/ieng6/cs15lsp23/cs15lsp23eu/stringsearch-data/technical/911report/chapter-10.txt
/home/linux/ieng6/cs15lsp23/cs15lsp23eu/stringsearch-data/technical/911report/chapter-11.txt
/home/linux/ieng6/cs15lsp23/cs15lsp23eu/stringsearch-data/technical/911report/chapter-12.txt
/home/linux/ieng6/cs15lsp23/cs15lsp23eu/stringsearch-data/technical/911report/chapter-13.1.txt
/home/linux/ieng6/cs15lsp23/cs15lsp23eu/stringsearch-data/technical/911report/chapter-13.2.txt
/home/linux/ieng6/cs15lsp23/cs15lsp23eu/stringsearch-data/technical/911report/chapter-13.3.txt
/home/linux/ieng6/cs15lsp23/cs15lsp23eu/stringsearch-data/technical/911report/chapter-13.4.txt
/home/linux/ieng6/cs15lsp23/cs15lsp23eu/stringsearch-data/technical/911report/chapter-13.5.txt
/home/linux/ieng6/cs15lsp23/cs15lsp23eu/stringsearch-data/technical/911report/chapter-2.txt
/home/linux/ieng6/cs15lsp23/cs15lsp23eu/stringsearch-data/technical/911report/chapter-3.txt
/home/linux/ieng6/cs15lsp23/cs15lsp23eu/stringsearch-data/technical/911report/chapter-5.txt
/home/linux/ieng6/cs15lsp23/cs15lsp23eu/stringsearch-data/technical/911report/chapter-6.txt
/home/linux/ieng6/cs15lsp23/cs15lsp23eu/stringsearch-data/technical/911report/chapter-7.txt
/home/linux/ieng6/cs15lsp23/cs15lsp23eu/stringsearch-data/technical/911report/chapter-8.txt
/home/linux/ieng6/cs15lsp23/cs15lsp23eu/stringsearch-data/technical/911report/chapter-9.txt
/home/linux/ieng6/cs15lsp23/cs15lsp23eu/stringsearch-data/technical/911report/preface.txt
```

As you can see, the output was all the reglar files inside the 911report directory. I could have also used the `file -name "*.txt"` command to do this.  

3rd command line operation: `find -size`
-

Use: the `find -size` is used to find files that are smaller or larger then a specified size. Here are two examples of how to use this command:  

1. You can use `-size` to find files that are smaller then a specified size. For example, if I wanted to find files inside the /technical directory that are smaller 
then 2 kilobytes, this would be my input command and the output:  

```
[cs15lsp23eu@ieng6-202]:~:575$ find /home/linux/ieng6/cs15lsp23/cs15lsp23eu/stringsearch-data/technical -type f -size -2k
/home/linux/ieng6/cs15lsp23/cs15lsp23eu/stringsearch-data/technical/plos/pmed.0020191.txt
/home/linux/ieng6/cs15lsp23/cs15lsp23eu/stringsearch-data/technical/plos/pmed.0020226.txt
```

As you can see, the terminal returned the only 2 files that are smaller then 2 kilobytes. Before the `-size` command, I also used the `-type` command to specify that I only 
wanted to find regular type files. Also, notice the minus sign. This is to specify that you want files *smaller* then you specified size. 

2. You can also use `-size` to find files that are larger then a specifies size. For example, if I wanted to find files inside the /technical directory that are larger then 
150 kilobytes, this would be my input and output:  

```
[cs15lsp23eu@ieng6-202]:~:580$ find /home/linux/ieng6/cs15lsp23/cs15lsp23eu/stringsearch-data/technical -type f -size +150k
/home/linux/ieng6/cs15lsp23/cs15lsp23eu/stringsearch-data/technical/911report/chapter-13.4.txt
/home/linux/ieng6/cs15lsp23/cs15lsp23eu/stringsearch-data/technical/911report/chapter-13.5.txt
/home/linux/ieng6/cs15lsp23/cs15lsp23eu/stringsearch-data/technical/911report/chapter-3.txt
/home/linux/ieng6/cs15lsp23/cs15lsp23eu/stringsearch-data/technical/government/About_LSC/commission_report.txt
/home/linux/ieng6/cs15lsp23/cs15lsp23eu/stringsearch-data/technical/government/Env_Prot_Agen/bill.txt
/home/linux/ieng6/cs15lsp23/cs15lsp23eu/stringsearch-data/technical/government/Env_Prot_Agen/multi102902.txt
/home/linux/ieng6/cs15lsp23/cs15lsp23eu/stringsearch-data/technical/government/Env_Prot_Agen/tech_adden.txt
/home/linux/ieng6/cs15lsp23/cs15lsp23eu/stringsearch-data/technical/government/Gen_Account_Office/GovernmentAuditingStandards_yb2002ed.txt
/home/linux/ieng6/cs15lsp23/cs15lsp23eu/stringsearch-data/technical/government/Gen_Account_Office/Statements_Feb28-1997_volume.txt
/home/linux/ieng6/cs15lsp23/cs15lsp23eu/stringsearch-data/technical/government/Gen_Account_Office/d01591sp.txt
/home/linux/ieng6/cs15lsp23/cs15lsp23eu/stringsearch-data/technical/government/Gen_Account_Office/pe1019.txt
```

As you can see, the terminal returned all the files in the /technical directory that were over 150 kilobytes. Again, I used the 
`-type` command before to specify that I want regular files found, and also notice the plus sign. This is to specify that I want files *larger* 
then the specified size.  

4th command line argument:  `find -mtime` 
-

Use: the `-mtime` command is used to find files that were modified before the specified amount of time. These are some examples:  

1. If I wanted to find all the files in /technical that were modified more then 21 days ago, this would be my input and output:  

```
[cs15lsp23eu@ieng6-202]:~:615$ find /home/linux/ieng6/cs15lsp23/cs15lsp23eu/stringsearch-data/technical -type f -mtime -21
/home/linux/ieng6/cs15lsp23/cs15lsp23eu/stringsearch-data/technical/biomed/1471-2334-1-13.txt
/home/linux/ieng6/cs15lsp23/cs15lsp23eu/stringsearch-data/technical/biomed/1471-2334-1-17.txt
/home/linux/ieng6/cs15lsp23/cs15lsp23eu/stringsearch-data/technical/biomed/1471-2334-1-21.txt
/home/linux/ieng6/cs15lsp23/cs15lsp23eu/stringsearch-data/technical/biomed/1471-2334-1-24.txt
/home/linux/ieng6/cs15lsp23/cs15lsp23eu/stringsearch-data/technical/biomed/1471-2334-1-9.txt
/home/linux/ieng6/cs15lsp23/cs15lsp23eu/stringsearch-data/technical/biomed/1471-2334-2-1.txt
/home/linux/ieng6/cs15lsp23/cs15lsp23eu/stringsearch-data/technical/biomed/1471-2334-2-24.txt
/home/linux/ieng6/cs15lsp23/cs15lsp23eu/stringsearch-data/technical/biomed/1471-2334-2-26.txt
/home/linux/ieng6/cs15lsp23/cs15lsp23eu/stringsearch-data/technical/biomed/1471-2334-2-27.txt
//more files...
```

As you can see, this command returns a lot of files. I only pasted a few of them, but this command essentially returned every single file in the /technical directory because they were all 
last changed 21 days ago. There were so many files that they didn't all fit in the terminal. Anyways, in the command I specified -21, which means more then 21 days ago.  

2. You can also use the `-mtime` command in tandem witht the `exec` command which allows us to execute functions on files. For example, if I wanted to find every file that was modified more 
than 21 days ago and delete them, this is what the input and output would be:  

```
[cs15lsp23eu@ieng6-202]:~:617$ find /home/linux/ieng6/cs15lsp23/cs15lsp23eu/stringsearch-data/technical -type f -mtime -21 -exec rm {} \;
[cs15lsp23eu@ieng6-202]:~:618$ cd stringsearch-data/
[cs15lsp23eu@ieng6-202]:stringsearch-data:619$ cd technical/
[cs15lsp23eu@ieng6-202]:technical:620$ ls
911report  biomed  government  plos
[cs15lsp23eu@ieng6-202]:technical:621$ cd 911report/
[cs15lsp23eu@ieng6-202]:911report:622$ ls
[cs15lsp23eu@ieng6-202]:911report:623$ cd /home/linux/ieng6/cs15lsp23/cs15lsp23eu/stringsearch-data/technical
[cs15lsp23eu@ieng6-202]:technical:624$ cd biomed
[cs15lsp23eu@ieng6-202]:biomed:625$ ls
[cs15lsp23eu@ieng6-202]:biomed:626$ cd /home/linux/ieng6/cs15lsp23/cs15lsp23eu/stringsearch-data/technical
[cs15lsp23eu@ieng6-202]:technical:627$ cd government
[cs15lsp23eu@ieng6-202]:government:628$ ls
About_LSC  Alcohol_Problems  Env_Prot_Agen  Gen_Account_Office  Media  Post_Rate_Comm
[cs15lsp23eu@ieng6-202]:government:629$ cd /home/linux/ieng6/cs15lsp23/cs15lsp23eu/stringsearch-data/technical
[cs15lsp23eu@ieng6-202]:technical:630$ cd plos
[cs15lsp23eu@ieng6-202]:plos:631$ ls
[cs15lsp23eu@ieng6-202]:plos:632$
```

As you can see, when I try to cd into each directory inside of /technical and use the ls command to see what files are inside each directory, all but 1 come up blank with no files. 
The government directory is the only one that is not empty because in our command, we specified that we wanted to find regular files, and the government directory is full of sub directories. 
Every other directory in /technical is now empty though. The curly braces in the `-exec` command are a place holder for the file that is being processed by the `-exec` 
command. The forward slash espaces the semi-colon that marks the end of the exec command.  

Sources
-
* https://man7.org/linux/man-pages/man1/find.1.html
* https://chat.openai.com/

