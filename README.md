# Xiaohua 雷达
都什么年代了 还在使用 虚拟机? 局域网? 两台电脑? 开了加速器就失效的雷达?

醒一醒好吧!现在可是2018年 Cloud 云服务时代

只要打开浏览器输入网址 即可享受雷达!

# 如何搭建自带加速器的云端雷达?
(复制时请复制""内的内容)

第一步 
我们要把自己的服务器变成一个SS代理
如何操作呢? 复制粘贴以下代码
如何看代码是否执行完成了 可以进行下一步操作了?
看到终端出现 [root@******* _centos ~]#的时候就代表可以进行下一步操作了 !

"wget --no-check-certificate -O shadowsocks-all.sh https://raw.githubusercontent.com/teddysun/shadowsocks_install/master/shadowsocks-all.sh"










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


# 教程结束!
QQ:839387596
By:Xiaohua
