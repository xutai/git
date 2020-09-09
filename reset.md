 在commit的时候去掉node_modules文件夹及其子目录与文件
```


ref: Stage all but one folder [duplicate]

// won't work!!
git add .
git rm node_modules -r

// working
git add .
git reset -- node_module


git-reset - Reset current HEAD to the specified state
```
- [https://stackoverflow.com/questions/20160503/stage-all-but-one-folder](https://stackoverflow.com/questions/20160503/stage-all-but-one-folder)

- [https://git-scm.com/docs/git-reset](https://git-scm.com/docs/git-reset)