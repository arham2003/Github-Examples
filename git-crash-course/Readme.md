## Git Hidden Folder

There is a hidden folder called `.git` which tells you that our project is a git repo.

if we want to create a git repo in a new project we'd create folder and then initialize that repo using `git init`
```
mkdir /workspaces/tmp/new-project
cd /workspaces/tmp/new-project
git init 
touch Readme.md
code Readme.md
git status
git add Readme.md
# make changes to readme .md
git commit -m "add readme file" 
```

## Cloning

we can clone three ways: HTTPS, SSH, Github CLI

Since we're using github codespaces we'll create a temporary directory in our workspace

```sh
mkdir /workspaces/tmp
cd /workspaces/tmp
```

### HTTPS
```sh
git clone https://github.com/arham-trial/Github-Examples.git
cd Github-Examples
```

### SSH

```sh
git clone git@github.com:arham-trial/Github-Examples.git
cd Github-Examples
```

we will need to create our own key:
```sh
ssh-keygen -t rsa
```

For WSL users and if you create non default path key you might need to add it:
```sh
eval "ssh-agent"
ssh-add /home/andrew/.ssh/alt-github_id_rsa
```

we can test our connection here:
```sh
ssh -T git@github.com
```
### Github CLI



## Commits

When we want to commit code we can write git commit which will open up the commit edit message in the editor of choice.

```sh
git commit
```

Make a commit and commit message wtihout opening an editor:
```sh
git commit -m "your message"
```

## Branches

## Remotes

## Stashing

## Merging

## Add
When we want to stage changes that will be included in the commit 
We can use the "." to add all possible files.

```
git add Readme.md
git add .
```

## Reset

Reset allows you to move staged files to be unstaged.
This is useful when you want to revert all files not to be committed.

```
git add .
git reset
```

> git reset will revert a git add.

## Status

Git status shows you what files will or will not be committed.

```
git status
```

## Gitconfig File

The gitconfig file is what stores your global configurations for git such as email, name, editor and more.

showing the contents of our .gitconfig file:

```
git config --list
```

When you first install git on a machine you are suppose to setup your name and email:
```sh
git config --global user.name "Joe doe"
git config --global user.email johndoe@example.com
 
```


## log

git Log will show recent git commits to the git tree.