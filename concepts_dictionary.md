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
