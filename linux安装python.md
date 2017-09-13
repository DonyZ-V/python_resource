# Linux 系统下安装 python 库集合

> sudo apt-get install python3-dev build-essential libssl-dev libffi-dev libxml2 libxml2-dev libxslt1-dev zlib1g-dev
> sudo apt-get install python3
> sudo apt-get install python3-pip

## Linux 管理 python 版本

> whereis python 查看 python 路径<br>
> rm /usr/bin/python 删除命令行里 python 的指向(这个要获得root权限),然后通过 ln -s /usr/bin/python3.5 /usr/bin/python 重新关联<br>
> 获取root权限：sudo passwd root , 设置好了之后 , su root , 输入密码 , 再次禁用 sudo passwd -l root

### 安装 Mongodb

> sudo apt-get mongodb

### 安装 redis

> sudo apt-get redis-server<br>
> 注释掉 127.0.0.1 ,可以让远程连接<br>
> 设置 requirepass 可以设置登陆密码,登陆的时候 redis-cli -a [password]

### 安装 Mysql

> sudo apt-get install mysql-server mysql-client<br>
> mysql -uroot -p<br>
> show databases;  use mysql;  <br>
> 修改配置文件：sudo su -> cd mysql.conf.d -> vi mysqld.cnf , 注释掉 127.0.0.1 就可以远程连接了