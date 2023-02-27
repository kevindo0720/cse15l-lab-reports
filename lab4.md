# LAB REPORT 4

In this report, I will be reporting on how I followed the baseline steps as listed on CSE 15L's github page. 

Before all of the steps listed below, I already made sure to removed any fork I made of the repository. 

# PART 1 - ssh into remote account


![image](login)

Here I logged into my remote server account using `ssh cs15lwi23apn@ieng6.ucsd.edu`. I do not have to use password anymore since I already followed 
the instructions listed on the page to create a key and attach it to my github account.



# PART 2 - clone the lab7 repo 

Here is an image of me using `git clone` to clone into the repo of lab7

![image](gitclone)



# PART 3 - running the JUnit tests

After cloning, I began running the JUnit Tests on the ListExampleTests Files. I used the following commands:
```
javac -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar *.java
java -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore ListExamplesTests

```



It showed errors as expected:






