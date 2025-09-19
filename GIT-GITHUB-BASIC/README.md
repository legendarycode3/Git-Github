#### INTRODUCTION TO GIT AND GITHUB

"Git" is the underlying technology for version control. It is the tool that tracks changes and manages the history of your code.

"GitHub" is a service that hosts Git repositories and provides a platform for collaboration and project management around those repositories. 

"Git" is an open-source, distributed version control system (VCS) that tracks changes in source code during software development. It allows multiple developers to work on the same project simultaneously without overwriting each other's work.

"Git" is a version control tool. In one way or the other you may need to use a git and a github.

You need to use git and github either to store your projects on the cloud or to collabrate with your team.

Version Control: It records changes to files over time, enabling developers to revert to previous versions, compare changes, and understand the evolution of the codebase.





#### 1. Install Git and Signup on Github

- Git:
  Install [git](https://git-scm.com/downloads)

- Github
  Signup on [github](https://github.com/)


####  2. Configure your name and your email :
git config --global user.name 'yourname'
git config --global user.email 'youremail'










#### CREATING THE FIRST VERSION OF CODE IN VERSION HISTORY , TYPICALLY USING A SYSTEM LIKE GIT , INVOLVES THE FOLLOWING (STEPS):

####  STEP 1. Create a local git repository

On this step your will create a folder (directory) for your project. A local repository is a project or a folder which is on your computer.
Go to start and type git bash. Git terminal will popup. On the terminal write:

    mkdir project_name
    cd project_name



####  STEP 2. Initialize Git 

After creating a new local repository  intitialize the repository by the following command:

   git init

After, the repository is intialized git tracks the changes in the files and folders.



####  STEP 3. Add file to the staging area

File can be added to the stagging area in multiple ways.
"To add single file"

   git add filename


"To add multiple files"

   git add filename1 filename2


"To add all files and folders at once"

   git add .



####  STEP 4. Commit the changes

Commiting means creating a snapshot of your project's current state and saving it to the local repository.

   git commit -m 'your message'

Note: Your commit message has to be associated with the changes.



####  STEP 5. Create Repository on Github

Go to [github](https://github.com/) and create a repository by click the plus icon on the top right corner.



####  STEP 6. Connect to a remote repository (e.g., GitHub, GitLab, Bitbucket)  - Recommended remote repository is: GitHub:

In this step you will connect your local git repository with your remote github repository

    git remote add origin remote_repository_ul


The word origin could be any word. It is a means to assign the repository url.
If this is step is passed without error, you are ready to push it to your remote github repository



## STEP 7. Push

Commits if you have any changes and be ready to push your files to your remote github repository
git push origin master

    git push  origin master

The "git push origin master" command in Git performs the following actions: 

git push: This is the core command to upload local commits to a remote repository.

origin: This is the default name given to the remote repository that your local repository is connected to.

master: This specifies the branch you are pushing. In this case, you are pushing the content of your local master branch to the master branch on the origin remote.










####  SOME EXTRA GIT COMMAND FEATURES  

#### 1. Unstage a file

    git reset HEAD filename


#### 2. Creating a branch
Creating a branch in Git means diverging from the main line of development to create a separate, independent line of work. This allows for changes to be made without affecting the main codebase until those changes are ready to be integrated..

To create branch:

- Only to create branch
    git branch branchname


- To create and checkout to the branch at the same time:
    git checkout -b branchname


-  To switch between branches:

    git checkout master
    git checkout branchname


- To list down all the branches:

    git branch


#### 3. Merge
Refers to the process of integrating changes from one or more branches into another branch.
When you work on an individual project or a team project you may have different branches. Mostly you will have master, develop and other branchs.Then you will merge other branchs to your develop and your develop to master. 

    git checkout develop
    git merge feature



#### 4. Pull
Refers to the action of retrieving and integrating changes from a remote Git repository into your local repository. This process essentially updates your local codebase with the latest modifications available on the remote server.
If your team merge new features to the develop. Then you will be behind, now you need to make your project to current stage by pulling from develop

    git checkout yourbranch
    git pull origin develop
    git checkout develop
    git merge yourbranch
    git push -u origin develop










## Git cheatsheet:
HERE ARE SOME MORE GIT CHEATSHEET :

git remote add <remote_name> <url>      //Link a local repository to a remote repository and give a name for this link

git remote                      //List all remote repositories that are linked

git remote -v                   //List all remote repositories (but with more detail)

git remote remove <remote_name>        //Removes a link to a remote repository

git remote remove origin              //Removes the link to the remote repository named
"origin"



git clone <url>                 // Download a remote repository from a url

git clone <url> <folder_name>       //Download the repository and give it a different
folder name

git fetch                       //Updates all remote tracking branches. Remote tracking branches (like origin/main) show what the branch looks like in the remote repository.


git --version //to check the version
git help            // To get help from git
git help commit       // To get commit help



git init              // Initilaizing git repository on local machine



git config --list         // to check what is configured
git config            // to get information about configuration
git config --global user.name "username"     //Configuring git user name
git config --global user.email "email"     //Configuring git user email



git add filename
git add first.txt # adding only one file
git add second.txt third.txt           // to add multiple file
git add .                //To add all the files and folders to the staging area



git commit -m 'commit message'       // after staging using add
git commit -a -m 'commit message'      // staging using a and commiting
git commit -am 'commit message'        // staging and committing
git commit -am "Message" #Grab every thing in the working copy and -a allows to skip the staging copy


git log  // To see the history on the repository
git log --author ="name" #To check change by specific user
git status  //To check changes or status of the file


