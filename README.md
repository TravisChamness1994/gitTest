# GitHub Introduction

### By Robert Trujillo, Alexander Sullivan, Arthur Hui and Travis Chamness

****"GitHub is a code hosting platform for version control and collaboration. It lets you and others work together on projects from anywhere." - guides.github.com****

This tutorial is created in the perspective of the linux terminal and may vary slightly for Mac or Windows users.

Learning to use github is a skill that is useful professionally and personally. This small tutorial will go over the basics of how to use github.

### Where to starts?

Begin by setting up an account at github.com. The account is free, and if you are using this professionally be sure to use a good username. GitHubs can act as a boost to your resume so take advantage of this if it fits your needs. The topics covered here will be primarily based on using the terminal to navigate github. 

### Installing Git

For Linux Debian - In terminal enter ```sudo apt-get install git```

For Linux Fedora - In terminal enter ```sudo yum install git```

For Mac - go to http://git-scm.com/download/mac

For Windows - got to http://git-scm.com/download/win

### Setting up git

We recommend before you begin creating local repositories that you first create a directory for your repositories. I created my directory at the terminal root. You can get to the root with ```$ cd ~``` command in Linux. The directory you choose to create can be named anything, but in keeping with context I chose to name my directory GitHub. Make the directory using ```$ mkdir <Directory Name>```  EX: ```$ mkdir GitHub ```in the command line and will produce a new directory of the ```Directory Name``` you have given. Enter the directory by now entering ```$ cd <Directory name>``` EX: ```$ cd GitHub```. This will be where we create our local repositories. 

Now that git is installed and set on the machine, it is important to give the user identity information. This information will be immutably added to anything added to git by the user. To ***set user information*** such as the user's name and email, use the ```git config --global``` option. 

To set the user's name to the git, use ```git config --global user.name "<Name>"``` 
Ex: ```git config --global user.name "Travis Chamness"```. 

To set the user's email, use ```git config --global user.name <email>```
Ex: ```git config --global user.email travischamness@email.com```.

Check your details successfully updated by entering ```git config --list``` which will display your git configuration information.

Ex:
```
user.name=Travis Chamness
user.email=travischamness@email.com
color.status=auto
color.branch=auto
color.interactive=auto
color.diff=auto
...
```

### Initializing a local git repository

Creating a local repository is done by entering ```$ git init <Repository Name>``` EX: ```$ git init gitTest```.  This is very much the same as creating a new directory and will appear in your repository directory that we created in the previous step. Check to make sure it was created by entering ```$ ls``` into the terminal. You should now see your created repository.

### Using the local repository

Enter the initialized repository using ```$ cd <Repository Name>``` where you can add files using the terminal. Once you have created or moved files to the repository, it is time to ***stage*** your git files. Staging is a term that describes preparing your files to be committed to your git repository. To stage, you will use the ```$ git add <File Name>``` command EX: ```$ git add helloWorld.c```. This will prepare the files added to be committed to your git repository. You can do this to multiple files at a time by entering a space between file names or truncate with the * symbol. EX: ```$ git add *.c``` adds any c files in the directory or ```$ git add *``` to add all files in the directory to the staging area. Lets make sure we successfully added files to the staging aread by entering ```$ git status``` into the terminal. This will display information on the repository such as the branch, commits, and the files to be commited which are the files added. EX: if adding a helloc.c file to the staging are, the process would start by adding the hello.c file with ```$ git add hello.c```, entering the ```$ git status``` command to check that the hello.c file was successfully staged and waiting to be commited under the "changes to be committed" portion. This command would produce the following output showing our added files.
```
On branch master
Your branch is up to date with 'origin/master'.

Changes to be committed:
  (use "git reset HEAD <file>..." to unstage)

        new file:   hello.c
```

***The next step is to commit the staged files.*** Commiting our added files will save them to our local repository for safe storage. To commit the file or files, use the ```git commit``` command to send the staged files to the repository. However, to commit, a commit message will always be needed. The commit message will provide context to what is being committed. To commit the hello.c file shown above, the command would be...

(Consider the state of your program and what has been modified in the commit message.)

```$ git commit -m "First commit for hello world program. Project complete."```

where ```-m``` is the message option for the commit which allows the user to incorporate the commit message in the command.  It is not mandatory to add the message this way, but may be the easiest method. Without adding the message option, a Vim text editor will be opened to prompt the user to add a message at the top of the file. 

Once committed, the version is now saved in your local repository. ***As the local repository accumulates, the commits and commit information can be viewed*** with the ```git log``` command which will produce a log in the following format.

```
[Comp:Folder User$ git log
commit 54b11d42e12dc6e9f070a8b5095a4492216d5320
Author: author <author@gmail.com>
Date:   Fri Jul 8 23:42:22 2016 +0300

This is last commit message

commit fd6cb176297acca4dbc69d15d6b7f78a2463482f
Author: author <author@gmail.com>
Date:   Fri Jun 24 20:20:24 2016 +0300

This is previous commit message

commit ab0de062136da650ffc27cfb57febac8efb84b8d
Author: author <author@gmail.com>
Date:   Thu Jun 23 00:41:55 2016 +0300

This is previous previous commit message
...
```
credit: https://stackoverflow.com/questions/2007662/rollback-to-an-old-git-commit-in-a-public-repo by Igor

The git log will become a useful way to track what has happened and by whome when working in the company of others. First, a remote repository must be created.

### Lets begin setting up your first remote repository! 

To start a remote repository, go to your profile at github.com and click the repositories section. Once there, click the New button to create a new repository. Follow the "Create a Repository" section of the following guide for a good graphical example and instructions ~ https://guides.github.com/activities/hello-world/. Once completed, lets get the remote repository and your local git on the same page.

Enter the terminal of your computer and navigate to your git directory that we created earlier in this tutorial. Here we will be cloning the remote repository to our local computer. To clone the repository enter the command ``` git clone <Repository Link>``` EX: ```$ git clone https://github.com/myGitHub/gitProject```. Once done, the ****gitProject**** should now be appearing in your local directory. Check by entering ```$ ls``` in your terminal to list the contents in your present directory. You can now enter that git by using the change directory command EX: ```$ cd gitProject```. Using this as our source for project work will allow us to work and commit versions of a project as well as push to a remote repository for the world to see and collobarate with.

***Pushing to the Remote Repository*** is an essential function when working with a cloned repository. To keep the remote repository current with the local repository, it requires the same add and commit process of the files we want to keep up to date, followed by a ```push``` command. Once you have successfully added and committed the files to your local repository enter ```$ git push``` into your terminal. Pushing will prompt you to verify your github credentials. Once successfully entered, the remote repository will then be up to date.

***Pulling from the Remote Repository*** is important to make sure that your local repository is up to date with your remote repository. If edits have been made on github.com or pushed to from other computers, update your local repository with the ```pull``` command. Enter the command ```$ git pull``` which will automatically update 
