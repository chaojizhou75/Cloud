# Xiaohua 雷达
都什么年代了 还在使用 虚拟机? 局域网 两台电脑的雷达?

醒一醒好吧!现在可是2018年 Cloud 云服务时代

只要打开浏览器输入网址 即可享受雷达!

# 如何搭建雷达?
(复制时请复制""内的内容)

首先在你的服务器终端  安装Github项目服务  
输入 "yum install git" 

然后输入Github项目地址 
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
