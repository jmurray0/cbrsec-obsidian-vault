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
git pull <-a>
```
Fetches changes from your current working repository. If it has updates, it will pull them. Useful for pulling from master.

```bash
git update-index [--assume-unchanged/--assume-changed] <file>
```
Modifies your local repo to ignore or prioritize the changes 