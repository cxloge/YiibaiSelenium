# Selenium环境安装设置

为了开发Selenium RC或webdriver脚本，用户必须确保他们有初始配置完成。有很多关联建立环境的步骤。这里将通过详细的讲解。

- 下载并安装Java
- 下载并配置Eclipse
- 配置Firebug和FirePath
- 配置Selenium RC
- 配置Selenium的webdriver

## 下载并安装Java

我们需要有JDK(Java开发工具包)安装序Selenium Webdriver/Selenium工作。让我们先来看看如何下载和安装Java。

步骤1： 导航到的网址：http://www.oracle.com/technetwork/java/javase/downloads/index.html

步骤2：转到“Downloads”部分，然后选择“JDK Download”。

![Selenium IDE 30](images/2153312441-0.jpg)

**步骤3：**选择“Accept License Agreement”单选按钮。

![Selenium IDE 31](images/2153315638-1.jpg)

**第4步：**选择合适的安装。在这种情况下它是“Windows 7-64'位。点击相应的链接和exe档案保存到硬盘。

![Selenium IDE 32](images/2153315V6-2.jpg)

**第5步：**运行下载的exe文件和安装程序向导。点击“Next”继续。

![Selenium IDE 33](images/2153314531-3.jpg)

**第6步：**选择功能，然后点击“Next”。

![Selenium IDE 34](images/2153316304-4.jpg)

**步骤7：**安装程序提取和相同的进度显示在向导中。

![Selenium IDE 35](images/2153315957-5.jpg)

**第8步：**用户可以选择安装位置，然后单击“Next”。

![Selenium IDE 36](images/2153312349-6.jpg)

**第9步：**安装程序安装JDK和新的文件将被复制。

![Selenium IDE 37](images/21533113H-7.jpg)

**第10步：**安装程序安装成功，并显示给用户。

![Selenium IDE 38](images/215331GG-8.jpg)

**步骤11：**要验证是否安装成功，转到命令提示符，然后只需键入Java的一个命令。该命令的输出如下所示。如果Java安装不成功，或者如果它没有安装它会引发“unknown command”的错误。

![Selenium IDE 48](images/2153315M8-9.jpg)

## 下载并配置Eclipse

第1步：根据操作系统体系结构导航到URL ：http://www.eclipse.org/downloads/ 并下载。

![Selenium IDE 39](images/2153315a0-10.jpg)

**第2步：**点击“Download”按钮。

![Selenium IDE 40](images/21533111Z-11.jpg)

**第3步：**下载将是一个压缩格式。解压缩的内容。

![Selenium IDE 41](images/2153316020-12.jpg)

**第4步：**找到eclipse.exe并双击该文件。

![Selenium IDE 42](images/2153311931-13.jpg)

**第5步：**配置工作区中选择开发位置。

![Selenium IDE 43](images/2153316426-14.jpg)

**第6步：**打开如下图所示的Eclipse窗口。

![Selenium IDE 44](images/215331H08-15.jpg)

## 配置Firebug和FirePath

要使用Selenium RC或webdriver来工作，我们需要根据自己的XPath或编号或名称等序列，以找出我们需要的工具/插件元素来定位元素。定位元素的各种方式被处理，详细在定位器章节。

步骤1：找到的网址：https://addons.mozilla.org/en-US/firefox/addon/firebug/ 并下载插件。

![Selenium IDE 62](images/21533135F-16.jpg)

**步骤2：**将插件安装程序显示给用户，它是在单击“Install”按钮开始安装。

![Selenium IDE 63](images/21533115Y-17.jpg)

**第3步：**安装完成后，我们可以通过启动插件导航到“Web Developer”>>“Firebug”。

![Selenium IDE 64](images/215331I04-18.jpg)

**第4步：**Firepath一个插件，它的工作原理中的萤火虫帮助用户抓住一个元素“Xpath”。导航到“https://addons.mozilla.org/en-US/firefox/addon/firepath/”安装Firepath

![Selenium IDE 65](images/2153312456-19.jpg)

**第5步：**插件安装程序显示给用户，它是在单击“Install”按钮开始安装。

![Selenium IDE 66](images/215331L04-20.jpg)

**步骤6：**现在推出“Firebug”导航到“Tools”>>“Webdeveloper”>>“Firebug”

![Selenium IDE 67](images/2153314U7-21.jpg)

### 示例

现在让我们了解如何使用Firebug和firepath一个例子。为了演示目的，我们将使用www.google.com并捕捉“google.com”文本框的属性。

步骤1：首先在下面的截图高亮点击箭头图标，将其拖动到我们想捕捉属性的对象。如下图所示，该对象的HTML / DOM将被显示。我们能够捕捉到的输入文本框的“ID”，我们可以进行交互。

![Selenium IDE 68](images/2153313113-22.jpg)

**步骤2：**为了获取对象的XPath，去“firepath”选项卡，然后执行以下步骤。

- 点击间谍图标。
- 选择控制，想要捕捉的XPath
- 将产生的所选择的控制的xpath

![Selenium IDE 69](images/2153314402-23.jpg)

## 配置Selenium RC

现在，就让我们来看看如何配置Selenium 的远程控制。我们将了解如何开发在即将到来的章节关于Selenium RC的章节，但是现在我们明白它只是配置的一部分。

第1步：找到selenium 下载部分http://www.seleniumhq.org/download/，并通过点击它的版本号，如下图所示下载Selenium服务器。

![Selenium IDE 45](images/215331Lb-24.jpg)

**第2步：**下载后，我们需要启动Selenium服务器。这样做，打开命令提示符并导航到下载的JAR文件保持如下所示的文件夹。

![Selenium IDE 46](images/2153314121-25.jpg)

**第3步：**启动服务器，使用命令“'java -jar <<downloaded jar name >>"如果已安装Java JDK正常，会得到一个成功的消息，如下图所示。现在，我们就可以开始写这将涉及在下一章Selenium RC的脚本。

![Selenium IDE 47](images/2153315108-26.jpg)

## 配置Selenium的webdriver

现在，就让我们来看看如何配置Selenium webdriver。我们将了解如何开发在即将到来的章节，Selenium webdriver的剧本，但是现在我们明白它只是配置的一部分。

**第1步：**找到selenium 下载部分http://www.seleniumhq.org/download/和下载selenium 的webdriver通过点击它的版本号，如下图所示。

![Selenium IDE 49](images/215331N49-27.jpg)

**第2步：**下载的文件是压缩格式，一个具有解压缩的内容映射到项目文件夹中。

![Selenium IDE 49](images/2153313116-28.jpg)

**步骤3：**如下图所示，将解压缩后的内容将被显示。如何将其映射到项目文件夹，如何启动脚本会处理在webdriver的章节。

![Selenium IDE 51](images/2153312241-29.jpg)