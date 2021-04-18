
## create tag
```
git tag tagName
git tag v1.0
```

## push tag
```
git push origin tagName
git push origin v1.0
```

## view tags
```
git tag
git tag -l "$pattern"
```

## delete tags
suppose you have a tag `v0.0.1-snapshot`
```
git push origin -d/--delete tagName
git push origin -d v0.0.1-snapshot
git push origin --delete v0.0.1-snapshot
```
```
$ git push origin -d v0.0.1-snapshot
To https://github.com/xutai/spring-demo
 - [deleted]         v0.0.1-snapshot
```