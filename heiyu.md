# linux下通过命令行开启黑阈

1. 安装adb调试工具debian系统下可以直接通过以下命令安装

   ```shell
   sudo apt-get install adb 
   ```

2. 打开手机usb调试,插入电脑usb接口,输入以下命令`lsusb`来查看手机识别码:

   ![1528706329158](/tmp/1528706329158.png)

3.手动加入adb驱动:

> 进入/etc/udev/rules.d/目录，新建一个文件，名为51-android.rules,打开并编辑,添加如下内容:
>
> ```shell
> SUBSYSTEM=="usb", ATTRS{idVendor}=="2a70", ATTRS{idProduct}=="4ee7", MODE="0666"
> ```
>
> 保存并退出

4.授予可读及执行权限:

```shell
sudo chmod a+rx 51-android.rule  
```

5.重启udev服务

```shell
sudo /etc/init.d/udev restart  
```

6.重启adb服务

```shell
adb kill-server 
```

7.开启黑阈服务:

```shell
adb devices
adb -d shell sh /data/date/me.piebridge.brevent/brevent.sh
```

具体结果:

adb devices 调试成功之后的结果:

![1528707439170](/tmp/1528707439170.png)

黑阈开启之后的结果:

![1528707384907](/tmp/1528707384907.png)

