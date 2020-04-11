虽然EXCEL是中低端运营狗屠龙刀一般的大杀器，但对于一些轻量级的数据处理需求，我更喜欢在VSCode使用CSV格式进行录入和处理，之后再根据需要转化为xlsx、markdown或者html格式的表格。

VSCode作为处理轻量级数据的贴身小匕首有以下的几个优势：

- 数据修改起来更加方便，比如批量增加个链接前缀，配合正则表达式能实现远超EXCEL的效率
- 作为中间数据格式，处理时能够和Python等编程语言无缝衔接，导出的时候又能和EXCEL无缝衔接
- 作为纯文本格式，可以使用Git进行版本管理，减少了数据丢失的风险，还能有详细的过程记录

安装了以下的插件之后，VSCode中处理轻量级数据的使用体验并不逊色于EXCEL：

- [Edit CSV](https://github.com/janisdd/vscode-edit-csv)：在表格样式中显示和修改CSV数据
- [Rainbow CSV](https://github.com/mechatroner/vscode_rainbow_csv)：CSV对齐显示、SQL运算
- [Data Preview](https://github.com/RandomFractals/vscode-data-preview)：数据分析和作图工具
- [CSV to Markdown Table Converter](https://marketplace.visualstudio.com/items?itemName=Marchiore.csvtomarkdown)：将CSV表格转化为Markdown表格

### 常用问题&使用技巧

1. 问：其他应用导出的CSV文件在EXCEL中显示乱码，如何处理？
- 答：使用VSCode打开CSV文件，通过`Change File Encoding - Save with Encoding`命令保存为`UTF-8 with BOM`编码即可恢复正常。


2. 问：如何批量修改某列或者某行？
- 答：按下`⌥`键，再使用鼠标垂直选择，即可开启块选择模式，在垂直方向上同时开启设置多个光标同时操作。按下`⌘`键，再使用鼠标点击，即可开启多选择模式，在任意方向上同时开启设置多个光标同时操作。

![](http://assets.libukai.top/img/VSCode_多重选择.gif)

