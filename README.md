# Git-Tutorial

Commit - an object
Branch - a reference to a commit; can have a tracked upstream
Tag - a reference (standard) or an object (annotated)
Head - a place where your working directory is now

## Git configuration

```bash
git config --global user.name "Your Name"
```

```bash
git config --global user.email "you@example.com"
```

## Starting A Project

```bash
git init [project name]
```

```bash
$ git clone [project url]
```

When you clone a repository with *git clone*, it automatically creates a remote connection called **origin** pointing back to the cloned repository.

## Day-To-Day Work

```bash
git status
```

```bash
git add [file]
```

```bash
git diff [file]
```

```bash
git diff --staged [file]
```

```bash
git checkout -- [file]
```

```bash
git reset [file]
```

```bash
git commit -m [message]
```

```bash
git rm [file]
```

## Git branching

```bash
git branch [-a]
```

```bash
git branch [branch_name]
```

```bash
git branch -m [old_name][new_name]
```

Both [Conservancy](https://sfconservancy.org/news/2020/jun/23/gitbranchname/) and the Git project are aware that the initial branch name, ‘master’, is offensive to some people.                                                                                                                             Many communities, both on [GitHub](https://github.com/github/renaming) and in the wider Git community, are considering renaming the default branch name of their repository from master. GitHub is gradually renaming the default branch of our own repositories from *master* to *main*.

```bash
git checkout [-b][branch_name]
```

```bash
git merge [-m][from name]
```

## Git Remote

```bash
git remote [-v]
```

```bash
git remote add [name] [URL]
```

Two of the easiest ways to access a remote repo are via the **HTTP** and the **SSH** protocols. HTTP is an easy way to allow anonymous, read-only access to a repository. But, it’s generally not possible to push commits to an HTTP address. For read-write access, you should [use SSH](https://docs.github.com/en/authentication/connecting-to-github-with-ssh) instead.

```bash
git remote remove [name]
```

```bash
git remote set-url [remote] [url]
```

```bash
git fetch [remote]
```

```bash
git pull [remote] [branch]
```

```bash
git push -u [remote] [branch]
```