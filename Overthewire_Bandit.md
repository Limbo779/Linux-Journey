## Level 0

- connect to server using ssh , "ssh bandit0@bandit.labs.overthewire.org -p 2220" 
- the above command asking host bandit.labs.overthewire.org to allow us to connect to bandit0 username at 2220 port

## Level 0 --> Level 1

- the file named readme has the password for next level
- this can be accesed using "cat" command after using ls to find all the available file

**Password to next level : ZjLjTmM6FvvyRnrb2rfNWOZOTa6ip5If**

**Command used : ls , cat**

## Level 1 --> Level 2

- the file named '-' has the password
- '-' can make the commandline confuse be because it will mistake it for flag stuffs
- so " cat /home/bandit1/'-' " gives the password , to deal to with stuff that will confuse the command line (like whitespace in file name) use quotation
- the current directory is found using 'pwd'

**Password to next level : 263JGJPfgU6LtdEvgfWU1XP5yac29mFx**

**Command used : pwd , cat , ls**

## Level 2 --> Level 3

- just like previous level the password is in '--spaces in this filename--'
- by the same technique as previous level command " cat /home/bandit2/'--spaces in this filename--' " will give the password

**Password to next level : MNk8KNH3Usiio41PRUEoDFPqfxLPlSmx**

**Command used : pwd , cat , ls**

## Level 3 --> Level 4

- i used "cd" to get into inhere/ direc 
- but using "ls" won't give any file names because they are hidden
- so using "ls -a" , where -a flag list all hidden files (usually dot files) , will give the file name '...Hiding-From-You' where password is present
- by using alias ll will execute command 'ls -al' , -al flag will combine -a and -l into one
- so finally command " cat /home/bandit3/inhere/'...Hiding-From-You' " will give the password (i used pwd to get current directory path)

**Password to next level : 2WmrDFRmJIq3IPxneAaMGhap0pFhF3NJ**

**Command used : ls -al , pwd , cat**

## Level 4 --> Level 5

- inside the inhere/ direc we have 10 files named '-file00' to '-file09'
- so using file command on each file will give you the details and type of the file
- " file /home/bandit4/inhere/'-file07' " command will give you the details of file '-file07'
- on checking for each file , '-file07' has ASCII Text type so it is human readable hence it has our password
- so command " cat /home/bandit4/inhere/'-file07' " will give us the password

**Password to next level : 4oQYVPkxZOOEOO5pTW81FB8j8lxXGUQw**

**Command used : ls , cd , pwd , file , cat**

