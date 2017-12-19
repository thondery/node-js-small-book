# 安装配置

### 1. 安装 nvm

> nvm 是 Node.js 的版本管理器，可以让你方便地管理 Node.js 版本。

```bash
$ cd ~ && curl -o- https://raw.githubusercontent.com/creationix/nvm/master/install.sh | bash
Or
$ cd ~ && wget -qO- https://raw.githubusercontent.com/creationix/nvm/master/install.sh | bash
```

windows 下安装 [nvm-windows](https://github.com/coreybutler/nvm-windows/releases)

### 2. 设置 Node.js 下载源

由于官方的源服务器设在国外，我们需要将源换成淘宝的镜像

```bash
$ export NVM_NODEJS_ORG_MIRROR=https://npm.taobao.org/mirrors/node/
```

nvm-windows

```bash
$ nvm node_mirror https://npm.taobao.org/mirrors/node/
$ nvm npm_mirror https://npm.taobao.org/mirrors/npm/
```

### 3. 安装 Node.js

```bash
$ nvm ls #查看本地安装版本
$ nvm ls-remote #查看远程Node版本
$ nvm install 8.9.3 #安装指定版本
$ nvm alias default 8.9.3 #将指定版本设为系统默认版本
```

nvm-windows

```bash
$ nvm ls #查看本地安装版本
$ nvm ls available #查看远程Node版本
$ nvm install 8.9.3 #安装指定版本
$ nvm use 8.9.3 #将指定版本设为系统默认版本
```

### 4. 设置 npm 各种源

```bash
$ npm set registry https://registry.npm.taobao.org  # npm 镜像源
$ npm set disturl https://npm.taobao.org/dist  # node-gyp 编译依赖的 node 源码镜像
# 常用淘宝镜像源
$ npm set sass_binary_site https://npm.taobao.org/mirrors/node-sass  # node-sass 二进制包镜像
$ npm set phantomjs_cdnurl https://npm.taobao.org/mirrors/phantomjs  # phantomjs 二进制包镜像
$ npm set electron_mirror https://npm.taobao.org/mirrors/electron  # electron 二进制包镜像

$ npm cache clean # 清空缓存
```

更多设置请查看 https://npm.taobao.org/mirrors/

### 5. 安装 nrm

nrm 可以帮助我们方便地切换并管理 npm 镜像源

```bash
$ npm i -g nrm

$ nrm ls  # 查看 npm 镜像源
$ nrm use taobao  # 设置 npm 镜像源为淘宝
```

### 6. 安装 yarn

```bash
$ npm i -g yarn

$yarn config set registry https://registry.npm.taobao.org  # 设置为淘宝的镜像源
```

### 7. 安装 babel

```bash
$ npm i -g babel-cli
```

<br />