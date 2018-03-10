# Git 命令参考

* git  init
* git config
* git add
* git commit
* git status
* git diff
* git diff -- HEAD [file]
* git log
* git relog
* git reset --hrad [HEAD^|commit_id]
* git reset HEAD [file]
* git checkout -- [file]
* git rm
* git push
* git pull

### 关联一个远程库

* git remote add origin [Repository ]
* git push -u origin master
* git push origin master

### 远程库克隆

* git clone  [Repository ]

### 创建与合并分支

* git checkout -b  [branch]    #创建并切换
*  git branch    #查看
* git branch   [branch]      #创建
* git checkout   [branch]      #切换
* git merge   [branch]      #合并
* git branch -d   [branch]     #删除

### 分支管理策略

* git merge --no-ff -m 
* git log --graph --pretty=oneline --abbrev-commit
* ​

### Bug分支

* git stash
* git checkout master
* git checkout -b issue-101
* git checkout master
* git merge --no-ff -m "merged bug fix 101" issue-101
* git branch -d issue-101
* git checkout dev
*  git status
*  git stash list
* git stash apply  | git stash drop
* git stash pop
* git stash apply stash@{0}

### Feature分支

* git checkout -b feature-vulcan
*  git branch -d feature-vulcan
* git branch -D feature-vulcan

### 多人协作

* git remote

* git remote -v

*  git push origin master      #推送分支

  master分支是主分支，因此要时刻与远程同步；

  dev分支是开发分支，团队所有成员都需要在上面工作，所以也需要与远程同步；

  bug分支只用于在本地修复bug，就没必要推到远程了，除非老板要看看你每周到底修复了几个bug；

  feature分支是否推到远程，取决于你是否和你的小伙伴合作在上面开发。

### 标签管理

* git tag v1.0
* git tag
* git log --pretty=oneline --abbrev-commit
* git tag v0.9 6224937
* git show v0.9
* git tag -a v0.1 -m "version 0.1 released" 3628164
* git tag -s v0.2 -m "signed version 0.2 released" fec145a
* git tag -d v0.1
* git push origin v1.0
* git push origin --tags
* git tag -d v0.9
* git push origin :refs/tags/v0.9
  - 命令`git push origin <tagname>`可以推送一个本地标签；
  - 命令`git push origin --tags`可以推送全部未推送过的本地标签；
  - 命令`git tag -d <tagname>`可以删除一个本地标签；
  - 命令`git push origin :refs/tags/<tagname>`可以删除一个远程标签。



### 自定义Git

* git config --global color.ui true
* git add -f App.class
* git check-ignore -v App.class
* git config --global alias.st status
* git config --global alias.unstage 'reset HEAD'