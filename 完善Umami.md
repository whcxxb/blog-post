> 记录下 Umami 网站统计工具的安装过程，以及使用过程中遇到的问题。

## 安装
- 官方网站：https://umami.is/

- 官方文档：https://umami.is/docs/

- 开源地址：https://github.com/umami-software/umami

本次采用docker安装，官方提供了docker-compose.yml文件，默认配置构建 umami 容器并启动 Postgres 数据库。

### 下载 Umami
```bash
git clone https://github.com/mikecao/umami.git
cd umami
```
### 确保docker和 docker-compose 已经安装
安装docker可以参考这篇文章：[Docker安装](https://www.cnblogs.com/Can-daydayup/p/16472375.html)
```bash
docker -v
# Docker version 24.0.4, build 3713ee1
docker-compose -v
# Docker Compose version v2.20.0
```


 

