使用git时出现的一些问题



1.

```
$ git push -u origin master
ssh: Could not resolve hostname https: Name or service not known
fatal: Could not read from remote repository.

Please make sure you have the correct access rights
and the repository exists.
```

查看[这篇文章](https://stackoverflow.com/questions/53129706/ssh-could-not-resolve-hostname-git-name-or-service-not-known-fatal-could-not)，和[这篇](https://stackoverflow.com/questions/10904339/github-fatal-remote-origin-already-exists)

不知道啥问题，**后来改了git上这个repository的名字**在尝试

`git remote -v`和`git remote set-url origin URLYouChoose`

