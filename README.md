# hostloc_getPoints

小鸡定时获取hostloc积分


**第一步**下载下列代码
https://github.com/nanyi212/hostloc_upgrade/blob/main/hostloc.py
**第二步**把175，176行代码改为
```
username = "账户"
password = "密码"
```

```
```
username = "账户1，账户2"
password = "密码1，密码2"
```
```

**第三步**上面文件上传到小鸡

**第四步**在小鸡里新建crontab任务

```
crontab -e
```


添加

```shell
10 2 * * * sleep 5;cd /root/hostloc/ && /usr/local/bin/python3 /root/hostloc/hostloc_auto_get_points.py
```
10 2 * * * sleep 5;cd /root/hostloc/ && /usr/bin/python3 /root/hostloc/hostloc.py
```

/root/hostloc/为你上传的路径

/usr/local/bin/python3为你小鸡python3的引用路径
/usr/bin/python3

**提示**

1.如果提示以下错误

```python
Traceback (most recent call last):
  File "/root/hostloc/hostloc_auto_get_points.py", line 6, in
   ...
```

请安装request模块

```shell
pip3 install requests
```

安装不上使用：
```
sudo apt install python3-package_name
```

2.老哥们可先运行成功以后再添加crontab任务

```shell
cd /root/hostloc/ && /usr/local/bin/python3 /root/hostloc/hostloc_auto_get_points.py
```

安装：
sudo apt-get update
sudo apt-get install python3-pip


pip3 install pyaes

pip3 install requests



env
HOSTLOC_USERNAME=username1,username2...
HOSTLOC_PASSWORD=password1,password2...
