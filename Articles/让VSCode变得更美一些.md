像我这样的强迫症患者，总是压抑不住内心地想要掌控一切细节的欲望。面对VSCode这把天天都要把玩的瑞士军刀，也希望除了功能之外，外观上也能按照自己的偏好进行全面的个性化定制。

### 一、字体美化

相对于更偏向于表面的主题美化，字体的选择更能触及灵魂。作为一个日常工作码字，偶尔写段脚本的跨界运营狗，我目前的字体配置效果如上页截图，具体为：

+ 英文：[FiraCode-Retina](https://zhuanlan.zhihu.com/p/28134371)
+ 中文：[方正纤黑](https://www.foundertype.com/index.php/FontInfo/index/id/194)

这两者配合起来使用的优势在于中英文的字体大小接近一致，字与字之间的间隔看起来非常舒服，而且英文字体支持连字符，写代码的时候一些特殊的字符也可以很😎的显示出来。

![](http://assets.libukai.top/img/fira_code_logo.jpg)

### 二、主题美化

搞定了字体，我们接着对大家喜闻乐见的主题（Theme）进行美化。主题主要影响两个方面，一方面是外观颜色，另一方面是语法高亮。俗话说，萝莉人妻各有所爱，建议大家也别看什么主题推荐了，直接到[官网主题页面](https://marketplace.visualstudio.com/search?target=VSCode&category=Themes&sortBy=Installs)去挨个尝试，看看哪个最合自己的口味直接选用就好了。

![](http://assets.libukai.top/img/VSCode_Themes.jpg)

当千挑万选找到了一个心仪的主题，却对某些小细节依旧不甚满意时，还可以通过自定义的配置文件进行进一步的修改。具体的配置项定义见此：[VSCode自定义配色方案
](https://www.cnblogs.com/garvenc/p/vscode_customize_color_theme.html)。

如果你像我一样，选中了一个主题就喜欢从一而终，那么直接在自定义的Setting文件中修改即可，具体的属性值示例如下，可以根据自己的需求添加和调整。

![](http://assets.libukai.top/img/Theme_Color.png)

### 三、图标美化

然后，必须美化的还包括侧边栏和文件标签中的文件图标。VSCode原生的文件图标的辨识度的确不太好，建议根据自己的喜好，选择一个更顺眼的方案。目前比较好的方案包括以下几种：

- [vscode-icons](https://marketplace.visualstudio.com/items?itemName=vscode-icons-team.vscode-icons)
- [Material Icon Theme](https://marketplace.visualstudio.com/items?itemName=PKief.material-icon-theme)
- [VSCode Great Icons](https://marketplace.visualstudio.com/items?itemName=emmanuelbeziat.vscode-great-icons)

![](http://assets.libukai.top/img/vscode_icons.jpg)

### 四、样式美化

最后，对于一个强迫症患者的倔强，还有最大的挑战是自定义侧边栏、状态栏、标签栏的样式。由于目前微软大爷并没有开放相应的API，所以能找到的方案都十分Geeky，在此列出仅供参考。

- [Customize UI](https://github.com/iocave/customize-ui)：调整边栏菜单图标的位置以及应用控件字体
- [VSCode hide top-right icons](https://stackoverflow.com/questions/47266613/vscode-hide-top-right-icons)：隐藏标签栏右上角的图标
- [如何配置透明发光的骚气 VSCode](https://juejin.im/entry/5cdbe7786fb9a032092ead73)：对整体的页面效果进行深度配置（效果见下方网络图片）

![](http://assets.libukai.top/img/VSCode_Transparent.png)
