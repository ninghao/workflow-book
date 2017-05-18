# Node.js

安装了 Node.js 的机器就可以运行 JavaScript 语言了。 也就是有了 Node.js 以后，你可以使用 JavaScript 语言去开发服务端的应用程序。

即使你不打算学习 Node.js，平时的开发学习与工作，你的电脑上也需要安装一个 Node.js。因为很多开发时用的工具都需要用到 Node.js 。

[https://nodejs.org](https://nodejs.org)

## 安装

在 Node.js 的官网可以下载适合在不同操作系统上使用的 Node.js 。 它的版本也很多（6.x，7.x ... ），有时我们可能需要为不同的项目使用不同版本的 Node.js，所以推荐使用 nvm 这个小工具来管理安装在系统上的 Node.js ，它可以在不同的 Node.js 版本中来回切换。

### macOS

**安装 nvm：**

```
curl -o- https://raw.githubusercontent.com/creationix/nvm/v0.33.2/install.sh | bash
```

**验证安装：**

```
command -v nvm
```

如果返回 `nvm` ，说明已经安装成功了。

**安装 node：**

用 nvm 安装 node：

```
nvm install node
```

系统上先有个能用的 Node.js 就可以了，以后我们可能会安装其它版本的 Node.js，或者配置项目使用不同版本的 Node.js。

**验证 node：**

```
node --version
```

上面的命令会返回系统上正在使用的 Node.js 的版本号。

[https://github.com/creationix/nvm](#)

### Windows

也有一个适用在 Windows 系统上的 nvm，安装前你需要先删除掉之前安装在系统上的 Node.js，卸载以后，如果安装目录还存在，你需要手工把这个目录删除掉。还有用 npm 的安装目录也需要删除掉，一般是在 C:\Users&lt;user&gt;\AppData\Roaming\npm 。

**安装 nvm：**

[https://github.com/coreybutler/nvm-windows/releases](https://github.com/coreybutler/nvm-windows/releases)

**安装 node：**

```
nvm install node
```

[https://github.com/coreybutler/nvm-windows](https://github.com/coreybutler/nvm-windows)

## 结语

我推荐使用 nvm 安装管理系统上的 Node.js，是因为很可能会用到不同版本的 Node.js。不过如果你嫌麻烦，直接在 Node.js 的官网上下载并安装某个版本的 Node.js 也行。不管怎样，你的系统上至少要有一个可用的 Node.js。

