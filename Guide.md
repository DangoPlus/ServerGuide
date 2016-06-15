# Vultr VPS服务器配置
## 一、更新Ubuntu软件源

`apt-get update`

## 二、更新Ubuntu软件
`apt-get upgrade`

## 三、Shadowsocks安装配置
`apt-get install python-pip`

`pip install -U setuptools`

`pip install shadowsocks`

### 1. 编辑配置文件
`创建/etc/shadowsocks.json文件`

    单用户
    {
      "server":"my_server_ip",
      "server_port":8388,
      "local_address": "127.0.0.1",
      "local_port":1080,
      "password":"mypassword",
      "timeout":300,
      "method":"aes-256-cfb",
      "fast_open": true
    }
    多用户
    {
    "server": "0.0.0.0",
    "port_password": {
        "8381": "foobar1",
        "8382": "foobar2",
        "8383": "foobar3",
        "8384": "foobar4"
     },
    "timeout": 300,
    "method": "aes-256-cfb"
    }


### 2. [优化shadowsocks连接](https://github.com/shadowsocks/shadowsocks/wiki/Optimizing-Shadowsocks)


### 3. 启动shadowsocks
`ssserver -c /etc/shadowsocks.json -d start`

### 4. 开机自动后台启动shadowsocks
`编辑/etc/rc.local文件，并添加启动shadowsocks的语句`

## 四、使用LNMP一键安装包安装服务器环境
### [安装教程](http://lnmp.org/install.html)
### [LNMP添加、删除虚拟主机及伪静态使用教程](http://lnmp.org/faq/lnmp-vhost-add-howto.html)
