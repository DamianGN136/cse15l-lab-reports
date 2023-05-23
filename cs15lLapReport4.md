Lab Report 4   


Going through the tasks starting at step 4:  

4. Logging into my ieng6 account:  

![step1](https://github.com/DamianGN136/cse15l-lab-reports/blob/main/Screen%20Shot%202023-05-22%20at%204.17.08%20PM.png)

Here at the very top I type the ssh command and enter my login in this format: `local_computer_username`@`host_username`  

5. Clone the fork of your repository from you Github account:  

You're going to want to access your github account and then go into the forked repository. Once you're in the repository, copy the URL link.    

![step2](https://github.com/DamianGN136/cse15l-lab-reports/blob/main/Screen%20Shot%202023-05-22%20at%204.49.39%20PM.png). 

Once you do that, in your ieng6 terminal, use the git clone command and paste your URL like this:  

![ste1](https://github.com/DamianGN136/cse15l-lab-reports/blob/main/Screen%20Shot%202023-05-22%20at%204.54.47%20PM.png)  

As I demonstrated in the image, after cloning the repository you can use the `ls` command in your ieng6 terminal to see all your files and directories to confirm that you have successfully cloned the repository onto your computer   

6. Run the tests and demonstrate that they fail:  

In order to run the tests, you need to `cd` into the lab7 repository from your ieng6 terminal. Use the commnand `cd` + `lab7`  
You can then use the `ls` command to look at the files within the lab7 repository. To run the files you can use the command `javac *.java`. This will compile using javac, but instead of one specific file it will compile every .java file in the repository. In this case it will run the ListExamples.java and ListExamplesTest.java files since they are the only two .java files in the repository. When you run this command, the tests should fail and the output should look like this:  

![step3](https://github.com/DamianGN136/cse15l-lab-reports/blob/main/Screen%20Shot%202023-05-22%20at%205.34.03%20PM.png)  

7. Edit the code file to fix the failing test:  

To edit the file that contains an error, we have to use Vim to edit the file. To do this, I used the command `vim ListExamples.java`. Type the full name of the file including the file extension. After inputting the command, it should look like this:  

![step4](



