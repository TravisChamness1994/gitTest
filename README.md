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

Enter the initialized repository

***Lets begin setting up your first remote repository!*** To start a repository, go to your profile and click the repositories section. Once there, click the New button to create a new repository. Follow the "Create a Repository" section of this guide for a good graphical example and instructions. https://guides.github.com/activities/hello-world/. You can name your repository anything you would like, but hello world is a good place to start practicing!

