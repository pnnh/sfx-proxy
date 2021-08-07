学习示例项目

尝试实现一个父子进程的示例

构建开发环境docker镜像

```shell
cd docker
docker build -t sfx-dev .
```

启动开发环境
```shell
docker run -p 2200:22 -d sfx-dev
```

请参考以下链接配置CLion远程开发环境

https://www.jetbrains.com/help/clion/remote-projects-support.html#deployment-entry

