<img src="https://user-images.githubusercontent.com/73097560/115834477-dbab4500-a447-11eb-908a-139a6edaec5c.gif"><br><br>


<h1 align="center">iOs calculator 😚👀</h1>




<img src="https://user-images.githubusercontent.com/73097560/115834477-dbab4500-a447-11eb-908a-139a6edaec5c.gif"><br><br>
<p align="center">
<img src="https://img.shields.io/badge/language-python-blue?style"/><img src="https://img.shields.io/github/stars/imfallah/ios-calculator"/><img src="https://img.shields.io/github/forks/imfallah/ios-calculator"/>
</p>

   


<h4 align="center">🛑Time to study 5 minutes⚠👁‍🗨</h4>

Table of contents✅✔
=================

<!--ts-->
   * 🔸[Installation⚠](#installation)
   
   * 🔸[About Code👨🏽‍💻](#abot-code)
     * 🏅[importing](#importing)
     * 🏅[Window](#-widow)
     * 🏅[Functions](#function)
     * 🏅[simple Buttons](#buttons_1)
     * 🏅[Number Butons](#number-buttons)
     * 🏅[Engineering Button](#-engineering-button)
     * 🏅[Run it](#-runing-)


   * 🔸[Mor Example💯🌏]()
     * 🥇[Project Video📺](#video-image-of-the-app-)
    
   * 🎁[`CONNECT ME🎃`](https://github.com/imfallah/ios-calculator/edit/main/README.md#%F0%9D%90%82%F0%9D%90%A8%F0%9D%90%A7%F0%9D%90%A7%F0%9D%90%9E%F0%9D%90%9C%F0%9D%90%AD-%F0%9D%90%8C%F0%9D%90%9E)

<!--ts-->


# ➕Installation⚠

## Install the Library with pip:

```python
pip install tk
pip install pillow
```

Update existing installation:`pip3 install (YOUR LIBRARY) --upgrade`
(update as often as possible because this library is under active development)

## The versions I used 😎:

`tk==0.1.0` install this version ~> `pip install tk==0,1.0`
`pillow==9.5.0` install this version ~> `pip install pillow==9.5.0`
"python 3.8" [download python](https://www.python.org)

# Abot Code🎃:

## ➕Importing:

```python
from tkinter import *
from tkinter import messagebox
from math import pi, e, sin, cos, tan, log
from PIL import Image , ImageTk 
```
## ➕ Widow:
1. `window = Tk()`: This line creates an instance of the `Tk` class that provides a main or root window for your user interface
2. `screenSize = "300x540"`: This line defines a string specifying the size of the window.
3. `window.geometry(screenSize)`: This line sets the size of the window based on the `screenSize` string.
4. `#window.resizable(0, 0)`: This line of code is commented out and will not be executed. If you uncomment this line of code, it will fix the size of the window and the user cannot change it.
5. `window.title("ios Caculat")`: This line sets the title of the window to "ios Caculat".
6. `window.overrideredirect(True)`: This line removes the window title and window controls, so your window will be a frameless window.
7. `window.geometry("300x540+{}+{}".format(window.winfo_screenwidth() // 2 -270, window.winfo_screenheight() // 2 - 270))`: This line defines the size and position of the window adjusts The window is placed in the center of the screen.
8. `bg = PhotoImage(file = "images/vec-resized.png")`: This line loads an image from the file "images/vec-resized.png" and assigns it to the variable `bg` to give
9. `img=PhotoImage(file="images/OIP (1).png")`: This line loads another image from the file "images/OIP (1).png" and assigns it to the `img variable. assigns
10. `window.iconphoto(True,img)`: This line sets the `img` image as the window icon.
```python
window = Tk()
screenSize = "300x540"
window.geometry(screenSize)
#window.resizable(0, 0)
window.title("ios Caculat")
window.overrideredirect(True)
window.geometry("300x540+{}+{}".format(window.winfo_screenwidth() // 2 -270, window.winfo_screenheight() // 2 - 270))
img=PhotoImage(file="images/OIP (1).png")
window.iconphoto(True,img)
```

<img src="https://github.com/imfallah/ios-calculator/blob/main/public/1.png" width="200" height="400"></img>


## ➕`Function`:
- `about()`: This function displays an information messagebox with the text "INSTA : @mrcode.co".

- `clickButton(item)`: This function appends the string representation of the input item to the current input text.

- `clearButton()`: This function clears the last character from the input text.

- `clearAll()`: This function clears all the text from the input field.

- `expand()`: This function changes the size of the window based on the current screen size.

- `equalButton()`: This function evaluates the mathematical expression in the input text and sets the result as the new input text. If the expression is not valid, it sets the input text to "ERROR...".
```python
#function
def about():
    messagebox.showinfo(""," INSTA  :    @mrcode.co")

def clickButton(item):
    global expression
    inputText.set(inputText.get()+(str(item)))

def clearButton():
    global expression
    expression = ""
    inputText.set(inputText.get()[0:-1])

def clearAll():
    inputText.set("")

def expand():
    if screenSize=="300x412":
        window.geometry("300x555")
    else:
        window.geometry("279x555")
def equalButton():
    result = ""
    try:
        result = eval(inputText.get())
        inputText.set(result)
    except:
        result = "ERROR..."
        inputText.set(result)
```
## ➕`Menu_bar`:
- `menubar = Menu(window,bg="black",fg="black")`: This line creates a new menu bar with a black background and black foreground.

- `filemenu` and `helpmenu`: These are dropdown menus added to the menu bar. The `filemenu` has an "Exit" option that closes the window, and the `helpmenu` has an "About" option that calls the `about()` function defined earlier.

- `expression = ""`: This line initializes the `expression` variable as an empty string.

- `inputText = StringVar()`: This line initializes `inputText` as a Tkinter `StringVar` object, which can be used to change the text in a widget.

- `inputFrame`: This is a frame for the input field with a width of 312, a height of 50, and a black highlight background.

- `inputField`: This is an entry field where the user can input their expression. It uses `inputText` as its text variable, so any changes to `inputText` will automatically update the text in the field.

- `mainFrame`: This is the main frame of the application with a width of 312, a height of 272.5, and a black background.

- `window.config(bg="black",menu=menubar)`: This line sets the background color of the window to black and assigns the previously created `menubar` as the window's menu.
-  
```python
#menubar
menubar = Menu(window,bg="black",fg="black")
filemenu = Menu(menubar, tearoff=0,bg="white",fg="black")
filemenu.add_separator()
filemenu.add_command(label="Exit", command=window.quit)
menubar.add_cascade(label="Edit", menu=filemenu)
helpmenu = Menu(menubar, tearoff=0,bg="white",fg="black")
helpmenu.add_command(label="About", command=about)
menubar.add_cascade(label="Help", menu=helpmenu)
expression = ""
inputText = StringVar()
inputFrame = Frame(window, width=312, height=50, bd=0, highlightbackground="black", highlightcolor="gray",highlightthickness=2)
inputFrame.pack(side=TOP)
inputField = Entry(inputFrame, font=('arial', 25, ), textvariable=inputText, width=50,fg="white", bg="black", bd=0,justify=RIGHT)
inputField.grid(row=0, column=0)
inputField.pack(ipady=13)
mainFrame = Frame(window, width=312, height=272.5, bg="black")
mainFrame.pack()

window.config(bg="black",menu=menubar)

```
<img src="https://user-images.githubusercontent.com/73097560/115834477-dbab4500-a447-11eb-908a-139a6edaec5c.gif"><br><br><img
                                                                                                                            
<img src="https://github.com/imfallah/ios-calculator/blob/main/public/2.png" width="200" height="400"></img>



## ➕`Buttons_1`:
- `ac`: This button clears all the text from the input field when clicked. It uses an image loaded from "images\ac.png".

- `clear`: This button clears the last character from the input text when clicked. It uses an image loaded from "images\clear.png".

- `divide`: This button appends a division operator ("/") to the input text when clicked. It uses an image loaded from "images\divide.png".

- `multiply`: This button appends a multiplication operator ("*") to the input text when clicked. It uses an image loaded from "images\multi.png".

- `minus`: This button appends a subtraction operator ("-") to the input text when clicked. It uses an image loaded from "images\minus.png".

- `point`: This button appends a decimal point (".") to the input text when clicked. It uses an image loaded from "images\point.png".

- `equals`: This button evaluates the mathematical expression in the input text and sets the result as the new input text when clicked. If the expression is not valid, it sets the input text to "ERROR...". It uses an image loaded from "images\equal.png".

```python
#Clear
ac = PhotoImage(file = r"images\ac.png")
acimage = ac.subsample(4,4)
ac = Button(mainFrame, text="AC", fg="black", image=acimage, bd=0, bg="black", cursor="hand2",
               command=lambda: clearAll()).grid(row=0, column=0, padx=1, pady=1)
clear = PhotoImage(file = r"images\clear.png")
clearimage = clear.subsample(4,4)
clear = Button(mainFrame, text="AC",activeforeground="black",activebackground="black", fg="black", image=clearimage, bd=0, bg="black", cursor="hand2",
               command=lambda: clearButton()).grid(row=0, column=1, padx=1, pady=1)


# ÷
divide = PhotoImage(file = r"images\divide.png")
divideimage = divide.subsample(4,4)
divide = Button(mainFrame,activeforeground="black",activebackground="black", text="/", fg="white",image=divideimage, bd=0, bg="black", cursor="hand2",
                command=lambda: clickButton("/")).grid(row=0, column=3, padx=1, pady=1)

multi = PhotoImage(file = r"images\multi.png")
multiimage = multi.subsample(4,4)
multiply = Button(mainFrame,activeforeground="black",activebackground="black", text="*", fg="white",image=multiimage, bd=0, bg="black", cursor="hand2",
                  command=lambda: clickButton("*")).grid(row=1, column=3, padx=1, pady=1)
# -
minus = PhotoImage(file = r"images\minus.png")
minusimage = minus.subsample(4,4)
minus = Button(mainFrame,activeforeground="black",activebackground="black", text="-", fg="white",image=minusimage, bd=0, bg="black", cursor="hand2",
               command=lambda: clickButton("-")).grid(row=2, column=3, padx=1, pady=1)
# . 
point = PhotoImage(file = r"images\point.png")
pointimage = point.subsample(4,4)
point = Button(mainFrame,activeforeground="black",activebackground="black", text=".", fg="black",image=pointimage, bd=0, bg="black", cursor="hand2",
               command=lambda: clickButton(".")).grid(row=4, column=2, padx=1, pady=1)

# = 
equal = PhotoImage(file = r"images\equal.png")
equalimage = equal.subsample(4,4)
equals = Button(mainFrame,activeforeground="black",activebackground="black", text="=", image=equalimage, fg="white", bd=0, bg="black", cursor="hand2",
                command=lambda: equalButton()).grid(row=4, column=3, padx=1, pady=1)
```

<img src="https://github.com/imfallah/ios-calculator/blob/main/public/3.png" width="200" height="400"></img>

## ➕`Number Buttons`:
- "Zero": clicking this button adds 0 to the input text. It uses an image downloaded from "images\0.png".
- 'nine': Clicking this button adds the number 9 to the input text. It uses an image downloaded from "images\nine.png".
You continue this sequence until all the numbers 0 to 9, which you can see all of them in the [projectfile](https://github.com/imfallah/ios-calculator/tree/main/main)
```python
# -- 0
zero = PhotoImage(file = r"images\0.png")
zeroimage = zero.subsample(4,4)
zero = Button(mainFrame,activeforeground="black",activebackground="black", text="0", fg="black",image=zeroimage, bd=0, bg="black", cursor="hand2",
              command=lambda: clickButton(0)).grid(row=4, column=0, columnspan=2, padx=1, pady=1)
```

                                           
###      0-1-2-3-4-5-6-7-8-9  
                                       

```python
# -- 9
nine = PhotoImage(file = r"images\nine.png")
nineimage = nine.subsample(4,4)
nine = Button(mainFrame,activeforeground="black",activebackground="black", text="9", fg="black", image=nineimage, bd=0, bg="black", cursor="hand2",
              command=lambda: clickButton(9)).grid(row=1, column=2, padx=1, pady=1)
```
<img src="https://github.com/imfallah/ios-calculator/blob/main/public/4.png" width="200" height="400"></img>

## ➕ Engineering Button:
- `expan_btn`: This button calls the `expand()` function when clicked. It uses an image loaded from "images\expan_btn.png".
- `bracket1` and `bracket2`: These buttons append an opening parenthesis "(" and a closing parenthesis ")" to the input text when clicked, respectively. They use images loaded from "images\bracket1.png" and "images\bracket2.png".
- `pi`: This button appends the value of pi (approximately 3.1415) to the input text when clicked. It uses an image loaded from "images\pi.png".
- `ee`: This button appends the value of e (approximately 2.7182) to the input text when clicked. It uses an image loaded from "images\eie.png".
- `sin_btn`, `cos_btn`, `tan_btn`, and `log_btn`: These buttons append the strings "sin(", "cos(", "tan(", and "log(" to the input text when clicked, respectively. They use images loaded from "images\sin_btn.png", "images\cos_btn.png", "images\tan_btn.png", and "images\log_btn.png".
- `expan`: This is a label with an image loaded from "images\expand.png". It's packed at the bottom of the window.
```python

expan_btn = PhotoImage(file = r"images\expan_btn.png")
expan_btnimage = expan_btn.subsample(4,4)
percentage = Button(mainFrame,activeforeground="black",activebackground="black", fg="black", image=expan_btnimage, bd=0, bg="black", cursor="hand2",
               command=lambda: expand()).grid(row=0, column=2, padx=1, pady=1)
# (
bracket1 = PhotoImage(file = r"images\bracket1.png")
bracket1image = bracket1.subsample(4,4)
bracket1 = Button(mainFrame,activeforeground="black",activebackground="black", text="pi", fg="black",image=bracket1image, bd=0, bg="black", cursor="hand2",
               command=lambda: clickButton("(")).grid(row=5, column=0, padx=1, pady=1)
# )
bracket2 = PhotoImage(file = r"images\bracket2.png")
bracket2image = bracket2.subsample(4,4)
bracket2 = Button(mainFrame,activeforeground="black",activebackground="black", text="pi", fg="black",image=bracket2image, bd=0, bg="black", cursor="hand2",
               command=lambda: clickButton(")")).grid(row=5, column=1, padx=1, pady=1)
# 3.14
pie=3.1415
pi = PhotoImage(file = r"images\pi.png")
piimage = pi.subsample(4,4)
pi = Button(mainFrame,activeforeground="black",activebackground="black", text="pi", fg="black",image=piimage, bd=0, bg="black", cursor="hand2",
               command=lambda: clickButton(pie)).grid(row=5, column=2, padx=1, pady=1)
# e
eie = 2.7182
ee = PhotoImage(file = r"images\eie.png")
eeimage = ee.subsample(4,4)
ee = Button(mainFrame,activeforeground="black",activebackground="black", text="pi", fg="black",image=eeimage, bd=0, bg="black", cursor="hand2",
               command=lambda: clickButton(eie)).grid(row=5, column=3, padx=1, pady=1)

sin_btn = PhotoImage(file = r"images\sin_btn.png")
sin_btnimage = sin_btn.subsample(4,4)
sin_btn = Button(mainFrame,activeforeground="black",activebackground="black", text="sin", fg="black",image=sin_btnimage, bd=0, bg="black", cursor="hand2",
               command=lambda: clickButton("sin(")).grid(row=6, column=0, padx=1, pady=1)

cos_btn = PhotoImage(file = r"images\cos_btn.png")
cos_btnimage = cos_btn.subsample(4,4)
cos_btn = Button(mainFrame,activeforeground="black",activebackground="black", text="cos", fg="black",image=cos_btnimage, bd=0, bg="black", cursor="hand2",
               command=lambda: clickButton("cos(")).grid(row=6, column=1, padx=1, pady=1)

tan_btn = PhotoImage(file = r"images\tan_btn.png")
tan_btnimage = tan_btn.subsample(4,4)
tan_btn = Button(mainFrame,activeforeground="black",activebackground="black", text="tan", fg="black",image=tan_btnimage, bd=0, bg="black", cursor="hand2",
               command=lambda: clickButton("tan(")).grid(row=6, column=2, padx=1, pady=1)

log_btn = PhotoImage(file = r"images\log_btn.png")
log_btnimage = log_btn.subsample(4,4)
log_btn = Button(mainFrame,activeforeground="black",activebackground="black", text="log", fg="black",image=log_btnimage, bd=0, bg="black", cursor="hand2",
               command=lambda: clickButton("log(")).grid(row=6, column=3, padx=1, pady=1)

expan = PhotoImage(file = r"images\expand.png")
expanimage = expan.subsample(4,4)
expan = Label(window, text="pi", fg="black",image=expanimage, bg="black").pack(side=BOTTOM)
```

<img src="https://github.com/imfallah/ios-calculator/blob/main/public/5.png" width="200" height="400"></img>
## ➕ Runing :
- `window.mainloop()`: This line starts the Tkinter event loop. The application will stay in the event loop until the window is closed.

`cd Main.py`


```python
window.mainloop()
```
<img src="https://github.com/imfallah/ios-calculator/blob/main/public/6.png" width="200" height="400"></img>  <img src="https://github.com/imfallah/ios-calculator/blob/main/public/calculatorgif.gif" width="200" height="400">



### Video image of the APP 📺

<img src="https://github.com/imfallah/ios-calculator/raw/main/public/ioscac.mp4" width="200" height="400">

# `𝐂𝐨𝐧𝐧𝐞𝐜𝐭 𝐌𝐞`🎮

<a herf="https://www.buymeacoffee.com/jokernets"><img src="https://cdn.buymeacoffee.com/buttons/v2/arial-yellow.png" alt="Buy Me A Coffee" width="180px">
<a href="mailto:joker.until33@gmail.com"><img align="center" width="60px" src="https://github.com/edent/SuperTinyIcons/raw/master/images/svg/gmail.svg" style="max-width: 100%;"></a><a href="https://www.linkedin.com/" target="blank"><img align="center" src="https://raw.githubusercontent.com/rahuldkjain/github-profile-readme-generator/master/src/images/icons/Social/linked-in-alt.svg" alt="https://www.linkedin.com/in/mohammadfallahnejad/" height="40" width="60" /></a>
