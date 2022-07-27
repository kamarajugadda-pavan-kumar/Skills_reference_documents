what is Git?
Git is a free and open source version control system.

what is version control?
The management of changes to documents, computer programs, large websites, and other collections of information.

Terms:
-Directory-> Folder
-Terminal or Command Line->Interface for Text Commands
-CLI->Command Line Interface
-cd->change Directory
-Code Editor->Word processor for writing Code
-Repository->Project, or the folder/place where your project is kept
-GitHub->A website to host your repositories online

Git Commands:
clone-> bring a repository that is hosted somewhere like GitHub into a folder on your local machine
add->track your files and changes in Git
commit->save your files in Git
push->upload Git commits to a remote repo, like GitHub
pull->Download changes from remote repo to your local machine, the opposite of push


method 1:
create a repository in GitHub and clone it to local storage using the Command
        git clone https://github.com/kamarajugadda-pavan-kumar/Git_demo.git
The link to clone can be obtained from the GitHub site ->repository ->code->clone

Then if user.email and user.name are not congigured , doit
```
git congif --get user.email
git config --get user.name
git config user.email "pavankd12@gmail.com"
git config user.name "pavan_kumar"
```

To check the remote origin
```
git remote -v 
```

To set remote origin
```
git remote add git@github.com:kamarajugadda-pavan-kumar/git_demo2.git
```

To know the status use Command
'git status'

To add a file for git to track use Command 'git add file_name' or 'git add .'  , dot indicates all files

To commit the changes made in the files use command "git commit -m 'any message about commit' "

To push the code to github , first create a public and private key using
"ssh-keygen -t rsa -b 4096 -C 'pavankd12@gmail.com' "
then print the key in '.pub' file using command 'type filename.pub'
then add the ssh key printed in the GitHub website
Then use command 'git push origin branch_name'


method 2:
create local repository and then add a origin path
First create a repository in GitHub and copy the origin path
then use command 'git init'
then use command 'git remote add origin git@github.com:kamarajugadda-pavan-kumar/git_demo2.git'
'git add .'
'git commit .'
'git push origin master'




If you dont have complete access to push the code you need to make a 'pull request'


========Branching:============
'git branch' to see the branches

'git checkout branch_name' is used to switch between branches

'git checkout -b branch_name' creates a new branch with that branch name and switches to that branch.

changes made on one branch can't be seen on other branch.

'git diff branch_name' gives the difference between two commits



===============pull request=====================
you can merge the branches by making a pull request from the feature branch, this can be done on GitHub
Now once the pull request is made , all the other users working on the project can see the changes and discuss and finally merge the branches.


The merged branch needs to be pulled on to local environment to see the changes, use command
'git pull origin main'

The merged branch is now redundant and can be deleted using the command
'git branch -d branch_name'



===========conflict==============
when you work on a big project master branch also gets updated, inorder to stay updated with the master branch you 'git merge master'.
If there are any conflict you need to resolve and then commit on your branch and then start working on your branch again.



============undoing commits in git==============
