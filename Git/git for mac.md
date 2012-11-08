 GitHub使用 Mac
 =========
 
###1.配置git和github

	$ cd ~/.ssh    //检查计算机ssh密钥

获得密钥：

	$ ssh-keygen -t rsa -C "defnngj@gmail.com"  //填写email地址，然后一直“回车”ok
 
 打开本地..\.ssh\id_rsa.pub文件。此文件里面内容为刚才生成人密钥。
 
 登陆github系统。
 
 点击右上角的Account Settings --->SSH Public keys ---> add another public keys
 
把你本地生成的密钥复制到里面（key文本框中）， 点击 add key 就ok了
 
接着打开git ，测试连接是否成功

	$ ssh -T git@github.com