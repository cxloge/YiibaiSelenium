# log4j日志

# YiibaiSelenium
# SeleniumIDE

## Selenium - IDE

Selenium的IDE(集成开发环境)是一个易于使用的Firefox插件,用于开发Selenium测试案例。它提供了一个图形用户界面，用于记录使用Firefox浏览器，用来学习和使用Selenium用户操作，但它只能用于只用Firefox浏览器不支持其它浏览器。

然而，所记录的脚本可以被转换成由Selenium 支持多种编程语言和脚本可以在各种其它的浏览器，以及被执行。

点击表格中了解详细列出了以下每一个功能。

| Title                                    | 描述                              |
| ---------------------------------------- | ------------------------------- |
| [下载Selenium IDE](http://www.yiibai.com/selenium/selenium_download_ide.html) | 本节介绍如何下载和配置Selenium IDE         |
| [Selenium IDE 特性](http://www.yiibai.com/selenium/selenium_ide_tool_features.html) | 本节介绍在Selenium IDE使用的功能          |
| [创建Selenium IDE 测试](http://www.yiibai.com/selenium/selenium_ide_test_creation.html) | 本节介绍了如何使用记录功能创建IDE测试            |
| [Selenium IDE 脚本测试](http://www.yiibai.com/selenium/selenium_ide_debugging.html) | 本节介绍Selenium IDE脚本的调试           |
| [插入验证点](http://www.yiibai.com/selenium/selenium_ide_verification_yiibais.html) | 在Selenium IDE插入验证在本节中讨论。        |
| [Selenium 模式匹配](http://www.yiibai.com/selenium/selenium_ide_pattern_matching.html) | 本节介绍如何使用IDE正则表达式来工作。            |
| [Selenium用户扩展](http://www.yiibai.com/selenium/selenium_user_extensions.html) | Java脚本，允许用户定制或添加新的功能。           |
| [不用浏览器执行](http://www.yiibai.com/selenium/selenium_ide_on_different_browser.html) | 本节介绍了如何在不同的浏览器执行Selenium IDE脚本。 |# Selenium IDE下载

## Selenium - IDE

**步骤 1 : **启动Firefox，然后导航到URL - http://seleniumhq.org/download/ （有时打不开，若打不开可能从这里下载：http://www.yiibai.com/siteinfo/download.html）。 在Selenium IDE部分，单击显示如下所示当前版本号的链接。

![Selenium IDE 1](http://www.yiibai.com/uploads/allimg/140831/152Z05540-0.jpg)

**步骤 2 :  **Firefox的附加组件通知弹出了允许和禁止的选项。用户必须允许安装。

![Selenium IDE 2](http://www.yiibai.com/uploads/allimg/140831/152Z045K-1.jpg)

**步骤3 : **加载项安装程序发出警告不可信的附加组件的用户。点击“Install Now”。

![Selenium IDE 3](http://www.yiibai.com/uploads/allimg/140831/152Z0FB-2.jpg)

**步骤 4 :  **Selenium IDE现在可以通过浏览访问 'Tools' >> 'Selenium IDE'。

![Selenium IDE 5](http://www.yiibai.com/uploads/allimg/140831/152Z05B4-3.jpg)

**步骤 5 : **在Selenium IDE，也可以直接从快速访问菜单栏访问，如下图所示。# SeleniumIDE不同的浏览器

Selenium IDE脚本只能对火狐的工具Firefox插件运行测试。使用Selenium-IDE开发的测试可以对其他浏览器所保存为Selenium网络驱动器或硒的远程控制指令码执行。脚本只能对火狐的工具Firefox插件运行测试。使用Selenium-IDE开发的测试可以对其他浏览器所保存为Selenium网络驱动器或硒的远程控制指令码执行。更多关于Selenium的webdriver和Selenium的远程控制，在后面的章节有详细讲解。

**第1步：**打开Selenium IDE任何已保存的测试

**第2步：**定位到“File”菜单，并选择“Export Test Suite As”，而选择将被列出。

![Selenium IDE 28](http://www.yiibai.com/uploads/allimg/140925/2019423J5-0.jpg)

**步骤3：**现在让我们导出脚本“WebDriver”，并将其保存为同样的名称。

**第4步：**如下图所示，显示保存webdriver文件。

![Selenium IDE 29](http://www.yiibai.com/uploads/allimg/140925/2019425147-1.jpg)# Selenium - IDE 工具特点

Selenium IDE的特点列出了一个简单的工具的帮助下提示，如下图所示。

![Selenium IDE 4](http://www.yiibai.com/uploads/allimg/140831/15314S621-0.jpg)

记录工具栏的功能进行说明如下。

![Selenium IDE 11](http://www.yiibai.com/uploads/allimg/140831/15314T925-1.jpg)# SeleniumIDE模式匹配

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
| verifyValue  | id=name     | regexp:[Tt]ax ([Yy]ear) |# Selenium IDE 测试

## Selenium IDE 测试

调试是为了发现和修复测试脚本，任何脚本开发的共同步骤是错误的处理。为了使这一过程更加稳固，我们可以使用Selenium IDE的一个插件叫“Power Debugger”

Step 1 : 安装Selenium IDE的Power Debugger，导航到 https://addons.mozilla.org/en-US/firefox/addon/power-debugger-selenium-ide/ 然后点击 "Add to Firefox" 链接如下所示：

![Selenium IDE 16](http://www.yiibai.com/uploads/allimg/140831/1Z1264051-0.jpg)

Step 2 : 现在启动 'Selenium IDE'  会发新的图标, "Pause on Fail" 在录制工具栏，如下图所示。点击它为 ON。 当再次点击，将它打开为"OFF"。

![Selenium IDE 17](http://www.yiibai.com/uploads/allimg/140831/1Z1261E3-1.jpg)

Step 3 : 用户可以打开 "pause on fail" 开或关在任何时间即使测试运行

Step 4 : 一旦测试在暂停的情况下，由于步骤中有一个失败，可以使用通常的暂停/步按钮继续执行测试。如果故障是在任何测试的情况下，最后一个命令执行不会被暂停。

Step 5 : 我们还可以使用断点来了解在这过程中到底发生了什么。插入一个特定步骤一个断点，执行从上下文“右键”，选择“toggle Break Yiibai”相关菜单。

![Selenium IDE 18](http://www.yiibai.com/uploads/allimg/140831/1Z12641N-2.jpg)

Step 6 : 插入断点则显示暂停图标，特定步骤如下所示。

![Selenium IDE 19](http://www.yiibai.com/uploads/allimg/140831/1Z1262341-3.jpg)

Step 7 : 当我们执行该脚本，该脚本将暂停执行插入断点的地方。这将有助于计算一个元素等的值/表示在用户执行过程中。

![Selenium IDE 20](http://www.yiibai.com/uploads/allimg/140831/1Z1262X6-4.jpg)# Selenium IDE测试创建

## Selenium IDE 测试创建

涉及使用IDE Selenium创建测试，如下面的步骤

1. 记录和测试添加命令
2. 保存测试记录
3. 保存测试程序
4. 执行测试记录

### 在测试中记录和添加命令

为了演示目的，我们将利用www.ncalculators.com，了解selenium的特点。

**步骤 1 :** 启动Firefox浏览器，然后导航到该网站 - http://www.ncalculators.com/

**步骤 2 :** 从工具菜单中打开Selenium IDE，按下录制按钮-即在右上角。

![Selenium IDE 7](http://www.yiibai.com/uploads/allimg/140831/1633424146-0.jpg)

**步骤 3 : **导航到 "Math Calculator" >> "Percent Calculator >> 输入"10" 作为 number1 并且输入 50 作为 number2 然后点击 "calculate".

![Selenium IDE 7](http://www.yiibai.com/uploads/allimg/140831/163342J94-1.jpg)

**步骤 4 :  **然后，用户可以插入检查点通过右键单击Web元素，并选择 "Show all available commands" >> 选择"assert text css=b 5"

![Selenium IDE 8](http://www.yiibai.com/uploads/allimg/140831/163342A38-2.jpg)

**步骤 4 : **所记录的脚本生成并被显示在以下脚本如下所示。

![Selenium IDE 9](http://www.yiibai.com/uploads/allimg/140831/1633424959-3.jpg)

### 保存记录的测试

**第1步：**保存测试用例可通过导航到 "File" >> "Save Test" 并将文件保存在选择的位置。该文件保存为.HTML为默认值。

该测试也可以保存扩展名为 .HTM，.SHTML和.XHTML。

![Selenium IDE 9](http://www.yiibai.com/uploads/allimg/140831/1633424959-3.jpg)

### 保存测试套件

测试套件是可以作为一个单独的实体来执行测试的集合。

步骤1：创建一个测试套件可通过导航到 "File" >> "New Test Suite" 如下所示：

![Selenium IDE 13](http://www.yiibai.com/uploads/allimg/140831/1633424059-5.jpg)

**步骤2：**该测试可以通过选择选项来记录，一个接一个 从 "File" 菜单中的"New Test Case" .

**步骤3：**个人测试使用单独的名称来保存 "Test Suite".

![Selenium IDE 14](http://www.yiibai.com/uploads/allimg/140831/1633426191-6.jpg)

### 执行记录的测试

所记录的脚本，执行的任何脚本可通过单击在工具栏中的按钮 "Play entire suite" 或 "Play current test" 。

**第1步： **运行状态可以可以看出，在显示的通过和失败的测试号状态窗格。

**第2步：**一旦步执行，用户可以看到结果在“Log”窗格。

**第3步：**在执行每个步骤之后，测试步骤的背景变成“绿色”，如果获得通过如果失败则为“红”，，如下图所示。

![Selenium IDE 15](http://www.yiibai.com/uploads/allimg/140831/1633422105-7.jpg)# Selenium IDE验证点

## Selenium IDE验证点

我们还开发了测试用例需要检查一个Web页面的属性。这需要维护和验证命令。有两种方法可以验证点到任何脚本

插入记录模式中的任何验证点单击“右键”元素，并选择“Show all Available Commands”，如下图所示。

![selenium ide 21](http://www.yiibai.com/uploads/allimg/140831/21141S311-0.jpg)

我们也可以通过执行“右键”，然后选择“Insert New Command”插入一个命令。

![selenium ide 22](http://www.yiibai.com/uploads/allimg/140831/21141T5B-1.jpg)

插入新的命令后，单击“Command”下拉列表，选择如下图所示的命令的列表提供适当的验证点

![selenium ide 23](http://www.yiibai.com/uploads/allimg/140831/21141Q1H-2.jpg)

下面是主要用于验证的命令，这有助于我们检查一个特定步骤已通过或失败。

- verifyElementPresent
- assertElementPresent
- verifyElementNotPresent
- assertElementNotPresent
- verifyText
- assertText
- verifyAttribute
- assertAttribute
- verifyChecked
- assertChecked
- verifyAlert
- assertAlert
- verifyTitle
- assertTitle

## 同步点

在程序执行时，应用程序可能由服务器的负载情况来决定响应速度，因此，它必需要应用和脚本同步。下面是几个命令，我们可以用它来确保脚本和应用程序同步。

- waitForAlertNotPresent
- waitForAlertPresent
- waitForElementPresent
- waitForElementNotPresent
- waitForTextPresent
- waitForTextNotPresent
- waitForPageToLoad
- waitForFrameToLoad# SeleniumRC

# Selenium RC

## 什么是Selenium - RC

Selenium-RC意思是Selenium的远程控制(又称Selenium1.0)，是主要Selenium项目持续很长一段时间Selenium webdriver(Selenium2.0)才生效存在性。现在Selenium RC是很难使用在webdriver具有更强大的功能，但用户仍可以继续开发使用rc脚本。

它允许我们编写的编程语言，如Java，C＃，Perl，Python和PHP创建更复杂的测试，如读写文件的全功率的帮助自动化的Web应用程序的UI测试，查询数据库，电子邮件的测试结果。

**注：**Selenium RC已被处理，只是为了理解图点和唯一webdriver进行详细说明，webdriver更强大和稳定。Selenium RC和webdriver比较在后面的章节讲解。

## Selenium RC的结构

Selenium RC的工作方式是这样，客户端库使用Selenium RC服务器经过每个Selenium命令来执行通信。然后服务器通过Selenium命令来使用Selenium核心JavaScript命令浏览器。

在浏览器中执行使用JavaScript解释器的Selenium 命令。

![Selenium IDE 52](http://www.yiibai.com/uploads/allimg/140926/1-14092606344Xc.jpg)

Selenium RC分为两部分。

- Selenium服务器启动和终止，除了它的浏览器解释并执行Selenese命令。它也通过拦截和验证器和测试的应用程序之间传递的HTTP消息作为HTTP代理。
- 客户端库，它提供了编程语言(Java，C＃，Perl，Python和PHP)和Selenium-RC服务器中的每一个之间的接口。

## RC - 脚本

现在让我们写使用Selenium远程控制的示例脚本。让我们用 http://www.calculator.net/ 来理解 Selenium RC。我们将使用“百分比计算器”，即在“数学计算器”模块目前执行百分比计算。

**第1步：**启动Selenium 的远程控制(带命令提示符的帮助下)在环境设置一章解释。

**第2步：**启动Selenium RC，打开Eclipse，并创建“New Project”，如下图所示之后。

![Selenium IDE 53](http://www.yiibai.com/uploads/allimg/140926/1-14092606351D60.jpg)

**第3步：**输入项目名称，然后单击“Next”按钮。

![Selenium IDE 54](http://www.yiibai.com/uploads/allimg/140926/1-140926063621X1.jpg)

**第4步：**验证源，项目，库和输出文件夹，然后单击“Finish”。

![Selenium IDE 55](http://www.yiibai.com/uploads/allimg/140926/1-140926063F9B3.jpg)

**第4步：**右键单击“project”容器，然后选择“Configure Build Path”。

![Selenium IDE 56](http://www.yiibai.com/uploads/allimg/140926/1-140926063P31N.jpg)

**第5步：**属性'selrcdemo“打开。导航到“Libaries”选项卡，并选择“Add External JARs”。选择我们下载了Selenium RC的jar文件，它会出现如下图所示。

![Selenium IDE 57](http://www.yiibai.com/uploads/allimg/140926/1-1409260639253E.jpg)

**第6步：**将引用的库如下图所示显示。

![Selenium IDE 58](http://www.yiibai.com/uploads/allimg/140926/1-140926064005T0.jpg)

**步骤7：**通过执行右键单击“src”文件夹中创建一个新的类文件，并选择“New”>>“class”。

![Selenium IDE 59](http://www.yiibai.com/uploads/allimg/140926/1-14092606405A36.jpg)

**第8步：**输入类文件的名称，并启用“public static void main”，如下图所示。

![Selenium IDE 60](http://www.yiibai.com/uploads/allimg/140926/1-14092606415O40.jpg)

**步骤9：**在文件夹结构中创建的创建的类，如下所示。

![Selenium IDE 70](http://www.yiibai.com/uploads/allimg/140926/1-140926064236331.jpg)

**第10步：**现在是时候进行编码。下面的代码有注释嵌入使读者了解。

```
package selrcdemo;
import com.thoughtworks.selenium.DefaultSelenium;
import com.thoughtworks.selenium.Selenium;

public class rcdemo 
{
	public static void main(String[] args) throws InterruptedException 
	{
		
	//Instatiate the RC Server
	Selenium selenium = new DefaultSelenium("localhost", 4444 , "firefox", "http://www.calculator.net");
	selenium.start();   // Start
	selenium.open("/");  // Open the URL
	selenium.windowMaximize();

	// Click on Link Math Calculator
	selenium.click("xpath=.//*[@id='menu']/div[3]/a");
	Thread.sleep(2500); // Wait for page load
	
	// Click on Link Percent Calculator
	selenium.click("xpath=.//*[@id='menu']/div[4]/div[3]/a");
	Thread.sleep(4000); // Wait for page load
	
	
	// Focus on text Box
	selenium.focus("name=cpar1");
	// enter a value in Text box 1
	selenium.type("css=input[name="cpar1"]", "10");

	// enter a value in Text box 2
	selenium.focus("name=cpar2");
	selenium.type("css=input[name="cpar2"]", "50");
	
	// Click Calculate button
	selenium.click("xpath=.//*[@id='content']/table/tbody/tr/td[2]/input");
	
	// verify if the result is 5
	String result = selenium.getText(".//*[@id='content']/p[2]");

		
	if (result == "5")
	{
		System.out.println("Pass");
	}else
	{
		System.out.println("Fail");
	}
		
	}

}

```

**第11步：**现在，让我们通过点击“Run”按钮执行该脚本。

**第12步：**脚本将开始执行和用户将能够看到在“Command History”选项卡上的命令历史记录。

![Selenium IDE 71](http://www.yiibai.com/uploads/allimg/140926/1-140926064435117.jpg)

**步骤13：**该应用程序的最终状态显示为如下。百分比的计算方法和它在屏幕上显示的结果如下所示。

![Selenium IDE 73](http://www.yiibai.com/uploads/allimg/140926/1-14092606452BL.jpg)

**步骤14：**在测试的输出被打印的Eclipse控制台上所示，因为我们已打印输出到控制台下面。实时输出写入到HTML文件或简单的文本文件。

![Selenium IDE 74](http://www.yiibai.com/uploads/allimg/140926/1-1409260646062B.jpg)# SeleniumSelenese命令

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
- **css=cssSelectorSyntax **- 使用CSS选择器选择元素# SeleniumTestNG

[TOC]

## 什么是TestNG

Test*NG是一个功能强大的测试框架，是Junit的一个增强版本，Junit在使用多年之前，TestNG才生效存在。NG 代表“下一代”。*

TestNG框架提供了以下功能和解答我们的问题：“为什么我们需要TestNG”？

- 注释可以帮助我们来组织使测试更容易。
- 灵活的测试配置。
- 测试例可以更容易地进行分组
- 可以使用TestNG实现测试并行
- 支持数据驱动测试
- 内置的报告

## Eclipse安装TestNG

**第1步：**启动Eclipse，选择“Install New Software”。

![Selenium IDE 93](http://www.yiibai.com/uploads/allimg/140928/2034591496-0.jpg)

**第2步：**输入网址为“http://beust.com/eclipse”，然后单击“Add”。

![Selenium IDE 94](http://www.yiibai.com/uploads/allimg/140928/20345964I-1.jpg)

**第3步：**打开添加存储库对话框输入名称为“TestNG”，然后点击“OK”

![Selenium IDE 95](http://www.yiibai.com/uploads/allimg/140928/2034595249-2.jpg)

**第4步：**点击“全Select All”和“TestNG”将被选择，如图所示。

![Selenium IDE 96](http://www.yiibai.com/uploads/allimg/140928/2034593346-3.jpg)

**第5步：**点击“Next”继续。

![Selenium IDE 97](http://www.yiibai.com/uploads/allimg/140928/2034595936-4.jpg)

**第6步：**检查被选中项目，然后单击“Next”。

![Selenium IDE 98](http://www.yiibai.com/uploads/allimg/140928/203459E48-5.jpg)

**第7步：**“Accept the License Agreement”，然后单击“Finish”。

![Selenium IDE 99](http://www.yiibai.com/uploads/allimg/140928/2034592225-6.jpg)

**第8步：**TestNG开始安装并且将示出进度如下。

![Selenium IDE 100](http://www.yiibai.com/uploads/allimg/140928/203459E25-7.jpg)

**第9步：**安全警告弹出的软件的有效性不能成立。单击“Ok”。

![Selenium IDE 101](http://www.yiibai.com/uploads/allimg/140928/20345a1K-8.jpg)

**第10步：**安装程序弹出的重启。单击“Yes”。

![Selenium IDE 102](http://www.yiibai.com/uploads/allimg/140928/2034595261-9.jpg)

## TestNG的注解

注释被正式添加到Java语言中JDK5和TestNG作出的选择使用注解来注解测试类。以下是一些使用注释的优点。更多关于[TestNG](http://www.yiibai.com/testng/index.html)可以在这里找到 [www.yiibai.com/testng/index.html ](http://www.yiibai.com/testng/index.html)

- TestNG识别是通过查找注释感兴趣的方法。因此，方法的名称不局限于任何模式或格式。
- 我们可以通过额外的参数来说明。
- 注释是强类型，所以编译器会标志任何错误。
- 测试类不再需要扩展什么（如测试用例，选择JUnit3）。

| Annotation        | 描述                                       |
| ----------------- | ---------------------------------------- |
| **@BeforeSuite**  | 被注释的方法将只在这个套件中的所有测试运行之前运行一次。             |
| **@AfterSuite**   | 被注释的方法将只在这个套件中的所有测试都运行后，运行一次。            |
| **@BeforeClass**  | 带注释的方法将只调用在当前类中的第一测试方法之前运行一次。            |
| **@AfterClass**   | 带注释的方法将仅在当前类中的所有的测试方法已经被执行之后运行一次。        |
| **@BeforeTest**   | 属于类<测试>中的任何测试方法标记运行之前被注释的方法将被运行。         |
| **@AfterTest**    | 被注释的方法都将属于该类别的<测试>标签内的测试方法运行后运行。         |
| **@BeforeGroups** | 这种配置方法，将之前运行的组的列表。此方法是保证属于任何这些基团的被调用的第一测试方法之前短暂运行。 |
| **@AfterGroups**  | 这种配置方法，将后运行的组的列表。这个方法保证了属于任何这些基团的被调用的最后一个测试方法之后不久运行。 |
| **@BeforeMethod** | 被注释的方法将每个测试方法之前运行。                       |
| **@AfterMethod**  | 被注释的方法将每个测试方法之后运行。                       |
| **@DataProvider** | 标记的方法为测试方法提供数据。被注释的方法必须返回一个Object[] []，其中每个Object []对象可以分配的测试方法的参数列表。想从这个DataProvider接收数据的@Test方法需要使用dataProvider名称等于这个注解的名字。 |
| **@Factory**      | 将方法标记为一个工厂，返回将使用了TestNG作为测试类的对象。该方法必须返回一个Object[]。 |
| **@Listeners**    | 定义了一个测试类监听器。                             |
| **@Parameters**   | 介绍了如何将参数传递到一个方法@Test。                    |
| **@Test**         | 标志着一个类或方法作为测试的一部分。                       |

## Eclipse创建TestNG项目

**第1步：**启动Eclipse，并创建一个“New Java Project”，如下图所示。

![Selenium IDE 53](http://www.yiibai.com/uploads/allimg/140928/20345942J-10.jpg)

**第2步：**输入项目名称，然后单击“Next”。

![Selenium IDE 103](http://www.yiibai.com/uploads/allimg/140928/20345922O-11.jpg)

**第3步：**找到“Libraries”选项卡，并单击添加Selenium远程控制服务器的JAR文件“Add External JAR's”，如图所示。

![Selenium IDE 113](http://www.yiibai.com/uploads/allimg/140928/2034595928-12.jpg)

**第4步：**添加JAR文件，如下图所示，然后单击“Add Library”。

![Selenium IDE 104](http://www.yiibai.com/uploads/allimg/140928/20345950B-13.jpg)

**第5步：**“Add Library”对话框打开。选择“TestNG”，然后点击“Next”在“Add Library”对话框。

![Selenium IDE 105](http://www.yiibai.com/uploads/allimg/140928/2034593R8-14.jpg)

**第6步：**添加“TestNG”类库加入如下图所示它显示出来。

![Selenium IDE 106](http://www.yiibai.com/uploads/allimg/140928/2034594F5-15.jpg)



**第7步：**当创建项目的结构将在下面所示的项目。

![img](http://www.yiibai.com/uploads/allimg/140928/2034592010-16.jpg)

**第8步：**右键点击“src”文件夹并选择“New”和“other”。

![Selenium IDE 108](http://www.yiibai.com/uploads/allimg/140928/2034595395-17.jpg)

**第9步：**选择“TestNG”，然后点击“Next”。

![Selenium IDE 109](http://www.yiibai.com/uploads/allimg/140928/2034596160-18.jpg)



**第10步：**选择“Source Folder”名称，并单击“Ok”。

![Selenium IDE 110](http://www.yiibai.com/uploads/allimg/140928/20345aG0-19.jpg)

**第11步：**选择“Package name”，类名，然后单击“Finish”。

![Selenium IDE 111](http://www.yiibai.com/uploads/allimg/140928/2034594G5-20.jpg)

**第12步：**在Package Explorer和创建的类将可以显示出来给用户。

![Selenium IDE 112](http://www.yiibai.com/uploads/allimg/140928/2034593Y7-21.jpg)

## 在TestNG的第一个测试

现在让我们使用TestNG启动脚本。为我们理解webdriver使用相同的示例脚本。我们将利用演示应用程序，www.calculator.net并执行％的计算器。

在下面的测试，你会发现，没有main方法，如TestNG将驱动程序的执行流程。初始化驱动程序后，它将执行“@BeforeTest'方法，其次是”@Test'，然后'@AfterTest“。请注意，可以在一个类中的任何数量“@Test”注解，但是“@BeforeTest'和'@AfterTest”只能出现一次。

```
package TestNG;
import java.util.concurrent.TimeUnit;
import org.openqa.selenium.*;
import org.openqa.selenium.firefox.FirefoxDriver;
import org.testng.annotations.AfterTest;
import org.testng.annotations.BeforeTest;
import org.testng.annotations.Test;

public class TestNGClass 
{
  WebDriver driver = new FirefoxDriver();

  @BeforeTest
  public void launchapp()
  {		
    //Puts a Implicit wait, Will wait for 10 seconds before throwing exception
    driver.manage().timeouts().implicitlyWait(10, TimeUnit.SECONDS);
    //Launch website
    driver.navigate().to("http://www.calculator.net");	
    driver.manage().window().maximize();
  }
		
  @Test
  public void calculatepercent()
  {
	// Click on Math Calculators 
	driver.findElement(By.xpath(".//*[@id='menu']/div[3]/a")).click();    

	// Click on Percent Calculators	
	driver.findElement(By.xpath(".//*[@id='menu']/div[4]/div[3]/a")).click();     

	// Enter value 10 in the first number of the percent Calculator
	driver.findElement(By.id("cpar1")).sendKeys("10"); 		

	// Enter value 50 in the second number of the percent Calculator    	
	driver.findElement(By.id("cpar2")).sendKeys("50");		

	// Click Calculate Button	
	driver.findElement(By.xpath(".//*[@id='content']/table/tbody/tr/td[2]/input")).click();	   

	// Get the Result Text based on its xpath    	
	String result = driver.findElement(By.xpath(".//*[@id='content']/p[2]/span/font/b")).getText();		  

	//Print a Log In message to the screen		
	System.out.println(" The Result is " + result);					
		
	if(result.equals("5"))
	{
		System.out.println(" The Result is Pass");
	}
	else
	{
		System.out.println(" The Result is Fail");
	}		    
  }

  @AfterTest
  public void terminatetest()
  {   
    driver.close();
  }
}

```

## 执行

通过在创建的XML执行右键单击并选择 "Run As" >> "TestNG Suite"进行测试执行

![Selenium IDE 189](http://www.yiibai.com/uploads/allimg/140928/2034591B1-22.jpg)

## 结果分析

输出被丢到了控制台，它会出现如下图所示。控制台输出也有执行摘要。

![Selenium IDE 114](http://www.yiibai.com/uploads/allimg/140928/20345945W-23.jpg)

TestNG的结果也可以看出在不同的标签。点击“HTML Report View”按钮，如下图所示。

![Selenium IDE 115](http://www.yiibai.com/uploads/allimg/140928/20345960P-24.jpg)

如下所示的HTML结果将被显示。

![Selenium IDE 117](http://www.yiibai.com/uploads/allimg/140928/2034591327-25.jpg)# SeleniumWebdriver

webdriver自动化俗称Selenium 2.0测试Web应用程序工具。 webdriver使用不同的底层框架，Selenium 遥控器使用JavaScript的Selenium 核嵌入式已经在有一定的局限性的浏览器中。 webdriver直接交互而不与Selenium 远程控制，依赖于服务器上的任何中介的浏览器。它是用在以下方面：

在Selenium开发者社区努力下，不断提高Selenium webdriver与Selenium的整合。

- MULT浏览器测试，包括对不能很好地支持Selenium的远程控制浏览器改进的功能(硒1.0)
- 处理多个帧，多个浏览器窗口，弹出窗口和警报。
- 复杂的页面导航。
- 高级用户导航，如拖动和拖放。
- 基于AJAX的UI元素

## 体系结构

webdriver最好用一个简单的架构图，说明，如下图所示。

![Selenium IDE 92](http://www.yiibai.com/uploads/allimg/140927/1552021019-0.jpg)

## Selenium RC VS webdriver

| Selenium RC                              | Selenium WebDriver                       |
| ---------------------------------------- | ---------------------------------------- |
| Selenium RC的结构复杂，因为服务器需要启动在开始试运行前。       | webdriver架构比Selenium RC简单，因为它控制着从操作系统层面的浏览器。 |
| Selenium服务器充当浏览器和Selenese的命令之间的中间人       | webdriver直接相互作用，以在浏览器和使用浏览器的引擎进行控制。      |
| Selenium RC的脚本执行速度较慢，因为它使用了Javascript来与RC互动 | webdriver的速度更快，因为它直接交互使用的浏览器。            |
| Selenium RC不能支持无头，因为它需要一个真正的浏览器一起工作。     | webdriver可以支持无头执行                        |
| 它是一个简单的API                               | 复杂，API相比，RC有点大                           |
| 减面向对象的API                                | 纯粹的面向对象的API                              |
| 不能测试移动应用程序                               | 可测试iPhone/Android应用程序                    |

## 使用webdriver脚本

让我们了解webdriver如何工作。为了演示目的，我们将使用http://www.calculator.net/。我们将执行“百分比计算器”，这是位于“数学计算器”。我们已经下载了所需要webdriver的JAR。请参阅环境设置一章。

第1步：从提取Eclipse文件夹中启动“Eclipse”。

![Selenium IDE 75](http://www.yiibai.com/uploads/allimg/140927/155202FI-1.jpg)

第2步：点击“Browse”按钮选择工作区。

![Selenium IDE 76](http://www.yiibai.com/uploads/allimg/140927/155202N25-2.jpg)

第3步：现在，创建“New Project”，从“File”菜单。

![Selenium IDE 53](http://www.yiibai.com/uploads/allimg/140927/15520252Y-3.jpg)

第4步：输入项目名称，然后单击“Next”。

![Selenium IDE 77](http://www.yiibai.com/uploads/allimg/140927/15520222B-4.jpg)

第五步：进入Libraries选项卡，并选中所有的JAR包文件，我们已经下载（请参阅环境搭建章）。添加引用Selenium webdriver的库文件夹中的所有JAR，selenium-java-2.42.2.jar和selenium-java-2.42.2-srcs.jar

![Selenium IDE 78](http://www.yiibai.com/uploads/allimg/140927/1552024Q3-5.jpg)

第6步：如下图所示创建包。

![Selenium IDE 79](http://www.yiibai.com/uploads/allimg/140927/15520230F-6.jpg)

第7步：现在，让我们创建一个通过执行'Class'右键单击程序包，然后选择“New”>>“Class”

![Selenium IDE 82](http://www.yiibai.com/uploads/allimg/140927/1552023F6-7.jpg)

第8步：现在命名类，并让它设置为main方法

![Selenium IDE 80](http://www.yiibai.com/uploads/allimg/140927/15520253B-8.jpg)

第9步：类概要如下所示。

![Selenium IDE 81](http://www.yiibai.com/uploads/allimg/140927/1552025358-9.jpg)

步骤10：现在是时候编写代码了。下面的脚本更容易理解，因为它清楚地解释了一步，在嵌入的注释步骤。请看看“Locators”一章，了解如何捕捉对象的属性。

```
import java.util.concurrent.TimeUnit;
import org.openqa.selenium.*;
import org.openqa.selenium.firefox.FirefoxDriver;

public class webdriverdemo
{
  public static void main(String[] args)
  {
	WebDriver driver = new FirefoxDriver();

    //Puts a Implicit wait, Will wait for 10 seconds before throwing exception
	driver.manage().timeouts().implicitlyWait(10, TimeUnit.SECONDS);

    //Launch website
	driver.navigate().to("http://www.calculator.net/");
	
	//Maximize the browser
	driver.manage().window().maximize();

    // Click on Math Calculators
	driver.findElement(By.xpath(".//*[@id='menu']/div[3]/a")).click();
  
    // Click on Percent Calculators
	driver.findElement(By.xpath(".//*[@id='menu']/div[4]/div[3]/a")).click();

	// Enter value 10 in the first number of the percent Calculator
    driver.findElement(By.id("cpar1")).sendKeys("10");

    // Enter value 50 in the second number of the percent Calculator
    driver.findElement(By.id("cpar2")).sendKeys("50");
    
    // Click Calculate Button
    driver.findElement(By.xpath(".//*[@id='content']/table/tbody/tr/td[2]/input")).click();

    // Get the Result Text based on its xpath
    String result = driver.findElement(By.xpath(".//*[@id='content']/p[2]/span/font/b")).getText();
    
	//Print a Log In message to the screen
    System.out.println(" The Result is " + result);
    
	//Close the Browser.
    driver.close();    
  }
}

```

第11步：以上脚本的输出将被打印在控制台。

![Selenium IDE 83](http://www.yiibai.com/uploads/allimg/140927/1552023408-10.jpg)

## 最常用的命令

下表列出了webdriver的最常用的命令以及它的语法，这将有助于我们开发webdriver脚本。

| Commmand                                | 描述                                       |
| --------------------------------------- | ---------------------------------------- |
| driver.get("URL")                       | 导航到应用程序                                  |
| element.sendKeys("inputtext")           | 输入一些文本输入框                                |
| element.clear()                         | 从输入框清空内容                                 |
| select.deselectAll()                    | 这将取消选择页面上的第一个选择所有选项：                     |
| select.selectByVisibleText("some text") | select the OPTION with the input specified by the user. |
| driver.switchTo().window("windowName")  | Moving the focus from one window to another |
| driver.switchTo().frame("frameName")    | swing from frame to frame                |
| driver.switchTo().alert()               | Helps in handling alerts                 |
| driver.navigate().to("URL")             | Navigate to the URL                      |
| driver.navigate().forward()             | To Navigate forward                      |
| driver.navigate().back()                | To Navigate back                         |
| driver.close()                          | Closes the current Browser associated with the driver |
| driver.quit()                           | Quits the driver and closes all the associated window of that driver. |
| driver.refresh()                        | Refreshes the current page.              |# Selenium定位器

在Selenium 的findElement()和findElements()方法通过webdriver和WebElement类提供的帮助进行webdriver定位元素。

- findElement()方法返回一个基于指定的搜索条件WebElement对象或最终抛出一个异常，如果没有找到符合搜索条件的任何元素。
- findElements()方法返回WebElements符合搜索条件的列表。如果没有发现的元素，则返回空列表。

下表给出了定位selenium 元素的webdriver的Java语法。

| Method               | Syntax                                   | 描述            |
| -------------------- | ---------------------------------------- | ------------- |
| By ID                | driver.findElement(By.id(<element ID>))  | 定位元素使用ID属性    |
| By name              | driver.findElement(By.name(<element name>)) | 定位使用Name属性的元素 |
| By class name        | driver.findElement(By.className(<element class>)) | 定位使用类属性的元素    |
| By tag name          | driver.findElement(By.tagName(<htmltagname>)) | 定位使用HTML标记元素  |
| By link text         | driver.findElement(By.linkText(<linktext>)) | 定位使用的链接文字链接   |
| By partial link text | driver.findElement(By.partialLinkText(<linktext>)) | 定位链接使用链接的文字部分 |
| By CSS               | driver.findElement(By.cssSelector(<css selector>)) | 定位使用CSS选择器的元素 |
| By XPath             | driver.findElement(By.xpath(<xpath>))    | 定位使用XPath查询元素 |

## 定位器的使用

现在让我们了解这些定位器方法每个人的实际使用情况与http://www.calculator.net帮助

1，根据ID：对象访问使用ID的帮助。在这种情况下，它是文本框的ID。该值使用SendKeys方法与ID(cdensity)的帮助下进入文本。

![Selenium IDE 84](http://www.yiibai.com/uploads/allimg/140927/1606391330-0.jpg)

```
driver.findElement(By.id("cdensity")).sendKeys("10");

```

2，按名称：访问对象时使用的名称的帮助。在这种情况下，它是文本框的名称。该值是使用SendKeys方法与ID(cdensity)的帮助下进入文本。

![Selenium IDE 85](http://www.yiibai.com/uploads/allimg/140927/1606396151-1.jpg)

```
driver.findElement(By.name("cdensity")).sendKeys("10");

```

3，通过类名：对象与类的名称，帮助进行访问。在这种情况下，它是WebElement的类名。该值可以用gettext方法进行访问。

![Selenium IDE 86](http://www.yiibai.com/uploads/allimg/140927/1606396457-2.jpg)

```
List<WebElement> byclass = driver.findElements(By.className("smalltext smtb"));

```

4，通过标签名：元素的DOM标签名称，这是很容易处理的表使用此方法。我们可以看一个例子了演示程序。

```
WebElement table = driver.findElement(By.id("calctable"));
List<WebElement> row = table.findElements(By.tagName("tr"));
int rowcount = row.size();

```

5，通过链接文本：此方法可以帮助我们找到与之相配的可见文本的链接元素。

![Selenium IDE 87](http://www.yiibai.com/uploads/allimg/140927/1606393607-3.jpg)

```
driver.findElements(By.linkText("Volume")).click();

```

5，通过部分链接文本：此方法可以帮助我们找到了部分匹配可见文本的链接元素。

![Selenium IDE 87](http://www.yiibai.com/uploads/allimg/140927/1606393607-3.jpg)

```
driver.findElements(By.partialLinkText("Volume")).click();

```

6，使用CSS：CSS的使用作为一种方法来识别网络对象，但不是所有的浏览器支持CSS标识。

```
WebElement loginButton = driver.findElement(By.cssSelector("input.login"));

```

7，通过Xpath：XML表示XML路径语言，是一种查询语言，用于从XML文档中选择节点。 XPath语言是基于XML文档的树表示，并提供选择使用各种标准的节点来浏览周围的树。

![Selenium IDE 88](http://www.yiibai.com/uploads/allimg/140927/160639C30-5.jpg)

```
driver.findElement(By.xpath(".//*[@id='content']/table[1]/tbody/tr/td/table/tbody/tr[2]/td[1]/input")).sendkeys("100");
```

# Selenium教程

# Selenium概述

## Selenium - 介绍

Selenium是一个开源的和便携式的自动化软件测试工具，用于测试Web应用程序有能力在不同的浏览器和操作系统运行。Selenium真的不是一个单一的工具，而是一套工具，帮助测试者更有效地基于Web的应用程序的自动化。

现在让我们了解selenium套件和使用这些工具。我们将着眼于以下工具功能：

| 工具                 | 描述                                       |
| ------------------ | ---------------------------------------- |
| Selenium IDE       | Selenium 集成开发环境（IDE）是一个Firefox插件，可以让测试人员跟着，需要测试的工作流程，以记录他们的行为。 |
| Selenium RC        | Selenium远程控制（RC）为旗舰测试框架，它允许多个简单的浏览器动作和线性执行。它使用的编程语言，如Java，C＃，PHP，Python和Ruby和Perl的强大功能来创建更复杂的测试。 |
| Selenium WebDriver | Selenium的webdriver前身是Selenium RC，直接发送命令给浏览器，并检索结果。 |
| Selenium Grid      | Selenium网格用于运行在不同的机器，不同的浏览器同时以最小化执行时间的并行测试的工具。 |

## Selenium优势

QTP和Selenium 都是市场上软件自动化测试最常用的工具。因此，selenium有更多的意义，现在selenium比较QTP/ UFT有更多的优点。

| Selenium                     | QTP/UFT                                  |
| ---------------------------- | ---------------------------------------- |
| Selenium 是一种开源工具。            | QTP是一个商业工具和成本涉及许可证。                      |
| 可以扩展它公开DOM各种技术。              | 有限的附加组件和需要附加组件的技术。                       |
| 可以在不同浏览器执行脚本。                | 可以运行测试在Firefox，IE和Chrome浏览器的特定版本。        |
| 可以执行各种操作系统的脚本。               | 仅适用于Windows操作系统。                         |
| 支持的移动设备。                     | 支持第三方工具的移动设备。                            |
| 执行在浏览器中测试，这不是必需的，重点是脚本执行的进度。 | 脚本执行的工具作用于浏览器（模拟用户操作）过程中需要重点             |
| 可以并联使用Selenium网格运行测试。        | QTP不能并行执行测试，但与质量控制整合QTP允许测试并行执行。质量控制也是一种商业工具。 |

## Selenium 缺点

现在我们讨论selenium较QTP的缺陷。

| Selenium                 | QTP/UFT                    |
| ------------------------ | -------------------------- |
| 仅支持基于Web的应用程序。           | 可以测试Web和桌面应用程序。            |
| 任何功能部件，例如对象存储库/恢复方案      | QTP已经或和恢复方案内置。             |
| 没有IDE，所以这样的脚本开发，不会快于QTP。 | 更直观的IDE，自动化，可以实现更快。        |
| 不能在浏览器中访问控制              | 可以在浏览器中访问控制，如收藏夹栏，后退和前进按钮。 |
| 没有默认生成测试报告。              | 默认的测试结果生成工具中。              |
| 用于参数设置，用户必须依赖于编程语言       | 参数是内置的，易于实现。               |# Selenium测试设计技术

有参与设计测试的各种组件。让我们了解一些参与设计的框架，以及重要的组成部分。点击了解其中的每个都应该可以明白

- [页面对象模型](http://www.yiibai.com/selenium/selenium_page_object_model.html)
- [使用Excel参数化](http://www.yiibai.com/selenium/selenium_parameterizing_using_excel.html)
- [log4j日志](http://www.yiibai.com/selenium/selenium_log4j_logging.html)
- [异常处理](http://www.yiibai.com/selenium/selenium_exception_handling.html)
- [多浏览器测试](http://www.yiibai.com/selenium/selenium_multi_browser_testing.html)
- [捕捉屏幕截图](http://www.yiibai.com/selenium/selenium_capture_screenshots.html)
- [捕获视频](http://www.yiibai.com/selenium/selenium_capture_video.html)# Selenium环境安装设置

为了开发Selenium RC或webdriver脚本，用户必须确保他们有初始配置完成。有很多关联建立环境的步骤。这里将通过详细的讲解。

- 下载并安装Java
- 下载并配置Eclipse
- 配置Firebug和FirePath
- 配置Selenium RC
- 配置Selenium的webdriver

## 下载并安装Java

我们需要有JDK(Java开发工具包)安装序Selenium Webdriver/Selenium工作。让我们先来看看如何下载和安装Java。

步骤1： 导航到的网址：http://www.oracle.com/technetwork/java/javase/downloads/index.htmll

步骤2：转到“Downloads”部分，然后选择“JDK Download”。

![Selenium IDE 30](http://www.yiibai.com/uploads/allimg/140925/2153312441-0.jpg)

**步骤3：**选择“Accept License Agreement”单选按钮。

![Selenium IDE 31](http://www.yiibai.com/uploads/allimg/140925/2153315638-1.jpg)

**第4步：**选择合适的安装。在这种情况下它是“Windows 7-64'位。点击相应的链接和exe档案保存到硬盘。

![Selenium IDE 32](http://www.yiibai.com/uploads/allimg/140925/2153315V6-2.jpg)

**第5步：**运行下载的exe文件和安装程序向导。点击“Next”继续。

![Selenium IDE 33](http://www.yiibai.com/uploads/allimg/140925/2153314531-3.jpg)

**第6步：**选择功能，然后点击“Next”。

![Selenium IDE 34](http://www.yiibai.com/uploads/allimg/140925/2153316304-4.jpg)

**步骤7：**安装程序提取和相同的进度显示在向导中。

![Selenium IDE 35](http://www.yiibai.com/uploads/allimg/140925/2153315957-5.jpg)

**第8步：**用户可以选择安装位置，然后单击“Next”。

![Selenium IDE 36](http://www.yiibai.com/uploads/allimg/140925/2153312349-6.jpg)

**第9步：**安装程序安装JDK和新的文件将被复制。

![Selenium IDE 37](http://www.yiibai.com/uploads/allimg/140925/21533113H-7.jpg)

**第10步：**安装程序安装成功，并显示给用户。

![Selenium IDE 38](http://www.yiibai.com/uploads/allimg/140925/215331GG-8.jpg)

**步骤11：**要验证是否安装成功，转到命令提示符，然后只需键入Java的一个命令。该命令的输出如下所示。如果Java安装不成功，或者如果它没有安装它会引发“unknown command”的错误。

![Selenium IDE 48](http://www.yiibai.com/uploads/allimg/140925/2153315M8-9.jpg)

## 下载并配置Eclipse

第1步：根据操作系统体系结构导航到URL ：http://www.eclipse.org/downloads/ 并下载。

![Selenium IDE 39](http://www.yiibai.com/uploads/allimg/140925/2153315a0-10.jpg)

**第2步：**点击“Download”按钮。

![Selenium IDE 40](http://www.yiibai.com/uploads/allimg/140925/21533111Z-11.jpg)

**第3步：**下载将是一个压缩格式。解压缩的内容。

![Selenium IDE 41](http://www.yiibai.com/uploads/allimg/140925/2153316020-12.jpg)

**第4步：**找到eclipse.exe并双击该文件。

![Selenium IDE 42](http://www.yiibai.com/uploads/allimg/140925/2153311931-13.jpg)

**第5步：**配置工作区中选择开发位置。

![Selenium IDE 43](http://www.yiibai.com/uploads/allimg/140925/2153316426-14.jpg)

**第6步：**打开如下图所示的Eclipse窗口。

![Selenium IDE 44](http://www.yiibai.com/uploads/allimg/140925/215331H08-15.jpg)

## 配置Firebug和FirePath

要使用Selenium RC或webdriver来工作，我们需要根据自己的XPath或编号或名称等序列，以找出我们需要的工具/插件元素来定位元素。定位元素的各种方式被处理，详细在定位器章节。

步骤1：找到的网址：https://addons.mozilla.org/en-US/firefox/addon/firebug/ 并下载插件。

![Selenium IDE 62](http://www.yiibai.com/uploads/allimg/140925/21533135F-16.jpg)

**步骤2：**将插件安装程序显示给用户，它是在单击“Install”按钮开始安装。

![Selenium IDE 63](http://www.yiibai.com/uploads/allimg/140925/21533115Y-17.jpg)

**第3步：**安装完成后，我们可以通过启动插件导航到“Web Developer”>>“Firebug”。

![Selenium IDE 64](http://www.yiibai.com/uploads/allimg/140925/215331I04-18.jpg)

**第4步：**Firepath一个插件，它的工作原理中的萤火虫帮助用户抓住一个元素“Xpath”。导航到“https://addons.mozilla.org/en-US/firefox/addon/firepath/”安装Firepath

![Selenium IDE 65](http://www.yiibai.com/uploads/allimg/140925/2153312456-19.jpg)

**第5步：**插件安装程序显示给用户，它是在单击“Install”按钮开始安装。

![Selenium IDE 66](http://www.yiibai.com/uploads/allimg/140925/215331L04-20.jpg)

**步骤6：**现在推出“Firebug”导航到“Tools”>>“Webdeveloper”>>“Firebug”

![Selenium IDE 67](http://www.yiibai.com/uploads/allimg/140925/2153314U7-21.jpg)

### 示例

现在让我们了解如何使用Firebug和firepath一个例子。为了演示目的，我们将使用www.google.com并捕捉“google.com”文本框的属性。

步骤1：首先在下面的截图高亮点击箭头图标，将其拖动到我们想捕捉属性的对象。如下图所示，该对象的HTML / DOM将被显示。我们能够捕捉到的输入文本框的“ID”，我们可以进行交互。

![Selenium IDE 68](http://www.yiibai.com/uploads/allimg/140925/2153313113-22.jpg)

**步骤2：**为了获取对象的XPath，去“firepath”选项卡，然后执行以下步骤。

- 点击间谍图标。
- 选择控制，想要捕捉的XPath
- 将产生的所选择的控制的xpath

![Selenium IDE 69](http://www.yiibai.com/uploads/allimg/140925/2153314402-23.jpg)

## 配置Selenium RC

现在，就让我们来看看如何配置Selenium 的远程控制。我们将了解如何开发在即将到来的章节关于Selenium RC的章节，但是现在我们明白它只是配置的一部分。

第1步：找到selenium 下载部分http://www.seleniumhq.org/download/，并通过点击它的版本号，如下图所示下载Selenium服务器。

![Selenium IDE 45](http://www.yiibai.com/uploads/allimg/140925/215331Lb-24.jpg)

**第2步：**下载后，我们需要启动Selenium服务器。这样做，打开命令提示符并导航到下载的JAR文件保持如下所示的文件夹。

![Selenium IDE 46](http://www.yiibai.com/uploads/allimg/140925/2153314121-25.jpg)

**第3步：**启动服务器，使用命令“'java -jar <<downloaded jar name >>"如果已安装Java JDK正常，会得到一个成功的消息，如下图所示。现在，我们就可以开始写这将涉及在下一章Selenium RC的脚本。

![Selenium IDE 47](http://www.yiibai.com/uploads/allimg/140925/2153315108-26.jpg)

## 配置Selenium的webdriver

现在，就让我们来看看如何配置Selenium webdriver。我们将了解如何开发在即将到来的章节，Selenium webdriver的剧本，但是现在我们明白它只是配置的一部分。

**第1步：**找到selenium 下载部分http://www.seleniumhq.org/download/和下载selenium 的webdriver通过点击它的版本号，如下图所示。

![Selenium IDE 49](http://www.yiibai.com/uploads/allimg/140925/215331N49-27.jpg)

**第2步：**下载的文件是压缩格式，一个具有解压缩的内容映射到项目文件夹中。

![Selenium IDE 49](http://www.yiibai.com/uploads/allimg/140925/2153313116-28.jpg)

**步骤3：**如下图所示，将解压缩后的内容将被显示。如何将其映射到项目文件夹，如何启动脚本会处理在webdriver的章节。

![Selenium IDE 51](http://www.yiibai.com/uploads/allimg/140925/2153312241-29.jpg)# Selenium用户扩展

## Selenium用户扩展

这很容易扩展Selenium IDE加入自定义操作，断言和定位，策略，这是通过添加方法，在JavaScript的帮助下Selenium 对象原型。在启动时，Selenium会自动寻找通过这些原型方法，使用名称的模式来识别哪些是行动，断言和定位器。

让我们使用JavaScript添加一个'while'循环在Selenium IDE。

**步骤 1 : **要添加js文件，首先导航到https://github.com/darrenderidder/sideflow/blob/master/sideflow.js和复制脚本和地点将其保存在本地文件夹下为 “sideflow.js”，如下图所示。

![Selenium IDE 24](http://www.yiibai.com/uploads/allimg/140925/1-140925201303Q6.jpg)

**第2步：**现在启动“Selenium IDE”，然后导航到"Options" >> "Options"，如下图所示。

![Selenium IDE 25](http://www.yiibai.com/uploads/allimg/140925/1-140925201330391.jpg)

**第3步：**点击“Browse”按钮下的“Selenium Core Extensions”区域产并指向我们已经保存在第1步中的js文件。

![Selenium IDE 26](http://www.yiibai.com/uploads/allimg/140925/2011421109-2.jpg)

**第4步：**重新启动Selenium IDE。

**第5步：**现在将有机会获得一些更多的命令，如 "Label" "While"等

**第6步：**现在，我们创造出在Selenium IDE内的循环，这是能够执行的，如下图所示。

![Selenium IDE 27](http://www.yiibai.com/uploads/allimg/140925/20114235S-3.jpg)# Selenium网格

Selenium网格是分布在多个物理或虚拟机测试，使我们能够并行(同时)执行脚本，导致执行所需的运行测试时间的工具。这给予我们快速而准确的反馈大大加快了跨浏览器和跨平台的测试。

Selenium网格使我们能够执行并行的webdriver或Selenium的远程控制的测试，它使用相同的代码的基础上，因此，代码不必存在它们执行系统上的多个实例。Selenium服务器的独立软件包包括集线器，webdriver，和Selenium RC网格执行脚本。

Selenium 网格具有枢纽和节点

- Hub - 集线器也可以理解为服务器充当中心点所在的测试将被触发。Selenium网格只有一个集线器，它是一台机器上启动一次。
- Node - 节点是Selenium实例附连到将执行测试的集线器。可以存在在其中可以是任何操作系统，并且可以包含任何所支持的浏览器Selenium网格的一个或多个节点。

## 体系结构

Selenium 网格的体系结构是用简单的流程图来解释。

![selenium_ide_121](http://www.yiibai.com/uploads/allimg/140928/21191H617-0.jpg)

## 使用网格工作

为了与网格工作，我们需要确保遵循一定的协议。下面是所涉及的主要步骤，了解他们的每一个细节。

- Configuring Hub
- Configuring Nodes
- Develop Script
- XML Preperation
- Test Execution
- Result Analysis

### 配置Hub

步骤1：从http://docs.seleniumhq.org/download/下载最新的Selenium服务器独立JAR文件。通过点击版本如下所示下载。

![selenium_ide_45](http://www.yiibai.com/uploads/allimg/140928/21191H9D-1.jpg)

第2步：使用以下命令启动Selenium服务器启动的集线器。现在，我们将使用端口“4444”启动集线器。

注：请确保端口＃4444运行没有被其他应用程序占用。

```
java -jar selenium-server-standalone-2.25.0.jar-port 4444-role hub -nodeTimeout 1000
```

![selenium_ide_122](http://www.yiibai.com/uploads/allimg/140928/21191I039-2.jpg)

第3步：现在打开浏览器，然后从集线器导航到http//localhost:4444 （其中已执行的系统步骤＃2）。

![selenium_ide_123](http://www.yiibai.com/uploads/allimg/140928/21191G046-3.jpg)

第4步：现在点击“console”链接，然后单击“view config”。将显示hub的配置。截至目前，我们还没有得到任何节点，因此我们将无法看到细节。

![selenium_ide_124](http://www.yiibai.com/uploads/allimg/140928/21191IQ5-4.jpg)

### 配置节点

第1步：登录到节点（想执行脚本），然后替换文件夹中的“selenium-server-standalone-2.42.2”。我们需要发起节点时指向selenium-server-standalone 的JAR。

第2步：使用以下命令启动Firefox节点。

```
java -jar D:JARselenium-server-standalone-2.42.2.jar -role node -hub http://10.30.217.157:4444/grid/register -browser browserName=firefox -port 5555

Where,
D:JARselenium-server-standalone-2.42.2.jar = Location of the Selenium Server Standalone Jar File(on the Node Machine)
http://10.30.217.157:4444 = IP Address of the Hub and 4444 is the port of the Hub
browserName = firefox (Parameter to specify the Browser name on Nodes)
5555 = Port on which Firefox Node would be up and running.
```

![selenium_ide_125](http://www.yiibai.com/uploads/allimg/140928/21191L427-5.jpg)

第3步：执行该命令后，现在回过头来集线器。导航到URL - http://10.30.217.157:4444和集线器现在会显示在所连接的节点。

![selenium_ide_126](http://www.yiibai.com/uploads/allimg/140928/21191I520-6.jpg)

第4步：现在，让我们启动Internet Explorer节点。用于启动IE浏览器节点，我们需要确保我们有下载的节点机上的Internet Explorer驱动程序。

第5步：要下载Internet Explorer的驱动程序，根据您的操作系统的架构导航到http://docs.seleniumhq.org/download/并下载。下载后解压缩exe文件，并将其放置其中有被称为同时推出IE浏览器节点上的一个文件夹。

![selenium_ide_131](http://www.yiibai.com/uploads/allimg/140928/21191G942-7.jpg)

第6步：使用以下命令启动IE浏览器。

```
C:>java -Dwebdriver.ie.driver=D:IEDriverServer.exe -jar D:JARselenium-server-standalone-2.42.2.jar -role webdriver -hub http://10.30.217.157:4444/grid/register -browser browserName=ie,platform=WINDOWS -port 5558

Where,
D:IEDriverServer.exe = The location of the downloaded the IE Driver(on the Node Machine)
D:JARselenium-server-standalone-2.42.2.jar = Location of the Selenium Server Standalone Jar File(on the Node Machine)
http://10.30.217.157:4444 = IP Address of the Hub and 4444 is the port of the Hub
browserName = ie (Parameter to specify the Browser name on Nodes)
5558 = Port on which IE Node would be up and running.
```

![selenium_ide_127](http://www.yiibai.com/uploads/allimg/140928/21191H611-8.jpg)

第7步：执行该命令后，现在再回到集线器。导航到URL- http://10.30.217.157:4444 集线器现在会显示所连接的IE浏览器节点。

![selenium_ide_128](http://www.yiibai.com/uploads/allimg/140928/21191M126-9.jpg)

第8步：现在我们启动Chrome节点。用于启动浏览器节点，我们需要确保我们有下载的节点机上浏览器的驱动程序。

第9步：下载Chrome浏览器驱动程序，导航到http://docs.seleniumhq.org/download/并导航到第三方浏览器驱动区域，然后单击版本号“2.10”，如下图所示。

![selenium_ide_132](http://www.yiibai.com/uploads/allimg/140928/21191H250-10.jpg)

第10步：下载基于操作系统的类型的驱动程序。我们会执行它在Windows环境，因此我们将下载的Chrome浏览器的Windows驱动程序。下载后解压缩exe文件，并将它具有同时启动Chrome节点被称为一个文件夹。

![selenium_ide_133](http://www.yiibai.com/uploads/allimg/140928/21191I625-11.jpg)

第11步：使用以下命令启动chrome 。

```
C:>java -Dwebdriver.chrome.driver=D:chromedriver.exe -jar D:JARselenium-server-standalone-2.42.2.jar -role webdriver -hub  http://10.30.217.157:4444/grid/register -browser browserName=chrome,platform=WINDOWS -port 5557

Where,
D:chromedriver.exe = The location of the downloaded the chrome Driver(on the Node Machine)
D:JARselenium-server-standalone-2.42.2.jar = Location of the Selenium Server Standalone Jar File(on the Node Machine)
http://10.30.217.157:4444 = IP Address of the Hub and 4444 is the port of the Hub
browserName = chrome (Parameter to specify the Browser name on Nodes)
5557 = Port on which chrome Node would be up and running.
```

![selenium_ide_129](http://www.yiibai.com/uploads/allimg/140928/21191HW0-12.jpg)

第7步：执行该命令后，现在再回集线器。导航到URL- http://10.30.217.157:4444 集线器现在会显示连接到chrome 节点。

![selenium_ide_130](http://www.yiibai.com/uploads/allimg/140928/21191KR5-13.jpg)

### 开发脚本

第1步：我们将开发使用TestNG测试。在下面的例子中，我们将推出使用远程webdriver可以在自己的能力传递给驱动器，这些浏览器驱动器所有信息节点上执行。

浏览器参数会从“XML”文件传递。

```
package TestNG;

import org.openqa.selenium.remote.DesiredCapabilities;
import java.util.concurrent.TimeUnit;
import org.openqa.selenium.*;
import org.testng.annotations.AfterTest;
import org.testng.annotations.BeforeTest;
import org.testng.annotations.Parameters;
import org.testng.annotations.Test;
import java.net.URL;
import java.net.MalformedURLException;

import org.openqa.selenium.remote.RemoteWebDriver;

public class TestNGClass 
{
  public WebDriver driver;
  public String URL, Node;
  protected ThreadLocal<RemoteWebDriver> threadDriver = null;
	
  @Parameters("browser")
  @BeforeTest
  public void launchapp(String browser) throws MalformedURLException
  {		
   String URL = "http://www.calculator.net";
   if (browser.equalsIgnoreCase("firefox")) 
   {
	 System.out.println(" Executing on FireFox");
	 String Node = "http://10.112.66.52:5555/wd/hub";
  	 DesiredCapabilities cap = DesiredCapabilities.firefox();
	 cap.setBrowserName("firefox");

	 driver = new RemoteWebDriver(new URL(Node), cap);
	 //Puts a Implicit wait, Will wait for 10 seconds before throwing exception
	 driver.manage().timeouts().implicitlyWait(10, TimeUnit.SECONDS);
		
	 //Launch website
	 driver.navigate().to(URL);	
	 driver.manage().window().maximize();		
   } 
   else if (browser.equalsIgnoreCase("chrome")) 
   {
	System.out.println(" Executing on CHROME");
    DesiredCapabilities cap = DesiredCapabilities.chrome();
	cap.setBrowserName("chrome");
	String Node = "http://10.112.66.52:5557/wd/hub";
	driver = new RemoteWebDriver(new URL(Node), cap);
	driver.manage().timeouts().implicitlyWait(10, TimeUnit.SECONDS);
		
	//Launch website
	driver.navigate().to(URL);	
	driver.manage().window().maximize();
   } 
   else if (browser.equalsIgnoreCase("ie")) 
   {
	 System.out.println(" Executing on IE");
	 DesiredCapabilities cap = DesiredCapabilities.chrome();
	 cap.setBrowserName("ie");
	 String Node = "http://10.112.66.52:5558/wd/hub";
	 driver = new RemoteWebDriver(new URL(Node), cap);
	 driver.manage().timeouts().implicitlyWait(10, TimeUnit.SECONDS);
	
	//Launch website
	driver.navigate().to(URL);	
	driver.manage().window().maximize();
   }
   else 
   {
      throw new IllegalArgumentException("The Browser Type is Undefined");
   }
 }
	 
	
  @Test
  public void calculatepercent()
  {
	driver.findElement(By.xpath(".//*[@id='menu']/div[3]/a")).click();     	
	// Click on Math Calculators  
	driver.findElement(By.xpath(".//*[@id='menu']/div[4]/div[3]/a")).click();     
	// Click on Percent Calculators
    driver.findElement(By.id("cpar1")).sendKeys("10"); 		
    // Enter value 10 in the first number of the percent Calculator
    driver.findElement(By.id("cpar2")).sendKeys("50");		
    // Enter value 50 in the second number of the percent Calculator    
    driver.findElement(By.xpath(".//*[@id='content']/table/tbody/tr/td[2]/input")).click();	    
    // Click Calculate Button
    String result = driver.findElement(By.xpath(".//*[@id='content']/p[2]/span/font/b")).getText();		    
    // Get the Result Text based on its xpath    
    System.out.println(" The Result is " + result);					
    //Print a Log In message to the screen
        
    if(result.equals("5"))
    {
    	System.out.println(" The Result is Pass");
    }
    else
    {
    	System.out.println(" The Result is Fail");
    }		    
  }
  
   @AfterTest
   public void closeBrowser() 
   {
	   driver.quit();	    
   }
}
```

步骤2：在浏览器中的参数将使用XML来传递。我们需要在项目文件夹创建相同的XML。

![selenium_ide_134](http://www.yiibai.com/uploads/allimg/140928/21191I304-14.jpg)

步骤3：从“General”中选择“File”，然后点击“Next”。

![selenium_ide_135](http://www.yiibai.com/uploads/allimg/140928/21191LY7-15.jpg)

第4步：输入文件的名称，然后单击“Finish”。

![selenium_ide_136](http://www.yiibai.com/uploads/allimg/140928/21191G230-16.jpg)

第5步：testng.xml文件是根据项目文件夹中创建如下图所示。

步骤6：XML的内容如下所示。我们创建3个测试，把它放在套件中parallel="tests"，让所有的测试并行执行。

```
<?xml version="1.0" encoding="UTF-8"?>
<!DOCTYPE suite SYSTEM "http://testng.org/testng-1.0.dtd">
<suite name="Suite" parallel="tests">
   <test name="FirefoxTest">
      <parameter name="browser" value="firefox" />
      <classes>
             <class name="TestNG.TestNGClass" />
      </classes>
   </test>

   <test name="ChromeTest">
      <parameter name="browser" value="chrome" />
      <classes>
             <class name="TestNG.TestNGClass" />
      </classes>
   </test>

   <test name="IETest">
      <parameter name="browser" value="ie" />
      <classes>
             <class name="TestNG.TestNGClass" />
      </classes>
   </test>
</suite>
```

### 测试执行

第1步：选择创建的XML并执行右键单击并选择 'Run As' >> 'TestNG Suite'

![selenium_ide_139](http://www.yiibai.com/uploads/allimg/140928/21191K5M-18.jpg)

第2步：现在打开的节点，在这里我们推出的所有浏览器节点。我们将能够同时看到所有三种浏览器中执行。

![selenium_ide_140](http://www.yiibai.com/uploads/allimg/140928/21191L049-19.jpg)

### 结果分析

步骤1：在完成执行时，我们将能够分析的结果及任何其他执行。结果汇总打印在控制台。以下是相同的快照。

![selenium_ide_142](http://www.yiibai.com/uploads/allimg/140928/21191JV2-20.jpg)

第2步：导航到选项卡和TestNG将显示结果摘要如下图所示“Results of Running Suite”。

![selenium_ide_141](http://www.yiibai.com/uploads/allimg/140928/21191J0U-21.jpg)

步骤3：当生成的HTML中，我们将能够看到HTML格式的测试结果。

![selenium_ide_143](http://www.yiibai.com/uploads/allimg/140928/21191K311-22.jpg)# Selenium页面对象模型

大家都知道，Selenium作用于webelements属性，例如ID，名称，Xpath等与QTP有一个内置的对象库(OR)，Selenium还没有NOT得到一个内置OR。

因此，我们需要建立或也应该是维护和按需访问。 Page对象模型(POM)是一种流行的设计模式，以创造一种与webelements特性中的每一个都使用一个类文件创建一个对象库。

## 优点

- 页面的对象模型是其中测试对象和功能被彼此分开，从而保持代码干净的实现。
- 对象保持独立的测试脚本。一个目的可以通过一个或多个测试脚本进行访问，因此，POM可以帮助我们创建对象一次和多次使用。
- 由于创建对象后，很容易访问和易于更新一个对象的特定属性。

## POM流程图

网页中的每一个创建对象和方法被开发专用于访问这些对象。让我们利用http://calculator.net来理解是一样的。

存在与之关联的各种计算器，并在特定的页面的那些对象中的每一个在一个单独的类文件为静态方法创建，他们都在'测试'class文件中的静态方法将被访问的对象进行访问。

![Selenium IDE 145](http://www.yiibai.com/uploads/allimg/140928/0F1352603-0.jpg)

## 示例

让我们来了解通过执行用于百分比计算器测试中实现POM 。

步骤1：创建一个包内一个简单的类(page_objects_perc_calc.java)文件，并创建这些对象标识符中的每一个方法，如下图所示。

```
package PageObject;

import org.openqa.selenium.*;
 
public class page_objects_perc_calc 
{
    private static WebElement element = null;
 
    // Math Calc Link
	public static WebElement lnk_math_calc(WebDriver driver)
	{
	     element = driver.findElement(By.xpath(".//*[@id='menu']/div[3]/a"));
	     return element;
	}
	
    // Percentage Calc Link
	public static WebElement lnk_percent_calc(WebDriver driver)
	{
	     element = driver.findElement(By.xpath(".//*[@id='menu']/div[4]/div[3]/a"));
	     return element;
	}
	
    // Number 1 Text Box
	public static WebElement txt_num_1(WebDriver driver)
	{
	     element = driver.findElement(By.id("cpar1"));
	     return element;
	}
	
    // Number 2 Text Box	
	public static WebElement txt_num_2(WebDriver driver)
	{
	     element = driver.findElement(By.id("cpar2"));
	     return element;
	}
	
    // Calculate Button	
	public static WebElement btn_calc(WebDriver driver)
	{
	     element = driver.findElement(By.xpath(".//*[@id='content']/table/tbody/tr/td[2]/input"));
	     return element;
	}	
	
    // Result	
	public static WebElement web_result(WebDriver driver)
	{
	     element = driver.findElement(By.xpath(".//*[@id='content']/p[2]/span/font/b"));
	     return element;
	}	
}
```

第2步：创建一个类主导入包，并为这些对象标识符中的每一个方法，如下图所示。

```
package PageObject;

import java.util.concurrent.TimeUnit;

import org.openqa.selenium.WebDriver;
import org.openqa.selenium.firefox.FirefoxDriver;

public class percent_calculator 
{
  private static WebDriver driver = null;
  
  public static void main(String[] args) 
  {
  	driver = new FirefoxDriver();
  	driver.manage().timeouts().implicitlyWait(10, TimeUnit.SECONDS);
  	driver.get("http://www.calculator.net");
  
  	// Use page Object library now
  	page_objects_perc_calc.lnk_math_calc(driver).click();		
  	page_objects_perc_calc.lnk_percent_calc(driver).click();
  	
  	
  	page_objects_perc_calc.txt_num_1(driver).clear();
  	page_objects_perc_calc.txt_num_1(driver).sendKeys("10");
  
  	page_objects_perc_calc.txt_num_2(driver).clear();
  	page_objects_perc_calc.txt_num_2(driver).sendKeys("50");
  
  	page_objects_perc_calc.btn_calc(driver).click();
  	
  	String result =  page_objects_perc_calc.web_result(driver).getText();		
  	
  	if(result.equals("5"))
  	{
  		System.out.println(" The Result is Pass");
  	}
  	else
  	{
  		System.out.println(" The Result is Fail");
  	}
  	
  	driver.close();
  }
}

```

## 输出

该测试被执行并且将结果打印在控制台。以下是相同的快照。

![Selenium IDE 146](http://www.yiibai.com/uploads/allimg/140928/0F1352242-1.jpg)# Summary

* [Introduction](README.md)
* [Selenium教程](Selenium教程.md)
* [Selenium概述](Selenium概述.md)
* [SeleniumIDE](SeleniumIDE.md)
* [SeleniumIDE下载](SeleniumIDE下载.md)
* [SeleniumIDE工具特点](SeleniumIDE工具特点.md)
* [SeleniumIDE测试创建](SeleniumIDE测试创建.md)
* [SeleniumIDE测试](SeleniumIDE测试.md)
* [SeleniumIDE验证点](SeleniumIDE验证点.md)
* [SeleniumIDE模式匹配](SeleniumIDE模式匹配.md)
* [Selenium用户扩展](Selenium用户扩展.md)
* [SeleniumIDE不同的浏览器](SeleniumIDE不同的浏览器.md)
* [Selenium环境安装设置](Selenium环境安装设置.md)
* [SeleniumRC](SeleniumRC.md)
* [SeleniumSelenese命令](SeleniumSelenese命令.md)
* [SeleniumWebdriver](SeleniumWebdriver.md)
* [Selenium定位器](Selenium定位器.md)
* [用户交互](用户交互.md)
* [文本框的相互作用](文本框的相互作用.md)
* [单选按钮互动](单选按钮互动.md)
* [复选框交互](复选框交互.md)
* [下拉框交互](下拉框交互.md)
* [Synchronization同步](Synchronization同步.md)
* [拖放](拖放.md)
* [键盘操作](键盘操作.md)
* [鼠标操作](鼠标操作.md)
* [多选择操作](多选择操作.md)
* [查找所有链接](查找所有链接.md)
* [Selenium测试设计技术](Selenium测试设计技术.md)
* [Selenium页面对象模型](Selenium页面对象模型.md)
* [使用Excel数据驱动](使用Excel数据驱动.md)
* [log4j日志](log4j日志.md)
* [异常处理](异常处理.md)
* [多浏览器测试](多浏览器测试.md)
* [捕捉屏幕截图](捕捉屏幕截图.md)
* [捕捉视频](捕捉视频.md)
* [SeleniumTestNG](SeleniumTestNG.md)
* [Selenium网格](Selenium网格.md)

# Synchronization同步

## 同步

要执行脚本，我们需要进行适当的操作后，等待应用程序之间的同步。来看看以达到同样的方式。

### THREAD.SLEEP

Thread.sleep代码是一个静态的等待，不是在脚本中使用，因为它是无需睡眠状态的一个很好的方法。

```
Thread.Sleep(1000);//Will wait for 1 second.
```

### 显式等待

一个明确的等待，等待某个条件进一步处理之前发生。它主要用于当我们想要点击或采取行动的对象，一旦它是可见的。

```
WebDriver driver =newFirefoxDriver();
driver.get("Enter an URL"S);WebElementDynamicElement=(newWebDriverWait(driver,10)).until(ExpectedConditions.presenceOfElementLocated(By.id("DynamicElement")));
```

### 隐式等待

隐式等待的情况下，如果网络驱动器找不到，因为它的不可用性的立即的对象。webdriver将等待指定的隐含的等待时间，也不会尝试在指定时间内找到的元素了。一旦指定的时间限制被超越，webdriver将尝试再次搜索该元素的最后一面。如果成功，将继续进行执行，但如果失败，它会抛出异常。这是一种全局的等待，这意味着这种等待是适用于整个驱动程序。因此，硬编码这种等待更长的时间时期将阻碍该脚本执行时间。

```
WebDriver driver = new FirefoxDriver();
driver.manage().timeouts().implicitlyWait(10, TimeUnit.SECONDS);
driver.get("Enter an URL");
WebElement DynamicElement = driver.findElement(By.id("DynamicElement"));
```

### 流利等待

FluentWait用于当webelement可以出现在5秒或者甚至它可以采取90秒。在这种情况下，我们定义的时间等待的状态的最大数量，以及与该查询的对象状态的是否存在等的频率。

让我们假定，我们将60秒可用一个元素在网页上，但每10秒检查一次它的存在。

```
Wait wait = new FluentWait(driver)
  .withTimeout(60, SECONDS)
  .pollingEvery(10, SECONDS)
  .ignoring(NoSuchElementException.class);
WebElement dynamicelement = wait.until(new Function<webdriver,webElement>() 
{
  public WebElement apply(WebDriver driver) 
  {
  return driver.findElement(By.id("dynamicelement"));
  }
 }
);
```
# 下拉框交互

在本节中，我们将了解如何使用下拉框进行交互。我们可以用“selectByVisibleText'或'selectByIndex'或'selectByValue'的方法选择一个选项。

让我们明白，如何使用交互复选框 - http://www.calculator.net/interest-calculator.htmll。我们还可以检查下拉框中选择/启用/可见。

![selenium_ide_182](http://www.yiibai.com/uploads/allimg/140927/21103510E-0.jpg)

```
import java.util.concurrent.TimeUnit;

import org.openqa.selenium.*;
import org.openqa.selenium.firefox.FirefoxDriver;
import org.openqa.selenium.support.ui.Select;

public class webdriverdemo
{
  public static void main(String[] args) throws InterruptedException
  {
	WebDriver driver = new FirefoxDriver();

	//Puts a Implicit wait, Will wait for 10 seconds before throwing exception
	driver.manage().timeouts().implicitlyWait(10, TimeUnit.SECONDS);


	//Launch website
	driver.navigate().to("http://www.calculator.net/interest-calculator.htmll");
	driver.manage().window().maximize();
	 
    // Selecting an item from Drop Down list Box
	Select dropdown = new Select(driver.findElement(By.id("ccompound")));
	dropdown.selectByVisibleText("continuously");
	
	//  you can also use dropdown.selectByIndex(1) to select second element as index starts with 0.
	//  You can also use dropdown.selectByValue("annually");    
        
    System.out.println("The Output of the IsSelected " + driver.findElement(By.id("ccompound")).isSelected());
    System.out.println("The Output of the IsEnabled " + driver.findElement(By.id("ccompound")).isEnabled());
    System.out.println("The Output of the IsDisplayed " + driver.findElement(By.id("ccompound")).isDisplayed());
    
    driver.close(); 
 
   }
}

```

## 输出

在执行时，向下设置与指定的值与命令的输出下拉显示在控制台中。

![selenium_ide_184](http://www.yiibai.com/uploads/allimg/140927/211035J22-1.jpg)# 使用Excel数据驱动

在设计测试，参数化测试是不可避免的。我们会利用Apache的POI- Excel JAR实现是一样的。它可以帮助我们来读取和写入到Excel中。

## 下载JAR

**第1步：**导航到URL- http://poi.apache.org/download.htmll并下载ZIP格式。

![selenium_ide_152](http://www.yiibai.com/uploads/allimg/140928/0F41RY5-0.jpg)

**第2步：**点击镜像链接下载JAR。

![selenium_ide_153](http://www.yiibai.com/uploads/allimg/140928/0F41U219-1.jpg)

**第3步：**解压缩到一个文件夹。

![selenium_ide_154](http://www.yiibai.com/uploads/allimg/140928/0F41V5J-2.jpg)

**第4步：**如下所示的解压缩后的内容将被显示。

![selenium_ide_155](http://www.yiibai.com/uploads/allimg/140928/0F41WF5-3.jpg)

**第5步：**现在创建一个新的项目，并在“External JARs”添加“POI-3.10.FINAL”文件夹中所有的jar包。

![selenium_ide_147](http://www.yiibai.com/uploads/allimg/140928/0F41W442-4.jpg)

**第6步：**现在，添加所有的“External JARs”在“OOXML-LIB”文件夹中。

![selenium_ide_148](http://www.yiibai.com/uploads/allimg/140928/0F41VM4-5.jpg)

**第7步：**现在，添加所有的“External JARs”在“lib”文件夹中。

![selenium_ide_149](http://www.yiibai.com/uploads/allimg/140928/0F41UY3-6.jpg)

**第8步：**如下图所示，显示已添加的JAR文件。

![selenium_ide_150](http://www.yiibai.com/uploads/allimg/140928/0F41TW9-7.jpg)

**第9步：**如下图所示的Package Explorer显示。此外附加“webdriver”相关的JAR

![selenium_ide_151](http://www.yiibai.com/uploads/allimg/140928/0F41R115-8.jpg)

## 参数

为了演示目的，我们将参数的百分比计算器测试。

**第1步：**我们将所有的参数需要使用Excel的％计算器的输入。所设计的excel如下所示。

![selenium_ide_156](http://www.yiibai.com/uploads/allimg/140928/0F41V238-9.jpg)

**第2步：**现在，我们将执行所有百分比计算器，所有指定的参数。

**第3步：**让我们创建通用的方法来访问使用导入JARS Excel文件。这些方法可以帮助我们获得一个特定的单元格数据或设置一个特定的单元格的数据等。

```
import java.io.*;
import org.apache.poi.xssf.usermodel.*;
    
public class excelutils 
{
   private XSSFSheet ExcelWSheet;
   private XSSFWorkbook ExcelWBook;

   //Constructor to connect to the Excel with sheetname and Path
   public excelutils(String Path, String SheetName) throws Exception 
   {
	  try 
	  {
	    // Open the Excel file
	    FileInputStream ExcelFile = new FileInputStream(Path);
	    // Access the required test data sheet
	    ExcelWBook = new XSSFWorkbook(ExcelFile);
	    ExcelWSheet = ExcelWBook.getSheet(SheetName);    
	  } 
	  catch (Exception e)
	  {
	    throw (e);           
	  }
   }
              
    //This method is to set the rowcount of the excel.
    public int excel_get_rows() throws Exception 
    {
	  try 
	  {
	     return ExcelWSheet.getPhysicalNumberOfRows();           
	  } 
	  catch (Exception e)
	  {
	  	throw (e);
         
	  }
    }
        

    //This method to get the data and get the value as strings.
    public String getCellDataasstring(int RowNum, int ColNum) throws Exception
    {
	   try
	   {
		   String CellData = ExcelWSheet.getRow(RowNum).getCell(ColNum).getStringCellValue();
		   System.out.println("The value of CellData " + CellData);
		   return CellData;
	   }
	   catch (Exception e)
	   {
	   	 return "Errors in Getting Cell Data";
	   }
    }
    
 
  //This method to get the data and get the value as number.
    public double getCellDataasnumber(int RowNum, int ColNum) throws Exception
    {
	   try
	   {
		  double CellData = ExcelWSheet.getRow(RowNum).getCell(ColNum).getNumericCellValue();
		  System.out.println("The value of CellData " + CellData);
		  return CellData;
		}
		catch (Exception e)
		{
			return 000.00;
		}
    }
}

```

**第4步：**现在，添加它将访问，我们已经开发了Excel的方法，主要的方法。

```
import java.io.*;
import org.apache.poi.xssf.usermodel.*;
    
public class excelutils 
{
   private XSSFSheet ExcelWSheet;
   private XSSFWorkbook ExcelWBook;

   //Constructor to connect to the Excel with sheetname and Path
   public excelutils(String Path, String SheetName) throws Exception 
   {
	  try 
	  {
		 // Open the Excel file
		 FileInputStream ExcelFile = new FileInputStream(Path);
		 // Access the required test data sheet
		 ExcelWBook = new XSSFWorkbook(ExcelFile);
		 ExcelWSheet = ExcelWBook.getSheet(SheetName);    
	
	   } 
	   catch (Exception e)
	   {
		   throw (e);           
	   }
   }
              
    //This method is to set the rowcount of the excel.
    public int excel_get_rows() throws Exception 
    {
	   try 
	   {
		   return ExcelWSheet.getPhysicalNumberOfRows();           
		} 
		catch (Exception e)
		{
			throw (e);
		
		}
    }
      

    //This method to get the data and get the value as strings.
    public String getCellDataasstring(int RowNum, int ColNum) throws Exception
    {
	   try
	   {
		   String CellData = ExcelWSheet.getRow(RowNum).getCell(ColNum).getStringCellValue();
		  //Cell = ExcelWSheet.getRow(RowNum).getCell(ColNum);
		  //String CellData = Cell.getStringCellValue();
		  System.out.println("The value of CellData " + CellData);
		  return CellData;
		}
		catch (Exception e)
		{
			return "Errors in Getting Cell Data";
		}
    }
    
   //This method to get the data and get the value as number.
    public double getCellDataasnumber(int RowNum, int ColNum) throws Exception
    {
	   try
	   {
		   double CellData = ExcelWSheet.getRow(RowNum).getCell(ColNum).getNumericCellValue();
		  //Cell = ExcelWSheet.getRow(RowNum).getCell(ColNum);
		  //String CellData = Cell.getStringCellValue();
		  System.out.println("The value of CellData " + CellData);
		  return CellData;
		}
		catch (Exception e)
		{
			return 000.00;
		}
    }    
}

```

## 输出

在执行脚本，输出显示在控制台中，如下图所示。

![Selenium IDE 157](http://www.yiibai.com/uploads/allimg/140928/0F41T092-10.jpg)# 单选按钮互动

在本节中，我们将了解如何使用单选按钮交互。我们可以使用“click”方法，并取消选择使用相同的“click”方法选择一个单选按钮的选项。

让我们明白，如何使用单选按钮交互- http://www.calculator.net/mortgage-payoff-calculator.htmll。我们还可以检查是否选择或使能的单选按钮。

![selenium_ide_178](http://www.yiibai.com/uploads/allimg/140927/21041GF4-0.jpg)

```
import java.util.concurrent.TimeUnit;
import org.openqa.selenium.*;
import org.openqa.selenium.firefox.FirefoxDriver;

public class webdriverdemo
{
  public static void main(String[] args) throws InterruptedException
  {
	WebDriver driver = new FirefoxDriver();

    //Puts a Implicit wait, Will wait for 10 seconds before throwing exception
	driver.manage().timeouts().implicitlyWait(10, TimeUnit.SECONDS);

	 
	 //Launch website
	 driver.navigate().to("http://www.calculator.net/mortgage-payoff-calculator.htmll");
	 driver.manage().window().maximize();
	 
	 // Click on Radio Button
	 driver.findElement(By.id("cpayoff1")).click();
	 
	 System.out.println("The Output of the IsSelected " + driver.findElement(By.id("cpayoff1")).isSelected());
	 System.out.println("The Output of the IsEnabled " + driver.findElement(By.id("cpayoff1")).isEnabled());
	 System.out.println("The Output of the IsDisplayed " + driver.findElement(By.id("cpayoff1")).isDisplayed());

	 driver.close(); 
    
	//Close the Browser.
    driver.close();    
  }
}

```

## 输出

在执行时，被选中的单选按钮和命令的输出显示在控制台中。

![selenium_ide_179](http://www.yiibai.com/uploads/allimg/140927/21041J0K-1.jpg)# 复选框交互

在本节中，我们将了解如何与交互复选框。我们可以使用“click”方法选择入住按钮选项，然后取消选择使用相同的“click”方法。

让我们明白，如何使用交互复选框 - http://www.calculator.net/mortgage-calculator.htmll。我们还可以检查是否选择/启用/可见光的复选框。

![selenium_ide_180](http://www.yiibai.com/uploads/allimg/140927/210H362T-0.jpg)

```
import java.util.concurrent.TimeUnit;
import org.openqa.selenium.*;
import org.openqa.selenium.firefox.FirefoxDriver;

public class webdriverdemo
{
  public static void main(String[] args) throws InterruptedException
  {
	WebDriver driver = new FirefoxDriver();

	//Puts a Implicit wait, Will wait for 10 seconds before throwing exception
	driver.manage().timeouts().implicitlyWait(10, TimeUnit.SECONDS);


	//Launch website
	driver.navigate().to("http://www.calculator.net/mortgage-calculator.htmll");
	driver.manage().window().maximize();
	 
    // Click on check Box
    driver.findElement(By.id("caddoptional")).click();
    
    System.out.println("The Output of the IsSelected " + driver.findElement(By.id("caddoptional")).isSelected());
    System.out.println("The Output of the IsEnabled " + driver.findElement(By.id("caddoptional")).isEnabled());
    System.out.println("The Output of the IsDisplayed " + driver.findElement(By.id("caddoptional")).isDisplayed());
    
    driver.close(); 
 
   }
} 
```

## 输出

在执行时，该复选框被点击命令后，选中(因为它是默认选中)和命令的输出显示在控制台中。

![selenium_ide_181](http://www.yiibai.com/uploads/allimg/140927/210H33556-1.jpg)# 多浏览器测试

用户可以同时执行多个浏览器中的脚本。为了演示，我们将充分利用我们已经采取了Selenium 网格相同的场景。Selenium 网格的例子，我们已经在远程执行脚本，在这里将在本地执行脚本。

即使对于这一点，我们必须确保我们有适当的驱动程序下载。请参考Selenium 网格章下载IE和Chrome浏览器的驱动程序。

## 示例

我们将在所有浏览器中同时执行％的计算用于演示目的。

```
package TestNG;

import org.openqa.selenium.chrome.ChromeDriver;
import org.openqa.selenium.firefox.FirefoxDriver;
import org.openqa.selenium.ie.InternetExplorerDriver;
import java.util.concurrent.TimeUnit;
import org.openqa.selenium.*;
import org.testng.annotations.*;


public class TestNGClass 
{
  private WebDriver driver;
  private String URL = "http://www.calculator.net";
	
  @Parameters("browser")
  @BeforeTest
  public void launchapp(String browser) 
  {		
      
   if (browser.equalsIgnoreCase("firefox")) 
   {
	 System.out.println(" Executing on FireFox");
	 driver = new FirefoxDriver();
	 driver.get(URL);
	 driver.manage().timeouts().implicitlyWait(10, TimeUnit.SECONDS);
	 driver.manage().window().maximize();		
   } 
   else if (browser.equalsIgnoreCase("chrome")) 
   {
	System.out.println(" Executing on CHROME");
	 System.out.println("Executing on IE");
	 System.setProperty("webdriver.chrome.driver", "D:chromedriver.exe");
	 driver = new ChromeDriver();
	 driver.get(URL);
	 driver.manage().timeouts().implicitlyWait(10, TimeUnit.SECONDS);
	 driver.manage().window().maximize();	
   } 
   else if (browser.equalsIgnoreCase("ie")) 
   {
	 System.out.println("Executing on IE");
	 System.setProperty("webdriver.ie.driver", "D:IEDriverServer.exe");
	 driver = new InternetExplorerDriver();
	 driver.get(URL);
	 driver.manage().timeouts().implicitlyWait(10, TimeUnit.SECONDS);
	 driver.manage().window().maximize();		
   }
   else 
   {
      throw new IllegalArgumentException("The Browser Type is Undefined");
   }
 }
	 
	
  @Test
  public void calculatepercent()
  {
	driver.findElement(By.xpath(".//*[@id='menu']/div[3]/a")).click();     	
	// Click on Math Calculators  
	driver.findElement(By.xpath(".//*[@id='menu']/div[4]/div[3]/a")).click();     
	// Click on Percent Calculators
    driver.findElement(By.id("cpar1")).sendKeys("10"); 		
    // Enter value 10 in the first number of the percent Calculator
    driver.findElement(By.id("cpar2")).sendKeys("50");		
    // Enter value 50 in the second number of the percent Calculator    
    driver.findElement(By.xpath(".//*[@id='content']/table/tbody/tr/td[2]/input")).click();	    
    // Click Calculate Button
    String result = driver.findElement(By.xpath(".//*[@id='content']/p[2]/span/font/b")).getText();		    
    // Get the Result Text based on its xpath    
    System.out.println(" The Result is " + result);					
    //Print a Log In message to the screen
        
    if(result.equals("5"))
    {
    	System.out.println(" The Result is Pass");
    }
    else
    {
    	System.out.println(" The Result is Fail");
    }		    
  }
  
   @AfterTest
   public void closeBrowser() 
   {
	   driver.close();	    
   }
}
```

创建一个XML这将有助于我们在参数设置浏览器的名字，不要忘记提及 parallel="tests"为了同时在所有浏览器中执行。

![selenium_ide_169](http://www.yiibai.com/uploads/allimg/140928/19195I014-0.jpg)

通过对XML文件进行右键点击执行脚本，然后选择 'Run As' >> 'TestNG' 方式，如下图所示。

![selenium_ide_139](http://www.yiibai.com/uploads/allimg/140928/19195MU2-1.jpg)

## 输出

所有的浏览器将平行展开，结果将被打印在控制台上。

注：对于我们在IE浏览器执行成功确保复选框“启用保护模式”下的“IE选项中的安全选项卡中选中或未在所有区域中未检查。

![selenium_ide_170](http://www.yiibai.com/uploads/allimg/140928/19195MI2-2.jpg)

TestNG的结果以HTML格式来查看详细的分析。

![selenium_ide_171](http://www.yiibai.com/uploads/allimg/140928/19195G0S-3.jpg)# 多选择操作

有时，我们会在一个情况来选择列表框或文本区域中两个或多个项目。要理解一样，我们会demostrate多个选择从列表中使用“http://demos.devexpress.com/aspxeditorsdemos/ListEditors/MultiSelect.aspx”。

## 例子

我们要从该列表中选择3个项目，如下图所示：

![selenium_ide_187](http://www.yiibai.com/uploads/allimg/140927/2133016040-0.jpg)

```
import java.util.List;
import java.util.concurrent.TimeUnit;

import org.openqa.selenium.*;
import org.openqa.selenium.firefox.FirefoxDriver;
import org.openqa.selenium.interactions.Actions;
import org.openqa.selenium.interactions.Action;

public class webdriverdemo
{
  public static void main(String[] args) throws InterruptedException
  {
	WebDriver driver = new FirefoxDriver();

	driver.manage().timeouts().implicitlyWait(10, TimeUnit.SECONDS);

	driver.navigate().to("http://demos.devexpress.com/aspxeditorsdemos/ListEditors/MultiSelect.aspx");
	//driver.manage().window().maximize();
	
	driver.findElement(By.id("ContentHolder_lbSelectionMode_I")).click();
	driver.findElement(By.id("ContentHolder_lbSelectionMode_DDD_L_LBI1T0")).click();
	
	Thread.sleep(5000);
		
	//  Perform Multiple Select 
	Actions builder = new Actions(driver);
	WebElement select = driver.findElement(By.id("ContentHolder_lbFeatures_LBT"));
	List<WebElement> options = select.findElements(By.tagName("td"));
	System.out.println(options.size());
	Action multipleSelect = builder.keyDown(Keys.CONTROL)
		.click(options.get(2))
		.click(options.get(4))
		.click(options.get(6))
		.build();
	multipleSelect.perform();

	driver.close(); 
 
   }
}
```

## 输出

当执行脚本，如上面显示的项目将被选中，在列表框的大小也将被打印在控制台上。

![selenium_ide_188](http://www.yiibai.com/uploads/allimg/140927/2133013607-1.jpg)# 异常处理

当我们正在开发测试中，我们要确保，即使测试失败的脚本可以继续执行。如果最坏的情况都处理不好意外的异常会被抛出。

如果发生异常，由于无法找到元素，或者预期的结果不与实际值相符，我们应该抓住这个异常并结束测试的逻辑方式，以防脚本本身突然终止。

## 语法

实际的代码应该放在try块和异常后的动作应该放在catch块。请注意：“finally'块就算没有问题，不管脚本是否已经被抛出的异常都会执行。

```
try
{
   //Perform Action
}
catch(ExceptionType1 exp1)
{
   //Catch block 1
}
catch(ExceptionType2 exp2)
{
   //Catch block 2
}
catch(ExceptionType3 exp3)
{
   //Catch block 3
}
finally
{
   //The finally block always executes.
}
```

## 示例

如果没有找到(因为任何好的理由)元素，我们应该确保走出的功能顺利。所以，总是需要有try-catch块，如果想要的跟做的是一样的。

```
public static WebElement lnk_percent_calc(WebDriver driver)throws Exception
{
  try
  {
    element = driver.findElement(By.xpath(".//*[@id='menu']/div[4]/div[3]/a"));
    return element;
  }
  catch (Exception e1)
  {
    // Add a message to your Log File to capture the error
      Logger.error("Link is not found.");
    
    // Take a screenshot which will be helpful for analysis.
    File screenshot = ((TakesScreenshot)driver).getScreenshotAs(OutputType.FILE);
	FileUtils.copyFile(screenshot, new File("D:frameworkscreenshots.jpg"));	
    
    throw(e1);
  }
}
```

# 拖放

作为一名测试人员，我们会在一个情况来执行“拖放”操作。我们将执行一拖拿起一棵树网格，可用于我们http://www.keenthemes.com/preview/metronic/templates/admin/ui_tree.htmll拖放操作。在下面的例子中，我们想拖动一个元素“禁用节点”从“最初打开”文件夹“父节点”文件夹。

![selenium_ide_185](http://www.yiibai.com/uploads/allimg/140927/21231I000-0.jpg)

```
import java.util.concurrent.TimeUnit;
import org.openqa.selenium.*;
import org.openqa.selenium.firefox.FirefoxDriver;
import org.openqa.selenium.interactions.Actions;
import org.openqa.selenium.interactions.Action;

public class webdriverdemo
{
  public static void main(String[] args) throws InterruptedException
  {
	WebDriver driver = new FirefoxDriver();

	//Puts a Implicit wait, Will wait for 10 seconds before throwing exception
	driver.manage().timeouts().implicitlyWait(10, TimeUnit.SECONDS);

	//Launch website
	driver.navigate().to("http://www.keenthemes.com/preview/metronic/templates/admin/ui_tree.htmll");
	driver.manage().window().maximize();
	 
 	WebElement From = driver.findElement(By.xpath(".//*[@id='j3_7']/a"));
	WebElement To = driver.findElement(By.xpath(".//*[@id='j3_1']/a"));
	Actions builder = new Actions(driver);
	Action dragAndDrop = builder.clickAndHold(From)
			.moveToElement(To)
			.release(To)
			.build();
	dragAndDrop.perform();
	
	driver.close(); 
 
   }
}
```

## 输出

执行拖放操作的输出之后将在下面，如图所示。

![selenium_ide_186](http://www.yiibai.com/uploads/allimg/140927/21231HC4-1.jpg)# 捕捉屏幕截图

截图捕获功能可以帮助我们在需要在运行时抓取截图，在特别是当故障发生。随着截图的帮助和日志信息，我们将能够更好地分析结果

截图是本地执行和Selenium 网格(远程)处决配置不同。让我们来看看他们每一个例子

## 本地主机执行

在下面的例子中，我们将计算百分比之后的截图。请确保给一个有效的路径，用以保存屏幕截图。

```
import java.io.File;
import java.io.IOException;
import java.util.concurrent.TimeUnit;

import org.apache.commons.io.FileUtils;
import org.openqa.selenium.*;
import org.openqa.selenium.firefox.FirefoxDriver;

public class webdriverdemo
{
  public static void main(String[] args) throws IOException
  {
	WebDriver driver = new FirefoxDriver();

    //Puts a Implicit wait, Will wait for 10 seconds before throwing exception
	driver.manage().timeouts().implicitlyWait(10, TimeUnit.SECONDS);

    //Launch website
	driver.navigate().to("http://www.calculator.net/");
	
	//Maximize the browser
	driver.manage().window().maximize();

    // Click on Math Calculators
	driver.findElement(By.xpath(".//*[@id='menu']/div[3]/a")).click();
  
    // Click on Percent Calculators
	driver.findElement(By.xpath(".//*[@id='menu']/div[4]/div[3]/a")).click();

	// Enter value 10 in the first number of the percent Calculator
    driver.findElement(By.id("cpar1")).sendKeys("10");

    // Enter value 50 in the second number of the percent Calculator
    driver.findElement(By.id("cpar2")).sendKeys("50");
    
    // Click Calculate Button
    driver.findElement(By.xpath(".//*[@id='content']/table/tbody/tr/td[2]/input")).click();

    // Get the Result Text based on its xpath
    String result = driver.findElement(By.xpath(".//*[@id='content']/p[2]/span/font/b")).getText();
    
    File screenshot = ((TakesScreenshot)driver).getScreenshotAs(OutputType.FILE);
	
	FileUtils.copyFile(screenshot, new File("D:screenshotsscreenshots1.jpg"));	
	
	//Print a Log In message to the screen
    System.out.println(" The Result is " + result);
    
	//Close the Browser.
    driver.close();    
  }
}

```

### 输出

在执行这个脚本，截图保存在“D:screenshots”文件夹中名为'screenshots1.jpg“，如下图所示。

## Selenium网格- 捕捉屏幕截图

当Selenium网格工作，我们应该确保从远程系统采取正确的截图。我们将充分利用增强的驱动程序。

## 例子

我们将连接到集线器Firefox的节点上执行该脚本。更多关于配置集线器和节点，请参阅Selenium网格章节。

```
package TestNG;

import org.openqa.selenium.remote.Augmenter;
import org.openqa.selenium.remote.DesiredCapabilities;
import org.openqa.selenium.TakesScreenshot;
import java.util.concurrent.TimeUnit;
import org.openqa.selenium.*;
import org.testng.annotations.AfterTest;
import org.testng.annotations.BeforeTest;
import org.testng.annotations.Parameters;
import org.testng.annotations.Test;
import java.io.File;
import java.net.URL;
import java.net.MalformedURLException;
import org.apache.commons.io.FileUtils;
import org.openqa.selenium.remote.RemoteWebDriver;
import java.io.IOException;

public class TestNGClass 
{
  public WebDriver driver;
  public String URL, Node;
  protected ThreadLocal<RemoteWebDriver> threadDriver = null;
	
  @Parameters("browser")
  @BeforeTest
  public void launchapp(String browser) throws MalformedURLException
  {		
   String URL = "http://www.calculator.net";
   if (browser.equalsIgnoreCase("firefox")) 
   {
	 System.out.println(" Executing on FireFox");
	 String Node = "http://10.112.66.52:5555/wd/hub";
  	 DesiredCapabilities cap = DesiredCapabilities.firefox();
	 cap.setBrowserName("firefox");

	 driver = new RemoteWebDriver(new URL(Node), cap);
	 //Puts a Implicit wait, Will wait for 10 seconds before throwing exception
	 driver.manage().timeouts().implicitlyWait(10, TimeUnit.SECONDS);
		
	 //Launch website
	 driver.navigate().to(URL);	
	 driver.manage().window().maximize();		
   } 
    else 
   {
      throw new IllegalArgumentException("The Browser Type is Undefined");
   }
 }
	 
	
  @Test
  public void calculatepercent() throws IOException
  {
	driver.findElement(By.xpath(".//*[@id='menu']/div[3]/a")).click();     	
	// Click on Math Calculators  
	driver.findElement(By.xpath(".//*[@id='menu']/div[4]/div[3]/a")).click();     
	// Click on Percent Calculators
	
	// Make use of augmented Driver to capture Screenshots.
	WebDriver augmentedDriver = new Augmenter().augment(driver);
    File screenshot = ((TakesScreenshot)augmentedDriver).getScreenshotAs(OutputType.FILE);
    FileUtils.copyFile(screenshot, new File("D:screenshots
emotescreenshot1.jpg"));
	
	// Please note - Screenshot would be saved on the system where the script is executed and NOT on remote machine.
		
    driver.findElement(By.id("cpar1")).sendKeys("10"); 		
    // Enter value 10 in the first number of the percent Calculator
    driver.findElement(By.id("cpar2")).sendKeys("50");		
    // Enter value 50 in the second number of the percent Calculator    
    driver.findElement(By.xpath(".//*[@id='content']/table/tbody/tr/td[2]/input")).click();	    
    // Click Calculate Button
    String result = driver.findElement(By.xpath(".//*[@id='content']/p[2]/span/font/b")).getText();		    
    // Get the Result Text based on its xpath    
    System.out.println(" The Result is " + result);					
    //Print a Log In message to the screen
        
    if(result.equals("5"))
    {
    	System.out.println(" The Result is Pass");
    }
    else
    {
    	System.out.println(" The Result is Fail");
    }		    
  }
  
   @AfterTest
   public void closeBrowser() 
   {
	   driver.quit();	    
   }
}
```

### 输出

当执行该脚本，截图被捕获并储存在指定的位置，如下所示。

![selenium_ide_173](http://www.yiibai.com/uploads/allimg/140928/19354V1E-1.jpg)# 捕捉视频

有时候我们未必能够分析故障只需用日志文件或截图的帮助。有时捕获完整的执行视频帮助。让我们了解如何捕捉视频。

我们将利用Monte媒体库的执行相同。

## 配置

第1步：导航到URL - http://www.randelshofer.ch/monte/index.htmll和下载屏幕记录JAR，如下图所示。

![selenium_ide_174](http://www.yiibai.com/uploads/allimg/140928/201Q13325-0.jpg)

第2步：下载后，添加JAR文件添加到当前项目的库。

![selenium_ide_175](http://www.yiibai.com/uploads/allimg/140928/201Q14T9-1.jpg)

第3步：我们会利用Java的AWT包来初始化显卡配置。

```
GraphicsConfiguration gc =GraphicsEnvironment.getLocalGraphicsEnvironment().getDefaultScreenDevice().getDefaultConfiguration();
```

第4步：它采用下列参数创建ScreenRecorder的一个实例。

| 参数           | 描述                    |
| ------------ | --------------------- |
| 显卡配置         | 提供了有关显示画面，例如大小和分辨率信息。 |
| 视频压缩格式       | 电影与帧/秒的数字输出格式（AVI）。   |
| 鼠标光标和刷新速率的颜色 | 指定的鼠标光标的颜色和刷新速率       |
| 音频格式         | 如果'NULL'音频不会被记录。      |

## 示例

我们将捕获简单的测试执行视频 - 百分比计算。

```
import java.io.File;
import java.io.IOException;
import java.util.concurrent.TimeUnit;
import org.apache.commons.io.FileUtils;
import org.openqa.selenium.*;
import org.openqa.selenium.firefox.FirefoxDriver;
import org.openqa.selenium.WebDriver;
import org.openqa.selenium.By;
import org.monte.media.math.Rational;
import org.monte.media.Format;
import org.monte.screenrecorder.ScreenRecorder;
import static org.monte.media.AudioFormatKeys.*;
import static org.monte.media.VideoFormatKeys.*;
import java.awt.*;

public class webdriverdemo
{
  private static ScreenRecorder screenRecorder;
  public static void main(String[] args) throws IOException, AWTException
  {
	  GraphicsConfiguration gconfig = GraphicsEnvironment
			  .getLocalGraphicsEnvironment()
			  .getDefaultScreenDevice()
			  .getDefaultConfiguration();
	  
	  screenRecorder = new ScreenRecorder(gconfig,
			  new Format(MediaTypeKey, MediaType.FILE, MimeTypeKey,
			  MIME_AVI),
			  new Format(MediaTypeKey, MediaType.VIDEO, EncodingKey,
			  ENCODING_AVI_TECHSMITH_SCREEN_CAPTURE,
			  CompressorNameKey, ENCODING_AVI_TECHSMITH_SCREEN_CAPTURE,
			  DepthKey, (int)24, FrameRateKey, Rational.valueOf(15),
			  QualityKey, 1.0f,
			  KeyFrameIntervalKey, (int) (15 * 60)),
			  new Format(MediaTypeKey, MediaType.VIDEO,
			  EncodingKey,"black",
			  FrameRateKey, Rational.valueOf(30)), null);
	
	WebDriver driver = new FirefoxDriver();
	
    // Start Capturing the Video
	screenRecorder.start();
	
    //Puts a Implicit wait, Will wait for 10 seconds before throwing exception
	driver.manage().timeouts().implicitlyWait(10, TimeUnit.SECONDS);

    //Launch website
	driver.navigate().to("http://www.calculator.net/");
	
	//Maximize the browser
	driver.manage().window().maximize();

    // Click on Math Calculators
	driver.findElement(By.xpath(".//*[@id='menu']/div[3]/a")).click();
  
    // Click on Percent Calculators
	driver.findElement(By.xpath(".//*[@id='menu']/div[4]/div[3]/a")).click();

	// Enter value 10 in the first number of the percent Calculator
    driver.findElement(By.id("cpar1")).sendKeys("10");

    // Enter value 50 in the second number of the percent Calculator
    driver.findElement(By.id("cpar2")).sendKeys("50");
    
    // Click Calculate Button
    driver.findElement(By.xpath(".//*[@id='content']/table/tbody/tr/td[2]/input")).click();

    // Get the Result Text based on its xpath
    String result = driver.findElement(By.xpath(".//*[@id='content']/p[2]/span/font/b")).getText();
    
    File screenshot = ((TakesScreenshot)driver).getScreenshotAs(OutputType.FILE);
	
	FileUtils.copyFile(screenshot, new File("D:screenshotsscreenshots1.jpg"));	
	
	//Print a Log In message to the screen
    System.out.println(" The Result is " + result);
    
	//Close the Browser.
    driver.close(); 
    
    // Stop the ScreenRecorder
    screenRecorder.stop();
  }
}
```

## 输出

录制的视频保存在“C:users<<UserName>>Videos”文件夹，如下图所示。

![selenium_ide_176](http://www.yiibai.com/uploads/allimg/140928/201Q1EW-2.jpg)

# 文本框的相互作用

在本节中，我们将了解如何使用文本框交互。我们可以把值转换成文本框中使用“SendKeys”方法，也使用getattribute("value")指令得到的文本文字。现在让我们来看看一个例子。

![selenium_ide_177](http://www.yiibai.com/uploads/allimg/140927/192A06402-0.jpg)

```
import java.util.concurrent.TimeUnit;
import org.openqa.selenium.*;
import org.openqa.selenium.firefox.FirefoxDriver;

public class webdriverdemo
{
  public static void main(String[] args) throws InterruptedException
  {
	WebDriver driver = new FirefoxDriver();

    //Puts a Implicit wait, Will wait for 10 seconds before throwing exception
	driver.manage().timeouts().implicitlyWait(10, TimeUnit.SECONDS);

    //Launch website
	driver.navigate().to("http://www.calculator.net/percent-calculator.htmll");
	
	//Maximize the browser
	driver.manage().window().maximize();

   	// Enter value 10 in the first number of the percent Calculator
    driver.findElement(By.id("cpar1")).sendKeys("10");
    
    Thread.sleep(5000);
	
    // Get the text box from the application
    String result = driver.findElement(By.id("cpar1")).getAttribute("value");
    
	//Print a Log In message to the screen
    System.out.println(" The Result is " + result);
    
	//Close the Browser.
    driver.close();    
  }
}

```

## 输出

显示上面的脚本的输出如下所示。

![selenium_ide_183](http://www.yiibai.com/uploads/allimg/140927/192A04149-1.jpg)

文本框的相互作用# 查找所有链接

*测试人员可能是在一个情况到grep网站上所有的链接。我们可以通过寻找与标记名称的所有元素就很容易到到“a”，因为我们知道，在HTML中任何一个环节的参考，我们需要使用“a”(锚)标签。*

## *示例*

```
import org.openqa.selenium.*;
import org.openqa.selenium.firefox.FirefoxDriver;
public class getalllinks
{
  public static void main(String[] args)
  {
	WebDriver driver = new FirefoxDriver();
	driver.navigate().to("http://www.calculator.net");
	java.util.List<WebElement> links = driver.findElements(By.tagName("a"));
	System.out.println("Number of Links in the Page is " + links.size());
	for (int i = 1; i<=links.size(); i=i+1)
	{
	  System.out.println("Name of Link# " + i - + links.get(i).getText());
	}    
  }
}
```

## *输出*

*该脚本的输出将会抛出到控制台，如下图所示。虽然有65个链接部分输出如下所示。*

![Selenium IDE 91](http://www.yiibai.com/uploads/allimg/140927/21353R559-0.jpg)# 用户交互

# 键盘操作

有时，我们会在一个情况输入一些组合键。例如：  按Ctrl键或Shift键。下面是用键盘操作交互的方法。

- sendKeys - 发送键，在浏览器的键盘表示。特殊键都没有文字，表示按键都为字符，或单独序列的一部分的认可。
- pressKey - 按键盘上不是文字的按键。键等功能键“F1”，“F2”或“Tab”或“Control”等，如果keyToPress是一个字符序列，不同的驱动程序实现可以选择抛出一个异常，或者在序列中读取的第一个字符。
- releaseKey - 执行按键事件后松开键盘上的一个键。它通常是拥有良好的非文本字符。

下面是语法来调用使用selenium webdriver的键盘功能。

```
void sendKeys(java.lang.CharSequence keysToSend)
void pressKey(java.lang.CharSequence keyToPress)
void releaseKey(java.lang.CharSequence keyToRelease)
```# 鼠标操作

有时，我们会在一个情况来执行一些复杂的鼠标事件，如双击，右键单击，将鼠标悬停在等下面是一些关键的鼠标操作，一个会在大多数应用程序碰到的。

- Click - 进行点击。我们还可以执行基于坐标的点击。
- contextClick - 执行上下文点击/右键单击一个元素或基于坐标
- doubleClick - 执行双击webelement或基于坐标。如果留空它执行双击当前位置。
- mouseDown - 执行一个元素上按下鼠标操作或基于坐标。
- mouseMove - 执行元素上的鼠标移动操作或基于坐标。
- mouseUp - 释放鼠标通常伴随着鼠标按下的动作和行为的基础上统筹。

```
void click(WebElement onElement)
void contextClick(WebElement onElement)
void doubleClick(WebElement onElement)
void mouseDown(WebElement onElement)
void mouseUp(WebElement onElement)
void mouseMove(WebElement toElement)
void mouseMove(WebElement toElement, long xOffset, long yOffset)
```