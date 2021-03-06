<div align="left">
<h1 align="left"> 🍨 Scoopet 🍨 </h1>
<p>
<a>
<img src="https://ci.appveyor.com/api/projects/status/kbd3a9mibncbx8ds?svg=true"/>
</a>
<a>
<img src="https://img.shields.io/github/languages/code-size/integzz/scoopet.svg">
</a>
<a>
<img src="https://img.shields.io/github/repo-size/integzz/scoopet.svg">
</a>
<a>
<img src="https://img.shields.io/github/license/integzz/scoopet">
</a>
</p>
</div>

<p></p>

<div>
<p>
一个用于 Windows 最佳命令行软件管理器<a href="https://github.com/lukesampson/scoop">Scoop</a>的脚本仓库：持续助力科研
</p>

<p align="left">
        <a href="README.md">English</a> | <a href="README_CN.md">简体中文</a>
</p>
</div>

对于熟悉 Scoop 的用户：

```
scoop bucket add scoopet https://github.com/integzz/scoopet
```

# :running: 开始

## :bike: 安装 Scoop

### :computer: 步骤 1：在 PowerShell 中打开远程权限

```powershell
Set-ExecutionPolicy RemoteSigned -scope CurrentUser
```

### :gear: 步骤 2：自定义 Scoop 安装目录

```powershell
$env:SCOOP='Your_Scoop_Path'
[Environment]::SetEnvironmentVariable('SCOOP', $env:SCOOP, 'User')
```

> 如果跳过该步骤， Scoop 将默认把所有用户安装的 App 和 Scoop 本身置于`c:/users/user_name/scoop`

### :hammer: 步骤 3：下载并安装 Scoop

```powershell
Invoke-Expression (New-Object System.Net.WebClient).DownloadString('https://get.scoop.sh')
```

### :book: 步骤 4：通过`scoop help`查看快速上手方法

更多信息，请访问 Scoop 官网 👉 https://scoop.sh/ 👈

## :car: 利用扩展库安装 App

### :train: 步骤 1：安装 Aria2 来加速下载

```powershell
scoop install aria2
```

如果使用VPN，需要通过如下命令关闭 aria2

```powershell
scoop config aria2-enabled false
```

### :ticket: 步骤 2：安装 Git 来添加新仓库

```powershell
scoop install git
```

### :airplane: 步骤 3：添加本仓库并更新，么么哒~ :kiss:

```powershell
scoop bucket add scoopet https://github.com/integzz/scoopet
scoop update
```

### :rocket: 步骤 4：安装 App

- 使用 `scoop search` 命令搜索 App 的具体名称

```powershell
scoop search <app_name>
```

- 利用插件`scoop-completion`协助安装

```powershell
scoop install scoop-completion
scoop install <app_name>
```

> 使用`scoop-completion`：键入 App 名称的前几个字母后敲击`tab`键进行补全

### :100: 步骤 5：查看官方推荐仓库

```powershell
scoop bucket known

main [默认]
extras [墙裂推荐]
versions
nightlies
nirsoft
php
nerd-fonts
nonportable
java
games
jetbrains
```

## :m: 其他

### Aria2的参数自定义

```powershell
# aria2 在 Scoop 中默认开启
scoop config aria2-enabled true
# 关于以下参数的作用，详见aria2的相关资料
scoop config aria2-retry-wait 4
scoop config aria2-split 16
scoop config aria2-max-connection-per-server 16
scoop config aria2-min-split-size 4M
```

## :star: 总结

### 科研工具

|           App            |    版本    | 安装文件 | 官网                                      |
| :----------------------: | :--------: | :------: | ----------------------------------------- |
|      CopyTranslator      |   9.2.0    | 社区 zip | https://copytranslator.github.io/         |
|    GeoGebra-Portable     |  6.0.604   | 官方 zip | https://www.geogebra.org/                 |
|          Gephi           |    0.92    | 官方 exe | https://gephi.org/                        |
|        Grammarly         |  1.5.68.0  | 官方 exe | https://www.grammarly.com/native/windows/ |
|         Julia-cn         |   1.5.0    | 镜像 exe | https://julialang.org/                    |
|         KingDraw         |  1.1.2.0   | 官方 exe | http://kingdraw.cn/                       |
|          LyX-cn          |   2.3.5    | 镜像 exe | https://www.lyx.org/                      |
|  Mathpix Snipping Tool   | 02.05.0017 | 官方 exe | https://mathpix.com/                      |
|     Mendeley Desktop     |   1.19.6   | 官方 exe | https://www.mendeley.com/                 |
|       Miniconda-cn       |   4.8.3    | 镜像 exe | https://conda.io/miniconda.html/          |
|         NetLogo          |   6.1.1    | 官方 msi | https://ccl.northwestern.edu/netlogo/     |
|         Obsidian         |   0.8.12   | 社区 exe | https://obsidian.md/                      |
| Cytoscape [构建中。。。] |   3.8.0    | 官方 zip | https://cytoscape.org/                    |

### 开发辅助

|          App           |      版本       |    安装文件     | 官网                                            |
| :--------------------: | :-------------: | :-------------: | ----------------------------------------------- |
|       Cyberduck        |   7.5.1.33324   |    官方 msi     | https://cyberduck.io/                           |
|    scoop-completion    |      0.2.3      |    社区 psm1    | https://github.com/Moeologist/scoop-completion/ |
|         uTools         |       1.3       |    官方 exe     | https://u.tools/                                |
| VirtualBox [含扩展包]  |     6.1.10      |    官方 exe     | https://www.virtualbox.org/                     |
| VMware Workstation Pro | 15.5.2-15785246 |    官方 exe     | https://www.vmware.com/                         |
|         WinGet         |    0.2.2521     | 社区 appxbundle | https://github.com/microsoft/winget-cli         |
|        分区助手        |       8.3       |    官方 zip     | https://www.disktool.cn/                        |

### 日常办公

|        App         |    版本     | 安装文件 | 官网                                               |
| :----------------: | :---------: | :------: | -------------------------------------------------- |
|   File Converter   | 7.2.5.32097 | 官方 msi | https://file-converter.org/                        |
|   Microsoft Edge   | 85.0.564.51 | 官方 7z  | https://www.microsoft.com/edge                     |
|  Office Tool Plus  |   7.6.0.1   | 社区 exe | https://github.com/YerongAI/Office-Tool/           |
| VeraCrypt-Portable |    1.246    | 社区 exe | https://www.veracrypt.fr/                          |
|   Wise Care 365    |  5.5.7.552  | 官方 exe | https://www.wisecleaner.com/wise-care-365.html     |
| Wise Disk Cleaner  | 10.3.1.783  | 官方 exe | https://www.wisecleaner.com/wise-disk-cleaner.html |
|     WPSOffice      | 11.1.0.9912 | 官方 exe | https://pc.wps.cn/                                 |
|      百度网盘      |  7.0.4.11   | 官方 exe | https://pan.baidu.com/                             |
|     灵格斯词霸     |    2.9.2    | 社区 zip | http://www.lingoes.cn/                             |

### 社交休闲

|        App        |     版本     | 安装文件 | 官网                                        |
| :---------------: | :----------: | :------: | ------------------------------------------- |
|       钉钉        |  5.1.21.19   | 官方 exe | https://www.dingtalk.com/                   |
|   洛雪音乐助手    |    1.0.1     | 官方 7z  | https://github.com/lyswhut/lx-music-desktop |
|    网易云音乐     | 2.7.1.198242 | 官方 exe | https://music.163.com/                      |
|       微信        |    2.9.5     | 官方 exe | https://pc.weixin.qq.com/                   |
|     腾讯会议      |  1.9.0.448   | 官方 exe | https://meeting.tencent.com/                |
|      You-Get      |   0.4.1403   | 社区 whl | https://github.com/soimort/you-get/         |
| QQ [构建中。。。] |    9.2.3     | 官方 exe | https://im.qq.com/pcqq/                     |
