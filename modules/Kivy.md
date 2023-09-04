## Installing
برای نصب این فریم ورک ابتدا باید یک محیط مجازی به وسیله پایتون بسازیم
`python -m virtualenv [venv-name]`
<br>

و برای فعال سازی آن باید به روش زیر عمل کنیم
**Windows**
`[venv-name]\Scripts\activate`
<br>

**Linux / macOs**
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
from kivy.uix.label import Label

def build(self):
  return Label(text='Hello world')
```
<br>

* ### TextInput
برای گرفتن ورودی از کاربر استفاده میشود
```python
from kivy.uix.textinput import TextInput
self.username = TextInput()
```
<br>

multiline <br>
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

در زیر برنامه‌‌ای را برای گرفتن username و password کاربرد مشاهده میکنید
```python
from kivy.app import App
from kivy.uix.gridlayout import GridLayout
from kivy.uix.label import Label
from kivy.uix.textinput import TextInput


class LoginScreen(GridLayout):

    def __init__(self, **kwargs):
        super(LoginScreen, self).__init__(**kwargs)
        self.cols = 2
        self.add_widget(Label(text='User Name'))
        self.username = TextInput(multiline=True)
        self.add_widget(self.username)
        self.add_widget(Label(text='password'))
        self.password = TextInput(password=True, multiline=False)
        self.add_widget(self.password)


class MyApp(App):

    def build(self):
        return LoginScreen()


if __name__ == '__main__':
    MyApp().run()
```
<br>

