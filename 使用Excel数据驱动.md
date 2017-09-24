# 使用Excel数据驱动

在设计测试，参数化测试是不可避免的。我们会利用Apache的POI- Excel JAR实现是一样的。它可以帮助我们来读取和写入到Excel中。

## 下载JAR

**第1步：**导航到URL- http://poi.apache.org/download.htmll并下载ZIP格式。

![selenium_ide_152](images/0F41RY5-0.jpg)

**第2步：**点击镜像链接下载JAR。

![selenium_ide_153](images/0F41U219-1.jpg)

**第3步：**解压缩到一个文件夹。

![selenium_ide_154](images/0F41V5J-2.jpg)

**第4步：**如下所示的解压缩后的内容将被显示。

![selenium_ide_155](images/0F41WF5-3.jpg)

**第5步：**现在创建一个新的项目，并在“External JARs”添加“POI-3.10.FINAL”文件夹中所有的jar包。

![selenium_ide_147](images/0F41W442-4.jpg)

**第6步：**现在，添加所有的“External JARs”在“OOXML-LIB”文件夹中。

![selenium_ide_148](images/0F41VM4-5.jpg)

**第7步：**现在，添加所有的“External JARs”在“lib”文件夹中。

![selenium_ide_149](images/0F41UY3-6.jpg)

**第8步：**如下图所示，显示已添加的JAR文件。

![selenium_ide_150](images/0F41TW9-7.jpg)

**第9步：**如下图所示的Package Explorer显示。此外附加“webdriver”相关的JAR

![selenium_ide_151](images/0F41R115-8.jpg)

## 参数

为了演示目的，我们将参数的百分比计算器测试。

**第1步：**我们将所有的参数需要使用Excel的％计算器的输入。所设计的excel如下所示。

![selenium_ide_156](images/0F41V238-9.jpg)

**第2步：**现在，我们将执行所有百分比计算器，所有指定的参数。

**第3步：**让我们创建通用的方法来访问使用导入JARS Excel文件。这些方法可以帮助我们获得一个特定的单元格数据或设置一个特定的单元格的数据等。

```java
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

```java
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

![Selenium IDE 157](images/0F41T092-10.jpg)