# zhamao-framework-starter
炸毛框架的快速开始模板，是炸毛框架开箱即用的项目。

注意：本快速模板分为 1.x 和 2.x 两个版本，目前默认拉取的都是 1.x 版本的，等炸毛框架 v2 正式发布后切换为 v2 版本的模板。

## 用法
```bash
composer create-project zhamao/framework-starter
cd framework-starter
vendor/bin/start server
```

## 指令
```bash
vendor/bin/start server                 # 以默认模式启动
vendor/bin/start server --log-debug     # 以 debug 的日志启动
vendor/bin/start server --debug-mode    # 以 debug 调试模式启动
composer run systemd                    # 生成 systemd 文件
```

## Composer 速度太慢
可尝试使用国内镜像源：
```bash
# 仅把当前项目的源地址改为国内
composer config repo.packagist composer https://mirrors.aliyun.com/composer/

# 取消国内源地址
composer config --unset repos.packagist
```
