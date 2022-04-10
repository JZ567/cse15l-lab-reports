

How to log into a course-specific account on `ieng6`. :tree:


### Installing Visual Studio Code
---
Visual Studio Code is a useful text editor that can be used to write, debug, and run code. To install VS Code, follow these steps:
1. Go to the Visual Studio Code [website](https://code.visualstudio.com/).
2. Click on the blue Download button on the top right corner of the website. Select the version to download that works with your computer.


![Download Button](Screenshot2.png)


3. Follow the remaining instructions given by VS Code to complete the installation. Once completed, you will be able to open the following page:

<br />

![VS Code](Screenshot3.png)

<br />

### Remotely Connecting
---
1. Open a terminal in VS Code by clicking Terminal --> New Terminal
2. Type `ssh cs15lsp22zzz@ieng6.ucsd.edu` into the terminal, replacing 'zzz' with the three unique letters you get for your account.
3. A message may pop up asking you if you want to continue connecting. Type `yes` and enter and then type your password. Now you should be remotely connected to a computer in the CSE basement.

The following should appear on your terminal once you have remotely connected:

<br />

![Connected](Screenshot4.png)

<br />

### Trying Some Commands
---
1. Try typing in some commands to the terminal. Some commands to try are `cd`, `ls`, `pwd`, `mkdir`, `cp`, and their variations.
2. One example of a command I ran was the `pwd` command which printed the path to the current folder I was in.
<br />

![pwd](Screenshot5.png)

### Moving files with scp
---
1. Log out of the remote server by typing `exit` and hitting enter
2. To move a file from your local computer to the server, type `scp filename.java cs15lsp22zzz@ieng6.ucsd.edu` replacing filename with the name of the file you wish to move and 'zzz' with the unique letters for your account.
<br />

An example is shown in the images below. The first screenshot shows running a file called WhereAmI.java from the client and then running the scp command on the WhereAmI file. The second screenshot shows connecting to the server and shows that the file WhereAmI.java is now there. Then WhereAmI.java is run from the remote server.
<br />

![image](Screenshot6.png)
<br />
![image](Screenshot7.png)

### Setting an SSH Key
In order to avoid having to type in a password everytime the ssh or scp command is run, we will set up an ssh key.
1. On your local computer, type `ssh-keygen`. 
2. You will be prompted to enter a file. Here, you type `/Users/<user-name>/.ssh/id-rsa` replacing user-name with the username on your local computer.
3. Do not enter a passphrase. Just click enter to skip.
4. Next run the ssh command as usual to log into the server.
5. Type `mkdir .ssh`
6. Logout of the server
7. Type `scp /Users/<user-name>/.ssh/id_rsa.pub cs15lsp22zzz@ieng6.ucsd.edu:~/.ssh/authorized_keys`, replacing user-name with the username on your local computer and 'zzz' with your unique letters.

Now you should be able to log into the server without a password, like this:
<br />

![image](Screenshot8.png)

<br />

### Optimizing Remote Running
Now we will try to run the commands with fewer keystrokes. Some examples of things you can do to speed up the remote running are:
* Writing a command in quotes ("") after the ssh command, to run it from the server, and then exit the server
* Separate multiple commands on the same line with semicolons
* Use the up arrow to recall previous commands

<br />

An example of copying the WhereAmI.java file to the server and running it from there using these tricks is shown below:
![image](Screenshot9.png)

<br />
<br />

This is the end of Lab Report 1. Thank you for reading! :) 
