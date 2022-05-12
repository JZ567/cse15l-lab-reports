# Lab Report 3

## Streamlining ssh Configuration

In this part of the lab, we changed the ssh login so that we would only have to type 'ieng6' instead of the entire 12 character username

Screenshot of .ssh/config file: 

![screenshot](Screenshot3rdRprt1.png)

<br />


Screenshot of ssh command logging me into my account:

![screenshot](Screenshot3rdRprt2.png)

<br />

Screenshot of scp command with alias:

![screenshot](Screenshot3rdRprt3.png)

<br />

## Setup Github Access from ieng6

In this part of the lab, we set up Github access from the ieng6 account, so that we can type git commands in the terminal to commit and push from the command line.

First, I created an ssh key from my ieng6 account.
Then, I typed in `cat ~/. ssh/id_rsa.pub` to copy the contents of id_rsa.pub to my clipboard and added it to Github.

![screenshot](Screenshot3rdRprt4.png)
![screenshot](Screenshot3rdRprt5.png)

<br />

Running git commands to commit and push a change to Github while logged into ieng6 account:

![screenshot](Screenshot3rdRprt10.png)

<br />

Link to the commit: [link](https://github.com/JZ567/markdown-parser-2/blob/main/MarkdownParse.java)

## Copy whole directories with scp -r

For this step, we copied the whole markdown-parser-2 directory with the scp command to the ieng6 server.

![screenshot](Screenshot3rdRprt6.png)

<br />

We can then compile and run the tests from the ieng server.
![screenshot](Screenshot3rdRprt7.png)

<br />

Lastly, we can combine these steps into one line:
![screenshot](Screenshot3rdRprt8.png)
