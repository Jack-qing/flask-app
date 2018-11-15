# flask-app
#移动租房
#项目运行
项目运行之前，请确保系统已经安装以下应用
1、ubuntu (14.04 及以上版本,推荐:16.04 linux_amd64位)
2、Python3+flask

#flask-app署
>sudo apt-get update
>sudo apt-get upgrade
>sudo apt install vim
>sudo apt install git
>更换国内apt源:
>原文件备份
>sudo cp /etc/apt/sources.list /etc/apt/sources.list.bak
>编辑源列表文件:
>sudo vim /etc/apt/sources.list
>将原来的列表删除，添加如下内容（中科大镜像源:
`deb http://mirrors.ustc.edu.cn/ubuntu/ xenial main restricted universe multiverse
deb http://mirrors.ustc.edu.cn/ubuntu/ xenial-security main restricted universe multiverse
deb http://mirrors.ustc.edu.cn/ubuntu/ xenial-updates main restricted universe multiverse
deb http://mirrors.ustc.edu.cn/ubuntu/ xenial-proposed main restricted universe multiverse
deb http://mirrors.ustc.edu.cn/ubuntu/ xenial-backports main restricted universe multiverse
deb-src http://mirrors.ustc.edu.cn/ubuntu/ xenial main restricted universe multiverse
deb-src http://mirrors.ustc.edu.cn/ubuntu/ xenial-security main restricted universe multiverse
deb-src http://mirrors.ustc.edu.cn/ubuntu/ xenial-updates main restricted universe multiverse
deb-src http://mirrors.ustc.edu.cn/ubuntu/ xenial-proposed main restricted universe multiverse
deb-src http://mirrors.ustc.edu.cn/ubuntu/ xenial-backports main restricted universe multiverse`
![](media/15379416656740/15379529039711.jpg)

![](media/15379416656740/15379531758622.jpg)
>esc : wq  保存vim编辑后的内容
>运行sudo apt-get update
>运行sudo apt-get upgrade

# python+flask安装
>由于兼容性问题Ubuntu16默认安装有python2.7和python3.5.2，因此在控制台输入python命令默认使用的python2.7，这里我们要使用python3.5必须输入python3，而且对应的pip也必须输入pip3。使用pycharm开发调试时必须激活虚拟环境，否则会报错。
>sudo apt-get install python-dev
>sudo apt install python3-pip
>更换pip源到国内源,因为海外源下载速度很慢，下载失败，包丢失。。。等多种问题
>linux系统:修改 ~/.pip/pip.conf (没有就创建一个)， 内容如下
>sudo mkdir  ~/.pip
>sudo vim pip.conf
![](media/15390947868425/15397696103269.jpg)
`[global]
index-url = https://pypi.tuna.tsinghua.edu.cn/simple`

###### 安装依赖
>sudo pip3 install -r requirements.txt

###### 本机安装redis
>sudo apt-get update
>sudo apt-get install redis-server
>redis-server
>redis-cli

###### 本机安装mysql
>wget http://repo.mysql.com/mysql-community-release-el7-5.noarch.rpm
>rpm -ivh mysql-community-release-el7-5.noarch.rpm
>yum update
>yum install mysql-server

>启动
>python3 manage.py runserver -p 0.0.0.0 -p 5000

