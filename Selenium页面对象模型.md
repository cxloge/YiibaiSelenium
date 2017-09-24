# Selenium页面对象模型

大家都知道，Selenium作用于webelements属性，例如ID，名称，Xpath等与QTP有一个内置的对象库(OR)，Selenium还没有NOT得到一个内置OR。

因此，我们需要建立或也应该是维护和按需访问。 Page对象模型(POM)是一种流行的设计模式，以创造一种与webelements特性中的每一个都使用一个类文件创建一个对象库。

## 优点

- 页面的对象模型是其中测试对象和功能被彼此分开，从而保持代码干净的实现。
- 对象保持独立的测试脚本。一个目的可以通过一个或多个测试脚本进行访问，因此，POM可以帮助我们创建对象一次和多次使用。
- 由于创建对象后，很容易访问和易于更新一个对象的特定属性。

## POM流程图

网页中的每一个创建对象和方法被开发专用于访问这些对象。让我们利用http://calculator.net来理解是一样的。

存在与之关联的各种计算器，并在特定的页面的那些对象中的每一个在一个单独的类文件为静态方法创建，他们都在'测试'class文件中的静态方法将被访问的对象进行访问。

![Selenium IDE 145](images/0F1352603-0.jpg)

## 示例

让我们来了解通过执行用于百分比计算器测试中实现POM 。

步骤1：创建一个包内一个简单的类(page_objects_perc_calc.java)文件，并创建这些对象标识符中的每一个方法，如下图所示。

```java
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

```java
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

![Selenium IDE 146](images/0F1352242-1.jpg)