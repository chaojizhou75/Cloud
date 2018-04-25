# Xiaohua 雷达
都什么年代了 还在使用 虚拟机? 局域网? 两台电脑? 开了加速器就失效的雷达?

醒一醒好吧!现在可是2018年 Cloud 云服务时代

只要打开浏览器输入网址 即可享受雷达!

# 如何搭建自带加速器的云端雷达?
# (复制时请复制""内的内容)

第一步 
我们要把自己的服务器变成一个SS代理
如何操作呢? 复制粘贴以下代码
如何看代码是否执行完成了 可以进行下一步操作了?
看到终端出现 

# [root@******* _centos ~]#

的时候就代表可以进行下一步操作了 !


# 安装SS插件 让服务器变成SS加速器 妈妈再也不用怕我裸连卡啦!

"wget --no-check-certificate -O shadowsocks-all.sh https://raw.githubusercontent.com/teddysun/shadowsocks_install/master/shadowsocks-all.sh"

"chmod +x shadowsocks-all.sh"

"./shadowsocks-all.sh 2>&1 | tee shadowsocks-all.log"
输入完这行代码后 会让你选择 安装SS还是SSR 看你自己需求
如果要简单 就选默认 第一个Shadowsocks 你可以可以直接按回车 默认就是第一个

之后会让你设置一个SS连接的密码password: 自己设置一个密码
回车

然后会让你设置一个端口 port  (1~65535 )自己选一个
回车

最后就是设置加密协议 这个默认就好直接回车aes-256-gcm
之后等待他自己安装完成  
完成后会出现红色字样 
就是你搭建的SS服务器节点信息 IP 密码 端口 加密协议 等.

# 以上是搭建SS代理的教程

# =======================================

# 接下来需要安装nodejs和npm (老方法 一行一行复制粘贴)
"curl https://raw.githubusercontent.com/creationix/nvm/v0.13.1/install.sh | bash"

"source ~/.bash_profile"

"nvm install v9.8.0"

"nvm alias default v9.8.0"

# =======================================

# 还需要安装一个libpcap  (老方法 一行一行复制粘贴)
"yum -y install gcc-c++"

"yum -y install flex"

"yum -y install bison"

"wget http://www.tcpdump.org/release/libpcap-1.8.1.tar.gz"

"tar -zxvf libpcap-1.8.1.tar.gz"

"cd libpcap-1.8.1"

"./configure"

"make"

"make install"

# =======================================

# 最后搭建雷达.
首先在你的服务器终端   
输入 "yum install git" 
 
"git clone https://github.com/XiaohuaCN/Cloud-Radar"

"cd Cloud-Radar/"

"npm i"

"npm i -g pino"

"npm install -g forever"

"forever start index.js sniff eth0 XX.XX.XX.XX | pino"
(此处 的XX.XX.XX.XX 填写你服务器的内网IP)

以上操作完成后 打开浏览器输入你的 服务器公网IP 然后在后面加上":20086"
就如你的公网IP是127.0.0.1  那你需要在浏览器地址栏内输入127.0.0.1:20086 然后回车
# =======================================

# 最后如何上游戏使用?
1.下载SSTap-Free 软件 https://share.weiyun.com/56wRJOW
打开后选择 那个+号图标 添加代理  选择添加一个SS/SSR代理
然后上面的服务器IP 密码 端口等 信息就是你之前搭建SS 的线路 照抄即可

填写好后 下面编辑并激活使用 打钩然后点保存   保存后点击右边的小闪电按钮
测试一下代理是否正常 显示TCP 绿色 UDP绿色 就可以了

2.连接SSTap-Free(模式选择绝地求生所有服)  然后打开网页 输入你搭建好的雷达网址:XXX.XXX.XXX.XXX:20086

3.上游戏吧
 

# 教程结束! 
QQ:839387596
By:Xiaohua
