## information science assignment for April

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

