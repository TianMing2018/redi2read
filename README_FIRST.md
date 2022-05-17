# Redi2Read

本项目是我基于 官网课程 <https://developer.redis.com/develop/java/redis-and-spring-course/> 和仓库创建

截止`2022-05-17`,官网文档有几个问题,我已经发起PR,但有几点备注如下:
- `jrejson` 已经有正式release版本,文档里的没必要再用了
- `pom.xml`中 repository 可以去掉,可能会妨碍拉取spring等其它包

### 自建项目步骤说明

```shell
# 创建SpringBoot项目 (基础的SpringBoot项目即可,可用附注 ①)
git init
git commit --allow-empty -m "git: initial empty commit"
# add submodule
git submodule add https://github.com/redis-developer/redismod-docker-compose.git docker
git submodule add https://github.com/redis-developer/redi2read-data.git src/main/resources/data

> ①: <https://start.spring.io/#!type=maven-project&language=java&platformVersion=2.6.7&packaging=jar&jvmVersion=11&groupId=com.redislabs.edu&artifactId=redi2read&name=redi2read&description=Demo%20project%20for%20Spring%20Boot&packageName=com.redislabs.edu.redi2read&dependencies=devtools,lombok,web,security,data-redis>