---
layout: article
key: page-resources-github
permalink: /resources/gitHub/
aside:
    toc: true
---

Back to [Resources](/resources/)

# Notes on git

These are working templates I use for projects using git and GitHub. While you may need more commands than listed here, 99% of the time I largely use the ones shown below and google my way out of the occasional sticky situation.

Repository is abbreviated as **repo**!



### Most basic repo
initialize a new repo, creating a new directory: `git init repo_name`
<br>
move into repo: `cd repo_name`
<br>
create the first file: `touch README.md`
<br>
stage this file: `git add README.md`
<br>
&nbsp;&nbsp;&nbsp;&nbsp;the dot specifies **all** unstaged files
<br>
save all staged files: `git commit -m "my first commit"`
<br>
specify the path to the remote repo on GitHub: `git remote add origin https://github.com/USERNAME/REPOSITORY.git`
<br>
push changes, saving them to the remote repo: `git push -u origin master`
<br>

After the initialization above, most work then invovles an endless loop of modifying code followed by
```
git commit --all -m 'some informative msg about what changed'
git push
```
Note that the push command here was used without the `-u origin master`, and the `--all` flag in the commit command stages the files for you! If you want to stage them as you go, before the commit, then use `git add --all`. If you don't want git to stage *deleted* files, then use `-a` instead of `--all`.



### Working with branches
For many projects, using branches is not strictly necessary, especially for beginners. A description of branches can be found [here](https://git-scm.com/book/en/v2/Git-Branching-Basic-Branching-and-Merging).

look at all your branches: `git branch -av`
<br>
create new branch: `git checkout -b new_branch_name`
<br>
after work is done, save changes: `git commit --all -m 'commit_message'`
<br>
optional, push new branch and changes to remote repository (repo): `git push -u origin new_branch_name`
<br>
&nbsp;&nbsp;&nbsp;&nbsp;notes: text after 'push' for setting upstream branch  

if everything in new branch **worked out**, integrate into master branch:
<br>
&nbsp;&nbsp;&nbsp;&nbsp;go back to master branch: `git checkout master`
<br>
&nbsp;&nbsp;&nbsp;&nbsp;merge new branch with master: `git merge new_branch_name`
<br>
&nbsp;&nbsp;&nbsp;&nbsp;delete branch because it's now redundant with master: `git branch -d new_branch_name`
<br>
&nbsp;&nbsp;&nbsp;&nbsp;update master in remote repo with these changes: `git push`
<br>
&nbsp;&nbsp;&nbsp;&nbsp;if you have pushed branch to remote repo, delete there too: `git push origin -d branch_name`

if your new branch **did not work out**: 
<br>
&nbsp;&nbsp;&nbsp;&nbsp;force delete branch ("force" because branch not merged): `git branch -D branch_name`
<br>
&nbsp;&nbsp;&nbsp;&nbsp;if you have pushed branch to remote repo, delete there too: `git push origin -d branch_name`

**NOTE**: work in branch can be completely local, merged with master, pushed, then deleted; *i.e.* it isn't strictly required to also create the branch in remote repo
<br>
<br>
For more information on branching with visualizations, see [here](https://git-scm.com/book/en/v2/Git-Branching-Basic-Branching-and-Merging)



### Edit another's repo (1)
This approach involves submitting your changes to someone's repo using a [branch](https://git-scm.com/book/en/v2/Git-Branching-Basic-Branching-and-Merging). This person may then decide to incorporate the changes. However, if you're not a [registered collaborator](https://stackoverflow.com/questions/3611256/forking-vs-branching-in-github) you may not be able to make a branch, so the next method (2) may be more appropriate.

download the remote repo on GitHub: `git clone https://github.com/USERNAME/REPOSITORY.git`
<br>
move into repo directory: `cd repo_name`
<br>
create a new branch: `git checkout -b my_branch`
<br>
make changes, then commit them: `git commit --all -m 'msg about changes'`
<br>
push changes to remote repo on GitHub: `git push -u origin my_branch`



### Edit another's repo (2)
This approach involves forking someone's repo, making a copy in your own GitHub account. You then make changes to this, and submit a pull request to this other user's account. I will make a simplifid template for this here, but this process is explained thoroughly [here](https://gist.github.com/Chaser324/ce0505fbed06b947d962).



