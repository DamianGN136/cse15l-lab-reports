Damian Nieto
LabReport 5

Part 1:

Student Request 

What environment are you using (computer, operating system, web browser, terminal/editor, and so on)?

I am working on a MacBook running MacOS. I am using the Chrome browser and also using VSCode as my terminal and editor. 

Detail the symptom you're seeing. Be specific; include both what you're seeing and what you expected to see instead. Screenshots are great, copy-pasted terminal output is also great. Avoid saying “it doesn't work”.

I am experiencing trouble trying to get my auto-grader to compile. I have written the bash script and and make sure that I get all my files within the grading-area file before compiling. But I keep getting this error:








I keep getting this error that seems to have something to do with junit. This is weird to me because I am already compiling my files using the junit libraries.

Detail the failure-inducing input and context. That might mean any or all of the command you're running, a test case, command-line arguments, working directory, even the last few commands you ran. Do your best to provide as much context as you can.

When running the bash script, I use this commend:

bash grade.sh https://github.com/ucsd-cse15l-f22/list-methods-lab3

The bash grade.sh is to run the bash file. The git hub link is the argument that my bash script takes. It clones the file and then grades it. In this case my code just checks to see if the desired file is in the git repository. This git hub repository link is the main repository I use to test my code. 

This is my code snippet:



The weird this is that everything worked fine during lab on the lab computers when I was logged into my ieng6 account. But now on my personal mac computer it doesn't work. I would really like some help solving this issue. Thank you in advance!

