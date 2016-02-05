title: 使用Sublime Text书写Markdown
date: 2016-02-05 16:11:31
categories:
- Web
tags:
- Markdown
- Sublime Text
---

## 什么是 Markdown

Markdown 是一种方便记忆、书写的纯文本标记语言，用户可以使用这些标记符号以最小的输入代价生成极富表现力的文档：它使用简单的符号标记不同的标题，分割不同的段落，**粗体** 或者 *斜体* 某些文字，它还可以

### 制作一份待办事宜 

- ~~使用Github进行代码管理~~
- ~~建立独立Blog~~
- 熟练Markdown的语法
- 使用$\LaTeX$写论文

### 书写一个质能守恒公式

$$E=mc^2$$

### 高亮一段代码

```python
@requires_authorization
class SomeClass:
    pass

if __name__ == '__main__':
    # A comment
    print 'hello world'
```
<!-- more -->
### 绘制表格

| Item        | Price   |  Numbers  |
| --------   | -----:  | :----:  |
| PC     | \$1600 |   1     |
| Pen        |   \$3   |   10   |
| Paper        |    \$1    |  200  |


不同于其它 *所见即所得* 的编辑器：你只需使用键盘专注于书写文本内容，就可以生成印刷级的排版格式，省却在键盘和工具栏之间来回切换，调整内容和格式的麻烦。**Markdown 在流畅的书写和印刷级的阅读体验之间找到了平衡。** 目前它已经成为世界上最大的技术分享网站 GitHub 和 技术问答网站 StackOverFlow 的御用书写格式。

---

## 什么是Sublime Text

[Sublime Text](http://www.sublimetext.com/)是一个代码编辑器，也是一个先进的文本编辑器。对比其他编辑器，体积小，运行速度快，界面漂亮，支持编译，重要的是具有几乎无限的拓展功能。

---

## 如何使用Sublime Text书写Markdown

*本文针对Sublime Text 3，Windows 10 x64系统*
 
Sublime Text拥有大量的插件进行功能拓展，在此介绍一套比较舒服的解决方案（MarkDown Editing+OmniMarkupPreviwer）。

### 安装插件的方法

- Ctrl+`调出console
- 输入以下代码
```python
import urllib.request,os,hashlib; h = '2915d1851351e5ee549c20394736b442' + '8bc59f460fa1548d1514676163dafc88'; pf = 'Package Control.sublime-package'; ipp = sublime.installed_packages_path(); urllib.request.install_opener( urllib.request.build_opener( urllib.request.ProxyHandler()) ); by = urllib.request.urlopen( 'http://packagecontrol.io/' + pf.replace(' ', '%20')).read(); dh = hashlib.sha256(by).hexdigest(); print('Error validating download (got %s instead of %s), please try manual install' % (dh, h)) if dh != h else open(os.path.join( ipp, pf), 'wb' ).write(by)
```
- Ctrl+Shift+P调出命令面板，选择Install Package。

### MarkDown Editing
MarkDown Editing支持Markdown语法高亮；支持Github Favored。 Markdown语法；自带3个主题。
安装后重启Sublime Text即可。

### OmniMarkupPreviwer
实时在浏览器中预览，如果大屏/双屏/多设备的话，具有很不错的体验。快捷键如下：
Ctrl+Alt+O: Preview Markup in Browser
Ctrl+Alt+X: Export Markup as HTML
Ctrl+Alt+C: Copy Markup as HTML
如果想要更好的体验，可以修改*Sublime Text 3/Packages/OmniMarkupPreviewer.sublime-settings* 文件。

```java
"server_host": "127.0.0.1",
"mathjax_enabled": true
```
修改``server_host``为局域网地址便可实现多设备实时预览(默认为localhost)。

开启`mathjax_enabled`可以支持使用$\LaTeX$语法编辑数学公式。


More info: [Sublime插件：Markdown篇](http://www.jianshu.com/p/aa30cc25c91b)

---