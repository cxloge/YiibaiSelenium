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

```java
WebDriver driver =newFirefoxDriver();
driver.get("Enter an URL"S);
WebElementDynamicElement=(newWebDriverWait(driver,10)).until(ExpectedConditions.presenceOfElementLocated(By.id("DynamicElement")));
```

### 隐式等待

隐式等待的情况下，如果网络驱动器找不到，因为它的不可用性的立即的对象。webdriver将等待指定的隐含的等待时间，也不会尝试在指定时间内找到的元素了。一旦指定的时间限制被超越，webdriver将尝试再次搜索该元素的最后一面。如果成功，将继续进行执行，但如果失败，它会抛出异常。这是一种全局的等待，这意味着这种等待是适用于整个驱动程序。因此，硬编码这种等待更长的时间时期将阻碍该脚本执行时间。

```java
WebDriver driver = new FirefoxDriver();
driver.manage().timeouts().implicitlyWait(10, TimeUnit.SECONDS);
driver.get("Enter an URL");
WebElement DynamicElement = driver.findElement(By.id("DynamicElement"));
```

### 流利等待

FluentWait用于当webelement可以出现在5秒或者甚至它可以采取90秒。在这种情况下，我们定义的时间等待的状态的最大数量，以及与该查询的对象状态的是否存在等的频率。

让我们假定，我们将60秒可用一个元素在网页上，但每10秒检查一次它的存在。

```java
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