![](image/26.png)

- untracked：未跟踪，即存在于工作区，没有加入到缓存区。使用git add之后就被加入到了暂存区，变成了staged
- staged：工作区的文件git add之后变成这种状态，继续git commit提交到分支之后就变为unmodified
- modified：一个文件add到暂存区同时又commit之后，又对其进行了修改，就变成了modified，需要再次add和commit
- unmodified：一个文件add到暂存区同时又commit之后，就变成这种状态，如果修改它一下就变成了modified。