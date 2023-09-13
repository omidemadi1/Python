## Variables

برای تعریف یک متغیر در زبان پایتون فقط کافیست یک اسم برای آن انتخاب کرد و آن را برابر با مقداری قرار داد

```python
student_count = 30
print(student_count)

➡️ 30
```

```python
x = 1
print(x)

➡️ 1
```
<br>
<br>

## Data Types

انواع داده هایی که میتوان از آنها استفاده کرد

| Text Type: | str |
| --- | --- |
| Numeric Types: | int, float, complex |
| Sequence Types: | list, tuple, range |
| Mapping Type: | dict |
| Set Types: | set, frozenset |
| Boolean Type: | bool |
| Binary Types: | bytes, bytearray, memoryview |
| None Type: | NoneType |

* ### Number
اعداد صحیح ، اعداد اعشاری ، اعداد ترکیبی

* ### Strings
 برای داده های متنی استفاده میشود
اگر در نمایش نوشتار بخواهیم ادامه یک جمله را در سطر بعدی نمایش دهیم باید از "", '' استفاده کنیم.
```python
print("'Hi omid
welcome to python"'

➡️ Hi omid
welcome to python
```

 len()
برای اینکه بفهمیم طول کاراکترمان چقدر است و از چند حرف تشکیل شده است میتوانیم از دستور زیر استفاده کنیم

```python
course = "python programming"
len(course)
print(len)

➡️ 18
```
```python
print(len(course))
➡️ 18
```
برای اینکه بدانیم در یک متن کلمه ای که دنبال آنیم وجود دارد یا خیر میتوانیم از دستور زیر استفاده کنیم

```python
txt = "The best things in life are free!"
print("free" in txt)
```
برای فهمیدن نبودن آن کلمه در متن از دستور زیر استفاده میکنیم

```python
txt = "The best things in life are free!"
print("expensive" not in txt)
```

strip()
برای حذف کردن اسپس های اضافه در ابتدا و انتهای متن استفاده میشود
```python
a = " Hello, World! "
print(a.strip())
```

reaplace()
برای عوض کردن جای یک حرف با حرف دیگر استفاده میشود
```python
a = "Hello, World!"
print(a.replace("H", "J"))
-> Jello, World!
```

split()
در صورت استفاده از این فانکشن متن به صورت لیست به شما برگردانده میشود. برای اینکار باید همراه با این فانکشن یک حرف را اضافه کنیم که مفسر بداند متن باید از کجا جدا بشود
```python
a = "Hello, World!"
print(a.split(","))
-> ['Hello', ' World!']
```

Format()
برای ترکیب 'int' و 'str' استفاده میشود
```python
age = 36
txt = "My name is John, and I am {}"
print(txt.format(age))
-> My name is John, and I am 36
```
از این دستور میتوانیم به صورت نامحدود در ترکیب متن با اهداد استفاده کنیم
```python
quantity = 3
itemno = 567
price = 49.95
myorder = "I want {} pieces of item {} for {} dollars."
print(myorder.format(quantity, itemno, price))
-> I want 3 pieces of item 567 for 49.95 dollars.
```
همچنین میتوانیم داخل ‘{ }’ را شماره گذاری کنیم که متغیر ها در جایی که میخواهیم قرار بگیرند
```python
quantity = 3
itemno = 567
price = 49.95
myorder = "I want to pay {2} dollars for {0} pieces of item {1}."
print(myorder.format(quantity, itemno, price))
-> I want to pay 49.95 dollars for 3 pieces of item 567
```
<br>

همچنین میتوانیم برای این که توضیح دهیم متغیر چگونه نمایش داده شود از پارامتر های مختلفی استفاده کنیم.
```python
price = 49
txt = "The price is {:.2f} dollars"
print(txt.format(price))
-> The price is 49.00 dollars
```
<br>

تمام پارامترهایی که میتوانیم از آنها استفاده کنیم. <br>
**Python String format() Method (w3schools.com)** <br>
اگر بخواهیم از متغیر های بیشتری در متن استفاده کنیم باید به شکل زیر عمل کنیم :
```python
quantity = 3
itemno = 567
price = 49
myorder = "I want {} pieces of item number {} for {:.2f} dollars."
print(myorder.format(quantity, itemno, price))
-> I want 3 pieces of item number 567 for 49.00 dollars.
```
<br>

همچنین میتوانیم در براکت ها از ایندکس متغیر ها استفاده کنیم تا هر کدام در جایی که میخواهیم استفاده شوند.
```python
age = 36
name = "John"
txt = "His name is {1}. {1} is {0} years old."
print(txt.format(age, name))
-> His name is John. John is 36 years old.
```
<br>

همچنین میتوانیم متغیر ها را در براکت نام گذاری کنیم و سپس به آنها مقدار دهیم.
```python
myorder = "I have a {carname}, it is a {model}."
print(myorder.format(carname = "Ford", model = "Mustang"))
-> I have a Ford, it is a Mustang.
```
<br>

اگر بخواهیم در یک متن از “” استفاده کینم میتوانیم از \ به شکل زیر از آن استفاده کنیم.
```python
txt = "We are the so-called \"Vikings\" from the north."
Print(txt)
-> We are the so-called "Vikings" from the north.
```
<br>
جدول زیر مربوط به ترکیب و استفاده از موارد خاص میباشد
| Code | Result |
| --- | --- |
| \' | Single Quote |
| \\ | Backslash |
| \n | New Line |
| \r | Carriage Return |
| \t | Tab |
| \b | Backspace |
| \f | Form Feed |
| \xhh | Hex value |
<br>

فانکشن هایی که در 'str' میتوان از آن ها استفاده کرد.
| Method | Description |  |  |
| --- | --- | --- | --- |
| capitalize() | Converts the first character to upper case | isupper() | Returns True if all characters in the string are upper case |
| casefold() | Converts string into lower case | join() | Joins the elements of an iterable to the end of the string |
| center() | Returns a centered string | ljust() | Returns a left justified version of the string |
| count() | Returns the number of times a specified value occurs in a string | lower() | Converts a string into lower case |
| encode() | Returns an encoded version of the string | lstrip() | Returns a left trim version of the string |
| endswith() | Returns true if the string ends with the specified value | maketrans() | Returns a translation table to be used in translations |
| expandtabs() | Sets the tab size of the string | partition() | Returns a tuple where the string is parted into three parts |
| find() | Searches the string for a specified value and returns the position of where it was found | replace() | Returns a string where a specified value is replaced with a specified value |
| format() | Formats specified values in a string | rfind() | Searches the string for a specified value and returns the last position of where it was found |
| format_map() | Formats specified values in a string | rindex() | Searches the string for a specified value and returns the last position of where it was found |
| index() | Searches the string for a specified value and returns the position of where it was found | rjust() | Returns a right justified version of the string |
| isalnum() | Returns True if all characters in the string are alphanumeric | rpartition() | Returns a tuple where the string is parted into three parts |
| isalpha() | Returns True if all characters in the string are in the alphabet | rsplit() | Splits the string at the specified separator, and returns a list |
| isascii() | Returns True if all characters in the string are ascii characters | rstrip() | Returns a right trim version of the string |
| isdecimal() | Returns True if all characters in the string are decimals | split() | Splits the string at the specified separator, and returns a list |
| isdigit() | Returns True if all characters in the string are digits | splitlines() | Splits the string at line breaks and returns a list |
| isidentifier() | Returns True if the string is an identifier | startswith() | Returns true if the string starts with the specified value |
| islower() | Returns True if all characters in the string are lower case | strip() | Returns a trimmed version of the string |
| isnumeric() | Returns True if all characters in the string are numeric | swapcase() | Swaps cases, lower case becomes upper case and vice versa |
| isprintable() | Returns True if all characters in the string are printable | title() | Converts the first character of each word to upper case |
| isspace() | Returns True if all characters in the string are whitespaces | translate() | Returns a translated string |
| istitle() | Returns True if the string follows the rules of a title | upper() | Converts a string into upper case |
|  |  | zfill() | Fills the string with a specified number of 0 values at the beginning |
<br>

* ### Boolean
درست(true) ، غلط(false)
برای مواردی که بخواهیم یک تصمیم گیری در برنامه داشته باشیم بسیار به کار میرود
به عنوان مثال : اگر ادمین بود یک سری دسترسی های خاص به آن بدهیم
```python
is_publish = True
print(is_publish)
➡️ true
```
<br>
<br>

## Operator
برای مقایسه مقادیر به کار میرود. که همان علامت های (( < = > )) در ریاضی میباشد
این عملگرها از نوع بولین میباشند
```python
print(10>3)
➡️ true
```
```python
print(10<3)
➡️ false
```
<br>

برای چک کردن برابری در 2 طرف از '==' استفاده میکنیم
(آیا طرف راست با طرف چپ برابر است؟)
```python
print(3==3)
➡️ true
```
<br>

همچنین میتوانیم برابر نبودن طرفین را هم مشخص کینم که باید از '=!' استفاده کنیم
```python
print(3!=4)
➡️ True
```
<br>

از این عملگرها میتوانیم در فرمت داده‌ی ‘استرینگ’ هم استفاده کرد
```python
print("3" > "2")
➡️ true
```
<br>

در مقایسه حرف آنها را برحسب نمایش عددیشان مقایسه میکند
ord( )
برای آنکه بفهمیم نمایش عددی یک حرف چیست باید از این فانکشن اسفاده کنیم
```python
print(ord("a"))
print(ord("m"))
print("ali" > "mohammad")

➡️ 97
109
false
```
<br>


* ### Ternary operator
برای مرتب گردن و تمیز تر کردن کد استفاده میشود
```python
temp = 15
message = "it's warm" if temp > 30 else "it's cold"
print(message)

➡️ it's cold
```
<br>


* ### logical operators

از این عملگر ها برای ساخت شرط های پیچیده تر استفاده میکنیم.<br>
سه عملگر منطقی داریم or / and / not
<br>
از ترکیب عملگرهای مقایسه ای و منطقی میتوان شرط های پیچیده تری ساخت
```python
high_income = true
good_credit = true

if good_credit and high_income :
     print("eligible")
else : 
     print("not eligible")

➡️ eligible
```
<br>

```python
high_income = true
good_cretid = true 
student = false

if not student and(good_cridet or high_income) : 
     print("Eligible")
else : 
     print("not eligible")

➡️ eligible
```
<br>

* ### Between condition

```python
age = 22 

if 18< age < 65 : 
     print("eligible")

➡️ eligibl
```
<br>
<br>

## Lists
یک دیتا تایپ از نوع کامپلکس میباشد<br>
میتوان در آن از تعداد زیادی عناصر مختلف استفاده کرد<br>
برای ایجاد لیست باید از '[ ]' استفاده کرد.
```python
letters = ["a", "b", "c"]
print(letters)

➡️ ['a' , 'b' , 'c']
```
<br>

عناصر دخل لیست میتوانند خودشان از نوع لیست باشند
```python
matrix = [[0, 1], [2, 3]]
print(matrix)

➡️ [[0, 1], [2, 3]]
```
<br>

برای درست کردن یک لیست با 100 عدد صفر میتوانیم از تکنیک زیر استفاده کنیم
```python
zeros = [0] * 100
print(zeros)

➡️ [0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0]
```
<br>

میتوانیم 2 لیست را باهم ترکیب کنیم
```python
letters = ["a", "b", "c"]
zeros = [0] * 5
combined = letters + zeros

print(combined)

➡️ ['a', 'b', 'c', 0, 0, 0, 0, 0]
```
<br>

* ### len()
برای اینکه بفهمیم در یک لیست چند عنصر وجود دارد استفاده میشود
```python
thislist = ["apple", "banana", "cherry"]
print(len(thislist))
-> 3
```
<br>

نوشتن اعداد پشت سرهم به صورت یک لیست :<br>
برای این کار ابتدا باید از فانکشن درونی لیست ()list استفاده کنیم
ورودی این فانکشن بیاد از نوع قابل پیمایش باشد
این فانکشن مقدار ورودی ای که دریافت کرده را به صورت یک لیست به ما برمیگرداند
```python
numbers = list(range(20))
print(numbers)

➡️ [0, 1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13, 14, 15, 16, 17, 18, 19]
```
<br>

* ### Change list item
برای اینکه بخواهیم یکی از عناصر داخل لیست را تغییر بدهیم میتوانیم از روش زیر استفاده کنیم.

```python
letters = ["a", "b", "c", "d"]
letters[0] = 2

print(letters)

➡️ [2, 'b', 'c', 'd']
```
<br>

* ### unpaking
برای این ب کار میرود که عناصر داخل لیست را به متغیرهای جدید اعمال کنیم
```python
numbers = [1, 2, 3]
frist , second, third = numbers

print(frist , second, third)

➡️ 1 2 3
```
<br>

برای اینکار باید تعداد متغیرهای سمت چپ برابر با تعداد عناصر داخل لیست باشد. <br>
اگر برابر نبودند یا اگر به تعداد خاصی از عناصر لیست نیاز داشتیم میتوانیم برای جلوگیری از ارور از روش زیر استفاده کنیم
```python
numbers = [1, 2, 3, 4, 5, 6]
frist , second, *other = numbers

print(frist , second, other)

➡️ 1 2 [3, 4, 5, 6]
```
<br>

### unpacking operator
برای اینکه بتوانیم عناصر داخل لیست را از لیست خارج کنیم ب کار میرود
```python
num = [1, 2, 3]

print(*num)

➡️ 1 2 3
```
<br>

از این دستور میتوانیم برای همه دستورات قابل پیمایش استفاده کنیم.
```python
num = [*range(5)]
print(num)

➡️ [0, 1, 2, 3, 4]

x = [*"hello"]
print(x)

➡️ ['h', 'e', 'l', 'l', 'o']
```
<br>

همچنین میتوانیم محتوای 2 لیست را با یک دیگر ترکیب کنیم
```python
first = [1, 2]
second = [3, 4]

x = [*first, *second]

print(x)

➡️ [1, 2, 3, 4]
```
<br>

* ### ZIP
برای ترکیب 2 لیست در درون یک لیست ب کار میرود.
```python
list 1 = [1, 2, 3]
list2 = [10 , 20, 30]

print(list(zip(list1, list2)))

➡️ [(1, 10), (2, 20), (3, 30)]
```
<br>

ورودی فانکشن زیپ باید از نوع قابل پیمایش باید یعنی میتوانیم یک str هم به عنوان ورودی به آن بدهیم.
```python
list 1 = [1, 2, 3]
list2 = [10 , 20, 30]

print(list(zip(list1, list2, "abc")))

➡️ [(1, 10, 'a'), (2, 20, 'b'), (3, 30, 'c')]
```
<br>

* ### پیمایش لیست
```python
letters = ["a", "b", "c"]

for letter in letters :
     print(letter)

➡️ a
b
c
```
<br>

اگر بخواهیم بدانیم که در چرخه هر حرف چه index دارد از کلمه enumerate استفاده میکنیم
```python
letters = ["a", "b", "c"]

for letter in enumerate(letters) : 
     print(letter)

➡️ (0, 'a')
(1, 'b')
(2, 'c')
```
<br>

* ### Add list item
Insert() <br>
برای اضافه کردن ایتم در لیست به کار میرود به این شکل که اندکسی که میخواهیم ایتم در آن قرار بگیرد را وارد کرده و سپس آن ایتم را وارد میکنیم.
```python
thislist = ["apple", "banana", "cherry"]
thislist.insert(2, "watermelon")
print(thislist)
-> ['apple', 'banana', 'watermelon', 'cherry']
```
<br>

append() <br>
برای اضافه کردن ایتم در انتهای لیست به کار میرود.
```python
thislist = ["apple", "banana", "cherry"]
thislist.append("orange")
print(thislist)
-> ['apple', 'banana', 'cherry', 'orange']
```
<br>

extend() <br>
برای برای ادغام کردن عناصر داخل یک لیست دیگر در درون لیست استفاده میشود.
```python
thislist = ["apple", "banana", "cherry"]
tropical = ["mango", "pineapple", "papaya"]
thislist.extend(tropical)
print(thislist)
-> ['apple', 'banana', 'cherry', 'mango', 'pineapple', 'papaya']
```
<br>

* ### Remove list items
remove() <br>
برای حذف کردن یک ایتم مخصوص استفاده میشود.
```python
thislist = ["apple", "banana", "cherry"]
thislist.remove("banana")
print(thislist)
-> ['apple', 'cherry']
```
<br>

pop() <br>
برای حذف کردن یک ایتم از لیست به وسیله ایندکس آن استفاده میشود.
```python
thislist = ["apple", "banana", "cherry"]
thislist.pop(1)
print(thislist)
-> ['apple', 'cherry']
```
<br>

اگر هنگام استفاده ازاین دستور ایندکسی را به عنوان ورودی به آن ندهید اخرین عنصر لیست را حذف میکند.
```python
thislist = ["apple", "banana", "cherry"]
thislist.pop()
print(thislist)
-> ['apple', 'banana']
```
<br>

del() <br>
این دستوربرای حذف کردن عنصر یک لیست به وسیله ایندکس آن استفاده میشود.
```python
thislist = ["apple", "banana", "cherry"]
del thislist[0]
print(thislist)
-> ['banana', 'cherry']
```
<br>

همچنین این دستور میتواند یک لیست را به طور کامل پاک کند.
```python
thislist = ["apple", "banana", "cherry"]
del thislist
```
<br>

clear() <br>
برای پاک کردن درون یک لیست استفاده میشود.
```python
thislist = ["apple", "banana", "cherry"]
thislist.clear()
print(thislist)
-> [ ]
```
<br>

### یافتن یک عنصر در لیست
برای اینکه اندیس یک عنصر را بفهمیم باید از روش زیر استفاده کنیم

```python
letters = ["a", "b", "c"]
print(letters.index("b"))

➡️ 1
```
<br>

برای اینکه بفهمیم یک عنصر چند بار در لیست تکرار شده باید از count استفاده کنیم
```python
letters = ["a", "b", "c"]
print(letters.count("b"))

➡️ 1
```
<br>

* ### Sort lists
sort() <br>
برای اینکه بتوانیم لیست خود را به صورت برعکس مرتب کنیم باید به روش زیر عمل کنیم.
```python
thislist = ["orange", "mango", "kiwi", "pineapple", "banana"]
thislist.sort(reverse = True)
print(thislist)
-> ['pineapple', 'orange', 'mango', 'kiwi', 'banana']
```
<br>

برای سفارشی سازی کردن ترتیب لیست باید به روش زیر عمل کنیم :
```python
def myfunc(n):
  return abs(n - 50)

thislist = [100, 50, 65, 82, 23]
thislist.sort(key = myfunc)
print(thislist)
-> [50, 65, 23, 82, 100]
```
<br>

این دستور به حروف کوچک و بزرگ حساس است و ابتدا کلماتی که با حروف بزرگ نوشته شده باشد را مرتب میکند و سپس به سراغ کلاماتی میرود که با حروف کوچک شروع شده‌اند.<br>
اگر بخواهیم این حساسیت را از بین ببریم میتوانیم از دستور زیر استفاده کنیم :
```python
thislist = ["banana", "Orange", "Kiwi", "cherry"]
thislist.sort(key = str.lower)
print(thislist)
```
<br>

برای اینکه بتوانیم اعداد را به صورت نزولی مرتب کنیم باید از روش زیر استفاده کنیم.
```python
numbers = [3, 20, 1, 7, 4]
numbers.sort(reverse=True)

print(numbers)

➡️ [20, 7, 4, 3, 1]
```
<br>

علاوه بر sort میتوانیم از فانکشن درونی sorted هم برای مرتب سازی استفاده کنیم.
```python
numbers = [3, 20, 1, 7, 4]
print(sorted(numbers))

➡️ [1, 3, 4, 7, 20]
```
<br>

در این روش لیست اصلی ما تغییری نمیکند و در واقع یک لیست جدید درست میکند<br>
اگر عناصر تشکیل دهنده لیست غیر از str بود باید به صورت زیر عمل کنیم.
```python
Items = [
     ("product1", 10)
     ("product2", 9)
     ("product3", 12)
]

def sort_items(items)
     return items[1]

items.sort(key = sort_items)
print(items)

➡️ [('product2', 9), ('product1', 10), ('product3', 12)]
```
<br>

برای سفارشی سازی کردن ترتیب لیست باید به روش زیر عمل کنیم.
```python
def myfunc(n):
  return abs(n - 50)

thislist = [100, 50, 65, 82, 23]
thislist.sort(key = myfunc)
print(thislist)
-> [50, 65, 23, 82, 100]
```
<br>

* ### Copy lists
copy() <br>
از این دستور برای کپی کردن یک لیست استفاده میشود
```python
thislist = ["apple", "banana", "cherry"]
mylist = thislist.copy()
print(mylist)
-> ['apple', 'banana', 'cherry']
```
<br>

list() <br>
روش دیگر برای کپی کردن یک لیست استفاده از این دستور می‌باشد.
```python
thislist = ["apple", "banana", "cherry"]
mylist = list(thislist)
print(mylist)
```
<br>
<br>

## Tuples
تاپل همان لیست است با این فرق که فقط قابلیت خواندن دارد.
برای ساخت تاپل باید از '( )' استفاده کنیم
```python
point = (1, 2)
print(point)

➡️ (1, 2)
```
<br>

تاپل ها را هم میشود مانند لیست ها با هم ترکیب کرد.
```python
point = (1, 2) + (3, 4)
print(point)

➡️ (1, 2, 3, 4)
```
<br>

برای تبدیل یک لیست به تاپل باید از فانکشن ()tuple استفاده کنیم.
```python
list = [1, 2]
point = tuple(list)
print(point)

➡️ (1, 2)
```
<br>

ورودی فانکشن تاپل از نوع قابل پیمایش میباشد و میتوانیم هر عنصر قابل پیمایشی به عنوان ورودی به آن بدهیم.<br>
برای اینکه بتوانیم یک تاپل را ویرایش کنیم باید ابتدا آن را به لیست تبدیل کنیم و سپس آن را تغییر دهیم.
```python
x = ("apple", "banana", "cherry")
y = list(x)
y[1] = "kiwi"
x = tuple(y)
print(x)
-> ("apple", "kiwi", "cherry")
```
<br>
<br>

## Set
خواص مجموعه این است که هیچ عدد تکراری در آن قرار نمیگیرد.<br>
برای استفاده از مجموعه باید از '{ }' استفاده کنیم
```python
numbers = {1, 2, 3}
print(numbers)

➡️ {1, 2, 3}
```
<br>

برای تبدیل یک لیست به مجموعه باید از فانکشن ()set استفاده کنیم.
```python
num = [1, 1, 2, 3, 4]

unique = set(num)
print(unique)

➡️ {1, 2, ,3, 4}
```
<br>

* ### Add set items
add() <br>
برای اضافه کردن یک عنصر به یک مجموعه استفاده میشود.
```python
thisset = {"apple", "banana", "cherry"}
thisset.add("orange")
print(thisset)
-> {'banana', 'orange', 'apple', 'cherry'}
```
<br>

update() <br>
برای ترکیب کردن دو مجموعه استفاده میشود.
```python
thisset = {"apple", "banana", "cherry"}
tropical = {"pineapple", "mango", "papaya"}
thisset.update(tropical)
print(thisset)
-> {'apple', 'mango', 'cherry', 'pineapple', 'banana', 'papaya'}
```
<br>

Discard() و remove() <br>
هر ۲ برای حذف کردن عنصری از داخل مجموعه ها استفاده میشود.
```python
thisset = {"apple", "banana", "cherry"}
thisset.remove("banana")
print(thisset)
-> {'apple', 'cherry'}
```
```python
thisset = {"apple", "banana", "cherry"}
thisset.discard("banana")
print(thisset)
-> {'apple', 'cherry'}
```
<br>

pop() <br>
این دستور به صورت رندوم یکی از عناصر داخل مجموعه را حذف میکند
```python
thisset = {"apple", "banana", "cherry"}
x = thisset.pop()
print(x)
print(thisset)
-> cherry
{'banana', 'apple'}
```
<br>

union() <br>
این دستور میتواند برای یک مجموعه سوم تعریف شود که از ترکیب ۲ مجموعه قبلی ساخته شده است.
```python
set1 = {"a", "b" , "c"}
set2 = {1, 2, 3}
set3 = set1.union(set2)
print(set3)
-> {3, 1, 'c', 2, 'a', 'b'}
```
<br>

* ### اجتماع گیری
```python
num = [1, 2, 1, 3, 4]

first = set(num)
sec = {1, 5}

print(first | sec)

➡️ {1, 2, 3, 4, 5}
```
<br>

symmetric_difference_update() و symmetric_difference() <br>
این دستور برعکس دستور قبل عمل میکند یعنی وجه اشتراک ۲ مجموعه را پاک میکند و بقیه عناصر آن را نگه میدارد.
```python
x = {"apple", "banana", "cherry"}
y = {"google", "microsoft", "apple"}
x.symmetric_difference_update(y)
print(x)
-> {'google', 'banana', 'microsoft', 'cherry'}
```
```python
x = {"apple", "banana", "cherry"}
y = {"google", "microsoft", "apple"}
z = x.symmetric_difference(y)
print(z)
-> {'google', 'banana', 'microsoft', 'cherry'}
```
<br>

* ### اشتراک گیری
```python
num = [1, 2, 1, 3, 4]

first = set(num)
sec = {1, 5}

print(first & sec)

➡️ {1}
```
<br>

intersection_update() و intersection() <br>
این دستور اشتراک ۲ مجموعه را میگیرد یعنی فقط عناصری که در هر ۲ مجموعه باشد را نگه میدارد.
```python
x = {"apple", "banana", "cherry"}
y = {"google", "microsoft", "apple"}
x.intersection_update(y)
print(x)
-> {'apple'}
```
```python
x = {"apple", "banana", "cherry"}
y = {"google", "microsoft", "apple"}
z = x.intersection(y)
print(z)
-> {'apple'}
```
<br>

متدهای دیگری که میتوانید در مجموعه ها از آنها استفاده کنید.
| Method |	Description |
| --- | --- |
| add() |	Adds an element to the set |
| clear() |	Removes all the elements from the set |
| copy() |	Returns a copy of the set |
| difference()	| Returns a set containing the difference between two or more sets |
| difference_update() |	Removes the items in this set that are also included in another, specified set |
| discard()	| Remove the specified item |
| intersection()	| Returns a set, that is the intersection of two other sets |
| intersection_update()	| Removes the items in this set that are not present in other, specified set(s) |
| isdisjoint()	| Returns whether two sets have a intersection or not |
| issubset()	| Returns whether another set contains this set or not |
| issuperset()	| Returns whether this set contains another set or not |
| pop()	| Removes an element from the set |
| remove()	| Removes the specified element |
| symmetric_difference()	| Returns a set with the symmetric differences of two sets |
| symmetric_difference_update()	| inserts the symmetric differences from this set and another |
| union()	| Return a set containing the union of sets |
| update()	| Update the set with the union of this set and others |
<br>
<br>

## Dictionaries
get() <br>
برای دست آوردن مقدار یک متغییر در دیکشنری ها استفاده میشود.
```python
thisdict = {
  "brand": "Ford",
  "model": "Mustang",
  "year": 1964
}
x = thisdict.get("model")
print(x)
-> Mustang
```
<br>

keys() <br>
با این دستور میتوان تمام متغییرهای درون دیکشنری را به دست آورد.
```python
thisdict = {
  "brand": "Ford",
  "model": "Mustang",
  "year": 1964
}
x = thisdict.keys()
print(x)
-> dict_keys(['brand', 'model', 'year'])
```
<br>

values() <br>
برای به دست آوردن تمام مقدارها استفاده میشود.
```python
 thisdict = {
  "brand": "Ford",
  "model": "Mustang",
  "year": 1964
}
x = thisdict.values()
print(x)
-> dict_values(['Ford', 'Mustang', 1964])
```
<br>

items() <br>
این دستور تمام مقدار ها و متغییر ها رو به صورت یک تاپل در یک لیست به ما برمیگرداند.
```python
thisdict = {
  "brand": "Ford",
  "model": "Mustang",
  "year": 1964
}
x = thisdict.items()
print(x)
-> dict_items([('brand', 'Ford'), ('model', 'Mustang'), ('year', 1964)])
```
<br>

update() <br>
برای تغییر دادن مقدار یک متغییر استفاده میشود.
```python
thisdict = {
  "brand": "Ford",
  "model": "Mustang",
  "year": 1964
}
thisdict.update({"year": 2020})
print(thisdict)
-> {'brand': 'Ford', 'model': 'Mustang', 'year': 2020}
```
<br>

همچنین به روش زیر هم میتوان اقدام کرد.
```python
car = {
"brand": "Ford",
"model": "Mustang",
"year": 1964
}
x = car.values()
car["year"] = 2020
print(x)
-> dict_values(['Ford', 'Mustang', 2020])
```
<br>

برای اضافه کردن یک آیتم درون یک دیکشنری باید به روش زیر اقدام کنیم.
```python
thisdict = {
  "brand": "Ford",
  "model": "Mustang",
  "year": 1964
}
thisdict["color"] = "red"
print(thisdict)
-> {'brand': 'Ford', 'model': 'Mustang', 'year': 1964, 'color': 'red'}
```
<br>

pop() و del() <br>
این دستور یک متغییر را با مقدار آن پاک میکند.
```python
thisdict = {
  "brand": "Ford",
  "model": "Mustang",
  "year": 1964
}
thisdict.pop("model")
print(thisdict)
-> {'brand': 'Ford', 'year': 1964}
```
```python
thisdict = {
  "brand": "Ford",
  "model": "Mustang",
  "year": 1964
}
del thisdict["model"]
print(thisdict)
-> {'brand': 'Ford', 'year': 1964}
```
<br>

popitem() <br>
برای پاک کردن اخرین آیتم درون دیکشنری از آن استفاده میشود.
```python
thisdict = {
  "brand": "Ford",
  "model": "Mustang",
  "year": 1964
}
thisdict.popitem()
print(thisdict)
-> {'brand': 'Ford', 'model': 'Mustang'}
```
<br>

متدهای دیگری که در دیکشنری میتوان از آن ها استفاده کرد.
| Method |	Description |
| --- | --- |
| clear()	| Removes all the elements from the dictionary |
| copy()	| Returns a copy of the dictionary |
| fromkeys()	| Returns a dictionary with the specified keys and value |
| get()	| Returns the value of the specified key |
| items()	| Returns a list containing a tuple for each key value pair |
| keys()	| Returns a list containing the dictionary's keys |
| pop()	| Removes the element with the specified key |
| popitem()	| Removes the last inserted key-value pair |
| setdefault()	| Returns the value of the specified key. If the key does not exist: insert the key, with the specified value |
| update()	| Updates the dictionary with the specified key-value pairs |
| values()	| Returns a list of all the values in the dictionary|
<br>
<br>

## If / Else
برای آنکه بتوانیم از تصمیم گیری در برنامه استفاده کنیم کاربرد دارد. <br>
برای استفاده از عبارت شرطی باید از if استفاده کنیم.
```python
temp = 35
if temp > 30 :
     print("it's warm")
     print("drink water")

➡️ it's warm
drink water
```
```python
temp = 20 
if temp > 30 
     print("it's warm")
     print("drink water")

➡️
```
<br>

اگر بخواهیم شرط دیگری اضافه کنیم باید از elif استفاده کنیم.
```python
temp = 20
if temp >30 : 
     print("it's warm")
elif temp > 20 :
     print("it's nice")

➡️ it's nice
```
<br>

و اگر بخواهیم تعریف کنیم ک شرط ما در هیچ یک از عبارات شرطی ما قرار نداشت چه اتفاقی بیوفتد، باید از else استفاده کنیم.
```python
temp = 15
if temp > 30 : 
     print("it's warm")
elif temp > 20 : 
     print("it's nice")
else : 
     print("it's cold")

➡️ it's cold
```
<br>
<br>

## while
در این حلقه ابتدا نفسر پایتون درست یا غلط بودن شرط مارا بررسی میکند، اگر درست بود وارد حلقه میشود و دستور های داخل حلقه را اجرا میکند و در صورتی که غلط بود وارد حلقه نمیشود و ادامه دستورات خارج از حلقه را اجرا میکند
```python
number = 100

while number > 0 : 
     print(number)
     number // = 2

print("done")

➡️ 100
50
25
12
6
3
1
done
```
<br>
<br>

## for
برای تکرار استفاده میشود
```python
for number in range(4) : 
     print("massage")

➡️ massage
massage
massage
massag
```
<br>

غیر از ()range میتوان از 'str' و لیست ها هم استفاده کرد

```python
for x in "omid" : 
     print(x)

➡️o
m
i
d
```
<br>

برای ایجاد یک متغییر به صورت لیست باید از '[ ]' استفاده کرد

```python
number = [1, 2, 3, 4]

for x in [1, 2, 3, 4]
     print)x)

➡️ 1
2
3
4
```
<br>

در حلقه for  میتوانیم محموده مشخص کنیم و همچنین میتوانیم اضافه کنیم که این محدوده به شکل شمارده شود.
```python
for x in range(2, 30, 3):
  print(x)
-> 2, 5, 8, 11, 14, 17, 20, 23, 26, 29
```
<br>

* ### enumerate()
یک تابعی است که ورودی آن از نوع پیمایشگر میباشد. کار آن این است که اندکس و اعضای آن پیمایشگر را به نمایش میگذارد.
```python
l = ["a", "b", "c", "d"]
for i, j in enumerate(l) :
 print(i , ":" , j)
```
اگر بخواهیم که شمارش ایندکس ها از عدد دلخواه ما باشد به شکل زیر عمل میکنیم :
```python
l = ["a", "b", "c", "d"]
for i, j in enumerate(l, 5) :
 print(i , ":" , j)
```
<br>

* ### reversed()
برای برعکس شمارده شدن یک پیمایشگر استفاده میشود.
```python
x = ["ali", "reza", "neda", "mina]
for i in reversed(x):
 print(i)
```
<br>

استفاده از دستور else در حلقه for
```python
successful = true

for number in range(3) : 
     print("attempt")
     if succssful : 
          print("successful")
          break
     else : 
          print("not successful")

➡️ attempt
successful
```
<br>

حلقه های تو در تو
```python
for x in range(4) : 
     for y in range(2):
          print(f"({x}, {y})")

➡️(0, 0)
(0, 1)
(1, 0)
(1, 1)
(2, 0)
(2, 1)
(3, 0)
(3, 1)
```
<br>
<br>

## fanction

یک قطعه کد میباشد که میتوان آن را بارها استفاده کنید. <br>
برای ساخت یک فانکشن باید از ()def استفاده کنیم که بعد از آن باید یک اسم برای فانکشن خود استفاده کنیم.
```python
def greet() : 
     print("hi every one")

greet()

➡️ hi every one
```
<br>

* ### parametr
```python
def greet(firstname, last name) : 
     print(f"(hi frist name}, {last name}")

greet(reza, amiri)

➡️ hi reza amiri
```
<br>

### انواع فانکشن
نوع اول یک task را انجام میدهد و نوع دوم یک مقدار را به ما برمیگرداند. <br>
برای اینکه بتوانیم از فانکشن نوع دوم استفاده کنیم باید از کلمه return استفاده کنیم
```python
def get_greeting(frist_name) : 
     return f"hi {frist_name}

message = get_greeting("omid")

➡️ hi omid
```
<br>

* ### keyword arguments
در واقع مقادیری هستند که نگام صدا زدن تابع به آن میدهیم.
```python
def increment(number, by) : 
     return number + by 

print(increment(1, 2))

➡️ 3
```
```python
def increment(number, by)
     return number + by 

print(increment(number = 1, by = 2))

➡️ 3
```
<br>

* ### arguman difult
برای موقعی به کار میرود که ما بخواهیم در صورت وارد نکردن ورودی دوم از دیفالتی که برای آن تعریف کردیم استفاده کنیم
```python
def increment(number, by = 1) :
     return number + by 

print(increment(20))

➡️ 21
```
<br>

* ### *arguman
برای این به کار میرود که به تعداد دلخواه بتوانیم ورودی بدهیم
```python
def multiply(*numbers) : 
     totals = 1 
     for number in numbers : 
          totals *= number
     return total

print(multiply(2, 4, 5, 6, 9))

➡️ 2160
```
<br> 

* ### **arguman
میتوان هر مقدار کلید مقدار به متغیر داد
```python
def save_user(**user) : 
     print(user)

save_user(id = 1, name = ali, age = 32)

➡️ {id = 1, name = ali, age = 32}
```
<br>
تایپ این مقدار از نوع دیکشنری میباشد<br>

* ### doc string
این ویژگی برای تعریف کردن تابع استفاده میشود یعنی توضیحاتی که با آن میتوان نحوه عمکرد تابع را متوجه شد. برای اینکار باید از (""" """) استفاده کنیم و متن خود را بین آن ها قرار دهیم.<br>
و گر بخواهیم به اطلاعات آن توضیحات دسترسی پیدا کینم میتوانیم از این دستور استفاده کنیم :
```python
def max3(x, y, z):
 """Receives three number as onput and return the largest of them"""
 return max(x, y, z)
print(max.__doc__)
-> Receives three number as onput and return the largest of them
```
<br>

همچنین در صورت نیاز برای خواندن نحوه عمل کرد یم تابع در یک ماژول دیگر میتوان از این روش استفاده کرد فقط کافیست به جای max3 نام آن تابع را استقاده کنید.<br>
این نکته را در نظر داشته باشید که توضیحات باید اولین خط از یک تابع باشند یعنی قبل آن ها متغیر یا دستوری تعریف نشده باشد.<br>
همچنین برای دستری داشتن به این توضیحات میتوانیم از دستور `(max3)help` نیز کمک بگیریم.<br>

* ### scope
به این معنی ک اگر در یک function یک متغییر یا یک پارامتر تعریف کنیم آن متغییر پارامتر دیگر متعلق به آن function میباشد و بیرون از آن اعتباری ندارند.
```python
def greet():
     message = "a"

print(message)

➡️ Error : name 'message' is not defined
```
<br>

## lambda function
یک تابع بی نام است که در آن میتوان اعمال کوچکی را تعریف کرد.<br>
ساختار lambda به این شکل این که ما ابتدا خود تابع را فرا میکنیم سپس در جلوی آن ورودی را تعریف کرده و در جلوب آن عملی که میخواهم در آن انجام شود را مبنویسیم.
```python
a = lambda x : x**2
print(a(5))
-> 25
```
<br>
در نظر داشته باشید که این تابع را حتما باید در یک متغیر دیگر ذخبره کرد.<br>

* ### map()
این دستور ۲ ورودی دریافت میکند، یکی از ورودی ها از نوع تابع و دیگری از توع لیست است.<br>
کار آن به این کل است که اعضای لیستی که به آن دادیم را به ترتیب به عنوان ورودی به تابع میدهد و نتیجه را به ما بر میگرداند.<br>
برای دسترسی و استفاده از آن باید این دستور را ابتدا به لیست تبدیل کرد.
```python
def func(x):
 return x**2

list = [1, 2, 3, 4]
new = list(map(func, list))
print(new)
print(lsit)

-> [1, 4, 9, 16]
-> [1, 2, 3, 4]
```
<br>

همین کار را میتوانیم به کمک تابع lambda به صورت خلاصه تر انجام دهیم.
```python
list = [1, 2, 3, 4]
new = list(map(lambda x : x**2, list))
print(new)

-> [1, 4, 9, 16]
```
```python
Items = [
     ("product1", 10)
     ("product2", 9)
     ("product3", 12)
]

prices = list(map(lambda item: item[1], items))]
print(prices)

-> [9, 10, 12]
```
<br>

* ### filter()
کار برد این دستور به این شکل است که ورودی های یک لیست را به تابع میدهد و اگر true بود آن ها را نگه میدارد و اگر false بود آن ها را حذف میکند.<br>
در نظر داشته باشید که این دستور هم ۲ ورودی میگرید یکی تابع و دیگری لیست.<br>
برای دسترسی و استفاده از آن باید این دستور را ابتدا به لیست تبدیل کرد.
```python
def func(x):
 if x > 5:
  return True
 else:
  return False

list = [1, ,9, 10, 0, 5, 4, 2, 3, 4, 5, 6, 7]
new = list(filter(func, lis))
print(new)

-> [9, 10, 6, 7]
```
<br>

همچنین میتوان این کار با با کمک تابع lambda به صورت کوتاه تری نوشت.
```python
list = [1, ,9, 10, 0, 5, 4, 2, 3, 4, 5, 6, 7]
new = list(filter(lambda x : x > 5, lis))
print(new)

-> [9, 10, 6, 7]
```
```python
Items = [
     ("product1", 10)
     ("product2", 9)
     ("product3", 12)
]

filtered = list(filter(lambda item: item[1] >= 10, items))]
print(filtered)

-> [('product3', 12), ('product1', 10)]
```
<br>

* ### list comprehension
برای مرتب کردن کد به کار میرود و میتواند جایگزین filter , map باشد
```python
Items = [
     ("product1", 10)
     ("product2", 9)
     ("product3", 12)
]

price = [item[1] for item in items]

print(price)

➡️ [9, 10, 12]
```
```python
Items = [
     ("product1", 10)
     ("product2", 9)
     ("product3", 12)
]

filtered = [item for item in items if item[1] >= 10]

print(filtered)

➡️ [('product3', 12), ('product1', 10)]
```
<br>
<br>

## Decorator
برای اعمال تغیرات یک تابع به وسیله تابع دیگری به کار میرود.<br>
برای اینکار باید ابتدا یک تابع معرفی کنیم که میخواهیم با توجه به آن بر روی توابع دیگر ما آن تغیرات اعمال شوند.
```python
def dec(func):
 def inner():
  print("*" * 20)
  func()
  print("*" * 20)
 return inner

@dec
def f()
 print("ali")

@dec
def f2():
 print("omid")

f()
f2()

-> ********************
-> ali
-> ********************
-> ********************
-> omid
-> ********************
```
<br>

همچینین ما میتوانیم از دکوراتور های متعددی بر روی یک تابع استفاده کنیم
```python
def plus(func):
	def inner(*x, **y):
		print("+" * 20)
		func(*x, **y)
		print("+" * 20)
	return inner

def star(func):
 def inner(*x, **y):
  print("*" * 20)
  func(*x, **y)
  print("*" * 20)
 return inner

@plus
@star
def msg(name):
 print("i am ", name)

msg(ali)

_> ++++++++++++++++++++
-> ********************
-> ali
-> ********************
-> ++++++++++++++++++++
```
<br>

همچنین میتوانیم برای دکوراتور ها ورودی هم در نظر گرفت، به این شکل که تابع دکوراتور باید از چند تابع تشکیل شود
```python
def star(num):
	def inner1(func):
		def inner2(*args, **kwargs):
			print("*" * num)
			func(*args, **kwargs)
			print("*" * num)
		retunr inner2
	return inner1

@star(5)
def msg(name):
	print("i am", name)

msg(ali)

-> *****
-> ali
-> *****
```
<br>

به مثال زیر توجه کنید <br>
این برنامه قصد دارد که اجازه دست رسی یک سری از کاربر ها را به برنامه قطع کند
```python
password = {"ali" : "24369871", "reza01" : "547925", "neda1375" : 645564"}
blacklist = {"neda1375", "reza01"}

def ban(func):
	def inner(*args, **kwargs):
		if args[0] in blacklist:
			print("This user is blackes!!!")
		else :
			func(*args, **kwargs)
	return inner


@ban
def print_password(username):
	print(username, " : ", password[username])


@ban
def change_password(username, new_password)
	password[username] = new_password
	print(username, " : ", password[username])


print_password(ali)
change_password(neda1375, 12345)

-> ali : 24369871
-> This user is blocked!!!
```
<br>

مثال زیر برای به دست آوردن زمانی است که یک تابع برای اجرا لازم دارد
```python
from time import perf_counter

def time_calculation(func):
	def wrapper_decorator(*args, **kwargs):
		start_time = perf_counter()
		value = func(*args, **kwargs)
		end_time = perf_counter()
		run_time = end_time - start time
		print("The run time of", func.__name__, "is", run_time)
		return value
	return wrapper_decorator


@time_calculation
def A (y):
	sum = 0
	for i in range(y):
		s += i**2


@time_calculation
def B (x):
	fact = 1
	for i in range(1, x+1):
		facr *= i


A(100000)
B(10000)

-> 5.684652135
-> 12.43184654
```
<br>
<br>

## Generator
جنراتورها یا مولد ها به ما در تمیز کردن و بهمینه تر شدن کد ها کمک میکند <br>
جنراتور ها ماهیت تنبلی دارند، یعنی تمام اطلاعات را هم زمان ذخیره نمیکنند و تنها در زمانی اطلاعات را به ما نشان میدهند که به آن ها نیاز داشته باشیم <br>
برای اینکه بتوانیم یک جنراتور بسازیم باید از کلمه کلیدی 'yield' استفاده کنیم <br>
و برای این که بتوانیم به آن دسترسی داشته باشیم باید از ()next استفاده کنیم <br>
```python
def func(x):
	yield x**2

x = func(5)
print(next(x))

-> 25
```
<br>

رفتار این تابع به این شکل است که هر بار که آن را به وسیله ()next صدا میزنیم مرحله بعدی را اجرا میکند
```python
def func(x):
	print("reza")
	yield x**2
	print("hello")
	yield x
	print("ok")
	yield x - 2

x = func(5)
print(next(x))

-> reza
-> 25
```
```python
def func(x):
	print("reza")
	yield x**2
	print("hello")
	yield x
	print("ok")
	yield x - 2

x = func(5)
print(next(x))
print(next(x))
print(next(x))

-> reza
-> 25
-> hello
-> 5
-> ok
-> 3
```
<br>

برنامه هر بار که به دستور yield برسد مکث میکند و منتظر میماند تا دوباره آن را صدا بزنیم تا ادامه برنامه را برای ما اجرا کند <br>
و در صورتی که تعداد دفعاتی که آن را صدا میزنیم از خود آن بیشتر باشد با ارور مواجه میشویم <br>

* ### for in generator
```python
def my_generator():
	for i in range(1000):
		yield i**2


g = my_generator()
print(next(g))
print(next(g))
print(next(g))
print(next(g))

-> 0
-> 1
-> 4
-> 9
```
<br>

میتوانیم از این تابع هر کجا که نیاز داشتیم استفاده کنیم و هر دفعه که آن را صدا بزنیم عدد بعدی را به ما نشان میدهد <br>
اگر بخواهیم تمام عناصر داخل این تابع را صدا بزنیم میتوانیم به روش زیر عمل کنیم
```python
def my_generator():
	for i in range(5:
		yield i**2


g = my_generator()
for i in g:
	print(i)

-> 0
-> 1
-> 4
-> 9
-> 16
```
<br>

در این روش بعد از اینکه به انتهای شمارش رسید دیگر با ارور مواجه نمیشویم <br>
همچنین میتوانیم از جنراتور ها به صورت تو در تو استفاده کنیم. یعنی یک جنراتور را به عنوان ورودی به یک جنراتور دیگر بدهیم
```python
def square_gn(nums):
	for i in nums:
		yield i**2


def even_gn(nums):
	for i in nums:
		if i % 2 == 0:
			yield i


print(sum(square_gn(even_gn([1, 2, 3, 4, 7, 9, 1, 5, 2, 9, 6]))))
-> 60
```
<br>

* ### Coroutine
رفتاری در جنراتور هاست که باعث ایجاد همزمان خروجی و ورودی میشود <br>
```python
def my_gen():
	print("start!!")
	while True:
		name = yield
		print("My name is", name)


g = my_gen()
next(g)
g.send("reza")
g.send("ali")

-> start!!
-> My name is reza
-> My name is ali
```
<br>

در اینجا ما yield را به یک متغیر نسبت دادیم <br>
سپس به کمک متد ()send یک مقدار را به آن متغیر نسبت دادیم و با هر بار صدا زدن این متد میتوانیم یک مقدار جدید به آن متغیر نسبت دهیم <br>
این نکته را در نظر بگیرید که اگر بخواهیم از این متد استفاده کنیم حتما باید قبل از آن از ()next استفاده بکنیم
 <br>
 <br>

## Function attribute
هر تابع دارای یک سری ویژگی ها و صفات میباشد که میتواند کار خاصی را انجام بدهد <br>

* ### __name__
این متد یا ویژگی برای این به کار میرود که بخواهیم اسم تابع را به دست بیاوریم
```python
def fun():
	pass


print(func.__name__)
-> func
```
<br>

* ### __doc__
هر تابع میتواند برای خود یک دفترچه داشته باشد که کار آن معرفی تابع و نحوه عملکرد تابع را توضیح میدهد <br>
این متن باید در اولین خط بعد از ساخت تابع ایجاد شود <br>
این متد برای این استفاده میشود که ما بخوایهم به آن متن دسترسی داشته باشیم
```python
def func():
	"this is a function"
	pass


print(func.__doc__)
-> this is a function
```
<br>

همچنین ما میتوانیم برای توابع خود ویژگی هایی که میخواهیم را اضافه کنیم <br>
برای این کار کافیست بعد از اسم تابع یک نقطه بگذاریم و سپس برای آن ویژگی اسم در نظر بگیرم و آن را مقدار دهی کنیم
```python
def ave(li):
	return sum(li) / len(li)


def ave2(li):
	return sum(li) / len(li)


ave.school_name = "tabatabayi"
ave2.school_name = "bahonar"

print(ave.school_name)
print(ave2.school_name)

-> tabatabayi
-> bahonar
```
<br>

* ### setattr()
این دستور برای تنظیم کردن یک ویژگی برای تابع به کار میرود به عبارتی همان کاری که در بالا انجام میدادیم را میتوانیم به کمک این دستور انجام دهیم  <br>
نحوه کارکرد این دستور به این شکل است که باید سه مورد را به عنوان ورودی به آن بدهیم <br>
وردی اول باید نام تابع باشد، ورودی دوم اسم صفت یا متدی که میخواهیم به آن بدهیم و سومین ورودی باید نقداری باشد که میخواهیم آن متد داشته باشد
```python
def ave(li):
	return sum(li) / len(li)


setattr(ave, "school_name", "bahonar")
print(ave.school_name)

-> bahonar
```
<br>
<br>

## Recursive Function
تابع بازگشتی به تابعی میگویند که درون بدنه خود خود تابع را صدا بزند <br>
توابع بازگشتی از دو بخش درست میشوند، بخش اول آنها ساختاری است که باعث توقف تابع میشود و بخش دوم آنها ساختاری است که باعث ادامه تابع میشود

```python
def fact(x):
	if x == 0 or x == 1:
		return 1
	return x * fact(x-1)

-> 120
```
<br>

## Arrays
برای دنباله های طولانی تر از اعداد استفاده میشود. آرایه فضای کمتر را اشغال میکند و همچنین  عملکرد بهینه تری را دارد
برای استفاده ابتدا باید ماژول آن را وارد کنیم
```python
from array import array
```
<br>

برای استفاده از آرایه باید 2 ورودی به آن بدهیم، یکی از آن ها تایپ کد است و دیگری لیستی که میخواهیم به آن بدهیم. <br>
[type code](https://docs.python.org/3/library/array.html) <br>
عناصر در آرایه باید از یک تایپ باشند.
```python
from array import array

number = array("i", [1, 2, 3])
print(number)

➡️ array('i', 1, 2, 3)
```
<br>
تمام مواردی که در لیست کاربرد دارد در آرایه ها هم صادق میباشند.
<br>
<br>

## Classes
کلاس وسیله ای است برای ساخت ابجکت و ابجکت نمونه ای از یک کلاس میباشد. <br>
برای ساخت کلاس باید از کلمه کلیدی class استفاده کنیم. <br>
برای نام گذاری کلاس ها باید حروف اول هر کلمه به صورت بزرگ نوشته شود. 
```python
class MyClass :
	  		x = 5
m = MyClass()
print(m.x)
-> 5
```
<br>

* ### __init__()
این فانکشن در ابتدا و در شروع تمام کلاس ها اجرا میشود. <br>
کار این فانکش مقدار دادن و تنظیم کردن اشیا داخل کلاس ها است.
```python
class Person :
  def __init__(self, name, age) :
    self.name = name
    self.age = age
p1 = Person("John", 36)
print(p1.name)
print(p1.age)
-> John
36
```
<br>

* ### __srt__()
این فانکشن زمانی استفاده میشود که ما بخواهیم خروجی ما از کلاس به صورت 'str' باشد. <br>
اگر از این فانکشن برای خروجی 'str' استفاده نکنیم، خروجی به شکل زیر خواهد بود :
```python
class Person :
  def __init__(self, name, age) :
    self.name = name
    self.age = age
p1 = Person("John", 36)
print(p1)
    <__main__.Person object at 0x15039e602100>->    
```
<br>

اما اگر از این فانکشن استفاده کنیم، خروجی به شکل زیر میشود.
```python
class Person :
  def __init__(self, name, age) :
    self.name = name
    self.age = age
  def __str__(self) :
    return f"{self.name}({self.age})"    
p1 = Person("John", 36)
print(p1)
->  John(36)
```
<br>

همچنین میتوان در کلاس ها فانکشن های مختلفی را برای تعریف خصوصات یک شی تعریف کرد.
```
class Person :
  def __init__(self, name, age) :
    self.name = name
    self.age = age
  def myfunc(self) :
    print("Hello my name is " + self.name)
p1 = Person("John", 36)
p1.myfunc()
-> Hello my name is John
```
<br>

* ### self
این پارامتر اشاره به کلاسی دارد که در حال حاضر از آن استفاده میکنیم و این امکان را به ما میدهید که مقدار ها و متغیییر هایی را در داخل کلاس معرفی کینم. <br>
این پارامتر لزوما یک پارامتر با اسم ثابت نیست و در صورت دلخواله میتوان اسم آن را عوض کرد ولی برای اینکه بتواند کار خود را انجام دهد باید آن را در ابتدای پارامتر های داخل کلاس معرفی کنیم.
```python
class Person :
  def __init__(mysillyobject, name, age) :
    mysillyobject.name = name
    mysillyobject.age = age
  def myfunc(abc) :
    print("Hello my name is " + abc.name)
p1 = Person("John", 36)
p1.myfunc()
-> Hello my name is John
```
<br>

برای اینکه بتوانیم به یک متغییر خارج از کلاس دسترسی اشته باشیم و برای آن مقدار تعریف کینم باید به روش زیر اقدام کنیم.
```
class Person :
  def __init__(self, name, age :
    self.name = name
    self.age = age
  def myfunc(self) :
    print("Hello my name is " + self.name)
p1 = Person("John", 36)
p1.age = 40
print(p1.age)
-> 40
```
<br>

* ### del
برای پاک کردن مقدار یک متغییر استفاده میشود.
```python
class Person :
  def __init__(self, name, age) :
    self.name = name
    self.age = age
  def myfunc(self) :
    print("Hello my name is " + self.name)
p1 = Person("John", 36)
del p1
print(p1)
-> NameError: 'p1' is not defined
```
<br>

* ### pass
یک کلاس را نمیتوان خالی رها کرد برای اینکه کلاس خالی نباشد میتوانیم از این دستور در آن استفاده کنیم.
```python
class Person :
  pass
```
<br>

* ### class vs instance attributes

کلاس اتریبیوت برای همه ابجکت ها یکسان عمل میکند ولی اینستنس اتریبیوت مختص ب هر ابجکت میباشد. <br>
به کلاس اتریبیوت میتوان به دو صورت دسترسی پیدا کرد هم با خواندن آبجکت و هم با خواندن کلاس.
```python
class Point : 
 default_color = "red"

 def __init(self, x, y) : 
  self.x = x
  self.y = y

 def draw(self) : 
  print(f"Point({self.x}, {self.y})")

point = Point(1, 3 )

print(point.default_color)
print(Point.default.color)

-> red
-> red
```
<br>

همچنین میتوانیم مقدار اتریبیوت را به دو صورت تغییر دهیم، هم به وسیله کلاس و هم به وسیله آبجکت. <br>
در نظر داشته باشید که اگر به وسیله آبجکت اتریبیوت کلاس را تغییر بدهیم فقط همان آبجکت تغییر میکند
```python
class Point : 
 default_color = "red"

 def init(self, x, y) : 
  self.x = x
  self.y = y

 def draw(self) : 
  print(f"Point({self.x}, {self.y})")

point = Point(1, 3 )
another = Point(5, 6)

Point.default_color = "blue" 

print(point.default_color)
print(Point.default.color)
print(another.default_color)

-> blue
-> blue
-> blue
```
```python
class Point : 
 default_color = "red"

def init(self, x, y) : 
  self.x = x
  self.y = y

 def draw(self) : 
  print(f"Point({self.x}, {self.y})")

point = Point(1, 3 )
another = Point(5, 6)

point.default_color = "blue" 

print(point.default_color)
print(Point.default.color)
print(another.default_color)

-> blue
-> red
-> red
```
<br>

* ### factory method
برای این به کار میرود که بخواهیم یک اتریبیوت ثابت داشته باشیم.
```python
class Point : 

 def init__(self, x, y) : 
  self.x = x
  self.y = y

 def zero (cls) : 
  return cls(0, 0)

 def draw(self) : 
  print(f"Point({self.x}, {self.y})")

point = Point.zero( )
point.draw( )

➡️ Point(0, 0)
```
<br>

* ### مقایسه آبجکت ها
به صورت پیش فرض مفسر پایتون مکان ذخیره سازی آبجکت ها را در رم مقایسه میکند. <br>
و اگر بخواهیم که به صورت دلخواه آن را تغییر بدهیم باید از روش زیر استفاده کنیم. <br>
برای اینکار باید از مجیک متد eq استفاده کنیم
```python
class Point : 

 def init(self, x, y) : 
  self.x = x
  self.y = y

 def eq(self, other):
  return self.x == other.x and self.y == other.y

 def draw(self) : 
  print(f"Point({self.x}, {self.y})")

point = Point(1, 3)
another = Point(4, 5)
print(point == another)

➡️ false
```
<br>

* ### عملگرهای محساباتی بر روی آبجکت
برای اعمال کردن عملیات های ریاضی مانند (جمع، تفریق، ضرب و تقسیم) استفاده میشود. <br>
برای اینکه بتوانیم آبجکت ها را با یک دیگر جمع کینم باید از مجیک متد add استفاده کنیم.
```python
class Point : 

 def init(self, x, y) : 
  self.x = x
  self.y = y

 def str(self):
  return f"({self.x}, {self.y})"

 def add(self, other):
  return Point(self.x + other.x , self.y + other.y)

point = Point(1, 3)
another = Point(4, 5)

print(point + another)

➡️ (5, 8)
```
<br>
<br>

## Inheritance
این ویژگی در پایتون این امکان را به ما میدهد که کلاس جدید ما ویژگی های کلاس قبلی را به ارث ببرد. یعنی یک کلاس جدید با همام ویژگی های کلاس قبل.
* ### Parent class
کلاسی است که ویژگی های از آن به ارث میرسد. آنرا کلاس پایه هم مینامند. <br>
هر کلاسی میتواند به عنوان کلاس پایه تعریف شود.
```python
class Person:
  def __init__(self, fname, lname):
    self.firstname = fname
    self.lastname = lname
  def printname(self):
    print(self.firstname, self.lastname)
#Use the Person class to create an object, and then execute the printname method:
x = Person("John", "Doe")
x.printname()
-> John Doe
```
<br>

* ### Child class
این کلاسی است که با ویژگی های به ارث برده ساخته میشود. <br>
برای ساخت این کلاس کافیست که اسم کلاس پایه را به عنوان پارامتر در آن وارد کنید.
```python
class Person:
  def __init__(self, fname, lname):
    self.firstname = fname
    self.lastname = lname

  def printname(self):
    print(self.firstname, self.lastname)
class Student(Person):
  pass
x = Student("Mike", "Olsen")
x.printname()
-> Mike Olsen
```
<br>

اگر در روند به ارث بردن یک کلاس در آن فانکشنی اضافه کنیم که در کلاس مادر وجود دارد، کلاس فرزند آن فانکشن به ارث برده را نادیده میگیرد و از اطلاعات فانکشن خود استفاده میکند. <br>
برای نگه داشتن تنظیمات آن میتوانیم به روش زیر عمل کنیم :
```
class Person:
  def __init__(self, fname, lname):
    self.firstname = fname
    self.lastname = lname
  def printname(self):
    print(self.firstname, self.lastname)
class Student(Person):
  def __init__(self, fname, lname):
    Person.__init__(self, fname, lname)
x = Student("Mike", "Olsen")
x.printname()
-> Mike Olsen
```
<br>

* ### Super()
این فانکشن این اجازه را به کلاس فرزند میدهد که تمام ویژگی های کلاس مادر را به ارث ببرد.
```python
class Person:
  def __init__(self, fname, lname):
    self.firstname = fname
    self.lastname = lname
  def printname(self):
    print(self.firstname, self.lastname)
class Student(Person):
  def __init__(self, fname, lname):
    super().__init__(fname, lname)
x = Student("Mike", "Olsen")
x.printname()
-> Mike Olsen
```
<br>

با استفاده از این فانکشن دیگر نیازی نست اسم پرامتر ها را وارد کید بلکه این دستور تمام ویژگی ها وتنظیمات را از کلاس مادر به ارث میبرد.
<br>
<br>

## Iterator
یک شی است که شامل تعداد قابل شمارشی از مقادیر است.<br>
یک شی قابل پیمایش است به این معنی که میتوانیم در مقادیر آن جستوجو کنیم.<br>
این دستور در واقع یک شی است که باعث اجرای پیمایشگر میشود و آن شامل متد های ‘()__iter__’ و ‘()__next__’ میشود.<br>

* ### Iterator vs Iterable
لیست ها، تاپب ها، مجموعه ها و دیکشنری ها پیمایشگر حساب میشوند.<br>
از متد ()iter میتوان برای پیمایش آن ها استفاده کرد.
```python
mytuple = ("apple", "banana", "cherry")
myit = iter(mytuple)
print(next(myit))
print(next(myit))
print(next(myit))
-> apple
banana
cherry
```
<br>

همچنین ‘str’ ها هم قابل پیمایش هستند که میتوان به صورت زیر آنها را هم پیمایش کرد:
```python
mystr = "banana"
myit = iter(mystr)
print(next(myit))
print(next(myit))
print(next(myit))
print(next(myit))
print(next(myit))
print(next(myit))
-> b
a
n
a
n
a
```
<br>

* ### Create an Iterator
برای اینکه بتوانیم یک کلاس یا آبجکت قابل پیمایش بسازیم باید از متد های ‘()iter’ و ‘()next’ استفاده کنیم.<br>

__iter__()<br>
شما میتوانیم عملیاتی که میخواهید روی آن انجام دهیم ولی در نظر داشته باشید که همیشه خود شی قابل پیمایش را برمیگرداند.<br>
__next__()<br>
میتوانید عملیاتی که میخواهید را روی آن انجام دهیم و آن همیشه عنصر بعدی دنباله را به شما برمیگرداند.
```python
class MyNumbers:
  def __iter__(self):
    self.a = 1
    return self
  def __next__(self):
    x = self.a
    self.a += 1
    return x
myclass = MyNumbers()
myiter = iter(myclass)
print(next(myiter))
print(next(myiter))
print(next(myiter))
print(next(myiter))
print(next(myiter))
-> 1
2
3
4
5
```
<br>

* ### StopIteration
اگر ب اندازه کافی از دستور next یا حلقه for استفاده کینم این عمل میتواند تا بینهایت ادامه پیدا کند. برای جلوگیری از این کار میتوانیم از این دستور استفاده کنیم. 
```python
class MyNumbers:
  def __iter__(self):
    self.a = 1
    return self
  def __next__(self):
    if self.a <= 20:
      x = self.a
      self.a += 1
      return x
    else:
      raise StopIteration
myclass = MyNumbers()
myiter = iter(myclass)
for x in myiter:
  print(x)
-> 1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13, 14, 15, 16, 17, 18, 19, 20
```
<br>
<br>

## Polymorphism
این لغتی در پایتون و برنامه نویسی به چیزی اتلاق میشود که با یک اسم بتواند در جاهای مختلف کار های مختلف انجام دهد.
```python
class Car:
  def __init__(self, brand, model):
    self.brand = brand
    self.model = model

  def move(self):
    print("Drive!")

class Boat:
  def __init__(self, brand, model):
    self.brand = brand
    self.model = model

  def move(self):
    print("Sail!")

class Plane:
  def __init__(self, brand, model):
    self.brand = brand
    self.model = model

  def move(self):
    print("Fly!")

car1 = Car("Ford", "Mustang")       #Create a Car class
boat1 = Boat("Ibiza", "Touring 20") #Create a Boat class
plane1 = Plane("Boeing", "747")     #Create a Plane class

for x in (car1, boat1, plane1):
  x.move()
-> Drive!
Sail!
Fly!
```
<br>

همچنین میتوانیم این دستور را در کلاس های فرزند هم اعمال کنیم.
```python
class Vehicle:
  def __init__(self, brand, model):
    self.brand = brand
    self.model = model

  def move(self):
    print("Move!")

class Car(Vehicle):
  pass

class Boat(Vehicle):
  def move(self):
    print("Sail!")

class Plane(Vehicle):
  def move(self):
    print("Fly!")

car1 = Car("Ford", "Mustang") #Create a Car object
boat1 = Boat("Ibiza", "Touring 20") #Create a Boat object
plane1 = Plane("Boeing", "747") #Create a Plane object

for x in (car1, boat1, plane1):
  print(x.brand)
  print(x.model)
  x.move()
-> Ford
Mustang
Move!
Ibiza
Touring 20
Sail!
Boeing
747
Fly!
```
<br>
<br>

## Try/Except
یک سری از ارور ها هستند که باعث کرش کردن برنامه میشوند.

* ### هندل کردن استثنا ها
برای از بین بردن ارور باید از روش زیر استفاده کنیم

```python
try : 
          age = int(input("age : "))
expect ValueError : 
          print("you didn't enter a valid age")

➡️ age : a
you didn't enter a valid age
```
<br>

* ### finally
بلاک فاینالی در هر صورت اجرا میشود یعنی هم در صورت داشتن ارور اجرا میشود هم در صورت نداشتن ارور
```python
try : 
          file = open("content.txt")
          age = int(input("age : "))
          xfactor = 10/age

expect (ValueError, ZeroDivisionError)  : 
          print("you didn't enter a valid age")

else :
          print("No exceptions where thrown")

finally : 
          file.close()

➡️ age : a
you didn't enter a valid age
```
<br>

* ### the with statement
یک روش جایگزین برای روش finally میباشد. <br>
این روش بر روی بعضی از ابجکت ها کار میکند.
```python
try : 
          with open("content.txt") as file : 
                    print("file oppened")

          age = int(input("age : "))
          xfactor = 10/age

expect (ValueError, ZeroDivisionError)  : 
          print("you didn't enter a valid age")

else :
          print("No exceptions where thrown")
```
<br>

در این روش مفسر پایتون بعد از اتمام کار فایل خوانده شده را میبندد. <br>
اگر بخواهیم خروجی های یک فایل را درون فایل دیگه ای بریزیم باید به شکل زیر عمل کنیم.
```python
with open("content.txt") as file, open("another.txt") as target : 
          print("file oppened")
```
<br>

* ### پرتاب استثنا
یعنی استثناهای خودمان را برای برنامه تعریف کنیم. <br>
برای این کار باید از کلمه کلیدی raise استفاده کنیم.
```python
def calculate_xfactor(age) : 
          if age <= 0 :
                    raise ValueError("age cannot be 0")
          return 10/age

calculate_xfactor(-1)

➡️ ValueError : age cannot be 0
```
<br>

برای هندل کردن این استثنا باید از روش زیر عمل کینم
```python
def calculate_xfactor(age) : 
          if age <= 0 :
                    raise ValueError("age cannot be 0")
          return 10/age

try : 
          calculate_xfactor(-1)

except ValueError as ex : 
          print(ex) 

➡️ ValueError : age cannot be 0
```
<br>

* ### لیست کامل استثناها

[https://docs.python.org/3/library/exceptions.html#exception-hierarchy](https://docs.python.org/3/library/exceptions.html#exception-hierarchy) <br>
اکسپشن ها از یک ساختار درختی درست شده اند که اگه از سر شاخه آن ها استفاده کنیم میتوانیم ارور هایی ک در زیرشاخه آن هست را هم هندل کنیم. <br>

* ### هزینه exception
استثنا ها یک هزینه زمانی دارند یعنی زمانی ک میخواهد برای اجرا شدن بیشتر است. <br>
**روش جایگزین**
```python
def calculate_xfactor(age) : 
          if age <= 0 :
                 return None
          return 10/age

xfactor = calculate_xfactor(-1)

if xfactor == None : 
          print("age cannot be 0 ")

➡️ age cannot be 0
```
<br>

برای انجام مقایسه زمان انجام برنامه باید از ماژول timeit استفاده کنیم
```python
from timeit import timeit

code 1 = """
def calculate_xfactor(age) : 
          if age <= 0 :
                    raise ValueError("age cannot be 0")
          return 10/age

try : 
          calculate_xfactor(-1)

except ValueError as ex : 
          pass
"""

code2 = """
def calculate_xfactor(age) : 
          if age <= 0 :
                 return None
          return 10/age

xfactor = calculate_xfactor(-1)

if xfactor == None : 
          pass
"""

print("code1", timeit(code1, number = 10000))
print("code2", timeit(code2, number = 10000))

➡️ code1 0.006304900016402826
code2 0.003800399979809299
```
<br>
<br>

## Modules
ماژول ها کتابخانه ای از کدها هستند. که میتوانید آنها را به کد خود اضافه کنید. <br>
برای ساخت آن ها باید کد خود را باپسوند .py ذخیره کنید. <br>
برای استفاده از آن هم باید از کلمه import استفاده کنید.
```python
import mymodule
mymodule.greeting("Jonathan")
-> Hello, Jonathan
```
<br>

شما میتوانید اسم یک ماژول را با استفاده از ‘as’ عوض کنید.
```python
import mymodule as mx
a = mx.person1["age"]
print(a)
-> 36
```
<br>

برای اینکه بفهمیم یک ماژول از چه قسمت هایی تشکیل شده است باید از فانکشن ‘dir()’ استفاده کنیم.
```python
import platform
x = dir(platform)
print(x)
```
<br>

* ### Datetime module
برای استفاده از تاریخ و ساعت کاربرد دارد.
```python
import datetime
x = datetime.datetime.now()
print(x)
-> 2023-08-18 17:07:55.657729
```
<br>

برای ساختن یک تاریخ میتوانیم به شکل زیر عمل کنیم.
```python
import datetime
x = datetime.datetime(2020, 5, 17)
print(x)
-> 2020-05-17 00:00:00
```
<br>

Strftime() <br>
در ماژول ‘datatime’ این قابلیت وجود دارد که بتوانیم خروجی آن را به گونه ای تغییر دهیم که به آن نیاز داریم.
| Directive | Description | Example |
| --- | --- | --- |
| %a | Weekday, short version |	Wed |
| %A | Weekday, full version | Wednesday |
| %w | Weekday as a number 0-6, 0 is Sunday | 3 |
| %d | Day of month 01-31 | 31 |
| %b | Month name, short version | Dec |
| %B | Month name, full version | December |
| %m | Month as a number 01-12	| 12 |
| %y | Year, short version, without century | 18 |
| %Y | Year, full version | 2018 |
| %H | Hour 00-23 | 17 |
| %I | Hour 00-12 | 05 |
| %p | AM/PM | PM |
| %M | Minute 00-59 | 41 |
| %S | Second 00-59 | 08 |
| %f | Microsecond 000000-999999 | 548513 |
| %z | UTC offset | +0100 |
| %Z | Timezone | CST |
| %j | Day number of year 001-366 | 365 |
| %U | Week number of year, Sunday as the first day of week, 00-53 | 52 |
| %W | Week number of year, Monday as the first day of week, 00-53 | 52 |
| %c | Local version of date and time |Mon Dec 31 17:41:00 2018 |
| %C | Century | 20 |
| %x | Local version of date | 12/31/18 |
| %X | Local version of time | 17:41:00 |
| %% | A % character | % |
| %G | ISO 8601 year | 2018 |
| %u | ISO 8601 weekday (1-7) | 1 |
| %V | ISO 8601 weeknumber (01-53) | 01 |
<br>
<br>

* ### Math module
برای استفاده های ریاضی در پایتون کاربرد دارد.

Min() <br>
برای پیدا کردن پایین ترین عدد به کار میرود.
Max() <br>
برای پیدا کردن بالا ترین عدد به کار میرود.
```python
x = min(5, 10, 25)
y = max(5, 10, 25)
print(x)
print(y)
-> 5
25
```
<br>

Pow() <br>
برای به توان رسوندن دو عدد استفاده میشود.
```python
x = pow(4, 3)
print(x)
-> 64
```
<br>

تمام فانکشن هایی که در این ماژول تعریف شده‌اند.
**Python math Module (w3schools.com)**
<br>
<br>

* ### Random
این ماژول برای اضافه کردن اعداد به صورت تصادفی استفاده میشود

random() <br>
یک عدد تصادفی بین (0.0 و 1.0) تولید میکند.
```python
from random import random
print(random())
-> 0.18024209212046738
```
seed() <br>
دنباله ای از اعداد تصادفی را تولید میکند. <br>
این نکته را در نظر بگیرید که با هر بار اجرای دوباره برنامه این دنباله اعداد تغییر نخواهد کرد در واقع این دنباله یک بار تولید میشود.
```python
from random import random, seed
seed(100)
print(random())
-> 0.9881136151518843
```
uniform() <br>
برای تعیین بازه اعداد تصادفی استفاده میشود.
```python
from random import uniform
print(uniform(5,15))
-> 13.18024209212046738
```
randint() <br>
برای تولید اعداد صحیح تصادفی در بازه دلخواه استفاده میشود.
```python
from random import randint
print(randit(5,15))
-> 13
```
randrange() <br>
برای تولید اعداد تصادفی با گام مشخص استفاده میشود. یعنی میتوانیم تعریف کنیم که حرکت اعداد به چه صورتی باشد.
```python
from random import randrange
print(randrange(5, 15 ,2))
print(randrange(5, 15 ,2))
print(randrange(5, 15 ,2))
-> 13
-> 9
-> 11
```
choice() <br>
برای انتخاب یکی از اعضای متغیر به صورت تصادفی استفاده میشود.
```python
from random import choice
x = ["a", "b", "c", "d"]
print(choice(x))
-> c
```
sample() <br>
به کمک این دستور میتوانیم یک لیست رندوم از لیست اولیه خود تولید کنیم.
```python
from random import sample
x = ["a", "b", "c", "d", "e"]
print(sample(x, 3))
print(sample(x, 3))
-> ['a', 'd', 'b']
-> ['b', 'e', 'c']
```
shuffle() <br>
این دستور به صورت اتفاقی ترتیب چینش یک متغییر را تغیر میدهد.
```python
from random import shuffle
x = ["a", "b", "c", "d"]
shuffle(x)
print(x)
-> ['d', 'b', 'c', 'a']
```
<br>
<br>
