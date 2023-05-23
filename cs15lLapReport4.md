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

In order to run the tests, you need to `cd` into the lab7 repository from your ieng6 terminal. Use the commnand `cd lab7`  
You can then use the `ls` command to look at the files within the lab7 repository. To run the files you can use the command `javac *.java`. This will compile using javac, but instead of one specific file it will compile every .java file in the repository. In this case it will run the ListExamples.java and ListExamplesTest.java files since they are the only two .java files in the repository. When you run this command, the tests should fail and the output should look like this:  

![step3](https://github.com/DamianGN136/cse15l-lab-reports/blob/main/Screen%20Shot%202023-05-22%20at%205.34.03%20PM.png)  

7. Edit the code file to fix the failing test:  

To edit the file that contains an error, we have to use Vim to edit the file. To do this, I used the command `vim ListExamples.java`. Type the full name of the file including the file extension. After inputting the command, it should look like this:  

![step4](https://github.com/DamianGN136/cse15l-lab-reports/blob/main/Screen%20Shot%202023-05-22%20at%206.27.32%20PM.png)  

After entering the vim screen, the selector is at the bottom of the screen. To make the change we want (change index1 to index2 in the last while loop), we can use the following commands:  
Command 1: `?1 <Enter>`  
  *Note:* The `?` in the command searches for things backwards through the document (starting from the bottom). In this case we are searching for a number 1 to replace it with 2 in the last while loop. After searching for it, it will highlight the first occurence of 1 at the botom of the page. Then hit the enter key  

Command 2: `n`  
   *Note:* The `n` command locates the next iteration of the last thing you searched for. Since the cursor should be at the bottom of the page when you open up vim, n will select iterations of n going from down-upwards. In thise case, the iteration of 1 that we need to change is right after the first iteration found by the find command so we will only press n one time to select what we want to change. 

Command 3:`x`  
   *Note:* The `x` command deletes the character that your cursur currently has selected. This is useful since we want to get rid of the number 1 and then replace it with 2.  
   
Command 4/5: `i`, then insert the number 2, then `<Esc>`  
   *Note:* The `i` command allows you to enter insert mode in vim. This will allow you to actually add text or delete it and do any other edits. Insert mode will allow you to start making edits in the place your cursor is currently in. Since the previous steps already took us to the exact spot we want to change, we can just insert the number 2 right after going into insert mode. After inserting the numer 2, you can press the escape key to exit insert mode  
   
Command 6: `:wq`  
   *Note:* The `:wq` saves the edits you have made and then exits vim  


8. Run the tests demonstrating that they now succeed  

![step5](https://github.com/DamianGN136/cse15l-lab-reports/blob/main/Screen%20Shot%202023-05-22%20at%207.23.53%20PM.png)  

By using `javac *.java` again you can run the java files again. The tests should run and pass, but for whatever reason on my end they still don't run. It looks like it has something to do with junit but I'm not sure.  

9. Commit and push the resulting change to your Github account:  

After returning to the ieng6 terminal, I used the command `git add ListExamples.java`. This adds the files that you want to commit. Then I used `git commit -m "message"` to commit the  file that was changed. the -m part of the command allows you to put a commit message right after it. It can be anything. Then I used `git push -u origin main`. This command allows you to push committed changes onto a branch. the `u` part of the command means that this is the first time you are pushing onto this repository. The `origin` means that you are setting that branch as the origin of the push. The `main` is name of the branch you are pushing onto. It should look like this:  

![step6](https://github.com/DamianGN136/cse15l-lab-reports/blob/main/Screen%20Shot%202023-05-22%20at%208.32.51%20PM.png)  

For whatever reason, after using the push command I am promted with a username and password request. After inputting them it then tells me that password authentication was removed. I'm not sure how to fix it and I didn't get a chance to ask in lab. 





