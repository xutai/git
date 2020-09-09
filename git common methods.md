
## git一些使用的方法



### gitlab 或 github 创建项目
```
git init
git add .
git remote add origin git@gitlab.com:insiderdejavu/mlgm.git
// github 如果只https的换，直接用给的链接
git commit -m "first commit"
git push -u origin master
```

### 设置账号和密码

在[git-config](https://git-scm.com/docs/git-config)这里，搜索`user.name`， `-global`这个在OPTIONS里面，那么到底是不是这个？不过倒是可以设置

```shell
$ git config --global user.name "xutai"
```

然而为什么每次提交`git push`的时候都要求输入账号和密码呢，看这个[Why is Git always asking for my password?](https://help.github.com/en/articles/why-is-git-always-asking-for-my-password)里面讲到[Caching your GitHub password in Git](https://help.github.com/en/articles/caching-your-github-password-in-git)。要让本地机器记住你的账号和密码








### 创建一个分支

`git brach -b someBranch`

-b是什么意思，看文档[git-branch](https://git-scm.com/docs/git-branch)的这句话

`Note: If you are creating a branch that you want to checkout immediately, it is easier to use the git checkout command with its -b option to create a branch and check it out with a single command.`

此外看[文档](https://git-scm.com/docs/git-checkout#Documentation/git-checkout.txt-emgitcheckoutem-b-Bltnewbranchgtltstartpointgt)里`git checkout -b|B-B <new_branch> [<start point>]`说到

```
Specifying -b causes a new branch to be created as if git-branch[1] were called and then checked out. In this case you can use the --track or --no-track options, which will be passed to git branch. As a convenience, --track without -b implies branch creation; see the description of --track below.

If -B is given, <new_branch> is created if it doesn’t exist; otherwise, it is reset. This is the transactional equivalent of

$ git branch -f <branch> [<start point>]
$ git checkout <branch>
```

### 将其他分支这整合到master分支
[文档](https://git-scm.com/docs/git-merge)
即`Documentation - Reference - Branching and Merging - merge`
案列：
```
我有一个分支branchOne, 我使用`git checkout master`切换到master分支，然后使用`git merge branchOne`将branchOne整合到master
```


### 推送一个分支到仓库

`git push origin branchName`

查[文挡](https://git-scm.com/docs/git-push#Documentation/git-push.txt-ltrefspecgt82308203)，有点像是`git push <repository <refspec>`