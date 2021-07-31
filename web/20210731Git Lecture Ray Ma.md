# 7.31/21 Git —Lecture —Ray M
## 主要知识点
- [1 Git global setup](#1-git-global-setup)
- [2 Git stash 缓存](#2-git-stash-缓存)
- [3 Branching](#3-Branching)
- [4 Git undo changes](#4-git-undo-changes)
- [5 Git Graph](#5-git-graph) 
- [6 Merge conflicts](#6-Merge-conflicts) 
- [7 Connect to remote repo](#7-connect-to-remote-repo) 
- [8 Update remote from local](#8-update-remote-from-local) 
- [9 Delete a remote branch](#9-delete-a-remote-branch) 


### 1 Git global setup

```jsx
**$ git config --global user.name "John Doe"
$ git config --global user.email johndoe@example.com**

Git automatically colors most of its output,The default setting is auto, 
which colors output when it’s going straight to a terminal

**$ git config --global color.ui auto**

You can pass --conflict either diff3 or merge (which is the default). If you 
pass it diff3, Git will use a slightly different version of conflict markers, 
not only giving you the “ours” and “theirs” versions, but also the “base”
 version inline to give you more context.

**$ git config --global merge.conflictstyle diff3**

By default, Git uses whatever you’ve set as your default  text editor 
to create and edit your commit and tag messages
**$ git config --global core.editor emacs**

```

### 2 Git stash 缓存

The git stash command takes your uncommitted changes (both staged and unstaged), saves them away for later use, and then reverts them from your working copy.

- git stash list 显示列表
git stash pop 移除
git stash apply --index

### 3 Branching

```jsx

git checkout -b //branch
git branch -d //delete
git fetch //Downloads all history from the remote tracking branches

git pull //Updates your current local working branch with all new
					//commits from the corresponding remote branch on GitHub.
					//git pull is a **combination** of **git fetch and git merge**

```

### 4 Git undo changes

```jsx
git-clean // Remove untracked files from the working tree
git revert // 用一个新的commit对历史记录回滚
git reset //从历史记录中删除commit

```

### 5 Git Graph

The main point of using a visualizer is to help you make sense of your branch history.

```jsx
git log --all --decorate --oneline --graph
```

### 6 Merge conflicts

```jsx
如果不想解决冲突：
git merge <branch name> --abort
git merge <branch name> --overwrite-ignore
git merge <branch name> --no-overwrite-ignore
```

### 7 Connect to remote repo

```jsx
git clone
git remote add <name> <url>
git remote rm <name>
git remote rename <old-name> <new-name>
```

### 8 Update remote from local

```jsx
git push <name> <branch>
git push <name> <local_branch>:<remote_branch>
```

### 9 Delete a remote branch

```jsx
git push -d <name> <branch>
git push <name> :<branch>
```

### 10 两种workflow: merge 和 rebase

![Image of differences](http://cdn.differencebetween.net/wp-content/uploads/2018/11/Difference-Between-Git-Rebase-and-Merge-.png)
