from adafruit_circuitplayground import cp
import time

GREEN = (0, 30, 0)
RED = (30, 0, 0)
OFF = (0, 0, 0)

def right():
    cp.pixels.fill(GREEN)
    time.sleep(1)
    cp.pixels.fill(OFF)

def wrong():
    cp.pixels.fill(RED)
    time.sleep(1)
    cp.pixels.fill(OFF)
    
def button_pressed():
    while True:
        if cp.button_a:
            while cp.button_a:
                print('Unpush the button')
                time.sleep(.2)
            return('A')
        if cp.button_b:
            while cp.button_b:
                print('Unpush the button')
                time.sleep(.2)
            return('B')

def padlock(combos=('A','B','B')):
    i = 0
    while i < len(combos):
        if button_pressed() == combos[i]:
            print('right!')
            i = i + 1
        else:
            print('wrong')
            wrong()
            i = 0
    right()

padlock()
