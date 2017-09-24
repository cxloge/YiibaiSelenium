# Selenium IDE测试创建

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

![Selenium IDE 15](http://www.yiibai.com/uploads/allimg/140831/1633422105-7.jpg)