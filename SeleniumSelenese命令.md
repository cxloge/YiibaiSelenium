# SeleniumSelenese命令

一个命令指的是什么Selenium有执行，Selenium命令有三种类型。点击以下更多地了解这些命令。

- [Actions](http://www.yiibai.com/selenium/selenium_commands_actions.html)
- [Accessors](http://www.yiibai.com/selenium/selenium_commands_accessors.html)
- [Assertions](http://www.yiibai.com/selenium/selenium_commands_assertions.html)

## 定位器

元素定位器有助于Selenium识别HTML元素和命令指引用。所有这些定位器可以在Mozilla浏览器的firepath和firebug插件的帮助下识别ID。请参考环境设置一章。

- **identifier=id **- 使用指定的“id”属性选择元素，如果没有匹配，选择的第一要素，其@name属性ID。
- **id=id **选择指定的“id”属性的元素。
- **name=name - **使用指定“name”属性选择第一个元素
- **dom=javascriptExpression** - Selenium通过评估指定的字符串，它允许我们遍历使用JavaScript的HTML文档对象模型找到一个元素。用户不能返回一个值，但可以评估计算作为块的表达式。
- **xpath=xpathExpression **- 找到使用XPath表达式的元素。
- **link=textPattern **- 选择链接元素(锚点标记内)，其中包含文字与指定模式匹配。
- **css=cssSelectorSyntax **- 使用CSS选择器选择元素