# Git_Github

----


> Clone Project From Github

`$ git clone https://github.com/test/test.git `

> Show Status Of Added Or Moddifed Files

`$ git status`

> To Add Files

`$ git add *`

`$ git add [filenames]`

> To Remove Files From Stage Area Before Commit 
> Restore and Clean

`$ git reset head [filename]` <br>
`$ git restore --staged [filename]` <br>
`$ git restore --staged *`<br>
`$ git clean -n`  //show which files will remove<br>
`$ git clean -f` // remove files from stage<br>

> Commit Repo

`$ git commit -m "comment"`

> Show Branch Name

`$ git branch` 

> Show Remote Name

`$ git remote -v` 

> To Push Local Repo To Remote Repo

`$ git push [RemoteName] [BranchName]`

`$ git push origin master`

> Get Last Update

`$ git pull origin` 

> Set Configuration

`$ git config --global user.email`

`$ git config --global user.email "asd@asd.com"`

`$ git config --global user.name "asd"`

`git config --global --edit` // Edit Configuration
 
> Create Public Key To Login Github Automatic

`$ ssh-keygen -t rsa -b 4096 -C "Your GitHub Email Here"` //Generate Key

`$ cat ~/.ssh/id_rsa.pub` // Get Key To Copy and Add SSH to Github Website

`$ ssh -T git@github.com"` // Test Key And Connection


> Create Repository From Existing Project

`$ git init` // after enter to folder project

`$ git  remote add origin [link_remote_repo]`  // link_remote_repo => created in github

`$ git push -u origin master"` // Push Data -u for pull then push

> Create Fork From Existing Project

<p> make fork from project then if you want edit it after then commit to master or new branch then create pull request to admin  </p>
<p> wait admin to accept your pull request  </p>

> Alias

`$ git config --global alias.br branch`

> Create Branch

`$ git branch` // Show Branches 

`$ git branch [BranchName]`

`$ git checkout [BranchName]` // Switch To Branch

`$ git checkout master` // back to master

`$ git branch -d BranchName` // Delete Branch

`$ git branch -D BranchName` // delete branch without confirm

`$ git checkout -b BranchName` // Create Branch And Switch To It

`$ git branch -m BranchName`  // Move / Rename Branch

after add branch create file and do some task then add files the commit 

<p> To merge branch direct to origin without pull request</p>

`$ git checkout master` // back to master 

`$ git merge BranchName`  // merge branch to master

`$ git push origin master` // master to origin

`$ git merge "Branch Name You Need To Merge"` // Merge Branch With Current Branch

<p> To merge branch to origin by pull request </p>

`test code here`

`$ git checkout [BranchName]` // goto branch <br>

`$ git push origin branchName` // to create pull request<br>

`$ git merge BranchName` // merge branch to master then can delete branch and commit master or add master to origin

`$ git push origin BranchName` // pull request to remote with branch

> Stash

`$ git stash` // Save Work To Stash to use later // hidding files from repo

`$ git stash pop` // Get Work From Stash

`$ git stash list` // List Items in Stash

`$ git stash save "comment"`  // Save Work To Stash With Description

`$ git stash apply` // pop last index without remove from stash

`$ git stash pop stash@{2}`  // Get Specific Stash

`$ git stash drop stash@{2}`  // Delete Stash

`$ git stash show`  // Show Lastest Added Stash Content

`$ git stash show stash@{2}`   // Show Specific Stash Content

`$ git stash clear` // Empty The Stash

> Log Details

`$ git log`

`$ git log --oneline`

`$ git log --oneline -3` // show three lines

`$ git log --stat`  // commit with what changes in files

`$ git log --oneline --graph --all --decorate`

> Ignoring Files and Directories

<p>create file .gitignore then add inside it extention of files ex.  *.log   permit some file added before !test.log </p>

> Compare

`git diff` //show what you edit working directory

`git diff --staged` //show what you edit staged area

> Remove Files From Repo

`git rm filename	// remove from working area`

`git rm -f filename // remove from staged area`

`git mv filename filename2` // rename file

> Undo To Previous Change

`git checkout "filename"` // undo changes from last commit

`git commit --amend -m "comment"` // to edit or change last commit 

`git checkout [SHA] filename`  // Reverting Commit to use with our changes then new commit

`git checkout [SHA] -- filename` // reverting specific filename | the same above

`git checkout [SHA] ` // reverting all files this hash commit

> Remove Commit | Resetting the head

`git reset --soft [SHA]` // move pointer to SHA and last head goto stage area 

`git reset [SHA]` // mixed move pointer to SHA and goto SHA to stage area and last head , SHA goto working directory

`git reset --hard [SHA]` //goto last head to working direc then move pointer to SHA and go SHA to working direc and delete last head for working direc

`git push origin master --force` // to update commit

> Merge:
* fast-forword    `git merge [BranchName]`
* true merge (fix conflict)   `git merge [BranchName]`

> Tag and Release

`$ git tag` // show tags <br>
`$ git tag v1.0` // create tag <br>
`$ git push origin v1.0` // push tag to origin  <br>
`$ git tag -a v2.0 -m "comment"` // create tag version 2 or anything <br>
`$ git push origin v2.0` // push tag to origin  <br>
`$ git tag -l v1.*` // list tags v1.* any  <br>
`$ git tag -d v1.0` // remove tag local <br>
`$ git push origin --delete v1.0` // remove tag remote

<p>After Finished tag create **Release** </p>
