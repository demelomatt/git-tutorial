# Git-tutorial

## Git configuration

```bash
git config --global user.name "Your Name"
```

Set the name that will be attached to your commits and tags.

```bash
git config --global user.email "you@example.com"
```

Set the e-mail address that will be attached to your commits and tags.

## Starting A Project

```bash
git init [project name]
```

Create a new local repository.

```bash
$ git clone [project url]
```

Downloads a project with the entire history from the remote repository.

When you clone a repository with *git clone*, it automatically creates a remote connection called **origin** pointing back to the cloned repository.

## Day-To-Day Work

```bash
git status
```

Displays the status of your working directory.

```bash
git add [file]
```

Add a file to the staging area.

```bash
git diff [file]
```

Show changes between working directory and staging area.

```bash
git diff --staged [file]
```

Shows any changes between the staging area and the repository.

```bash
git checkout -- [file]
```

Discard changes in working directory. This operation is unrecoverable.

```bash
git reset [file]
```

Revert your repository to a previous known working state.

```bash
git commit -m [message]
```

Create a new commit from changes added to the staging area.

```bash
git rm [file]
```

Remove file from working directory and staging area.

## Git branching

```bash
git branch [-a]
```

List all local branches in repository. With -a: show all branches (with remote).

```bash
git branch [branch_name]
```

Create new branch, referencing the current HEAD.

```bash
git branch -m [old_name][new_name]
```

Rename branch

Both [Conservancy](https://sfconservancy.org/news/2020/jun/23/gitbranchname/) and the Git project are aware that the initial branch name, ‘master’, is offensive to some people.                                                                                                                             Many communities, both on [GitHub](https://github.com/github/renaming) and in the wider Git community, are considering renaming the default branch name of their repository from master. GitHub is gradually renaming the default branch of our own repositories from *master* to *main*.

```bash
git checkout [-b][branch_name]
```

Switch working directory to the specified branch. With -b: Git will create the specified branch if it does not exist.

```bash
git merge [-m][from name]
```

Join specified [from name] branch into your current branch.

## Git Remote

```bash
git remote [-v]
```

List the remote connections you have to other repositories. -v include the URL of each connection.

```bash
git remote add [name] [URL]
```

Create a new connection to a remote repository. After adding a remote, you’ll be able to use      [name] as a convenient shortcut for [url] in other Git commands.

Two of the easiest ways to access a remote repo are via the **HTTP** and the **SSH** protocols. HTTP is an easy way to allow anonymous, read-only access to a repository. But, it’s generally not possible to push commits to an HTTP address. For read-write access, you should [use SSH](https://docs.github.com/en/authentication/connecting-to-github-with-ssh) instead.

```bash
git remote remove [name]
```

Remove the connection to the remote repository called [name].

```bash
git remote set-url [remote] [url]
```

Change your remote's URL

```bash
git fetch [remote]
```

Fetch changes from the remote, but not update tracking branches.

```bash
git pull [remote] [branch]
```

Fetch changes from the remote and merge current branch with its upstream.

```bash
git push -u [remote] [branch]
```

Push local branch to remote repository. S