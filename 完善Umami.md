> 记录下 Umami 网站统计工具的安装过程，以及使用过程中遇到的问题。

## 安装

- 官方网站：https://umami.is/

- 官方文档：https://umami.is/docs/

- 开源地址：https://github.com/umami-software/umami

本次采用 docker 安装，官方提供了 docker-compose.yml 文件，默认配置构建 umami 容器并启动 Postgres 数据库。

### 下载 Umami

```bash
git clone https://github.com/mikecao/umami.git
cd umami
```

### 安装 docker 和 docker-compose

安装 docker 可以参考这篇文章：[Docker 安装](https://www.cnblogs.com/Can-daydayup/p/16472375.html)

```bash
docker -v
# Docker version 24.0.4, build 3713ee1
docker-compose -v
# Docker Compose version v2.20.0
```

### 进入 umami 目录

```bash
# 启动容器
docker-compose up -d
```

此时访问 http://localhost:3000/ 就可以看到 umami 的安装界面了,可以用`curl`命令测试下

```bash
curl http://localhost:3000
```

![](https://wxxb.cc/static/img/1697525991809.png)

## Nginx 配置

```bash




```
