## Chocolatey

chocolatey 是用在 Windows 上的系统包管理工具。

[https://chocolatey.org/](https://chocolatey.org/)

## 安装

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

## 使用

使用 Chocolatey 安装软件包之前，可以先确定一下是否可以安装，先去搜索一下要安装的东西，如果能找到结果，就可以使用 Chocolatey 安装它：

```
choco search 关键词
```

找到结果以后，可以查看软件包的详细信息：

```
choco info 包的名字
```

也可以在线查看能用 Chocolatey 安装的包：

https://chocolatey.org/packages

确定是要安装的包，执行：

```
choco install 包的名字
```

升级包，执行：

```
choco upgrade 包的名字
```

删除包，执行：

```
choco uninstall 包的名字
```

## 练习

假设我们需要一个 rsync 工具，默认在 Windows 上不带这个工具，打开命令行界面，执行一下：

```
rsync
```

会返回：

```
rsync : 无法将“rsync”项识别为 cmdlet、函数、脚本文件或可运行程序的名称。请检查名称的拼写，如果包括路径，请
确保路径正确，然后再试一次。
```

决定要用 Chocolatey 安装一下这个工具，先搜索看看有没有：

```
choco search rsync
```

在返回的结果里找到了 rsync，可以进一步确认找到的就是我需要的 rsync：

```
choco info rsync
```

确定以后，执行安装：

```
choco install rsync
```

完成以后，再试一下：

```
rsync --help
```

这次就会返回 rsync 这个工具的帮助信息，说明已经在系统上成功的安装了这个工具。

