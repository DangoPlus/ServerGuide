# Vultr VPS服务器配置
## 一、更新Ubuntu软件源

　　　　`apt-get update`

## 二、更新Ubuntu软件
　　　　`apt-get upgrade`

## 三、Shadowsocks安装配置
　　　　`apt-get install python-pip`

　　　　`pip install -U setuptools`

　　　　`pip install shadowsocks`

## 编辑配置文件
　　　　`创建/etc/shadowsocks.json文件`

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
