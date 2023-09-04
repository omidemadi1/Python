## openpyxl

یکی از کتابخانه های پایتون هست که ب وسیله آن میتوان روی 'اکسل' کارکرد. <br>
این کتابخانه به ما اجازه میدهد که فایل های اسکل را بخوانیم روی آنها بنویسیم و روی آنها تغیرات ایجاد کنیم. <br>
برای اینکه بتوانیم از این کتابخانه استفاده کنیم ابتدا باید آن را به کمک cmd و کد زیر نصب کنیم.
```powershell
pip install openpyxl
```
<br>

و برای اینکه بتوانیم از این کتابخانه در کد خود استفاده کنیم ابتدا باید از دستور زیر استفاده کنیم.
```python
import openpyxl
```
<br>

* ### خواندن فایل ها
میتوانیم فایل های اکسل که قبلا وجود داشته را بخوانیم. مثل خواندن سلول ها، فرمتها و همچنین فرمول ها
```python
import openpyxl

# Load the workbook
workbook = openpyxl.load_workbook('example.xlsx')

# Get the active worksheet
worksheet = workbook.active

# Read the data from cells
name = worksheet['A2'].value
age = worksheet['B2'].value
country = worksheet['C2'].value

print(f"{name} is {age} years old and from {country}.")
```
<br>

* ### نوشتن فایل ها
ما همچنین میتوانیم به وسیله این کتابخانه فایل های جدید اضافه کنیم و همچنین فایل هایی که وجود دارند را تغییر بدهیم. مثل اضافه کردن صفحه جدید، اضافه کردن سلول های جدید و همچنین فرمت برای هر سلول
```python
import openpyxl

# Create a new workbook
workbook = openpyxl.Workbook()

# Get the active worksheet
worksheet = workbook.active

# Write some data to cells
worksheet['A1'] = 'Name'
worksheet['B1'] = 'Age'
worksheet['C1'] = 'Country'

worksheet['A2'] = 'John'
worksheet['B2'] = 25
worksheet['C2'] = 'USA'

# Save the workbook
workbook.save('example.xlsx')
```
<br>

* ### فرمت سلول ها
این کتابخانه به ما اجازه میدهد که فرمت های خاصی را برای سلول ها انتخاب کنیم مثل تغییر اندازه فونت، رنگ و استایل
```python
import openpyxl
from openpyxl.styles import Font, Alignment

# Load the workbook
workbook = openpyxl.load_workbook('example.xlsx')

# Get the active worksheet
worksheet = workbook.active

# Change the font and alignment of cells
name_cell = worksheet['A1']
name_cell.font = Font(bold=True, size=14)
name_cell.alignment = Alignment(horizontal='center')

# Save the workbook
workbook.save('example.xlsx')
```
<br>

* ### کار کردن با جدول ها
میتوانیم یک نمودار یا جدول در اکسل را با کمک این کتابخانه ایجاد کنیم.
```python
import openpyxl
from openpyxl.chart import BarChart, Reference, Series

# Load the workbook
workbook = openpyxl.load_workbook('example.xlsx')

# Get the active worksheet
worksheet = workbook.active

# Create a chart
chart = BarChart()

# Define the data for the chart
data = Reference(worksheet, min_row=2, max_row=3, min_col=2, max_col=3)

# Add the data to the chart
chart.add_data(data, titles_from_data=True)

# Set the chart title
chart.title = 'Age Comparison'

# Set the x-axis and y-axis titles
chart.x_axis.title = 'Name'
chart.y_axis.title = 'Age'

# Add the chart to the worksheet
worksheet.add_chart(chart, 'E1')

# Save the workbook
workbook.save('example.xlsx')
```
<br>

* ### دست زدن به اعتبار سنجی داده ها
این کتابخانه می تواند اعتبار سنجی داده ها را اداره کند، مانند اطمینان از اینکه داده های وارد شده به یک سلول معیارهای خاصی را برآورده می کند.
```python
import openpyxl
from openpyxl.worksheet.datavalidation import DataValidation

# Load the workbook
workbook = openpyxl.load_workbook('example.xlsx')

# Get the active worksheet
worksheet = workbook.active

# Define the data validation rules
age_validation = DataValidation(type="whole", operator="greaterThan", formula1=18)
age_validation.prompt = "Age must be greater than 18."
age_validation.error = "Invalid age entered."
age_validation.errorTitle = "Invalid Entry"

# Apply the validation rules to a range of cells
age_range = worksheet['B2:B10']
worksheet.add_data_validation(age_validation)
age_range.data_validation = age_validation

# Save the workbook
workbook.save('example.xlsx')
```
<br>

* ### کار با جداول محوری
شما می توانید جداول محوری در اکسل با استفاده از openpyxl, که یک ابزار قدرتمند برای تجزیه و تحلیل و خلاصه سازی داده ها ایجاد کنید. <br>
چند نمونه از دستوراتی که میتوانیم با این کتابخانه انجام دهیم
```python
Load the workbook
workbook = openpyxl.load_workbook('example.xlsx')

# Get the active worksheet
worksheet = workbook.active
```
<br>

شما میتوانید به یک صفحه خاص به وسیله اسم یا index آن دسترسی داشته باشید.
```python
# with name
worksheet = workbook['Sheet2']

# with index
worksheet = workbook.worksheets[1]

# Access a cell and get its value
cell = worksheet['A1']
print(cell.value)

# Create a new workbook
workbook = openpyxl.Workbook()

# Get the active worksheet
worksheet = workbook.active

# Write a value to a cell
worksheet['A1'] = 'Hello, world!'

# Save the workbook
workbook.save('example.xlsx')

# Merge cells
worksheet.merge_cells('A1:C1')

# Unmerge cells
worksheet.unmerge_cells('A1:C1')
```
<br>

برای اضافه کردن آیتم در ستون یا سطر بعدی باید از دستور زیر استفاده کنیم.
```python
import openpyxl

x = input(">> ")
y = input(">> ")

wb = openpyxl.load_workbook("test.xlsx")
ws = wb.active

row = ws.max_row + 1
ws.cell(row=row, column=1).value = x
ws.cell(row=row, column=2).value = y

wb.save("test.xlsx")
```
<br>

برای جست و جو کردن یک آیتم درون صفحه خود باید مراحل زیر را طی کنیم.
```python
wb = openpyxl.load_workbook("test.xlsx")
ws = wb.active

for row in ws.iter_row() :
     for cell in row :
          if omid in cell.value :
               print("it's here")
```
<br>

* ### کار کردن با ستون ها و سطر ها
```python
import openpyxl

# Load the workbook
workbook = openpyxl.load_workbook('example.xlsx')

# Get the active worksheet
worksheet = workbook.active

# Insert a new row
worksheet.insert_rows(2)

# Delete a row
worksheet.delete_rows(2)

# Insert a new column
worksheet.insert_cols(2)

# Delete a column
worksheet.delete_cols(2)

# Save the workbook
workbook.save('example.xlsx')
```
<br>

* ### ‏named range
```python
import openpyxl

# Load the workbook
workbook = openpyxl.load_workbook('example.xlsx')

# Get the active worksheet
worksheet = workbook.active

# Define a named range
age_range = openpyxl.workbook.defined_name.DefinedName('age', attr_text='Sheet1!$B$2:$B$10')

# Add the named range to the workbook
workbook.defined_names.append(age_range)

# Access the named range
named_range = workbook.defined_names['age']
print(named_range.attr_text)

# Save the workbook
workbook.save('example.xlsx')
```
<br>

* ### کار کردن با فرمول ها
```python
import openpyxl
from openpyxl.utils import FORMULAE

# Load the workbook
workbook = openpyxl.load_workbook('example.xlsx')

# Get the active worksheet
worksheet = workbook.active

# Write a formula to a cell
worksheet['D2'] = '=SUM(B2:C2)'

# Evaluate a formula in a cell
print(worksheet['D2'].value)
worksheet['D2'].value = worksheet['D2'].value

# List all available formulas
print(list(FORMULAE.keys()))

# Save the workbook
workbook.save('example.xlsx')
```
<br>

* ### کپی و پیست کردن سلول ها
```python
import openpyxl
from openpyxl.utils.cell import column_index_from_string, get_column_letter

# Load the workbook
workbook = openpyxl.load_workbook('example.xlsx')

# Get the active worksheet
worksheet = workbook.active

# Copy cells from one range to another
source_range = worksheet['A1:C3']
target_range = worksheet['D1:F3']

for row in range(1, source_range.max_row + 1):
    for col in range(1, source_range.max_column + 1):
        source_cell = source_range.cell(row=row, column=col)
        target_cell = target_range.cell(row=row, column=col)
        target_cell.value = source_cell.value

# Copy cells from one column to another
source_column = worksheet['A']
target_column = worksheet['D']

for index, source_cell in enumerate(source_column, start=1):
    target_cell = target_column[index]
    target_cell.value = source_cell.value

# Save the workbook
workbook.save('example.xlsx')
```
