如果是采用 scoop 安装的 sublime text

则拷贝到目录

```
C:\ProgramData\scoop\apps\sublime-text\current\Packages
```

或者

```
D:\Scoop\apps\sublime-text\current\Packages
```

Sublime手动安装汉化包

‍
下载

‍

下载地址: [github.com/rexdf/Chinese...](https://github.com/rexdf/ChineseLocalization/raw/st3-dev/ZH_CN.zip)

‍
开始手动安装

‍

1）选择菜单：Preferences --> Browse Packages
2）打开Sublime插件安装的包文件夹（如：`C:\Users\Administrator\AppData\Roaming\Sublime Text 3\Packages\User`）
3）下载Package Control并Copy到以上文件夹内
4）重启Sublime


```
cp .\sublime_text_4\ChineseLocalizations.sublime-package D:\00PackageManager\Scoop\apps\sublime-text\current\Packages\
```

---


# [Chinese Localization](https://raw.githubusercontent.com/rexdf/ChineseLocalization/st3-dev/README.md)

Simplified Chinese and Traditional Chinese Translation for Sublime Text 3. Support MainMenu TabMenu ContextMenu,etc.

I try to support more languages. Now Japanese is partially supported.

I add support to Deutsche(German) Русский(Russian) Español(Spanish) Հայերեն(Armenian) Svenska(Swedish) Français(French) in version 1.11.0.

### Manual Install

Clone this repository into `Sublime Text 3/Packages` using OS-appropriate location:

OSX:

    git clone -b st3 https://github.com/rexdf/ChineseLocalization.git ~/Library/Application\ Support/Sublime\ Text\ 3/Packages/ChineseLocalization

Windows:

    git clone -b st3 https://github.com/rexdf/ChineseLocalization.git "%APPDATA%\Sublime Text 3\Packages\ChineseLocalization"

Linux:

    git clone -b st3 https://github.com/rexdf/ChineseLocalization.git ~/.config/sublime-text-3/Packages/ChineseLocalization

---

~~Or just download this repo as zip, rename it to `ChineseLocalization.sublime-package` and put it to `Data\Installed Packages`. (Sublime Text 3 only)~~ You need to unpack and pack it again to make sure all files in the zip root rather than `ChineseLocalization-st3` folder. Or just unzip them to `ChineseLocalization` folder in `Data/Packages` folder(You can open that folder by click main menu `Preferences\Browse Packages...`).


### Package Control Install

**Recommand for 3124+, click Menu `Tools\Install Package Control` , then Menu `Preferences\Package Control ` , install `Chinese​Localizations`.**


![screenshot](https://raw.githubusercontent.com/rexdf/ChineseLocalization/readme/screenshot/SublimeChineseTranslation3.gif)


![screenshot](https://raw.githubusercontent.com/rexdf/ChineseLocalization/readme/screenshot/sublime_translation.png)

![screenshot](https://raw.githubusercontent.com/rexdf/ChineseLocalization/readme/screenshot/sublime_trans_linux.png)

### Usage

- [x] Help/Language/Simplified Chinese 简体中文
- [x] Help/Language/Traditional Chinese 正體中文
- [ ] Help/Language/Japanese 日本語
- [ ] Help/Language/Russian Русский
- [ ] Help/Language/Spanish Español
- [ ] Help/Language/French Français
- [ ] Help/Language/German Deutsche
- [ ] Help/Language/Swedish Svenska
- [ ] Help/Language/Armenian Հայերեն
- [x] Help/Language/English


### problems

Now this problem has been solved at st3-1.6.0.

~~Because almost every package has a `Main.sublime-menu`, So some package name maybe override the Default one.~~

~~AFAIK, minimal manual delete including~~:

+ **SublimeREPL** delete caption

+ **Minify** Overwrite, but delete

+ **Tag** delete mnemonic caption

+ **Indent XML** delete caption Selection

+ **HTMLBeautify** delete caption Edit

+ **GraphvizPreview** delete caption Edit

### Author & Contributors
- [Rexdf](https://github.com/rexdf)
- [FichteFoll](https://github.com/FichteFoll)
- [Patrick T.](https://github.com/Patricivs)
- [zhtw2013](https://github.com/zhtw2013)
- [LocalizedMenu](https://github.com/zam1024t/LocalizedMenu)
