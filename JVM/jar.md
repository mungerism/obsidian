---
aliases: [jar 包]
---

[[Class文件]] [[zip 包]]。将 `.zip` 后缀改为 `.jar`，一个 jar 包就创建成功。

如果要执行一个 jar 包的[[Class文件]]，可以使用 [[-classpath|-cp]] 参数将 jar 包放到 [[类路径|ClassPath]] 中：
`java -cp ./hello.jar abc.xyz.Hello`

在 IDE 中运行的 Java  程序，IDE 自动传入的 [[-classpath|-cp]] 参数是当前工程的 `bin` 目录和引入的 jar 包。