# Debian完全安装笔记

安装顺序：

1. 选择系统镜像

2. 制作启动u盘

3. 腾出硬盘空间

4. 进入u盘引导

5. 选择系统语言

6. 安装硬件驱动

7. 调整系统分区

   > 这里最好了解Linux文件系统的相关知识,知道每个分区的具体作用.

8. 选择软件及桌面系统

9. 安装引导，清理垃圾，最后重启

--------------

10. 添加软件源

11. 更新软件仓库缓存

12. 安装并配置sudo

    ```shell
    su
    apt-get install sudo
    gedit/vim/mousepad /etc/sudoers
    # 如下配置:
    
    # User privilege specification
    root	ALL=(ALL:ALL) ALL
    username	ALL=(ALL:ALL) ALL
    ```

    

13. 安装硬件驱动

    > sudo apt-get install firmware-*

14. 解决字体乱码问题

    **字体下载**

    > 开源的最好看的字体:思源黑体,思源宋体
    >
    > 背景:google和adobe联合开发,日本设计师执笔
    >
    > 思源宋体:Noto Fonts
    >
    > 思源黑体:Noto SansCJK
    >
    > > ps:微软雅黑字体也不错.

    **安装字体**

    >字体安装的文件夹:
    >
    >(1) /usr/share/fonts
    >
    >(2) /usr/local/share/fonts
    >
    >(3) /home/$username/.fonts
    >
    >字体安装的命令:
    >
    >(1) mkfontscale
    >
    >(2) mkfontdir
    >
    >(3) fc-cache                          //生成字体缓存
    >
    >(4)fc-list                                //列出已经安装的字体

    **设置系统语言**

    > 

15. 添加软件快捷键

-----------------

16. 安装其他基本软件（网易云音乐，输入法，编辑器，wps，git）

----

17. 进一步的桌面系统美化

