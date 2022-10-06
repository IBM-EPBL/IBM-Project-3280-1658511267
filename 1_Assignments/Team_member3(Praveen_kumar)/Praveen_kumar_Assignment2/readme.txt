import random
import math
import time

isAlarmRinging = False

def ringAlarm(temp, humid):
    isAlarmRinging = True
    print("Temperature is too high!!!")
    print("Temperature: " + str(temp) + "\N{DEGREE SIGN}C")
    print("Humidity: " + str(humid) + "%")
    print("\n")

def stopAlarm():
    isAlarmRinging = False
    
while True:
    time.sleep(1)
    
    temp = math.floor(random.uniform(0, 60) * 10) / 10  # In celsius
    humid = random.randint(20, 100)                     # In percentage
    
    if temp >= 40 and humid <= 55 and not isAlarmRinging:
        ringAlarm(temp, humid)
    else:
        stopAlarm()
