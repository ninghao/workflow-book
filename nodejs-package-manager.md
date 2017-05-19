# Node.js 包管理

把用 Node.js 做好的某个功能打成一个包（Package），在项目之间可以重复使用这些包。即使你开发的不是 Node.js 项目，也可能会用到 Node.js 的某些包。特别是做前端项目开发的时候，项目里用的很多工具都是 Node.js 的一个包。

这些 Node.js 的包之间会存在依赖关系，也就是一个包的功能，可能需要另一个包里提供的功能。Node.js 让你可以在项目里使用一个叫 package.json 的文件去描述包的依赖关系，使用工具，执行一行命令就可以安装项目需要的所有的包。这个工具会为你解决包之间的依赖关系。

有的包可以在服务端使用，有些是命令行工具，也有很多包可以用在前端，也就是直接在浏览器上去用。在你的项目里去，可以直接使用一些现成的包。你也可以创建自己的包，跟别人共享，或者只在自己团队的内部使用。

在项目里管理 Node.js 的包可以使用 npm 或 yarn。

## npm

npm（Node Package Manager），是一个包管理工具。安装了 Node.js 以后，会自带这个包管理工具。

[https://www.npmjs.com/](https://www.npmjs.com/)

### Yarn

Yarn 是可以代替 npm 的又一个 Node.js 包管理工具，它比 npm 更快更安全。

[https://yarnpkg.com](https://yarnpkg.com)

**Windows 安装：**

可以使用 chocolatey 安装 Yarn ：

```
choco install yarn
```

**macOS 安装：**

可以使用 Homebrew 安装 Yarn：

```
brew install yarn
```

## 创建项目

你得到一个别人做好的项目，发现项目的根目录下有个 package.json 文件，你首先要做的事就是去安装项目依赖的包，执行：

```
npm install
```

或使用 Yarn：

```
yarn install
```

### package.json

自己创建的项目，你要为项目添加一个 package.json，在项目下面执行：

```
npm init -y
```

或使用 Yarn：

```
yarn init -y
```

这个 package.json 里的内容一开始可能像这样：

```
{
  "name": "nodejs-project",
  "version": "1.0.0",
  "description": "",
  "main": "index.js",
  "scripts": {
    "test": "echo \"Error: no test specified\" && exit 1"
  },
  "keywords": [],
  "author": "wanghao <wanghao@ninghao.net>",
  "license": "ISC"
}
```

如果是用 Yarn 创建的，会更简单一点：

```
{
  "name": "nodejs-project",
  "version": "1.0.0",
  "main": "index.js",
  "license": "MIT"
}
```

### 添加依赖

为项目添加一个包，或者叫安装一个包，用 npm 会像这样：

```
npm install 包的名字
```

一般你需要把为项目安装的包在 package.json 文件里记录一下，所以在安装的时候你要添加一个 `--save` 或 `--save-dev` 选项。

```
npm install 包的名字 --save
```

如果安装的包要作为项目的开发时的依赖，可以使用 `--save-dev` 选项：

```
npm install 包的名字 --save-dev
```

举个例子理解一下什么时候用 --save ，什么时候用 --save-dev。比如你的项目需要一个登录功能，假设这个功能在一个包里，那么把这个包添加到你的项目的时候，要作为项目的普通的依赖，也就是使用 `--save` 选项。

再比如，你的项目在开发的时候需要在本地创建一个服务器，把这个功能包添加到项目的时候，可以作为项目的开发依赖，也就是安装的时候使用` --save-dev` 选项。







