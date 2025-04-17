从整个文件中搜寻字符串<br>
正则表达式：```"((?:\\"|\\\\|\\[^"]|[^"\\])*)"```<br>
输出的 JSON 的键格式：```文件名:行```<br>
文件名：文件名，包含相对路径<br>
行：第几行

根据规则筛选分为五个 JSON，从上至下筛选<br>
```asterisk.json```：含有```* ```的，基本可以确定是正常对话文本，可以无脑翻译<br>
```slash_underline.json```：含有斜杠或下划线的，基本可以确定不需要翻译<br>
```space.json```：含有空格的，基本都是菜单选项或者对话的后半段，可以看着来翻译<br>
```upper.json```：含有大写的<br>
```others.json```：剩下的

```UpdateLineAfterUpdated.py```可以在原有IL更新后更新json中key的行数 (By DeepSeek)