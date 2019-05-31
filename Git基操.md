### **Git 分布式版本控制系统**

- 首先要县创建一个版本库，里面所有的文件都可以被git管理，创建时选择一个合适的位置，创建一个空目录

  >$ madir learngit

  cd到这个目录下，用pwd命令可以显示当前目录，为/User/bias/learngit

- 通过git init命令把这个目录变成Git可以管理的仓库

  > $ git init

  成功后下面会显示Initialized empty Git repository in /Users/bias/learngit/.git/

  这个时候在目录下就会出现一个.git目录，这个目录是Git用来跟踪管理版本库的，是一个隐藏的目录，可以用ls -ah命令查看

- 把要用的文件放到learngit目录下(子目录也可以),因为这是git仓库的路径，下面就是把文件放到Git仓库的两步

  - 用命令git add告诉git，把文件添加到仓库

    > $ git add 小贴士.txt

    执行这个命令，没有任何提示即成功

  - 用命令git commit告诉git，把文件**提交**到仓库

    >  $ git commit -m "加入小贴士"

    后面会显示

    > [master (root-commit) 420ed2d] 加入小贴士
    >
    >  1 file changed, 576 insertions(+)
    >
    >  create mode 100644 "\345\260\217\350\264\264\345\243\253.txt"

    **git commit命令**，**-m后面输入的是本次提交的说明，可以输入任何内容。**

    执行成功后显示一个文件被改动，插入576行内容

- 总结就是先创建一个文件夹，然后用git init初始化，之后用git add和git commit加入和说明加入的说明。

- **<u>注意commit可以一次提交多个文件，即可以add好几个之后，直接一个commit就会把当前暂存区的所有文件都放入master</u>**

---

- 用git status可以实时掌握库的状态，可以看哪些文件修改了但是没有add和commit

- 用git diff 小贴士.txt可以查看具体修改了什么内容

  ![image-20190531124510793](/Users/bias/Library/Application Support/typora-user-images/image-20190531124510793.png)

---

- 用**git log**可以查看提交的日志**<u>(HEAD指针指向当前最新版本，版本更新就是改变HEAD的指向)</u>**git中用HEAD表示最新的版本，HEAD^表示上一个，HEAD^^表示上上个，多的话就用HEAD~3，表示上三个。

- 要回退到上一个版本就用**git reset**

  > $ git reset --hard HEAD^

  以上图为例输入这个后下面就会显示HEAD is now at f4cfb8(就是commit id)  加入海盗分金

- 这时如果还想回去的话如果命令行没关的话还是可以的，找到上一个的commit id，输入前几位就行。

  > $ git reset --hard a02b54

- 如果命令行关了但是还是想恢复，可以用**git reflog**命令，这个会记录你的每一次命令，可以在里面找到对应版本的commit id。