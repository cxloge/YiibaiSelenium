# Selenium网格

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

![selenium_ide_143](http://www.yiibai.com/uploads/allimg/140928/21191K311-22.jpg)