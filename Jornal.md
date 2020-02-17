# This is a journal for comp sci - March 12th


- what did we do?
  We talked about how dice system's going to work.
  We also added some new functions on algorithm which we made last class.

- What did I learn?
  How to define the variable outside → then call them by "global x"
  color code ex:(255, 0, 0)
  3ways to express the equation(These equations have same solution indeed)
   - One =  One + 1
   - One += 1
   - One ++
  How to make a bar graph
  
-----------------------------------------------------------------------------------------------------------
ones=0
twos=0
threes=0
fours=0
fives=0
sixes=0


def setup():
    size (600,600)
    background(255)
    barGraph() 
    
def draw():
    x=0
    delay(500) 
    mouseClick() 
    barGraph() 
    
def barGraph() :
    global ones
    fill(0)
    textSize(20) 
    for x in range(6):
        text(x+ 1,(50+50*x), 580)
    
    rect(50, 550 - ones, 20, ones)
    rect(100, 550 - twos, 20, twos)
    rect(150, 550 - threes, 20, threes)
    rect(200, 550 - fours, 20, fours)
    rect(250, 550 - fives, 20, fives)
    rect(300, 550 - sixes, 20, sixes)
    

def mouseClick():
    global ones, twos, threes, fours, fives, sixes
    background(255)
    stroke(128)
    fill(255)
    rect(100,100, 400, 400, 10)
    stroke(255,0,255)
    strokeWeight(10)

    
    
    n=random(0,6)
    print(n)
    if 0<=n<1:
        circle(300,300,50)
        ones += 1
        print("number of times one has been rolled: ", ones)
    if 1<=n<2:
        circle(200,200,50)
        circle(400,400,50)
        twos += 1
        print("number of times one has been rolled: ", twos)
    if 2<=n<3:
        circle(200,200,50)
        circle(400,400,50)
        circle(300,300,50)
        threes += 1
        print("number of times one has been rolled: ", threes)
    if 3<=n<4:
        circle(200,200,50)
        circle(400,200,50)
        circle(200,400,50)
        circle(400,400,50)
        fours += 1
        print("number of times one has been rolled: ", fours)
    if 4<=n<5:
        circle(200,200,50)
        circle(400,200,50)
        circle(200,400,50)
        circle(400,400,50)
        circle(300,300,50)
        fives += 1
        print("number of times one has been rolled: ", fives)
    if 5<=n<6:
        circle(200,200,50)
        circle(400,200,50)
        circle(200,400,50)
        circle(400,400,50)
        circle(200,300,50)
        circle(400,300,50)
        sixes += 1
        print("number of times one has been rolled: ", sixes)
