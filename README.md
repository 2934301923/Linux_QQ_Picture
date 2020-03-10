# 解决Wine_QQ无法加载图片的解决方法
问题都是一样的，如果无法加载图片，原因是开启了IPV6，关闭即可<br>
首先用文本编辑器打开配置文件

```
 sudo gedit /etc/sysctl.conf
```

在文件的末尾添加以下代码

```
# IPv6 disabled
net.ipv6.conf.all.disable_ipv6 =1
net.ipv6.conf.default.disable_ipv6 =1
net.ipv6.conf.lo.disable_ipv6 =1
```
保存退出之后删掉用户的缓存

```
 sudo rm -rf ~/.deepinwine/Deepin-QQ
```

最后重启QQ，重新登录即可！