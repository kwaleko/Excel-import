# Excel-import
TASK : Import Excel file into Dynamixs AX

## Problems:
- Takes a lot of times since it insert data in the database record by record
- Reading data from EXCEL file is not efficient

## Solution :
1- save the excel file as tab-separated text

2- create Tmp table in dynamics AX and import the data form txt file to the temp table as bulk insert using [RecordInsertList](https://msdn.microsoft.com/en-us/library/recordinsertlist.aspx) it will be more faster

3- do the business logic while reading from the table 

4- after processing the business logic insert the data in the target table and make the class process on the server tier for better performance
