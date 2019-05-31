- 创建SSH Key

  > $ ssh-keygen -t rsa -C "790510103@qq.com"

  然后用户主目录下会出现.ssh目录，里面有连个文件id.rsa（私钥）和id_rsa.pub (公钥)

- 登陆Github，打开setting，SSH Key界面，点击Add SSH Key，填上任意title，在Key文本框里复制粘贴公钥id_rsa.pub文件中的内容。

