# Lab Report 4: Managing the Command Line
## This lab report demonstrates steps and ways to do some tasks all from the command line

## 1) Log into ieng6:

<img src="ieng6.png" width="400" height="200">

What I did to do this operation:
* Press <up> - The `ssh cs15lsp23cb@ieng6.ucsd.edu` command was 1 up in the search history,
  so I used the up arrow to access it on the terminal.
* Press <return>

## 2) Cloning fork into repository:

<img src="clonefork.png" width="400" height="100">

What I did to do this operation:
* Copied the URL `https://github.com/ucsd-cse15l-s23/lab7` on the web browser by pressing `command` then `c`
* Type `git clone` and copied the URL by pressing `command` v, into the command line on the terminal.
* Press <return>

## 3) Running the test file (test fails):

<img src="runTestFail.png" width="400" height="200">
  
What I did to do this operation:
* Copied the `javac -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar *.java` by pressing `command` then `c`,
  from the file `test.sh` in the GitHub repository (in web browser).
* Press `command` then `v` to copy the command into the terminal command line.
* Press <return> to compile the test file.
* Copied the `java -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore ListExamplesTests`
  by pressing `command` then `c`, from the file `test.sh` in the GitHub repository (in web browser).
* Press `command` then `v` to copy the command into the terminal command line.
* Press <return> to run the test file.
* Shows that the test failed.

   
## 4) Edit code in Vim:

<img src="fixedCode.png" width="400" height="300">

## 5) Running the test file (test succeeds):

<img src="runTestSuccess.png" width="400" height="200">

## 6) Commit and Push change to Github:

<img src="gitCommitPush.png" width="400" height="300">
