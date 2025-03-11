# Concepts

## Git as time machine

## Git vs Github

### Git

- Software
- Runs on your machine
- Keeps track of versions and changes of files
- Allows to navigate between different versions
- Creates local repository

### Github

- Online repository (remote)
- Can collect different git projects


## Concepts

### Developing area

- local folder
- where you work and write code



### Staging Area

- "space" where you stage your commits, where you get your files ready 
  to commit to the local repository.
- Files/folders are stage using `git add <file/folder name>`
- Especially important when working with multiple files.
- helps to organize the commits: 
   - stage multiple files that you commit together (because they or the made changes belong together)
   - allows you to have meaningful commits
   - allows you to use meaningful commit messages
   - allows you to separate changes to files that are unrelated.


### Local Repository

- created using `git init`
- stores all versions and all changes
- represented as `.git` file in your folder
- the `git init` command creates the `.git` file
- `git commit -m "<message>"` commits the staged files with a commit message
- every commit creates a "snapshot" of the complete projects


### Remote Repository

- back up for local repository
- allows collaboration (others can access files and request changes,...)
- should be linked to the local repository: "bridge between local and remote repository"
- the commit history can be "pushed" to the remote repository using the `git push` command.
- The commit history in the remote repository can be "pulled" from remote to local using the `git pull` command.


## .gitignore

- a text file that lists all the files and folders that should be ignored by git.
   - can be listed one by one
   - there are templates (for instance on/via github)
   - via expressions
       - *.csv: ignore ale .csv
       - !file.csv: (except this file)



## Check Differences in versions

- view the history of the commits using `git log`



## Important

- when you start with a local repository and want to link/create a remote 
  repository, a new remote repository should be created, but it should be 
  completely empty (no README, no .gitignore, ...)


## Collaborating

1. Make sure you are added as a collaborator to the remote (github) repository
2. clone the remote repository (ssh) and create a local repository
3. make changes, stage, commit (with a good message) and push


### Conflicts

**when you cannot push (due to a conflict):**

1. pull from the remote repository
2. fix the conflicts if necessary ("merge")
    - automatic diff visualizations help to see what is different, and what you can choose.
    - automatically a text editor opens

3. commit the the results
4. push to the remote repository


#### Avoid conflicts by

- always pulling before comitting/pushing
- pull often
- push often


## Tagging

- use tags to refer to a specific commit: Easy to find, easy to download as .zip


## Branching

A "branch" is an "alternative history", an new path of commits that can 
  (but does not have to) be merged to the main branch at a later stage.
- great for experimenting
- great for collaborations where multiple persons work on the same issue/file
- after merging, the branch history still exist. Hence, you can go back to commits in this branch

Important, git only *mirrors/reflects* the changes in a specific branch. Hence, a specific
state in a branch my be different form what you see in a browser. This can be 
confusing! 


When working in different branches, it is crucial that you are aware in which 
branch you are working. As only changes in this branch are showed. When checking 
out to another branch, these changes are not visible anymore. 



### Detached HEAD

When you go back in history, for instance by using `git checkout <commit ID>`, it 
is possible, BUT NOT ADVISED, to "change the past". If you do this, YOU SHOULD create 
a new branch. If not, you get a *detached HEAD*.

By using `git shwich -c <new name>` you can create a new branch from that commit.


