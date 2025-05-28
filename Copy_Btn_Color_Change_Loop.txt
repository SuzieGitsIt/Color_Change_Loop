import tkinter as tk
import random

def button_click(btn):
    color = random.choice(['red', 'blue', 'green'])
    btn.config(bg=color)
    print(btn)

window = tk.Tk()

for x in range(10):
    for y in range(10):
        btn = tk.Button(window)    
        btn.config(text=f'{x}{y}',height=1, width=1, command=lambda button=btn: button_click(button))
        btn.grid(column=x, row=y, sticky='nsew')

window.mainloop()