# 系统包管理

用命令去下载，升级，管理安装在系统上的软件。

## Windows

chocolatey 是用在 Windows 上的系统包管理工具。

### 安装

打开 Windows 系统的命令行界面，可以之前安装的 cmder ，用 Powershell ad Admin 这种模式创建一个 cmder 标签，然后在上面可以执行安装 chocolatey 。

**修改安全策略**

安装之前先修改一下系统的安全策略，执行：

```
Set-ExecutionPolicy AllSigned or Set-ExecutionPolicy Bypass
```

**安装 chocolatery**

再执行下面命令安装 chocolatery：

```
iex ((New-Object System.Net.WebClient).DownloadString('https://chocolatey.org/install.ps1'))
```

**测试**

安装完成以后你应该可以使用 choco 命令去管理系统上的软件包。

```
choco --help
```



