# Dbeaver

## dbeaver-EE

### 步骤

1. 安装 dbeaver ee
2. 进入 dbeaver ee 安装目录，删除 jre 目录下的文件
3. 从 temurin23-jre 中，全部解压到 jre 目录下
4. 复制 dbeaver-agent.jar 到安装目录
5. 修改 dbeaver.ini
6. 开始激活
7. 启动 dbeaver 并导入 license

```bash
scoop downlaod java/temurin23-jre
```

```bash
java -cp "plugins\*;.\dbeaver-agent.jar" com.dbeaver.agent.License
```

### 踩坑总结

- dbeaver-EE v25.2 替换的 jre 版本必须为 23，高于或低于这个版本都会异常
- dbeaver-agent.jar 的版本必须和 dbeaver-EE 的安装版本一致

## Dbeaver 调整语言

DBeaver 的界面语言可以根据您的偏好进行自定义。实现这一功能有两种方法：

### 在首选项中更改界面语言

1. 导航至 **Window -> Preferences -> User Interface**.  

![](https://dbeaver.com/docs/dbeaver/images/ug/UI-Language-Preferences.png)

1. 从下拉菜单中选择您需要的语言。
2. 点击“**Apply and Close**”按钮以保存您的设置。

**Note**: 如果 DBeaver 安装在无写权限的目录中，您可能无法通过界面直接更改语言。如果出现这种情况，请按照下文所述修改配置文件。

## 附录

### 参考资料

- [\[Bug\]: 求助，win下导入license报错 javax.crypto.BadPaddingException: Padding error in verification](https://github.com/wgzhao/dbeaver-agent/issues/21)
- [\[Bug\]: windows DBeaverUltimate 25.0 版本加上 javaagent 程序就打不开，去掉就能打开](https://github.com/wgzhao/dbeaver-agent/issues/18)
- [wgzhao-dbeaver-agent](https://github.com/wgzhao/dbeaver-agent)
