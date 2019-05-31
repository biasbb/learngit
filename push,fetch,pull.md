git push用来将本地分支的更新推送到远程主机

- 完整的命令格式为

  >  $ git push <远程主机名> <本地分支名> :<远程分支名>

  如果省略远程分支名，就表示将远程分支推送到与之有追踪关系的远程分支(一般就是同名的那个)

---

git fetch用来将远程仓库的跟新取回本地

- > $ git fetch <远程主机名> <远程分支名>

  即取回远程主机对应分支的更新。

  如果不加分支名就取回所有的更新

- 取回来的跟新在本地上要用"远程主机名/远程分支名"这样的形式读取，例如origin的master在本地就要用origin/master来读取

- >$ git branch 

  查看本地所有分支

  >$ git branch -r

  查看远程取回的分支

  > $ git branch -a

  查看所有的分支

- 取回远程分支，要用它来创建一个新的分支

  > $ git checkout -b dev origin/master

- 亦可以把取回的分支和当前分支合并

  > $ git merge origin/master

---

git pull就是取回远程主机的某个分支的更新，再与本地的置顶分支合并

- 完整格式为(注意与push后面几个参数的顺序相区分)

  > $ git pull  <远程主机名> <远程分支名>:<本地分支名>

  如果省略本地分支名，则表示与当前分支合并。

- 相当于是

  > $ git fetch origin master
  >
  > $ git merge origin/master

  上面就等于

  > $ git pull origin master:master

  

  