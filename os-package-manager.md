# 系统包管理

用命令去下载，升级，管理安装在系统上的软件。Windows 平台用 chocolatey，macOS 可以使用 Homebrew。

## Windows

chocolatey 是用在 Windows 上的系统包管理工具。

[https://chocolatey.org/](https://chocolatey.org/)

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

**choco**

安装完成以后你应该可以使用 `choco` 命令去管理系统上的软件包。

```
choco --help
```

## macOS

Homebrew 是用在 macOS 上的系统包管理工具。

[https://brew.sh/](https://brew.sh/)

### 安装

打开系统自带的终端工具，然后执行：

```
/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```

**brew**

安装成功以后，就可以使用 `brew` 命令去管理在 macOS 平台上的系统软件包了。

```
brew --help
```

---

1. 视频：[Homebrew](https://ninghao.net/video/4570?a=51729)



