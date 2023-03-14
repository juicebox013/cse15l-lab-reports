# Lab Report 4 by Justin Nguyen
---
In today's lab, students were tasked with editing and compiling a file through the terminal as fast as they can.
To do this, students are first required to log into their remote account for the course. However, this process 
takes a while as you need to enter your password and load in. To speed up the process for a shorter time, we
want to eliminate this step by `generating an ssh key for our respective ieng6 account`. 

## Generating SSH Keys
1. The first step to generate an ssh key is to log into your ieng6 account using `ssh cs15lwi13xxx@ieng6.ucsd.edu`
2. Then, you should copy the path that is provided after the line "your public key has been saved in"
3. Once you have this saved, you must log out of the remote account and enter the line of code 
   `scp <path to your public SSH key> cs15lwi23xxx@ieng6.ucsd.edu:~/.ssh/authorized_keys`
   
Now you are able to log into your remote account without typing your password !

## Baseline Challenge Tasks
The next part of the lab was to edit and complete a code using only the terminal in the shortest amount of time possible. 

1. To begin, you must first create a fork of [this repository](https://github.com/ucsd-cse15l-w23/lab7). 
Once this repository has been forked, the timer begins !

2. The first step would be to log into your remote account for the course using `ssh cs15lwi13xxx@ieng6.ucsd.edu`. Unlike 
last time, we don't have to type in our password as we have generated an SSH key prior, saving us time. 

3. The next step would be to clone the forked repository in the remote server. Instead of manually typing out the URL of 
our forked repository, you can shorten the time spent by a tremendous amount if we copy the link and then type `git clone <tab>`

4. Once the repository has been cloned, we want to show that the JUnit tests for the files run correctly and fail. To do this, we need 
to first change into the correct repository using cd `l<tab>`. This will automatically finish the line of code to say `cd lab7`, which is the directory we changed into. Then, we want to run the copy the line of code `$ javac -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar *.java` and enter it into the terminal using. This compiles the code and now we want to run it using the line of code 
`java -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore ListExamplesTests`. Do the same thing as before and enter it to the terminal to show that the tests fail.

5. The next step would be to edit the code and fix it. To do this, we want to nano into the file by typing nano `List<tab>`. You will be prompted with a large amount of code and you can navigate down by holding down `<down key>` 33 times. Then you want to change the code to say `"index2 += 1"` instead of `"index1 += 1"`. To do this, press the `<right key>` 13 times and then press the `<delete>` key once. Then press `<2>`. Once you have done this, press `<enter>` and then save the file by entering `<control><x>`. this will 

6. The next step would be to save and compile the files once again to show that they work. Instead of re copying/pasting the code, you can 
keep pressing `<up>` until you reach the line of codes. When you compile and run it again, it should work fine.
   
7. The final steps would be to commit and push the files to github by entering `$ git add ListExamples.java` and `$ git commit -m "List Examples was edited"`
    
youre done !
