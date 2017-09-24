# SeleniumIDE模式匹配

## Selenium - IDE模式匹配

在Selenium IDE中，如定位器，模式是selenium中经常使用的一种类型的参数。它允许用户描述特殊字符的模式。很多时候，我们想核实文字是动态的，在这种情况下，模式匹配是非常有用的。

模式匹配是用于所有验证点命令 - VerifyTextPresent，verifyTitle，verifyAlert，assertConfirmation，verifyText和verifyPrompt

有三种方法来定义一个模式 - 通配符，正则表达式和精确。

### 通配符

通配已经在Linux或Windows使用的文件匹配模式，而寻找一个特定的文件类型，如* doc或*.JPG，大多数技术人员。但通配硒只支持三个特殊字符：*，？和[]。

- * - 匹配任何数目的字符。
- ? - 匹配单个字符。
- [ ] - 所谓字符类，可以匹配括号内发现的任何单个字符。 [0-9]匹配任何数字

要指定selenium 命令glob，前缀与关键字的模式'glob ：“。例如，如果想搜索的文本“tax year 2013”或“tax year 2014”，那么可以使用“tax year *”来代替，如下图所示。

然而关键字的用法“glob:”是可选的，而指定文本模式，因为Selenium的匹配模式是默认。

| 命令                | 目标               | 值    |
| ----------------- | ---------------- | ---- |
| clickAndWait      | link=search      |      |
| verifyTextPresent | glob: tax year * |      |

### 精确模式

模式带有前缀“exact:'能匹配给定的文本。用户希望字符串值精确匹配，即没有globe 的操作符，我们可以使用“exact”的模式如下图所示。在这个例子中，操作符'*'将作为普通字符，而不是一个模式匹配通配符。

| 命令           | 目标           | 值    |
| ------------ | ------------ | ---- |
| clickAndWait | link=search  |      |
| verifyValue  | exact: *.doc |      |

### 正则表达式模式

正则表达式是当中匹配技术中可用的模式是最有用的。Selenium 支持完整的Java语言支持reugular表达模式。因此，用户通过不再受限于*，？和[]匹配模式。

要使用正则表达式模式，我们需要与任何前缀“regexp:”或“regexpi”。前缀“regexpi”是不区分大小写的。 glob: 和exact: 模式是正则表达式模式的子集。一切完成使用 glob: 和exact:可以完成与正则表达式。

### 示例

例如，下面将测试，如果与ID“name”输入的字段中包含字符串“tax year”，'Tax Year' 或 'tax Year'。

| 命令           | 目标          | 值                       |
| ------------ | ----------- | ----------------------- |
| clickAndWait | link=search |                         |
| verifyValue  | id=name     | regexp:[Tt]ax ([Yy]ear) |