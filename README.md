# github-demo-tsan
github-demo-tsan



# github-workshop

Aiming to understand the basics of github

**PART 1**

**Step 01: Installing Git**

The first two things you'll want to do are install git and create a free GitHub account.
https://git-scm.com/book/en/v2/Getting-Started-Installing-Git

https://gist.github.com/derhuerst/1b15ff4652a867391f03

**ssh keys and agent**

https://help.github.com/en/github/authenticating-to-github/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent

https://help.github.com/en/github/authenticating-to-github/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent

https://help.github.com/en/github/authenticating-to-github/adding-a-new-ssh-key-to-your-github-account


**Step 02: Initializing a Repository**

*cd Desktop*

*mkdir github-learn*

*cd github-learn*

*git init*


**Step 03: Create a file within the repo**

*touch printing.py*

{ Lets code to print something using python in this file }

*vi printing.py*

Once you've added or modified files in a folder containing a git repo, git will notice that changes have been made inside the repo. But, git won't officially keep track of the file.


**Step 04: Checking the status of our repo**

*git status*

After creating the new file, you can use the git status command to see which files git knows exist.
What this basically says is, "Hey, we noticed you created a new file called printing.py, but unless you use the 'git add' command we aren't going to do anything with it."


**Step 05: Commit**
A commit is a record of what files you have changed since the last time you made a commit.
To add a file to a commit, you first need to add it to the staging environment.

*git add <filename>*
  
*git commit -m "<insert commit message>"*
  
*git push*
  

**PART 2**

**BRANCHING IN GIT**

Branches allow you to move back and forth between 'states' of a project. For instance, if you want to add a new page to your website you can create a new branch just for that page without affecting the main part of the project. Once you're done with the page, you can merge your changes from your branch into the master branch. When you create a new branch, Git keeps track of which commit your branch 'branched' off of, so it knows the history behind all the files. 

**STEP 01 : Create a branch**
 *git checkout -b my_branch_name*
  
 *git branch*
  
 The branch name with the asterisk next to it indicates which branch you're pointed to at that given time. 
 
 **STEP 02: Pushing files to the branch**
 
  *git push origin yourbranchname*
  
Now we'll push the commit in your branch to your new GitHub repo. This allows other people to see the changes you've made. If they're approved by the repository's owner, the changes can then be merged into the master branch.

(If this is your first time using GitHub locally, it might prompt you to log in with your GitHub username and password.)

**STEP 02 : Merge branches to master**

*git checkout master*
*git merge my_branch_name*

First we run git checkout master to change the active branch back to master. Then we run the command git merge new-branch to merge the new feature into the master branch. Note that git merge merges the specified branch into the currently active branch. So we need to be on the branch that we are merging into.

**PART 03**

**git merge vs git rebase**

**STEP 01: UNDERSTANDING GIT MERGE**

*git checkout master*

*touch m1.txt*

"Commit it to the repo"

*git checkout -b feature*

*touch f1.txt*

"Commit it to the repo"

*git checkout master*

*touch m2.txt*

"Commit it to the repo"

*git checkout feature*

*git merge master*

**STEP 02: UNDERSTANDING GIT REBASE**

*git checkout master*

*touch m1.txt*

"Commit it to the repo"

*git checkout -b feature*

*touch f1.txt*

"Commit it to the repo"

*git checkout master*

*touch m2.txt*

"Commit it to the repo"

*git checkout feature*

*git rebase master*

**PART 04**

**git pull and fork**

Create a pull request to propose and collaborate on changes to a repository. These changes are proposed in a branch, which ensures that the master branch only contains finished and approved work.
Anyone with read permissions to a repository can create a pull request, but you must have write permissions to create a branch. If you want to create a new branch for your pull request and don't have write permissions to the repository, you can fork the repository first.


**Things to explore on :**

1. git stash

2. git as source control management tool in devops pipeline

3. github vs svn

4. troubleshooting github problems

5. git realease and labels
 


