# MyTools

## 浏览器插件

### 浏览器插件离线下载

- chrome: https://crxdl.com/，输入插件ID进行下载
- firefox: 官方仓库可直接下载（需要非 Firefox 指纹）
    - 语言包：https://addons.mozilla.org/zh-CN/firefox/addon/chinese-simplified-zh-cn-la/

### 安装插件

chrome & edge:

> [!note]
> 不能批量拖动 crx 文件进行安装，只能逐个添加

1. 在地址栏输入 chrome://extensions/
2. 打开 开发者模式 的开关
3. 拖动 xxx.crx 文件到 Chrome 中间即可


### 解决 Chrome 系浏览器安装插件无法启用

报错：

该扩展程序未列在 Chrome 应用商店中，并可能是在您不知情的情况下添加的。

解决思路：

1. 获取浏览器官方提供的管理模板
2. 在组策略中添加模板
3. 修改组策略，添加所需插件白名单

具体步骤：

1. 获取浏览器官方提供的管理模板

- **Google chrome**

首先，通过 [这篇帮助文档](https://support.google.com/chrome/a/answer/187202) 我们可以找到 [Chrome 管理模板的下载地址](https://dl.google.com/dl/edgedl/chrome/policy/policy_templates.zip)

- **Microsoft Edge**

可以从微软下载中心 [https://www.microsoft.com/en-us/edge/business/download](https://www.microsoft.com/en-us/edge/business/download) 下载最新版本的 Microsoft Edge ADMX 模板。

在 Microsoft Edge 商业下载页面上，选择频道/版本、构建版本和平台，然后点击“GET POLICY FILES”获取策略文件。

![](https://kenyons.oss-cn-shenzhen.aliyuncs.com/img/202408201405543.png)

点击“GET POLICY FILES”——下载 Microsoft Edge ADMX 组策略模板。

2. 导入组策略模板

将下载的管理模板进行解压，确保能访问 `\windows\adm\zh-CN` 子目录

按【Win+R】键打开运行，输入【gpedit.msc】确定，进入本地组策略编辑器。

![](https://img-blog.csdnimg.cn/direct/1fb8499b2528442c8aea5778f89e36fa.png)

点击【计算机配置 →管理模板】 ，右键菜单【添加/删除模板 →添加】

![](https://img-blog.csdnimg.cn/direct/3a443bdac652481798e8aaaf9da53618.png)

选择解压文件夹中的【windows/adm/zh-CN/msedge.adm】文件，将我们刚才找到的文件添加进去

![](https://img-blog.csdnimg.cn/direct/f69e3626e87b4ca58f47578c2b6513ff.png)

添加完成后，在管理模版列表中会出现【经典管理模块 ADM】

![](https://img-blog.csdnimg.cn/direct/026bfb68e35a42f09fa90bdf739dfa58.png)

打开【Microsoft Edge→扩展 →允许安装特定扩展】

![](https://img-blog.csdnimg.cn/direct/ae990cd176ed40238cd6f220193fe304.png)

选择【已启用】，然后点击【显示】进入白名单列表

![](https://img-blog.csdnimg.cn/direct/b63ebf8b37e948f59ed775d06b5ff309.png)

打开浏览器扩展界面，将不可用的插件 ID 填入白名单中

![](https://img-blog.csdnimg.cn/direct/aa429c6075e649f09fde623911124ace.png)

将图片中的插件的 ID 复制，输入到下面的方框里。

![](https://img-blog.csdnimg.cn/direct/6e76b44d1e814b17afa267ae8ec3fa01.png)

然后确认并应用，重启浏览器即可生效。

## 参考资料

- [给 Chrome 添加非应用商店扩展程序的正确姿势](https://blog.berd.moe/archives/add-third-app-to-chrome/)
- [全网最细教你解决 Edge 浏览器“本地安装此扩展不是来自任何已知来源”解决方法，超管用！](https://blog.csdn.net/buxihuanchongzi/article/details/140160258)
- [Download Microsoft Edge ADMX Group Policy Templates](https://www.anoopcnair.com/download-microsoft-edge-admx-group-policy-templates/)
