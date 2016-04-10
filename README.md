# Android-IM是一份Android即时通信的源码
######这份源码的来源是https://github.com/Pirngruber/AndroidIM 从这里下载之后，放在android studio里面编译通过后，上传到github上给自己做个备份。修改：导入android studio后修改了里面发送通知的地方，因为之前发送通知的代码已经过时了。
#####包含功能：
######服务器部分：

- 由简单的php脚本组成

######客户端部分：
- 登陆
- 注册
- 添加好友
- 赞成被添加
- 与好友列表中的好友发文字消息
- 好友在线离线状态显示
- 启动一个服务用来接受消息
- 来消息后从通知栏显示通知，退出应用(同时杀死后台服务)

#####使用说明：
1. 首先搭建服务器，就搭建一个amp(Apache+Mysql+php)服务器。然后将该代码android-im目录放到服务器根目录下面。
2. 进入Mysql新建一个数据库androidim，然后导入android_im.sql脚本新建项目所需要用到的表。
3. 修改index.php文件里面的配置，如下。至此就将该服务器搭建好了。
$dbHost = "localhost";//表示本地数据库
$dbUsername = "root";//数据库用户
$dbPassword = "123456";//数据库密码
$dbName = "androidim";//数据库的名字
4. 用android studio打开项目后，修改SocketOperator.java中AUTHENTICATION_SERVER_ADDRESS = "http://192.168.1.103/android-im/"; //192.168.1.103修改成服务器的IP地址。至此客户端也配置完成，就可以运行了。

##### *注意：关于该代码的使用发生的一切纠纷，于本人无关，多谢！*
