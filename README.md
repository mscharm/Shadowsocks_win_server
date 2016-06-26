#Windows上搭建ShadowSocks服务器
##安装python环境
###soft包里的
'''
python-2.7.9.amd64.msi  #安装时选择cmd_path
'''
###安装OpenSSL
soft包里的
'''
Win64OpenSSL-1_0_2h.exe #直接安装
'''
###安装Shadowsocks服务端
'''
pip install shadowsocks
'''
###编辑config.json
在python/Scripts/目录下 新建config.json文件，内容如下：
'''
{
"server":"0.0.0.0",
"server_port":6666,
"local_address":"127.0.0.1",
"local_port":"1080",
"password":"pass",
"timeout":"300",
"method":"aes-256-cfb"
}
'''
###ss服务器启动
在python/Scripts/下，Shift+右键在此处打开命令窗口，输入：
'''
ssserver -c config.json
'''
###sske客户端连接
新建服务器对应config.json连接即可。
##参考
* https://www.python.org/downloads/windows/
* https://slproweb.com/products/Win32OpenSSL.html
* https://sourceforge.net/projects/shadowsocksgui/files/dist/Shadowsocks-win-2.5.2.zip/download