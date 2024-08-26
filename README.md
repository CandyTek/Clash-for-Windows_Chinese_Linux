# Clash-for-Windows_Chinese_Linux
给linux打包中文版clash for windows

前往 [原版备份库](https://github.com/lantongxue/clash_for_windows_pkg/releases/tag/0.20.39) 下载 `Clash.for.Windows-0.20.39-x64-linux.deb` 文件

前往 [中文版汉化库](https://github.com/Z-Siqi/Clash-for-Windows_Chinese/releases/tag/CFW-V0.20.39_OPT-1) 下载 `Clash.for.Windows-0.20.39-Opt.1-linux-x64.tar.gz` 文件

解压 `Clash.for.Windows-0.20.39-Opt.1-linux-x64.tar.gz` ，把 resources 文件夹里的 `app.asar` 复制出来，该文件包含中文汉化信息

运行命令，解包 `Clash.for.Windows-0.20.39-x64-linux.deb` 文件

```bash
dpkg-deb -R （你的 Clash.for.Windows-0.20.39-x64-linux.deb 路径） （解包目标文件夹路径-空文件夹）
```

得到（解包目标文件夹）

把复制出来的中文汉化文件 `app.asar` 替换刚刚（解包目标文件夹）里的 `/opt/clash_for_windows/resources/app.asar` 文件

运行命令，重新打包

```bash
dpkg-deb -b （解包目标文件夹路径） （存放路径/xxx.deb）
```

完成，双击 `xxx.deb` 即可安装
