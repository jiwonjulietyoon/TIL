# Today I Learned
.

## Using GitHub - Command Line (via GitBash or Terminal)
Pushing local project to a new remote repository:

1. (On GitHub) Create new repository (don't initialize with README, license, etc. -> add these later)
2. (On GitBash/Terminal) Change current working directory to local project => `cd /folder_to_push/`
2. `git init` => initialize the local directory as a Git repository
3. `git status` => check repository commitment status
4. `git remote add origin https://github.com/whitejcme/TIL.git` => add the URL for the remote repository where the local repository will be pushed
    - `git remote -v` => check remote repository URL
    - `git remote remove origin` => delete remote repository URL
5.  `git push -u origin master ` & login to GitHub via pop-up
    - `git push origin master` => 


Other: 
- `git diff` => display changes made
- `git add filename` => add file to git commitment (run every time to commit any changes made)
- `git commit -m "commit comment"` => take snapshots
- `git log` => view snapshot records
- `git checkout` => go to specified previous snapshot
- `git reset --hard`
- `git pull`
- `git clone https://github.com/sspy1/python_basic.git` => clone files in mentioned github address into current working directory
