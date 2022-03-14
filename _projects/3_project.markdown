---
layout: page
title: Some Python Tkinter Practice
description: making mini-games with tinkler
img: /assets/img/11.jpg
importance: 1
category: work
---

Ball of random size and random color bouncing around if fired. tkinter practice dont judge lol

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        <img class="img-fluid rounded z-depth-1" src="{{ '/assets/img/fireball.png' | relative_url }}" alt="" title="example image"/>
    </div>
</div>
<div class="caption">
   
</div>

<pre><code>import tkinter as tk
import random

window = tk.Tk()
window.title('drawing gaem')
window.geometry('1000x800')

Instruction = tk.Label(window, text = 'Type in "fire" to fire le kannon!',
                       font = ('Times New Roman Greek', 50))

Instruction.pack()

button = tk.Button(window, text = "fire", width=10, height=4)

list_of_colors_we_use = ['Yellow', 'Red', 'Magenta', 'Black', 'White', 'Cyan', 'Blue']

button.pack()

class bouncing_ball:
    def __init__(self, canvas_, color_of_ball = 'Black', size_of_ball = 25, speedx = 10, speedy = 5):
        self.canvas = canvas_
        self.shape = self.canvas.create_oval(200, 200, 200+size_of_ball, 200+size_of_ball, fill = color_of_ball)
        self.speedx = speedx
        self.speedy = speedy
        self.active = True
        self.active_shape()

    def bouncing_ball_update(self):
        canvas.move(self.shape, self.speedx, self.speedy)
        position_of_balls = self.canvas.coords(self.shape)
        if position_of_balls[2] >=500 or position_of_balls[0] <= 0:
            self.speedx = self.speedx * -1
        if position_of_balls[3] >=500 or position_of_balls[1] <=0:
            self.speedy = self.speedy * -1
        
    def active_shape(self):
        if self.active:
            self.bouncing_ball_update()
            window.after(40, self.active_shape)

def cannon(canvas_, color_, size_):
    ball = bouncing_ball(canvas_, color_of_ball = color_, size_of_ball = size_)

#def debug(canvas_):
#    canvas_.create_rectangle(100, 100, 100, 100, fill = 'blue')

canvas = tk.Canvas(window, bg = 'white', height = 500, width = 500)

button.bind('<Button-1>',lambda event:cannon(canvas_ = canvas, color_ = list_of_colors_we_use[random.randint(0, 6)], 
    size_ = 10 + random.randint(10, 50)))
button.focus()

rectangle1 = canvas.create_rectangle(150, 230, 250, 200, fill = 'black')

circle1 = canvas.create_oval(100, 300, 200, 200, fill = 'black')

canvas.pack()

window.mainloop()
</code></pre>
