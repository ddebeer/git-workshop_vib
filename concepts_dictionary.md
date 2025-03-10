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

### Local Repository

- created using `git init`
- stores all versions and all changes
- represented as `.git` file in your folder
- the `git init` command creates the `.git` file
- `git commit -m "<message>"` commits the staged files with a commit message
- every commit creates a "snapshot" of the complete projects

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

