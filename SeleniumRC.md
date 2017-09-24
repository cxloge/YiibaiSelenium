# SeleniumRC

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

![Selenium IDE 74](http://www.yiibai.com/uploads/allimg/140926/1-1409260646062B.jpg)