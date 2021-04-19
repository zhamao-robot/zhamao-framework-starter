# zhamao-framework-starter
炸毛框架的快速开始模板，是炸毛框架开箱即用的项目。

[![Latest Stable Version](http://img.shields.io/packagist/v/zhamao/framework-starter.svg)](https://packagist.org/packages/zhamao/framework-starter)

注意：本快速模板目前拉取的都是 v2 的版本，如果想使用 v1 的版本，请使用版本号后缀 `^1.4`。

## 用法
```bash
composer create-project zhamao/framework-starter <你的项目名称>
cd <你的项目名称>
vendor/bin/start server
```

## 搭建环境
见炸毛框架文档：<https://docs-v2.zhamao.xin/>

## 手动构建环境（新）
炸毛框架提供了一个编译 PHP 和相关依赖的脚本，可直接运行（需要有 gcc，g++，autoconf，make，git，curl 这几个构建基本的包已安装）
```bash
./build-runtime.sh
```
他会下载 Swoole、PHP、openssl、composer 等源码并从源码编译到 `runtime` 目录下。

在构建成功后，所有的 PHP 二进制文件和相关依赖都被编译到 `./runtime/` 目录中，如不需要环境或环境出错，可直接删除此文件夹来删除环境，不污染主机环境。

使用这个用户态编译完成的 PHP：
```bash
runtime/bin/php -v                      # 查看 PHP 版本
runtime/bin/php vendor/bin/start server # 运行框架，也可运行其他 PHP 脚本
```

## 指令
```bash
vendor/bin/start server                 # 以默认模式启动
vendor/bin/start server --log-debug     # 以 debug 的日志启动
vendor/bin/start server --debug-mode    # 以 debug 调试模式启动
```

## Composer 速度太慢
可尝试使用国内镜像源：
```bash
# 仅把当前项目的源地址改为国内
composer config repo.packagist composer https://mirrors.aliyun.com/composer/

# 取消国内源地址
composer config --unset repos.packagist
```
