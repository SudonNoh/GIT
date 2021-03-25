## Pull 했을 경우 안되면 ?


#### <b>오류가 생기는 과정</b>  
1. A 컴퓨터에서 push
2. B 컴퓨터에서 작업을 하는 도중에 pull  


#### <b>해결 방법</b>
덮어쓰기

```git
error: Your local changes to the following files would be overwritten by merge:
```

```git
$ git fetch --all
Fetching origin
```

```git
$ git reset --hard origin/main
HEAD is now at ~~~ ## version
```
