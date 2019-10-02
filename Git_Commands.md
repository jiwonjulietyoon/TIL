## Git Clone !!

`git clone [repositoryURL] [directory]`

- _directory_ is optional. If omitted, git will create a new directory (under the repository name) in the current working directory.
- If _directory_ is specified, git will clone the repository there without creating any new directories

<br>

## Add Remote Repository

`git remote add [nickname] [repository url]`

- where _nickname_ replaces "origin"
- to push to this new remote repository (when `nickname` is `secondary`): `git push -u secondary master` (include `-u` the first time only)

<br>

## Git Branch

`git branch`

- show all branches (default: `master`)
- the one written in green is the current branch

`git branch [NameOfNewBranch]`

- create new branch under _NameOfNewBranch_

`git checkout [NameOfBranch]`

- switch to branch _NameOfBranch_

`git checkout -b [NameOfNewBranch]` 

- switch to new branch right after creating it

`git branch -d [NameOfBranchToDelete]`

- delete branch
- (`git pull` from the `master` branch BEFORE deleting secondary branches)

`git merge [NameOfBranchToMerge]`

- merge _NameOfBranchToMerge_ into current branch
- ex) when merging the `newWorld` branch into the `master` branch
  - 1. `git checkout master` (move to `master` branch)
    2. `git merge newWorld`

<br>

## Undo git force push

`git reflog`, and check which HEAD you want to restore to.

e.g) `git reset --hard HEAD@{4}`

This should restore all your commits lost due to force pushing.



<br>

## .gitignore

- which files/folders to exclude from git commits
- https://gitignore.io/api/django

<br>

## git rm -r --cached fileName.txt

- does not update changes when pushing to Git (버전 관리는 그만하고 싶을 때)

<br>


## Git Reset
- git config —system —unset credential.helper
- git config --global --unset credential.helper
- git config --global --unset-all user.name
- git config --global --unset-all user.email

<br>

<br>


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

<br>

1. Make changes directly on GitHub remote repository (online)
   1. modified testfile1
   2. created testfile3
2. `git pull origin master` to download AND integrate the latest changes from the remote repository with the local project
   1. (assuming that there aren't any merge conflicts to occur)

<br>

<br>

## Using GitHub - Command Line (via GitBash or Terminal)

Pushing local project to a new remote repository:

1. (On GitHub) Create new repository (don't initialize with README, license, etc. -> add these later)
2. (On GitBash/Terminal) Change current working directory to local project => `cd /folder_to_push/`
3. `git init` => initialize the local directory as a Git repository
4. `git status` => check repository commitment status
5. `git remote add origin https://github.com/whitejcme/TIL.git` => add the URL for the remote repository where the local repository will be pushed
   - `git remote -v` => list all remote repositories and the corresponding URL
   - `git remote remove origin` => delete remote repository URL
6. `git push -u origin master ` & login to GitHub via pop-up
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



