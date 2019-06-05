- 创建SSH Key

  > $ ssh-keygen -t rsa -C "790510103@qq.com"

  然后用户主目录下会出现.ssh目录，里面有连个文件id.rsa（私钥）和id_rsa.pub (公钥)

- 登陆Github，打开setting，SSH Key界面，点击Add SSH Key，填上任意title，在Key文本框里复制粘贴公钥id_rsa.pub文件中的内容。



因为git和github远程仓库之间是使用ssh通信的，远方仓库需要确实是你推送的内容就要进行验证私钥，只有私钥匹配才有推送权限

![屏幕快照 2019-06-05 21.04.11](../../Pictures/屏幕快照 2019-06-05 21.04.11.png)

