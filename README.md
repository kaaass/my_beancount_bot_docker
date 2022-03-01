# my_beancount_bot_docker
@KAAAsS 个人使用的 Beancount Bot 镜像，基于 [kaaass/beancount_bot_costflow_docker](https://github.com/kaaass/beancount_bot_costflow_docker)。具体用例请参考：[kaaass/my-beancount-template](https://github.com/kaaass/my-beancount-template)。

## 使用

### 通过 Docker

```shell
docker run -d \
  -v ./bean:/bean \
  -v ./config:/config \
  kaaass/my_beancount_bot_docker
```

### 通过 Dockerfile

1. 下载 `docker-compose.yml`
2. 执行 `docker-compose up -d`

## 参数

环境变量：

- **BEANCOUNT_BOT_CONFIG**：beancount_bot 的配置文件路径，默认 `/config/beancount_bot.yml`

目录：

- **/init.d**：初始脚本。所有 `.sh` 文件会在容器启动时通过 `sh xx.sh` 执行

## See also

- [kaaass/beancount_bot](https://github.com/kaaass/beancount_bot)：Bot 核心
- [kaaass/beancount_bot_costflow](https://github.com/kaaass/beancount_bot_costflow)：Costflow 语法插件

