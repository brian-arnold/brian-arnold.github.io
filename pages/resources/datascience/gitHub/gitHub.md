---
layout: article
key: page-resources-github
permalink: /resources/datascience/github
aside:
    toc: true
---

Back to [Resources](/resources/)

# What is Git/GitHub?


Git is a set of commands used to save versions of your code, while GitHub is a web-based service that will store or host your code online. You can use Git without Github, but you cannot use GitHub without Git!

Git has *many* commands, some of which can be very useful, but I typically use only a handful of them. Below I have a series of commands I routinely use most of the time. When I encounter some issues that other commands can help with, I just Google the problem and find the command.

Repository is abbreviated as **repo**!

### Most basic repo
- first create a repo on GitHub following [these instructions](https://docs.github.com/en/get-started/quickstart/create-a-repo)
- use the command line to clone this repo to your computer `git clone https://github.com/USERNAME/REPOSITORY_NAME`
    - replace USERNAME and REPOSITORY_NAME with appropriate values
- move into this cloned repo, which should be a subdirectory within the directory you're currently in: `cd REPOSITORY_NAME`
- create or add files, e.g. `touch test.txt`
- "stage" this file: `git add test.txt`
- save or "commit" all staged files: `git commit -m "my first commit"`
    - this is now a saved checkpoint named "my first commit"
- `test.txt` is only on your local computer, so "push" this commit to the remote repo on GitHub to update it: `git push -u origin main`

After the initialization above, most work then invovles an endless loop of adding/modifying code followed by
```
git add --all . # this adds all new changes, assuming you are in the base directory of the repo
git commit -m 'some informative msg about what changed'
git push
```
Note that the push command here was used without the `-u origin main`, and the `--all` flag in the commit command stages the files for you! If you want to stage them as you go, before the commit, then use `git add --all`. If you don't want git to stage *deleted* files, then use `-a` instead of `--all`.



### Working with branches
Using a branch is a useful way to modify someone's code while keeping the original intact! If your changes don't work out the way you would have liked, you can just delete the branch. If they do work out, you can *merge* your branch with the original code. A description of branches can be found [here](https://git-scm.com/book/en/v2/Git-Branching-Basic-Branching-and-Merging).

- look at all your branches: `git branch -av`
- create new branch: `git checkout -b new_branch_name`
- after work is done, save changes: `git commit --all -m 'commit_message'`
- optional, push new branch and changes to remote repository (repo): `git push -u origin new_branch_name`
    - the text after 'push' for setting upstream branch  

- if everything in new branch **worked out**, integrate into main branch:
    - go back to main branch: `git checkout main`
    - merge new branch with main: `git merge new_branch_name`
    - delete branch because it's now redundant with main: `git branch -d new_branch_name`
    - update main in remote repo with these changes: `git push`
    - if you have pushed branch to remote repo, delete there too: `git push origin -d branch_name`

- if your new branch **did not work out**: 
    - force delete branch ("force" because branch not merged): `git branch -D branch_name`
    - if you have pushed branch to remote repo, delete there too: `git push origin -d branch_name`

**NOTE**: work in branch can be completely local, merged with main, pushed, then deleted; *i.e.* it isn't strictly required to also create the branch in remote repo
<br>
<br>
For more information on branching with visualizations, see [here](https://git-scm.com/book/en/v2/Git-Branching-Basic-Branching-and-Merging)



### Edit another's repo (1)
This approach involves using a [branch](https://git-scm.com/book/en/v2/Git-Branching-Basic-Branching-and-Merging) to submit changes to someone's repo to which you have write-access. This person may then decide to incorporate the changes. However, if you're not a [registered collaborator](https://stackoverflow.com/questions/3611256/forking-vs-branching-in-github) you may not be able to make a branch, so the next method (2) may be more appropriate.

- download the remote repo on GitHub: `git clone https://github.com/USERNAME/REPOSITORY.git`
- move into repo directory: `cd repo_name`
- create a new branch: `git checkout -b my_branch`
- make changes, then commit them: `git commit --all -m 'msg about changes'`
- push changes to remote repo on GitHub: `git push -u origin my_branch`
- navigate to the repo on GitHub and create a [pull request](https://docs.github.com/en/github/collaborating-with-issues-and-pull-requests/creating-a-pull-request)


### Edit another's repo (2)
When you do not have write access to someone's repo, you may fork their repo, making a copy in your own GitHub account. You then make changes to this, and submit a pull request to this other user's account. I will make a simplifid template for this here, but this process is explained thoroughly [here](https://gist.github.com/Chaser324/ce0505fbed06b947d962).



