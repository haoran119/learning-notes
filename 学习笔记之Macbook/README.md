# 学习笔记之Macbook

* [写给Mac新手的入门指南 - 威锋网](https://mp.weixin.qq.com/s/pqmqGZhNwevx57KeLnzZmg)
    * 篇一：Mac小白基础知识
    * 篇二：Mac小白装机必备
    * 篇三：这些小技巧让你的mac用起来更顺手
    * 篇四：如何让你的mac更安全
    * 篇五：在Mac上如何访问IE Only的网站
* [Mac 键盘快捷键 - 官方 Apple 支持 (中国)](https://support.apple.com/zh-cn/HT201236)
    * 文稿快捷键
        * Fn-上箭头：Page Up：向上滚动一页。
        * Fn-下箭头：Page Down：向下滚动一页。
        * Fn-左箭头：Home：滚动到文稿开头。
        * Fn-右箭头：End：滚动到文稿末尾。
        * Command-上箭头：将插入点移至文稿开头。
        * Command-下箭头：将插入点移至文稿末尾。
        * Command-左箭头：将插入点移至当前行的行首。
        * Command-右箭头：将插入点移至当前行的行尾。
        * Option-左箭头：将插入点移至上一字词的词首。
        * Option-右箭头：将插入点移至下一字词的词尾。
* [Mac 提升开发效率的小工具](https://mp.weixin.qq.com/s/TZHjpWcPeGvuQUgP6cmCpw)
   * https://juejin.im/post/5b0e99436fb9a009e405dbb6

## FAQ

* Numbers
    * 单元格内输入=可以快速新建公式，如果不行的话，选中单元格，然后选择格式->单元格->数据格式->数字。
    * 如何统一Numbers里表格的宽度？ - Mac综合讨论区 - 威锋论坛 - 威锋网（http://bbs.feng.com/read-htm-tid-8325154.html）
* Mac分屏怎么用？Mac Split View屏幕分割的两种教程_苹果MAC_操作系统_脚本之家 （http://www.jb51.net/os/MAC/385430.html）
* Mac显示桌面快捷键，Mac显示桌面手势_百度经验（http://jingyan.baidu.com/article/915fc414f232e651394b202c.html）
* Mac键盘失灵
    * 重启电脑后输入密码界面键盘按键都没反应。。。怀疑是打开了鼠标键，查了一下连按5下option键，还是没反应。。。突然发现连按5下command键解决问题。。。吓一身冷汗
* Cisco AnyConnect VPN reinstall报错已经存在？
    * 卸载时没用Uninstall AnyConnect.app，所以有残留。
    * https://community.cisco.com/t5/other-wireless-mobility-subjects/osx-removing-remains-from-unusual-anyconnect-uninstall/td-p/2401645
        * `sudo pkgutil --forget com.cisco.pkg.anyconnect.vpn`
    * https://community.cisco.com/t5/vpn-and-anyconnect/how-to-uninstall-any-connect-from-my-imac/td-p/2562866
        * 需要有root权限
        * `cd /opt/cisco/anyconnect/bin`
        * `sh vpn_uninstall.sh`
* How to ssh linux server ？
    * 安装MacPorts / Putty，需要等一段时间
        * Download and install MacPorts
        * `$ sudo port -v selfupdate`
        * `$ sudo port install putty`
    * Use the following command to convert the .ppk format private key to a standard PEM format private key:
        * `$ puttygen id_rsa.ppk -O private-openssh -o privatekey.pem`
    * Make sure permissions on the private key file are set properly. It should only be readable by the user that owns it.
        * `$ chmod go-rw privatekey.pem`
    * Clear known_hosts if hit "WARNING: REMOTE HOST IDENTIFICATION HAS CHANGED! Add correct host key in /Users/hao/.ssh/known_hosts to get rid of this message."
        * `$ vim ~/.ssh/known_hosts`
    * Use the key for login
        * `$ ssh -i privatekey.pem username@hostname`
        * `$ ssh username@hostname`
        * Permanently added 'rtcma-rhel-cc12.acfr.usyd.edu.au,172.16.156.86' (ECDSA) to the list of known hosts.
    * [PuTTY SSH client for Mac OS X - Download, Tutorial | SSH.COM](https://www.ssh.com/ssh/putty/mac/)
    * [How to install Putty on Mac (OS X El Capitan) | onvinetech](https://onvinetech.wordpress.com/2016/01/26/49/)
    * [The MacPorts Project -- Download & Installation](https://www.macports.org/install.php)
* How to mount remote folder over ssh ?
    * install FUSE and SSHFS for mac
    * `sudo mkdir ~/mnt/usyd`
    * `sudo sshfs -o allow_other,defer_permissions USER@XXX.XXX.XXX.XXX:/ ~/mnt/usyd`
    * or
    * `sudo sshfs -o allow_other,defer_permissions,IdentityFile=~/Downloads/ssh/privatekey.pem USER@XXX.XXX.XXX.XXX:/ ~/mnt/usyd`
    * [How To Use SSHFS to Mount Remote File Systems Over SSH | DigitalOcean](https://www.digitalocean.com/community/tutorials/how-to-use-sshfs-to-mount-remote-file-systems-over-ssh)
        * https://www.digitalocean.com/community/tutorials/how-to-use-sshfs-to-mount-remote-file-systems-over-ssh
    * [Home - FUSE for macOS](https://osxfuse.github.io/)https://osxfuse.github.io/
* How to fix Address already in use on mac ?
    * Identify the process that is using the port: You can use the lsof command in your terminal to check which process is using a specific port. If you know the port number that's causing the issue, say 8000, you can use the following command:
        * `sudo lsof -i :8000`
        * This command should list all processes using the port 8000. Look for the PID (Process ID) in the output.
    * Terminate the process: Once you have the PID, you can terminate the process with the kill command. If the PID was 1234, for instance, you'd use:
        * `kill -9 1234`
        * The -9 option ensures that the process is forcibly killed.
        * If the process doesn't terminate, it's usually because it's being run by a root user or system process. In such cases, try using sudo:
            * `sudo kill -9 1234`
            * Please replace 1234 with the actual PID you've found in step 1.
            * Once the process has been killed, you should be able to start your application again without the "Address already in use" error.
