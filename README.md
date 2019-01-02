# Today I Learned
.

## GitHub - Command Line Notes 2019.01.02.
1. `git clone https://github.com/whitejcme/Test.git`
   - Clone repository into the current working directory
2. make whatever changes in the local directory
   1. modified already existing file, testfile1
   2. created new file, testfile2
3. change current working directory to local project
4. `git status`
   - will show that testfile1 has been modified and that testfile2 is untracked (needs to be added to include in what will be committed)
5. `git add testfile2.md`
   - add testfile2 to the list of files to commit to repository
   - better yet, `git add .` to add all files in the directory to the list of files that needs to be committed (doing so will include both modified and newly created files)
6. `git commit -m "added testfile2.md"`
7. `git push origin master`
   - at this point, both testfile1 and testfile2 will have been successfully updated on the GitHub remote repository (online)

.

1. Make changes directly on GitHub remote repository (online)
   1. modified testfile1
   2. created testfile3
2. `git pull origin master` to download AND integrate the latest changes from the remote repository with the local project
   1. (assuming that there aren't any merge conflicts to occur)

.

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
