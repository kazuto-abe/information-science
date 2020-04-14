## information science assignment - COVID-19

### April 7th
①　Read the article "How your personal computer can help science battle the coronavirus while you sleep"　by John D'Anna for Arizona Republic Magazine.

The important idea is to manage to understand how protein works. 
Because proteins are so tiny we could not see them all, figuring out protein is a bit challenging task for scientists. 
So one of the ways that scientists are trying to address this problem is making and observing how proteins work in a virtual situation. (using computer simulation )
However, they need a bunch of computing power. 
According to Bowman,  carrying out just one calculation on his Mac book pro takes 500 years. By contrast, the Stanford program has launched a network called the “super-cluster” of countless computers. 
The computers will be building up own network to individuals. For a scientist, focusing on the current pandemic is pretty natural because they shifted on how proteins function and malfunction.
Horvath said, "Of course we're all scientists here, so one of the things we wanted to do was take a look at the COVID-19 virus and see if maybe we could take some of our unused resources and use them to help solve that problem,".
Above all, they will be utilizing this system because anyone could contribute to the current circumstance.


In my opinion, people should enable get to the resources of their individual computers. 
In the emergency situation, we need all citizen support and contributions.


I guess there are any risks whether it is a solvable issue or not. 
The biggest risk we will be facing is that hacking or exploiting from another computer. 
Therefore they necessary to prove how extensive the security system works and how strong is it.


#### What should be some behaviors (at least 3) that we will need to include in our simulation to be a realistic approximation of the current situation in the world? Explain.
1. It should be assigned some individual information: nationality, age, gender, how many kids do you have, health status and history,  etc...
This is because It makes more efficiency when we analyze what type of tendency they have, also how strong are they. 
However, I do not think It has to be really specific setting such as face parts, just need a symbol it can be recognized for everyone.

2. Detail of symptoms what if they get COVID-19 already. 
By classifying symptoms, I can get a better understanding of COVID-19. What more, this is slightly related to individual information because we can judge what’s going on from their relationship. <br>

3. Population distribution, in order to figure out how many possibilities are there to get a virus. Some people might go to crowded cities, on the other hand, some people might live in the countryside. 



②　Follow the Video: InfoSci Intro.mp4 to understand the topic for the next weeks
These are my key points: 

・The purpose is how computer science can help us understand the situation that happens in the world right now.
・ Computer simulation is the process of algorithmic modeling, performed on a computer, which is designed to predict the behavior of and/or the outcome of a real-world or physical system. 
(how Coronavirus spread out themselves. It can be compared to a different strategy, lockdown VS closing border without lockdown for example.)

What would we need?
- A computer programming language → Processing Python
- A way of representing people → Video1
- A way of representing individuals in a community. → Video 2
- A way of representing interactions between individuals
- A way of representing sick, healthy and recovered individuals.

#### Q. What did I do<br>
→Initially, I was scanning and analyzing the article about how a personal computer can help the fight against COVID-19. 
Secondly, I tried to understand the process of computer simulation, and how does it work using the initial video Dr.Ruban gave us. 
Then I considered what would we need to carry out this simulation: computer programming language, people, individuals in a community, etc...
Thirdly,  I actually started working on the computer simulation it shows how coronavirus spread themselves. In order to express the individual for each, I made one circle and let it move randomly.
So that I used a new function which can be adding the random number within the range I set. ( In this case, I set -10 to 10)
Furthermore, I made the lists to substitute some variable of coordinate that I added.
For the next step,  Because no circle needed to move outside of the maximum coordinate, I added the boundary conditions using “if” sentences. (for the first task, I necessary to add three more boundary conditions) <br>
This is the code of the first task:

```python
 #bounderies conditions
        if x[i] > 500:
            x[i] = 500
        if x[i] < 0:
            x[i] = 0
        if y[i] > 500:
            y[i] = 500
        if y[i] < 0:
            y[i] = 0
```

For the final step, create 10 individuals using the setup method. ( So we could not type manually)
In this part, I change the number inside of the “for loop” how many times it has to be repeated, then I made the empty lists. In terms of lists I made already, It also needs to use the append method according to the web page.
(Append method is to add variable or number or label into the list which is already made in the past)<br>

So code will be the following:

```python
# definition of variables

x = [] # a list, which is a collection of values
y = []

for i in range(10):
    x.append(random(0,500))
    y.append(random(0,500))
    
def setup():
    size(500,500)
    
def draw():
    global x, y
    background(255)
    strokeWeight(2)
    
    
    #create list individual
    # when I make lists, it always counts from "0"
    for i in range(10):
        circle(x[i], y[i], 40)
        
        #substitute into two variables
        # random: I can set the range of the number. (then outtput some number randomly)
        x[i] = x[i] + random(-10,10)
        y[i] = y[i] + random(-10,10)
        #bounderies conditions
        if x[i] > 500:
            x[i] = 500
        if x[i] < 0:
            x[i] = 0
        if y[i] > 500:
            y[i] = 500
        if y[i] < 0:
            y[i] = 0
    # Let it move slower
    delay(100)
```

#### Q. What did I learn<br>
→ For the article, it’s described how computer science could contribute to the virus, I gained both ways of critical thinking and factual opinion based on evidence.

For the coding as a practical assignment, these things are what I learnt.

 - I relearned how to make a “for loop” properly, and combine with other functions such as random function, append function, and so on.
 - Likewise, I was struggling with how to utilize the empty list, but I eventually managed to finish this task using research material.
→ our final task was to create 10 circle which is represented each individual without coding all coordinates step by step.
Because I figured out how could I use the append method within the empty list, my researching skill is polished a lot. (I did not think I could complete the final task with my current programming skill so)


#### Q. What question do I have <br> 

I wonder if whether I should type this code outside of the “setup” which is defined initially or inside.
In addition, I would like to get information about markdown in GitHub because I sometimes feel frustrated. (for instance, how to attach the image, hyperlink, etc…)



### April 14th

#### Q. What did I do <br>

First of all, we’ve watched the instruction video which shows us how to use “for loop” in Python. It says that “i” is often represented the loop variable and we can use any name instead. Also what “range” means how many times it has to be repeated. (We could put the very specific number like “range(2, 10, 2) ”) → Which means the range starts from 2 to 9 (10 is not included), It might be the step of 2. By using this for loop, we don’t need to type each number manually inside of the variable definition.<br> In the second part of the video, It’s about how to add the interactions with people using the Pythagorean Theorem. We will be setting neighbors and individuals for example, then we necessary to calculate the distance between neighbors and individuals. 
Therefore If the distance is much shorter than the number we set, It is indicating infected already. According to Pythagorean Theorem, hypotenuse(c) =  sqrt(a**2 + b**2) so that we can use this equation for estimating a distance. <br>
In the last part of the video, It initially indicates us :<br>
- Adding a new list that could judge the individual whether healthy or infected.
- Making a new append function for the judging system
- In order to calculate the distance, we should  add a new function (using “def”)
  Also, put the Pythagorean Theorem formula inside of the “def” function, then output themselves using the return function.
- Putting an “if” method into a “def setup”. which is for changing the color depends on individuals are infected or not. (healthy = TRUE, infected = FALSE)
  * If the neighbor is as same as the individual, it’s not going to happen anything.<br>
	 →Using “continue” function which means skip to the next iteration
  * “Len” function might be useful for counting the number inside of the list. (Because we don’t have to get back to change the number every single time. <br>

For the last thing, I have to do is that looking through the slide it’s written about the task for week 29. Then we’re going to manage to do those tasks eventually.<br>

#### Task Part1

①: Create a new file in processing and create a program that prints 100 bears
This is my code ↓ <br>

``` python
def setup():
    for num in range(0,101):
        if num == 1:
            print("bear:" + str(num))
        else:
            print("bears:" + str(num))

```
- This is a basic structure of how the same program is repeating. I just put the “for loop” and its range from 0 to 101 (because 100 has to be included). 
However, for the special case as showing “bear”(without “s”), I necessary to add if method inside of the “for loop”. Then I used “print” for showing up text and number of bears. <br>

②: Create a program that prints the years from 1900 to 2000
This is my code ↓  <br>

``` python
def setup():
    for num in range(1900, 2001):
        print("The year is: " + str(num))
```
- I guess this is the simplest example of using “for loop”. By setting range starts from 1900 to 2001, it will be showing up the number. <br>

③: Create a program that prints the conversion for Celsius to Fahrenheit from 0 C to 100 C
This is my code ↓ <br>

``` python
def setup():
    for c in range(100):
        f = c * 1.8 + 32 # formula 
        print(str(c) + "C are " + str(f) + "F") 
```
- This was a bit complex example of using “for loop”, but I finally finished coding up. For the first step,  I looked up what is a formula for Celsius to Fahrenheit in general. Then I put the formula in the “for loop” (c stands for Celsius, f stands for Fahrenheit)
Eventually, I tried to output the result using the “print” function. (As you can see above, I mashed text and variable up) <br>

#### Task part2

①: Add a bar graph at the bottom right corner of the screen that counts the number of infected people and the number of healthy people. It should also show the numbers: <br>

- For the first step, I set the variables: for the infected graph, for the healthy graph, for the text of the infected graph, and for the text of the healthy graph.
(Because a graph represented for healthy people will be going down, variable which is for healthy graph is set a number for individuals.  On the other hand, a graph represented for infected people is set a number of “0” because the graph will be going up) <br>

``` python
#variable for the bargraphs
redb = 0
whiteb = 25

#conting for infected people
redbtxt = 0
whitebtxt = 25
```
For the second step, I declared that I would use a “barGraph” function inside of the “setup” function. (once again, “setup” function will be running only at the beginning. <br>

``` python
def setup():
    size(500,500)
    #create random individual
    for ind in range(25):
        x.append(random(0,500))
        y.append(random(0,500))
        h.append(True)  # now, all individuals are healthy
    barGraph()
```
First of all, now, I could use a “barGraph” function that I declared in the second step.
Initially I have to be able to use the variables which are defined outside of the bargraph function.
In order to call them all, I used the “global” method as usual. Then using the “rect” function that is to form two types of rectangles as a graph: infected one and a healthy one. ( at the same time, I necessary to put appropriate x coordinate and y coordinate inside) For repeating the entire process to creating a bar graph and its label, I made a “for loop” within the range which is number of individuals. (So I guess I could use “Len” function in here) Furthermore, I generated a judgment program in order to get the consequences clearly from a bar graph how many people infected;  if the individual’s health status is false (that means infected), the red bar graph and its label will be added 1, and the white bar graph and its label will be minus 1. <br>

``` python
def barGraph():
    global redb, whiteb, redbtxt, whitebtxt
    fill(255, 0, 0)
    rect (420, 470, -redb*4, 15)
    fill (255)
    rect (420, 450, -whiteb*4, 15)
    whiteb = 25
    redb = 0
    for bar in range (25):
        if h[bar] == False:
            redb += 1
            redbtxt += 1
            whiteb -= 1
            whitebtxt -= 1
    textSize(13)
    fill(0)
    text("Infected", 430, 485)
    text("Healthy", 430, 458)
    text(str(redb), 270, 485)
    text(str(whiteb),270, 460) 
```


②: Add a counter for the number of times the simulation has run, this is the same as counting the number of times the Draw function is run.<br>
This is my entire code through Task part3 ↓<br>

``` python
# definition of variables

x = [] # a list, which is a collection of values
y = []
h = [False, True] #False => infected 
# h = health status

#variable for the bargraphs
redb = 0
whiteb = 25

#conting for infected people
redbtxt = 0
whitebtxt = 25

#counting how many times the Draw function is run
ct = 0

def setup():
    size(500,500)
    #create random individual
    for ind in range(25):
        x.append(random(0,500))
        y.append(random(0,500))
        h.append(True)  # now, all individuals are healthy
    barGraph() 

def distance(x1, x2, y1, y2):
    a = (x1 - x2)
    b = (y1 - y2)
    c = sqrt(a**2 + b**2)
    return c
    # return is like an output function
    # difference between return and print??
    
def barGraph():
    global redb, whiteb, redbtxt, whitebtxt
    fill(255, 0, 0)
    rect (420, 470, -redb*4, 15)
    fill (255)
    rect (420, 450, -whiteb*4, 15)
    whiteb = 25
    redb = 0
    for bar in range (25):
        if h[bar] == False:
            redb += 1
            redbtxt += 1
            whiteb -= 1
            whitebtxt -= 1
    textSize(13)
    fill(0)
    text("Infected", 430, 485)
    text("Healthy", 430, 458)
    text(str(redb), 270, 485)
    text(str(whiteb),270, 460) 
    text("Iteration# ", 20, 470) 
    text(str(ct), 80, 470)

def draw():
    global x, y, redb, whiteb, ct, redbtxt, whitebtxt
    background(255)
    strokeWeight(2)
    barGraph()
    ct += 1
    #show the individuals
    # len function is to count how many value it has in the list.
    # In this case, circles will be showing up depends on how many individual there are.
    for ind in range(len(x)):
        if h[ind] == True:
            fill(255) #It will be showing white, it means healthy
        else:
            fill(255, 0, 0) # It will be showing red, it means infected
        circle(x[ind], y[ind],40) 
       
        #calculate the distance to each neighbour 
        for nei in range(len(x)): 
            if nei == ind:
                continue # it means skip to the next iteration(kurikaesi )
            d = distance(x[ind], x[nei], y[ind], y[nei])
            if d < 40 and (h[nei] == False or h[ind] == False):
                #infection happens
                h[ind] = False
                h[nei] = False
                
        
    #create list individual
    # when I make lists, it always counts from "0"
    for m in range(len(x)):
        #substitute into two variables
        # random: I can set the range of the number. (then outtput some number randomly)
        x[m] = x[m] + random(-10,10)
        y[m] = y[m] + random(-10,10)
        #bounderies conditions
        if x[m] > 500:
            x[m] = 500
        if x[m] < 0:
            x[m] = 0
        if y[m] > 500:
            y[m] = 500
        if y[m] < 0:
            y[m] = 0
    # Let it move slower
    delay(100)
```

Basically I only added a small three changes in here.
- I put the one global variable It’s written “ct” that is to count how many times the Draw function is run. (At the beginning, It’s set as zero )
- By adding equation as “ct = ct + 1” inside of the draw function, the number of times the simulation has run becomes larger.
- In order to output those, I’ve used the “text” function as well as question1. 

#### What did I learn

I would write it after I finish coding Task part3

#### What questions do I have

- What is the difference between the return function and the print function?
- What if I could not really see the graph and its label because they and each individual are overlapping each other.












