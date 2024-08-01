# spin-a-yarn




#python program on spin a yarn
from turtle import*
state={'turn':0}
def spinner():
    clear()
    angle=state['turn']/10
    left(angle)
    forward(100)
    dot(90,'red')
    back(100)
    left(90)
    forward(100)
    dot(90,'green')
    back(100)
    left(90)
    forward(100)
    dot(90,'violet')
    back(100)
    left(90)
    update() 
    forward(100)
    dot(90,'brown')
    back(100)
    left(90)
    update() 
def animate():
    if state['turn']>0:
        state['turn']-=1
    spinner()
    ontimer(animate,20)
def flick():
    state['turn']+=50
tracer(False)
width(20)
onkey(flick,'space')
listen()
animate()
done()
    
