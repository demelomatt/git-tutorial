# Git-tutorial

## Git configuration

Set the name that will be attached to your commits and tags.

```bash
git config --global user.name "Your Name"
```

Set the e-mail address that will be attached to your commits and tags.

```bash
git config --global user.email "you@example.com"
```

## Starting A Project

Create a new local repository.

```bash
git init [project name]
```

Downloads a project with the entire history from the remote repository.

```bash
$ git clone [project url]
```

When you clone a repository with *git clone*, it automatically creates a remote connection called **origin** pointing back to the cloned repository.

## Day-To-Day Work

Displays the status of your working directory.

```bash
git status
```

Add a file to the staging area.

```bash
git add [file]
```

Show changes between working directory and staging area.

```bash
git diff [file]
```

Shows any changes between the staging area and the repository.

```bash
git diff --staged [file]
```

Discard changes in working directory. This operation is unrecoverable.

```bash
git checkout -- [file]
```

Revert your repository to a previous known working state.

```bash
git reset [file]
```

Create a new commit from changes added to the staging area.

```bash
git commit -m [message]
```

Remove file from working directory and staging area.

```bash
git rm [file]
```

## Git branching

List all local branches in repository. With -a: show all branches (with remote).

```bash
git branch [-a]
```

Create new branch, referencing the current HEAD.

```bash
git branch [branch_name]
```

Rename branch

```bash
git branch -m [old_name][new_name]
```

Both [Conservancy](https://sfconservancy.org/news/2020/jun/23/gitbranchname/) and the Git project are aware that the initial branch name, ‘master’, is offensive to some people.                                                                                                                             Many communities, both on [GitHub](https://github.com/github/renaming) and in the wider Git community, are considering renaming the default branch name of their repository from master. GitHub is gradually renaming the default branch of our own repositories from *master* to *main*.

Switch working directory to the specified branch. With -b: Git will create the specified branch if it does not exist.

```bash
git checkout [-b][branch_name]
```

Join specified [from name] branch into your current branch.

```bash
git merge [-m][from name]
```

## Git Remote

List the remote connections you have to other repositories. -v include the URL of each connection.

```bash
git remote [-v]
```

Create a new connection to a remote repository. After adding a remote, you’ll be able to use      [name] as a convenient shortcut for [url] in other Git commands.

```bash
git remote add [name] [URL]
```

Two of the easiest ways to access a remote repo are via the **HTTP** and the **SSH** protocols. HTTP is an easy way to allow anonymous, read-only access to a repository. But, it’s generally not possible to push commits to an HTTP address. For read-write access, you should [use SSH](https://docs.github.com/en/authentication/connecting-to-github-with-ssh) instead.

Remove the connection to the remote repository called [name].

```bash
git remote remove [name]
```

Change your remote's URL

```bash
git remote set-url [remote] [url]
```

Fetch changes from the remote, but not update tracking branches.

```bash
git fetch [remote]
```

Fetch changes from the remote and merge current branch with its upstream.

```bash
git pull [remote] [branch]
```

Push local branch to remote repository. S

```bash
git push -u [remote] [branch]
```