# Rojeen2
# tkinter code
import tkinter
from tkinter import *
window = tkinter.Tk()

label_title = tkinter.Label(window, font=("Arial",25), text="interior designers").grid(row=0,column=1)

# name
label_name = tkinter.Label(window, font=("Arial",12), text="Full Name:").grid(row=1, column=0)
tkinter.Entry(window).grid(row=1,column=1)

# address
label_address = tkinter.Label(window,font=("Arial",12), text="Home address:").grid(row=1,column=2)
address = tkinter.Entry(window)

# height
label_Height = tkinter.Label(window,font=("Arial",12), text="Insert height:").grid(row=2,column=0)
Height = tkinter.Entry(window)
Height.grid(row=2,column=1)

# paint type
def sel_paint():
    selection ="you have selected the option" + str(var.get())
    label.config(text=selection)
paint_type = IntVar()
label_paint_Type = tkinter.Label(window, text ="Paint Type").grid(row=4,column=0)
rb1 = Radiobutton(window,text="luxury",variable=paint_type,value=1,command=sel_paint)
rb1.grid(row=5,column=1)
rb1 = Radiobutton(window,text="standard",variable=paint_type,value=2,command=sel_paint)
rb1.grid(row=5,column=1)


# undercoat
CheckVar1 = IntVar()
label_Height = tkinter.Label(window,font=("Arial",12), text="undercoat:").grid(row=4,column=0)
tkinter.Checkbutton(window, text = "required",variable = CheckVar1,onvalue = 1, offvalue=0).grid(row=5,column=1)

def calculate():
    tkinter.Label(window,text ="total is £14.15").grid(row=7,column=3)


tkinter.Button(window,text = "calculate",command = calculate).pack()

window.mainloop()
