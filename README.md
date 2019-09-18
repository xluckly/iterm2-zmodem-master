# iterm2-zmodem-master
现在博客上的链接都过期了 其他版本的下载后还是会出现·rz之后卡死的问题 
1、首先需要下载安装iterm2,下载地址:下载后安装

http://www.iterm2.cn/download

2、使用brew 安装lrzsz

  终端输入brew install lrzsz,如果没有安装homeBrew需要先安装
   安装完成后检查 ls -alh /usr/local/bin/sz 是否存在

3、添加trigger

lrszs命令安装成功之后就是要创建两个脚本到/usr/local/bin目录, 下载上面两个脚本 到/usr/local/bin后 chmod 777 下载的脚本

最后修改iterm2的配置:

 打开iterm2------  同时按 command和,键 -------Profiles ----------  Default ------- Advanced ------ Triggers的Edit按钮
 Regular expression: /*/*B0100

 Action: Run Silent Coprocess

 Parameters:/usr/local/bin/iterm2-send-zmodem.sh

 Regular expression: /*/*B00000000000000

 Action: Run Silent Coprocess

 Parameters:/usr/local/bin/iterm2-recv-zmodem.sh
