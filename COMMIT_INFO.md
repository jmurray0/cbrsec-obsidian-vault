A simple guide to `git` commands in bash to work around the `cbrsec-obsidian-vault` repository.

## STARTING OUT

You're going to need `git` and `gh` for your command line. In your package manager, make sure you include both of them.

Navigate to a working folder and run the following commands:
```bash
mkdir gits
git init
git commit -m "initial commit"
```
This will initialize a local git repository.

Now, you'll want to add an origin for our remote repository.
```bash
git remote add origin https://github.com/jmurray0/cbrsec-obsidian-vault/
```
This will set "remote" as our repository.

Now navigate to your branch.
```bash
git checkout prod-<YOURNAME>
git pull -a
```
Your folder should now be replaced by the master branch.

## PULLING FROM BRANCHES

If you need to fetch a specific file (like an updated version of this one) from your branch, you need to move branches, pull the file, then move back to your old branch to prevent yourself from pushing to master.

```bash
git checkout master
git pull COMMIT_INFO.md
git checkout prod-<YOURNAME>
```

## COMMAND LIST

```bash
git status
```
Shows basic information about your git CLI, such as current working branch, update status, etc.

```bash
git fetch
```
Updates your remote-tracking branches.

```bash
git pull <file/dir/-a>
```
Fetches changes from your current working repository. If it has updates, it will pull them. Useful for pulling from master. `-a` means all.

```bash
git push <file/dir/-a>
```
Pushes a specific file or directory to your local repository. `-a` means all.

```bash
git commit <file/dir/-a>
```
Uploads a specific file or directory to remote repository. `-a` means all.

```bash
git checkout <branch>
```
Updates your local container of branches. Adds previously unknown branches from remote.

```bash
git update-index [--assume-unchanged/--assume-changed] <file/dir>
```
Modifies your local repo to ignore or prioritize the changes of a specific file or directory.