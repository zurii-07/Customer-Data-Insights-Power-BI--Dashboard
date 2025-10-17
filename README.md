# Customer-Data-Insights-Power-BI--Dashboard
In this project I have used a dataset on a customer transactions for different products which I will analyse this data and build a Power BI Dashboard.

1. Open Power BI Desktop and create a new project by clicking "blank report".
2. Rename the project as you like and give its location to a new folder.
3. Add the data files which you are going to make insights from to that folder.
4. Comeback to the Power BI interface and click "Get data from another source".
5. Now you will have the ability to upload any type of file. Upload the files one after the other choosing the correct format.
6. In my case, I uploaded one excel file, transformed it before loading it. and did the other file in .txt format the same procedure.
7. You can also do the method, upload the two data files first, load them and finally transform them one by one.

So let's continue with my approach to the project. 
First with transformation of data in the Text data file:

8. Text Data (Invoice Data) File Transformation.

⦁	Change the "Sales" column's data type from "Integer" to "Fixed Decimal Number" to show it as a currency,
⦁	Merge Year, Month, Day columns by selecting them using Ctrl + Select the columns, command then merged them into one as "Date". (Separator should be /, New Column Name = Date)
⦁	Change the data type of new "Date" column into Date.

Secondly the transformation of data in Excel data file:

9. Excel Data (Customer Data) File Transformation.

⦁	Select the "CityProvince" column and split the column by delimiter. Choose custom and '('. Split at: left-most delimiter and click OK. Rename the first column as "City" and the next as "Province". In the new "Province" column replace '(' with nothing.
⦁	Remove Columns that don't need for the insights such as customer email, telephone number, address etc. Go to choose columns in Home --> manage columns tab and untick the not needed columns and click OK.

10. Transformations for both files are done. Click close and apply.

11. In Power BI we don't merge tables. Power BI auto detects new relationships between tables when data is loaded.
    In this project:
⦁	Fact Table is Invoice Data
⦁	Lookup Table is Master Customer Data

12. Now create insights by clicking Visualizations tab and selecting what features you need to compare from each table's columns and you are done. You can insert any number of pages.
e.g.:
⦁	Insert Chart with Slicer
⦁	Insert Tables with Quick Measures
⦁	Insert Map Chart
⦁	Insert Line Chart
⦁	Add KPI Chart to Dashboard

13. All are done. Lastly save and publish your report on web and share the report with others.
