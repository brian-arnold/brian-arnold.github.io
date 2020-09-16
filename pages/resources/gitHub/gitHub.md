---
layout: article
key: page-resources-github
permalink: /resources/gitHub/
---

Back to [Resources](/resources/)

# Notes on git

### Starting a new repository
### Contributing to an existing repository
### Working with branches

look at all your branches: `git branch -av`
<br>
create new branch: `git checkout -b new_branch_name`
<br>
after work is done, save changes: `git commit -a -m 'commit_message'`
<br>
optional, push new branch and changes to remote repository: `git push -u origin new_branch_name`
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
&nbsp;&nbsp;&nbsp;&nbsp;update master in remote repository with these changes: `git push`
<br>
&nbsp;&nbsp;&nbsp;&nbsp;if you have pushed branch to remote repository, delete there too: `git push origin -d branch_name`

if your new branch **did not work out**: 
<br>
&nbsp;&nbsp;&nbsp;&nbsp;force delete branch ("force" because branch not merged): `git branch -D branch_name`
<br>
&nbsp;&nbsp;&nbsp;&nbsp;if you have pushed branch to remote repository, delete there too: `git push origin -d branch_name`

**NOTE**: work in branch can be completely local, merged with master, pushed, then deleted; *i.e.* it isn't strictly required to also create the branch in remote repository
<br>
<br>
For more information on branching with visualizations, see [here](https://git-scm.com/book/en/v2/Git-Branching-Basic-Branching-and-Merging)

