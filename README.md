# iStoreOS/OpenWrt一键备份与恢复脚本 <img alt="GitHub release (by tag)" src="https://img.shields.io/github/downloads/wukongdaily/OpenBackRestore/v1.0/total?label=%E4%B8%8B%E8%BD%BD%E6%AC%A1%E6%95%B0&labelColor=%2332CD32&color=black">
## 🤔 这是什么？

该项目可以轻松备份iStoreOS已安装的软件和配置,当系统恢复出厂设置或重置后，可以一键恢复原来的软件和配置。<br>
该项目Fork自悟空大佬，优先使用其源码：https://github.com/wukongdaily/OpenBackRestore <br>
本人RAX3000M运行报错：tar: /overlay: Cannot stat: No such file or directory <br>
备份脚本文件backup.run中，“/overlay”修改为“/rom/overlay”，就能正常备份 <br>
如遇类似报错，可在后台“系统-挂载点”页面，或者用命令行“df -h”，查看overlay的实际挂载路径，替换即可

## 🚀 方法一 命令行方式

### 1. 生成备份`/tmp/upload/backup.tar.gz`
```bash
wget -O backup.run https://raw.githubusercontent.com/jumplong/OpenBackRestore/master/backup/backup.run && sh backup.run
```
> 备份仓库
```bash 
wget -O backup.run https://mirror.ghproxy.com/https://raw.githubusercontent.com/jumplong/OpenBackRestore/master/backup/backup.run && sh backup.run
```
> 每次备份都是完整的,可以经常备份,比如每月备份一次
### 🤔 如何自定义备份的路径？方法如下
https://github.com/wukongdaily/OpenBackRestore/wiki
```bash
# 举例说明 假设要备份到 /mnt/sata1-4目录
wget -O backup.run https://raw.githubusercontent.com/jumplong/OpenBackRestore/master/backup/backup.run
sh backup.run /mnt/sata1-4
```

### 2. 恢复备份 

**使用前提** 将备份档案提前上传到 `/tmp/upload/` 目录,如图<br><br>![huifu](https://github.com/jumplong/OpenBackRestore/assets/143675923/cd111f10-e6aa-4011-a046-b3004f77c7eb)

> 确定备份文件已经上传了 再执行如下命令即可恢复,恢复完成后会自动重启
### ❤️恢复命令如下

```bash
wget -O restore.run https://raw.githubusercontent.com/jumplong/OpenBackRestore/master/backup/restore.run && sh restore.run
```
> 备份仓库
```bash 
wget -O restore.run https://mirror.ghproxy.com/https://raw.githubusercontent.com/jumplong/OpenBackRestore/master/backup/restore.run && sh restore.run
```


## 🚀 方法二 手动方式

> 1、在release页面下载backup.run或restore.run<br>
https://github.com/wukongdaily/OpenBackRestore/releases/latest <br>
> 2、打开iStore应用商店,点击手动安装,将run文件拖拽上去即可执行。<br>
![image](https://github.com/jumplong/OpenBackRestore/assets/143675923/54fdc034-ed4f-4f81-8aa7-0de556e0c3e2)

# 💰打赏原作者💰
<img src="https://github.com/wukongdaily/tvhelper-docker/assets/143675923/1f92c5ba-1b6b-4967-a1ab-20697159badc" width="30%" />


