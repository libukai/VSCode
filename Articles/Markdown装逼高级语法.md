最原教旨版本的 Markdown 语法非常简单，只能实现最基础的标记格式。后来随着 Github 这个搞基网站日渐火热，使用人群也日益扩大，为了满足更多更复杂的需求，Github Flavored Markdown （下文简称 GFM） 这个加强版本应运而生。

GFM 目前已成为了事实上的互联网通用标准，完全可以实现一次书写，跨平台无忧使用。另外，因为我们在 VSCode 中安装了 Markdown Preview Enhanced 这个扩展（下文简称 MPE），所以还可以实现一些更高级的效果，这部分内容将在文中特别说明。

最后再强调一下， Markdown 是一种非常简单的语法。不要看本文挂上了"高级"的名头，但其实这些语法也并不复杂，非常值得再花 30 分钟再学习一下。

### 一、目录

对于我这样喜欢写又臭又长文章的人，在开头插入文章目录便于快速跳转，能大大减轻因浪费了读者时间而产生的愧疚感。

插入目录的语法和效果如下（*属于MPE 的增强功能*）：

```Markdown
[TOC]
```

![](http://assets.libukai.top/img/MarkdownToc.jpg)

### 二、表格

EXCEL 是每个人运营人爱与恨永恒的根源之一。在 Markdown 语法中，这份爱与恨比较简单，只能满足简单的纯展示型需求。

表格的语法注意事项和展示效果如下：

+ 表头属性下方，必须有`----`的分隔行
+ 列的对齐方式可以通过在分割线前后添加`:`来实现。
+ `^`和`>`分别可用于实现列和行的合并（*属于MPE 的增强功能*）。
+ MPE 还可以直接在 Markdown 文档中嵌入 CSV 文件，有兴趣的朋友可以在 MPE 的[中文使用说明](https://shd101wyy.github.io/markdown-preview-enhanced/#/zh-cn/)中详细了解。

```Markdown
|表头属性 1 | 表头属性 2 | 表头属性 3 |
|:--------|:---------:|-------:|
|左对齐 | 居中 | 右对齐|
|> |向右合并 |向上合并 |
|左对齐 | 居中 | ^|
```

![](http://assets.libukai.top/img/Markdown表格.jpg)

### 三、待办事项

运营狗永远有干不完的活，永远有勾不完的待办事项。为了满足运营狗的需求，Markdown 语法良好支持待办事项，让你找不到任何偷懒划水的理由。

待办事项的语法和效果如下：

```Markdown
- [ ] 永远干不完的活
    - [ ] 永远可以提升的效率
    - [X] 永远不够用的薪水
```

- [ ] 永远干不完的活
    - [ ] 永远可以提升的效率
    - [x] 永远不够用的薪水

### 四、上标、下标、脚注

除了基础教程里面的加粗、斜体和删除外，Markdown 里面还可以支持上标、下标、脚注等专业格式，专业人士专用，逼格不输Word。（*属于MPE 的增强功能*）

相关的语法和效果如下：

```Markdown
30^th^
H~2~O

Content [^1]

[^1]: 嗨！这是一个孤独的脚注

```

![](http://assets.libukai.top/img/Markdown标注.jpg)


### 五、代码块

不懂技术的产品不是一个好运营，作为一个合格的运营狗，就算不懂也绝对不能对代码有畏惧之心。

悄悄说个小诀窍，简单使用连续3个 ` 前后包夹，就可以实现代码高亮配色，绝大多数产品狗都不会哦。


```Python
def getkey(user_file):
    '''清理非标准化的微博地址，提取用户的 UID 或者个性化域名'''
    url_key_list = []
    listnum = 0
    with open(user_file, 'r') as url_list:
        for url in url_list:
            listnum += 1
            try:
                keyword = re.search(r'\/(\d{10})|com\/(\w{4,32})|\/p\/\d{6}(\d{10})|^(\d{5,10})$', url).groups()
                url_key_list.append([key for key in keyword if key is not None][0])
            except AttributeError:
                print('第 %d 行格式有误：' % listnum, url)
        if listnum != len(url_key_list):
            unuseful = listnum - len(url_key_list)
            print('\n注意：总计发现%d个错误格式，请修正后再执行' % unuseful)
            sys.exit()
    return url_key_list
```

除了大块成段的引用之外，还可以在行内进行引用。

```Markdown
在行内使用`引用`语法，可以起到比加粗更引人注意的强调效果。
```

在行内使用`引用`语法，可以起到比加粗更引人注意的强调效果。
