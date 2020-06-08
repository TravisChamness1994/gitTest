# GitHub Introduction

***By Robert Trujillo, Alexander Sullivan, Arthur Hui and Travis Chamness***

"GitHub is a code hosting platform for version control and collaboration. It lets you and others work together on projects from anywhere." - guides.github.com

This tutorial is created in the perspective of the linux terminal and may vary slightly for Mac or Windows users.

Learning to use github is a skill that is useful professionally and personally. This small tutorial will go over the basics of how to use github.

***Where to starts?*** Begin by setting up an account here at github.com. The account is free, and if you are using this professionally be sure to use a good username. GitHubs can act as a boost to your resume so take advantage of this if it fits your needs. The topics covered here will be primarily based on using the terminal to navigate github. 

***Installing Git:***

For Linux Debian - In terminal enter ```sudo apt-get install git```

For Linux Fedora - In terminal enter ```sudo yum install git```

For Mac - go to http://git-scm.com/download/mac

For Windows - got to http://git-scm.com/download/win

***Setting up git***

We recommend before you begin creating local repositories that you first create a directory for your repositories. I created my directory at the terminal root. You can get to the root with ```$ cd ~``` command. The directory you choose to create can be named anything, but in keeping with context I chose to name my directory GitHub. Make the directory using ```$ mkdir <Directory Name>```  EX: ```$ mkdir GitHub ```in the command line and will produce a new directory of the directory name you have given. Enter the directory by now entering ```$ cd <Directory name>``` EX: ```$ cd GitHub```. This will be where we create our local repositories. 

***Initializing a local git repository***

Creating a local repository is done by entering ```$ git init <Repository Name>``` EX: ```$ git init gitTest```. This is very much the same as creating a new directory and will appear in your repository directory that we created in the previous step. Check to make sure it was created by entering ```$ ls``` into the terminal. You should now see your created repository.

***Using the local repository***

Enter the initialized repository using ```$ cd <Repository Name>``` where you can add files using the terminal. Once you have created or moved files to the repository, it is time to ***stage*** your git files. Staging is a term that describes preparing your files to be committed to your git repository. To stage, you will use the ```$ git add <File Name>``` command EX: ```$ git add helloWorld.c```. This will prepare the files added to be committed to your git repository. You can do this to multiple files at a time by entering a space between file names or truncate with the * symbol. EX: ```$ git add *.c``` adds            any c files in the directory or ```$ git add *``` to add all files in the directory to the staging area. Lets make sure we successfully added files to the staging aread by entering ```$ git status``` into the terminal. This will display information on the repository such as the branch, commits, and the files to be commited which are the files added. EX: if adding a helloc.c file to the staging are, the process would start by adding the hello.c file with ```$ git add hello.c```, entering the ```$ git status``` command to check that the hello.c file was successfully staged and waiting to be commited under the "changes to be committed" portion. This command would produce the following output showing our added and in th
```
On branch master
Your branch is up to date with 'origin/master'.

Changes to be committed:
  (use "git reset HEAD <file>..." to unstage)

        new file:   hello.c
```

The next step is to commit the staged files. Commiting our added files will save them to our local repository for safe storage. To commit the file or files, use the ```git commit``` command to send the staged files to the repository. However, to commit, a commit message will always be needed. The commit message will provide context to what is being committed. To commit the hello.c file shown above, the command would be...

(Consider the state of your program and what has been modified in the commit message.)

```$ git commit -m "First commit for hello world program. Project complete."```

where ```-m``` is the message option for the commit which allows the user to incorporate the commit message in the command.  It is not mandatory to add the message this way, but may be the easiest method. Without adding the message option, a Vim text editor will be opened to prompt the user to add a message at the top of the file. 

Once committed, the version is now saved in your local repository and can be 

***Lets begin setting up your first remote repository!*** To start a repository, go to your profile and click the repositories section. Once there, click the New button to create a new repository. Follow the "Create a Repository" section of this guide for a good graphical example and instructions. https://guides.github.com/activities/hello-world/. You can name your repository anything you would like, but hello world is a good place to start practicing!

