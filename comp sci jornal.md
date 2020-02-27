# This is a journal for comp sci - Feb 20th

・what did we do? 
 - we revised how we call variable by using "global..."
 - we used "for loop" to repeat them all
 - we made a checkered for optical illusion
    → then we drew a couple of lines and square.
  
・what did I learn 
 - How to make a square
 - usage for "for loop" and "if"
 

・*Homework*
→ make own optical illusion

This is a today's optical illusion(not homework)

---------------------------------------------------------------------------------------------------------------

offset = 50

def mouseClicked():
    global offset
    offset += 1
        

def setup() :
    size(500,500)
    background(255)
    
def draw() :
    stroke(0)
    y = 50
    for row in range(9):
        line(0,y,500,y)
        y = y + 50
     
    fill(0)
    stroke(255)
    y = 0
    for row in range(5):
        x = 0
        for s in range(5):
            square(x,y, 50)
            x += 100
        y = y + 100
    # these are the odd rows
    y = 50
    global offset
    for row in range(5):
        x = 0 + offset
        for s in range(5):
            square(x,y, 50)
            x += 100
        y = y + 100
