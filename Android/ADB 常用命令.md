熟练使用 **adb 命令** 有助于提高开发效率。 很多公司在面试时也会询问有没有用过 adb 命令，常用的有哪些？若能脱口而出，将直接说明你经常使用。

不多说，直接上命令了。

---

- **启动 adb 服务：**`adb start-server`
- **关闭 adb 服务：**`adb kill-server`
- **查看所有连接成功的设备：**`adb devices`

---

> **以下命令，若只有一台设备，可忽略命令中的 `-s 设备名`**。

例如：**进入指定在线设备的 shell：**`adb -s 设备名 shell`【若只有一台，可直接使用：`adb shell`】

- **进入指定在线设备的 shell：**`adb -s 设备名 shell`
- **重启手机：**`adb -s 设备名 reboot`
- **重启到bootloader,即刷机模式：**`adb -s 设备名 reboot bootloader`
- **重启到 recovery，即恢复模式：**`adb -s 设备名 recovery`
- **查看 logcat：** `adb -s 设备名 logcat`
- **清除 log 缓存：**`adb -s 设备名 logcat -c`
- **安装 APP：**`adb -s 设备名 install -r xxx.apk`(xxx表示 apk 的全路径，通常情况下，输入完-r后直接将apk 拖到命令窗口)
- **卸载 APP：**`adb -s 设备名 uninstall 包名`
- **将手机中的文件复制出来：**`adb -s 设备名 pull 文件全路径 目的地全路径`
- **向手机发送文件：**`adb -s 设备名 push 文件全路径 目的地全路径`

---

> **以下命令，若没有进入到设备的 shell，需要在最前面添加 `adb -s 设备名 shell ` 才能执行**

- **清除指定应用的数据：**`pm clear 包名`
- **启动某个应用的某个 Activity：**`am start -n 包名/包名.Activity名`
- **查看进程信息：**`ps`
- **查看所有已安装的应用的包名：**`pm list packages -f`
- **查看栈顶 Activity，可以用来获取包名，可以用来查看其它 APP 的包名：**`dumpsys activity top`
- **内存使用情况 Memory Usage：**`dumpsys meminfo`
- **包信息 Package Information：**`dumpsys package`
- **查看手机 CPU 以及手机架构：**`cat /proc/cpuinfo`
- **刷新一次内存信息，然后返回：**`top -n 1`
- **查看 WiFi 密码：**` cat /data/misc/wifi/*.conf`(需要权限)

------

> **文章若有不对之处，欢迎在 `Issues` 指正，谢谢~**
>
> **邮箱：liuguangmingcn@163.com**

