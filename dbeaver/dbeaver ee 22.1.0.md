# dbeaver ee 22.1.0

## 资源下载

- dbeaver ee 22.1.0

https://download.dbeaver.com/enterprise/22.1.0/dbeaver-ee-22.1.0-win32.win32.x86_64.zip

https://dbeaver.com/files/

- 从 AdoptOpenJDK 下载 jre-11

https://adoptium.net/zh-CN/temurin/releases/?version=11&os=windows&arch=x64&package=jre

- dbeaver-agent，提取码：`hvx1`

https://pan.baidu.com/s/1Ci_g6SHRaYL923FnH6zX1g

## 具体步骤

1. 下载 dbeaver ee 22.1.0 之后解压；
2. 解压 jre-11，然后将全部内容拷贝至 dbeaver 目录下并全部替换；
3. 下载 dbeaver-agent 并解压之后，拷贝 dbeaver-agent.jar 至 dbeaver 目录下；
4. 修改 `dbeaver.ini` 文件，在文件最后添加如下两行，也可以使用完整的 `dbeaver.ini`直接进行替换

```ini
-javaagent:dbeaver-agent.jar
-Dlm.debug.mode=true
```

完整的 `dbeaver.ini`

```ini
-startup
plugins/org.eclipse.equinox.launcher_1.6.400.v20210924-0641.jar
--launcher.library
plugins/org.eclipse.equinox.launcher.win32.win32.x86_64_1.2.400.v20211117-0650
-vmargs
-XX:+IgnoreUnrecognizedVMOptions
--add-modules=ALL-SYSTEM
-Dosgi.requiredJavaVersion=11
-Xms128m
-Xmx2048m
-Djavax.net.ssl.trustStoreType=WINDOWS-ROOT
-Ddbeaver.distribution.type=zip
-javaagent:dbeaver-agent.jar
-Dlm.debug.mode=true

```

**ps:**

1. 下载 jre 是据说 DBeaver自带的`jre`被精简，未验证；
2. orace 未提供 jre-11，而直接使用 jdk-11 过于臃肿

`DBeaverUE`专用激活码

```
aYhAFjjtp3uQZmeLzF3S4H6eTbOgmru0jxYErPCvgmkhkn0D8N2yY6ULK8oT3fnpoEu7GPny7csN
sXL1g+D+8xR++/L8ePsVLUj4du5AMZORr2xGaGKG2rXa3NEoIiEAHSp4a6cQgMMbIspeOy7dYWX6
99Fhtpnu1YBoTmoJPaHBuwHDiOQQk5nXCPflrhA7lldA8TZ3dSUsj4Sr8CqBQeS+2E32xwSniymK
7fKcVX75qnuxhn7vUY7YL2UY7EKeN/AZ+1NIB6umKUODyOAFIc8q6zZT8b9aXqXVzwLJZxHbEgcO
8lsQfyvqUgqD6clzvFry9+JwuQsXN0wW26KDQA==
```

## 踩坑笔记

从 Oracle 下载 jdk -11 之后，可以使用如下命令进行 JRE 生成

> 但是生成的 jre 无法启动 dbeaver

```powershell
bin/jlink.exe --module-path jmods --add-modules java.desktop --output jre
```

## 参考资料

- https://www.cnblogs.com/youngyajun/p/16469795.html
- https://zhile.io/2019/05/08/dbeaver-license-crack.html