# **Lab Report 1 - Remote Access Tutorial**
## Welcome to CSE 15L! This page will guide you to log into your course-specific account on `ieng6`! 

## Step 1: Installing Visual Studio Code
To download and install VS Code, simnply visit their website [here!](https://code.visualstudio.com/),
and follow through with the instructions of your operating system (macOS or Windows). 

Once you have installed VS Code, make a new folder in your computer device. Then on your VSCode, open a new foler. You should be able to open it and view a window that looks like this: 

<img src="VSCode.png" width="500" height="300">

## Step 2: Connecting to a remote server 
By now, you should have obtained your course-specific account for CSE15L with your new password. 
```
Account username ex: `cs15lsp23cb@ieng.ucsd.edu` 
```
*If you are on Windows, please follow the instruction [here](https://gitforwindows.org/) to download `git`. Once it is installed, set your default terminal to use the new `git bash` that was just installed by following the instructions [here]( https://stackoverflow.com/questions/42606837/how-do-i-use-bash-on-windows-from-the-visual-studio-code-integrated-terminal/50527994#50527994). 


In your VSCode, open a new Terminal. 

<img src="NewTerminal.png" width="500" height="200">

Paste `ssh cs15lsp23zz@ieng6.ucsd.edu` in your command line, replacing `zz` with the two letters assigned in your course-specific account. 

As this would be your first time connecting, you will likely be promptted with a message that ends with 
```
Are you sure you want to continue connecting (yes/no/[fingerprint])?
Password:
```
Type **yes** on the command line and when it prompts `password:`, type in your new password (the password will not show on screen as you type it). 
Then this should appear on your terminal: 

<img src="ssh.png" width="300" height="200">


You are now connected remotely a computer in the CSE basement! This will allow any commands you run on your terminal to be run on the compuetr as well!

**Some errors you might find:**
The screen shot above shows a successful remote connection. However I did not use my course-specific account, but rather my regular student account in order to connect remotely. When I tried using my course-specific account, I kept running into this error message:

<img src="ssh.png" width="300" height="200">

We are still not sure why I am getting this error message, but if you happen to come across this error message, ask one of the tutors or even go to one of the TA's office hours. You can also ask a question on StemEd!

## Step 3: Run Some Commands!
This final step is for you try out so commands on the terminal! 
Here are some commands and their expected outputs that you can try: 
`cd`
(This command changes the current working directory to the user's home directory)

`cd~`
bash: cd~: command not found...
(This command produces "command not found" becuase I did not put a space before ~ when I should have. This command also changes the current working directory to the user's home directory)

`ls -lat`

<img src="ls-lat.png" width="300" height="200">
(This command lists the files and directories in the current working directory)

`ls -a`
![Image](las-a.png)

`ls <directory>`
![Image](ls <directory>.png)

(This command lists all the files in the specified directory (in this case Desktop). However my terminal in this case does not have access to my Desktop. This explains the screenshot above in which the ouput says "no such file or directory".)

`cp /home/linux/ieng6/cs15lsp23/public/hello.txt ~/`

`cat /home/linux/ieng6/cs15lsp23/public/hello.txt`
![Image](cp&cat.png)
(cp command copy files or directories from one location to another, in this case it copies the hello.txt file. cat command displays the contents of the file, as shown in the screenshot).


**To log out of the server and terminate the terminal:** 
* Ctrl-D
* Paste the command `exit`

## Yay! You are now set up for CSE15L :)
