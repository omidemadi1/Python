## Installing
برای نصب این فریم ورک ابتدا باید یک محیط مجازی به وسیله پایتون بسازیم <br>

`python -m virtualenv [venv-name]`
<br>

و برای فعال سازی آن باید به روش زیر عمل کنیم <br>

**Windows** <br>
`[venv-name]\Scripts\activate`
<br>

**Linux / macOs** <br>
`source kivy_venv/bin/activate`
<br>

حالا در این محیط میتوانیم اقدام به نصب این فریم ورک کنیم <br>
برای نصب میتوانید از دستور زیر استفاده کنید <br>

`python -m pip install "kivy[base]" kivy_examples`
<br>

## Getting Start
* ### Label
برای نمایش دادن متن به کار میرود
```python
import kivy
from kivy.app import App
from kivy.uix.label import Label

class MyApp(App)
  def build(self):
    return Label(text='Hello world')

if __name__ == "__main__":
  MyApp().run()
```
<br>

برای اینکه بتوانیم اندازه نوشته خود را تغییر بدهیم باید به روش زیر عمل کنیم
```python
import kivy
from kivy.app import App
from kivy.uix.label import Label

class MyApp(App)
  def build(self):
    return Label(text='Hello world', font_size=72)

if __name__ == "__main__":
  MyApp().run()
```
<br>

* ### TextInput
برای گرفتن ورودی از کاربر استفاده میشود
```python
from kivy.uix.textinput import TextInput
self.username = TextInput()
```
<br>

**multiline** <br>
برای این به کار میرود که بخواهیم به کاربر اجازه دهیم در چند خط بنویسد.
```python
from kivy.uix.textinput import TextInput
self.username = TextInput(multiline=True)
```
<br>

اگر بخواهیم در ورودی متن نمایش داده نشود و به جای آن '*' نمایش داده شود میتوانیم به روش زیر اقدام کنیم
```python
from kivy.uix.textinput import TextInput
self.password = TextInput(password=True, multiline=False)
```
<br>

در زیر برنامه‌‌ای را برای گرفتن username ,password و email از کاربر را مشاهده میکنید
```python
import kivy
from kivy.app import App
from kivy.uix.label import Label
from kivy.uix.gridlayout import GridLayout
from kivy.uix.textinput import TextInput


class LoginScreen(GridLayout):
  def __init__(self, **kwargs):

    # Call login screen constructor
    super(LoginScreen, self).__init__(**kwargs)

    # Set columns
    self.cols = 2

    # Add widgets for username
    self.add_widget(Label(text='User Name'))
    self.username = TextInput(multiline=False)
    self.add_widget(self.username)

    # Add widgets for password
    self.add_widget(Label(text='Password'))
    self.password = TextInput(password=True, multiline=False)
    self.add_widget(self.password)

    # Add widgets for email adress
    self.add.widgets(Labale(text="Email Adress"))
    self.email = TextInput(multiline=False)
    self.add_widget(self.email)


class MyApp(App):
    def build(self):
        return LoginScreen()


if __name__ == '__main__':
    MyApp().run()
```
<br>

* ### Button
برای اضافه کردن دکمه به برنامه خود باید به روش زیر اقدام کنیم
```python
from kivy.uix.button import Button

self.done = Buttton(text="Done", font_size=32)
self.add_widget(self.done)
```
<br>

برای اینکه تعریف کنیم بعد از فشردن دکمه چه اتفاقی بیوفتد باید به روش زیر اقدام کنیم
```python
import kivy
from kivy.app import App
from kivy.uix.label import Label
from kivy.uix.gridlayout import GridLayout
from kivy.uix.textinput import TextInput
from kivy.uix.button import Button

class Done(GridLayout):
  def__init__(self, **kwargs):

    super(Done, self).__init__(**kwargs)
    self.cols = 2

    self.done = Buttton(text="Done", font_size=32)
    self.done.bind(on_press=self.press)
    self.add_widget(self.done)


  def press (self, instance):
    self.add_widget(Label(text="Your regester is done!"))
```
<br>

اگر بخواهیم که بعد از اینکه کاربر دکمه را فشار داد نوشته باکس ها از بین بروند میتوانیم به روش زیر عمل کنیم <br>
در ادامه برنامه‌ای که قبلا برای صفحه login نوشته بودیم را کامل میکنیم
```python
import kivy
from kivy.app import App
from kivy.uix.label import Label
from kivy.uix.gridlayout import GridLayout
from kivy.uix.textinput import TextInput
from kivy.uix.button import Button

class LoginScreen(GridLayout):
  def__init__(self, **kwargs):

    super(LoginScreen, self).__init__(**kwargs)
    self.cols = 2

    # Add widgets for username
    self.add_widget(Label(text='User Name'))
    self.username = TextInput(multiline=False)
    self.add_widget(self.username)

    # Add widgets for password
    self.add_widget(Label(text='Password'))
    self.password = TextInput(password=True, multiline=False)
    self.add_widget(self.password)

    # Add widgets for email adress
    self.add.widgets(Labale(text="Email Adress"))
    self.email = TextInput(multiline=False)
    self.add_widget(self.email)

    # Add done button
    self.done = Buttton(text="Done", font_size=32)
    self.done.bind(on_press=self.press)
    self.add_widget(self.done)


  def press (self, instance):
    self.add_widget(Label(text="Your regester is done!"))

    # Clear the input boxes
    self.username.text = ""
    self.password.text = ""
    self.email.text = ""


class MyApp(App):
    def build(self):
        return LoginScreen()


if __name__ == '__main__':
    MyApp().run()
```
<br>

## Height and Width
اگر بخواهیم که عرض دکمه ما تمام صفحه را بگیرد باید یک صفحه دیگر برای آن تعریف کنیم، یعنی یک GridLayout برای دکمه و یک GridLayout برای ورودی های دیگرمان
```python
import kivy
from kivy.app import App
from kivy.uix.label import Label
from kivy.uix.gridlayout import GridLayout
from kivy.uix.textinput import TextInput
from kivy.uix.button import Button

class LoginScreen(GridLayout):
  def__init__(self, **kwargs):

    super(LoginScreen, self).__init__(**kwargs)
    self.cols = 1

    # Create a second gridlayout
    self.top_grid = GridLayout()
    self.top_grid.cols = 2

    # Add widgets for username
    self.top_grid.add_widget(Label(text='User Name'))
    self.username = TextInput(multiline=False)
    self.top_grid.add_widget(self.username)

    # Add widgets for password
    self.top_grid.add_widget(Label(text='Password'))
    self.password = TextInput(password=True, multiline=False)
    self.top_grid.add_widget(self.password)

    # Add widgets for email adress
    self.top_grid.add.widgets(Labale(text="Email Adress"))
    self.email = TextInput(multiline=False)
    self.top_grid.add_widget(self.email)

    # Add the new top_grid to our app
    self.add.widget(self.top_grid)

    # Add done button
    self.done = Buttton(text="Done", font_size=32)
    self.done.bind(on_press=self.press)
    self.add_widget(self.done)


  def press (self, instance):
    self.add_widget(Label(text="Your regester is done!"))

    # Clear the input boxes
    self.username.text = ""
    self.password.text = ""
    self.email.text = ""


class MyApp(App):
    def build(self):
        return LoginScreen()


if __name__ == '__main__':
    MyApp().run()
```
<br>

اگر بخواهیم برای وردی ها و یا دکمه خود اندازه تعریف کنیم میتوانیم به روش زیر عمل کنیم
```python
self.done = Buttton(
text="Done",
font_size=32,

# For set height
size_hint_y = None,
height = 50,

# For set width
size_hint_x = None,
width = 200
)
```
<br>

همچنین میتوانیم یک خصوصیات ظاهری را برای کل یک GridLayout در نظر بگیریم

```python
self.top_grid = GridLayout(
row_force_default = True,
row_default_height = 40,
col_force_default = True,
col_default_width = 100
)
```
<br>

## Kivy Design Language
هنگام نوشتن یک برنامه ما میتوانیم کد هایی که برای اجرای برنامه به آن نیاز داریم را در یک فایل و کدهایی که برای ساختن شکل ظاهری آن برنامه است را در یک فایل دیگر با پسوند kv. ذخیره کنیم و سپس در فایل اصلی آن کدها را فرا خوانی کنیم <br>
برای اینکار نام گذاری فایل دوم بسیاز مهم است، نام آن باید با نام برنامه یک باشد

```python
class login(App):
    def build(self):
        return LoginScreen()
```
<br>

برای مثال با توجه به نام گذاری بالا نام گذاری فایل دووم ما باید به این شکل باشد <br>
**login.kv** <br>

پس برنامه ما به این شکل ذخیره میشود

```python
import kivy
from kivy.app import App
from kivy.uix.label import Label
from kivy.uix.gridlayout import GridLayout
from kivy.uix.textinput import TextInput
from kivy.uix.widget import Widget
from kivy.properties import ObjectProperty

class MyGridLayout(Widget):

  name = ObjectProperty(None)
  password = ObjectProperty(None)
  email = ObjectProperty(None)

  def press (self):
    print("Your regester is done!")

    # Clear the input boxes
    self.username.text = ""
    self.password.text = ""
    self.email.text = ""


class MyApp(App):
    def build(self):
        return LoginScreen()


if __name__ == '__main__':
    MyApp().run()
```
```kv
# This should be same with your class name in your frist file
<MyGridLayout>

  # Give this element id for frist file can read this element
  name : name
  password : password
  email : email

  # Our frist GridLayout
  GridLayout:
    cols:1

    # Make size for entire app
    size : root.width, root.height

    #Our second GridLayout in our frist GridLayout
    GridLayout:
      cols:2

      Label:
        text : "Name"
      TextInput:
        id : name
        multiline : False

      Label:
        text : "Password"
      TextInput:
        id : password
        multiline : False
        password : True

      Label:
        text : "Email"
      TextInput:
        id : email
        multiline : False

    Button:
      text : "Done"
      font_size : 32

      # For when we click on button, action
      on_press : root.press()
```
<br>

