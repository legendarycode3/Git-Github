#### INTRODUCTION TO GIT AND GITHUB  <br/>

"Git" is the underlying technology for version control. It is the tool that tracks changes and manages the history of your code.  <br/>

"GitHub" is a service that hosts Git repositories and provides a platform for collaboration and project management around those repositories.  <br/>

"Git" is an open-source, distributed version control system (VCS) that tracks changes in source code during software development. It allows multiple developers to work on the same project simultaneously without overwriting each other's work. <br/>

"Git" is a version control tool. In one way or the other you may need to use a git and a github.  <br/>

You need to use git and github either to store your projects on the cloud or to collabrate with your team.  <br/>

Version Control: It records changes to files over time, enabling developers to revert to previous versions, compare changes, and understand the evolution of the codebase.   <br/>





#### 1. Install Git and Signup on Github    <br/>
   
- Git:   <br/>
  Install [git](https://git-scm.com/downloads)   <br/>

- Github  <br/>
  Signup on [github](https://github.com/)


####  2. Configure your name and your email :   <br/>
git config --global user.name 'yourname'    <br/>
git config --global user.email 'youremail'   <br/>  <br/>











#### CREATING THE FIRST VERSION OF CODE IN VERSION HISTORY , TYPICALLY USING A SYSTEM LIKE GIT , INVOLVES THE FOLLOWING (STEPS):   <br/>

####  STEP 1. Create a local git repository    <br/>

On this step your will create a folder (directory) for your project. A local repository is a project or a folder which is on your computer.
Go to start and type git bash. Git terminal will popup. On the terminal write:  <br/>

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









------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
####  SOME EXTRA GIT COMMAND FEATURES  
------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

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










## Git cheatsheets:
**HERE ARE SOME MORE GIT CHEATSHEET :**

git remote add <remote_name> <url>        // Link a local repository to a remote repository and give a name for this link    <br/>

git remote                       // List all remote repositories that are linked    <br/>

git remote -v                    // List all remote repositories (but with more detail)    <br/>

git remote remove <remote_name>         // Removes a link to a remote repository    <br/>

git remote remove origin               // Removes the link to the remote repository named     <br/>
"origin"



git clone <url>                <br/>  // Download a remote repository from a url or clone and existing repo  <br/>

git clone <url> <folder_name>       // Download the repository and give it a different
folder name

git fetch                       <br/> // Updates all remote tracking branches. Remote tracking branches (like origin/main) show what the branch looks like in the remote repository.   <br/>


git --version              //to check the version   <br/>
git help                 // To get help from git  <br/>
git help commit         // To get commit help  <br/>



git init             // Initilaizing git repository on local machine  <br/>



git config --list        // to check what is configured   <br/>
git config         // to get information about configuration  <br/>
git config --global user.name "username"      // Configuring git user name   <br/>
git config --global user.email "email"      // Configuring git user email     <br/>



git add filename        <br/>
git add first.txt       // adding only one file   <br/>
git add second.txt third.txt            // to add multiple file   <br/>
git add .                // To add all the files and folders to the staging area     <br/>
git add -p      // Chosing which part of a file to stage: </br>
git rm <file>   // Adding untracked file or unchanged changes </br>
git rm <file>   // Delete file </br>
git reset <file>  // Unstage one file </br>
git status       // Check what you added </br>
git reset       // Unstage everything </br>
git mv <old> <new>   //Move file  </br>
git rm --cached <file>   //Tell Git to forget about a file without deleting it </br>



git commit                           // Make a commit </br>
git commit -m 'commit message'        // after staging using add    <br/>
git commit -a -m 'commit message'      // staging using a and commiting     <br/>
git commit -am 'commit message'        // staging and committing     <br/>
git commit -am "Message"     //Grab every thing in the working copy and -a allows to skip the staging copy     <br/>


git log        // To see the history on the repository      <br/>
git log --author ="name"   // To check change by specific user       <br/>
git status     // To check changes or status of the file       <br/>
git switch -c <name>   //reate a branch


git checkout <name> OR git switch <name>  // Switch branches </br>
git branch            // List branch </br>
git branch -d <name>   //Delete branch </br>
git branch -D <name>     //Force delete a branch </br>
git checkout -b <name> or git switch -c <name>    //Create a branch  </br>



git show <commit>       //Show diff between a commit and its parent </br>
git diff <commit> <file>   //Diff one file since a commit  </br>
git diff <commit> <commit>   //Diff two commits. </br>
git diff <commit> --stat  OR  git show <commit> --stat   //Show a summary of a diff </br>



git restore <file>  OR git checkout <file>     //Delete unstaged changes to one file </br>
git restore --staged --worktree <file>  or  git checkout HEAD <file>    //Delete all staged and unstaged changes to one file </br>
git reset --hard         //Delete all staged and unstaged changes  </br>
git stash               //'Stash' all staged and unstaged changes  </br>
git clean               //Delete untracked files </br>




git reset HEAD^       //"Undo" the most recent commit (keep your working directory the same) </br>
git reflog BRANCHNAME   //Undo a failed rebase  </br>
git rebase -i HEAD~6      //Squash the last 5 commits into one. </br>
git commit --amend         //Change a commit message (or add a file you forgot) </br>




git log main or  git log --graph main  or  git log --oneline        //Look at a branch's history  </br>
git log --follow <file>         //Show every commit that modified a file, including before it was renamed
git blame <file>            //Show who last changed each line of a file  </br>
git log <file>            //Show every commit that modified a file </br>
git log -G banana         //Find every commit that added or removed some text </br>




git checkout <commit> <file>  OR  git restore <file> --source <commit>     //Get the version of a file from another commit  </br>


git remote add <name> <url>            //Add a Remote  </br>




git push origin main               //Push the main branch to the remote origin  </br>
git push -u origin <name>         //Push a branch that you've never pushed before  </br>
git push --tags                  //Push tags  </br>
git push                        //Push the current branch to its remote "tracking branch"  </br>
git push --force-with-lease      //Force push   </br>




git fetch origin main            //Fetch changes (but don't change any of your local branches)  </br>
git pull origin main  OR  git pull         //Fetch changes and then merge them into your current branch   </br>
git pull --rebase               //Fetch changes and then rebase your current branch  </br>




git config user.name 'Your Name'      //Set a config option  </br>
git config alias.st status            //Add an alias   </br>
git config --global ...            //Set option globally </br>
man git-config                  //ee all possible config options </br> 



.git/config                        //Local git config  </br>
.gitignore                        //List of files to ignore </br>
~/.gitconfig                     //Global git config  </br>




git pull origin $(current_branch)   //Fetch and merge latest changes from the remote </br>
Ctrl+Shift+p                   //Pull latest changes.  </br>
git switch -c <name>            //Create and switch to a new branch </br>



git switch banana & git switch main            //git rebase main  </br>
git switch main & git merge banana               //Combine with merge  </br>
git cherry-pick <commit>
