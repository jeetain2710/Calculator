#Calculator GUI

from tkinter import *
win = Tk()
win.title("calculator")
operator=" "
text_input = StringVar()
win.geometry('340x370')

def bttnclk(num):
    global operator
    operator = operator + str(num)
    text_input.set(operator)

def screenclear():
    global operator
    operator = " "
    text_input.set(" ")

def equalfun():
    global operator
    sumup = str(eval(operator))
    text_input.set(sumup)


entry1 = Entry(win,bd = 30,font=('times', 20,'bold'),fg='brown', insertwidth=4, bg='Powder Blue',justify = 'right',textvariable=text_input)
entry1.grid(columnspan=6)

button0 = Button(win,text=0,font=('times', 20),padx = 16,command = lambda:bttnclk(0),bd = 8,bg = 'powder blue')
button0.grid(row=6,column= 1,)
button1 = Button(win,text=1,font=('times', 20),padx = 16,command = lambda:bttnclk(1),bd = 8,bg = 'powder blue')
button1.grid(row=5, column=1)
button2 = Button(win, text=2,font=('times', 20),padx = 16,command = lambda:bttnclk(2),bd = 8,bg = 'powder blue')
button2.grid(row=5, column=2)
button3 = Button(win,text=3,font=('times', 20),padx = 16,command = lambda:bttnclk(3),bd = 8,bg = 'powder blue')
button3.grid(row = 5,column = 3)
button4 = Button(win,text=4,font=('times', 20),padx = 16,command = lambda:bttnclk(4),bd = 8,bg = 'powder blue')
button4.grid(row = 4,column = 1)
button5 = Button(win,text=5,font=('times', 20),padx = 16,command = lambda:bttnclk(5),bd = 8,bg = 'powder blue')
button5.grid(row = 4,column = 2)
button6 = Button(win,text=6,font=('times', 20),command = lambda:bttnclk(6),padx = 16,bd = 8,bg = 'powder blue')
button6.grid(row = 4, column = 3)
button7 = Button(win,text=7,font=('times', 20),padx = 16,bd = 8,command = lambda:bttnclk(7),bg = 'powder blue')
button7.grid(row = 3, column = 1)
button8 = Button(win,text=8,font=('times', 20),command = lambda:bttnclk(8),padx = 16,bd = 8,bg = 'powder blue')
button8.grid(row = 3, column = 2)
button9 = Button(win,text=9,font=('times', 20),padx = 16,bd = 8,command = lambda:bttnclk(9),bg = 'powder blue')
button9.grid(row = 3, column = 3)

button11 = Button(win,text="+",font=('times', 20),padx = 16,bd = 8,command = lambda:bttnclk("+"),bg = 'powder blue')
button11.grid(row = 6, column = 4)
button12 = Button(win,text="-",font=('times', 20),padx = 16,bd = 8,command = lambda:bttnclk("-"),bg = 'powder blue')
button12.grid(row = 5, column =4 )
button13 = Button(win,text="*",font=('times', 20),padx = 16,bd = 8,command = lambda:bttnclk("*"),bg = 'powder blue')
button13.grid(row = 4, column =4 )
button14 = Button(win,text="/",font=('times', 20),padx = 16,bd = 8,command = lambda:bttnclk("/"),bg = 'powder blue')
button14.grid(row = 3, column =4 )
button15 = Button(win,text="=",font=('times', 20,'bold'),command=equalfun,padx = 16,bd = 8,bg = 'powder blue')
button15.grid(row = 6, column =2 )
button16 = Button(win,text="C",font=('times', 20,'bold'),padx = 16,command = screenclear,bd = 8,bg = 'powder blue')
button16.grid(row = 6, column =3 )

win.mainloop()
