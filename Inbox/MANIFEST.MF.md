[[jar]]里 [[META-INF 目录]]下，纯文本。可以指定 [[Main-Class]] 和其它信息，JVM会自动读取。

如果指定了 [[Main-Class]]就可以不必在命令行指定启动的类名:
`java -jar hello.jar`

[[jar]]如果还包含其它 jar，需要在 [[MANIFEST.MF]] 文件里配置[[类路径|ClassPath]]。

```
Manifest-Version: 1.0
Spring-Boot-Classpath-Index: BOOT-INF/classpath.idx
Implementation-Title: reading
Implementation-Version: 0.0.1-SNAPSHOT
Start-Class: com.xiaonei.reading.ReadingApplication
Spring-Boot-Classes: BOOT-INF/classes/
Spring-Boot-Lib: BOOT-INF/lib/
Build-Jdk-Spec: 1.8
Spring-Boot-Version: 2.3.1.RELEASE
Created-By: Maven Jar Plugin 3.2.0
Implementation-Vendor: Pivotal Software, Inc.
Main-Class: org.springframework.boot.loader.JarLauncher
```