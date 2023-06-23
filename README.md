# MobileRobot-Openloopcontrol
## Aim:

To develop a python control code to move the mobilerobot along the predefined path.

## Equipments Required:
1. RoboMaster EP core
2. Python 3.7

## Procedure

Step1: Initiate the MobileRobot.

Step2:Connect your PC with the MobileRobot through Wi-Fi.

Step3:Open batter_level.py file and check the battery.

Step4:Open the other Python files and Program the movements of the robot using python.

Step5:Execute the python program and record the movements.


## Program
```python
# Developed by: S.ANUSHARON
# Register no.: 212222240010

from robomaster import robot
import time
from robomaster import camera

if __name__ == '__main__':
    ep_robot = robot.Robot()
    ep_robot.initialize(conn_type="ap")

    ep_chassis = ep_robot.chassis
    ep_led = ep_robot.led
    ep_camera = ep_robot.camera

     print("Video streaming started.....")
    ep_camera.start_video_stream(display=True, resolution = camera.STREAM_360P)

    ''' 
    x = x-axis movement distance,( meters) [-5,5]
    y = y-axis movement distance,( meters) [-5,5] 
    z = rotation about z axis ( degree)[-180,180]
    xy_speed = xy axis movement speed,( unit meter/second)  [0.5,2]

    '''
    ep_chassis.move(x=2, y=0, z=0, xy_speed=0.95).wait_for_completed()
    ep_led.set_led(comp="all",r=0,g=255,b=0,effect="on") 
    ep_chassis.move(x=0, y=0, z=-90, xy_speed=1).wait_for_completed()
    ep_led.set_led(comp="all",r=204,g=255,b=255,effect="on") 
    ep_chassis.move(x=2, y=0, z=0, xy_speed=1).wait_for_completed()
    ep_led.set_led(comp="all",r=204,g=204,b=255,effect="on") 
    ep_chassis.move(x=0, y=0, z=-90, xy_speed=1).wait_for_completed()
    ep_led.set_led(comp="all",r=0,g=0,b=0,effect="on")
    ep_chassis.move(x=1, y=0, z=0, xy_speed=1).wait_for_completed()
    ep_led.set_led(comp="all",r=0,g=0,b=0,effect="on") 
    ep_chassis.move(x=0, y=0, z=-90, xy_speed=1).wait_for_completed() 
    ep_led.set_led(comp="all",r=0,g=0,b=128,effect="on") 
    ep_chassis.move(x=2, y=0, z=0, xy_speed=1).wait_for_completed() 
    ep_led.set_led(comp="all",r=0,g=0,b=128,effect="on")
    ep_chassis.move(x=0, y=0, z=-30, xy_speed=1).wait_for_completed() 
    ep_led.set_led(comp="all",r=0,g=0,b=128,effect="on") 
    ep_chassis.move(x=1, y=0, z=0, xy_speed=1).wait_for_completed() 
    ep_led.set_led(comp="all",r=0,g=0,b=128,effect="on")
    


  
 
 
    
    ep_camera.stop_video_stream()
    print("Stopped video streaming.....")

    ep_robot.close()

```

## MobileRobot Movement Image:

![robo](./img/robomaster.png)

Insert image here

![startpoint](https://github.com/Anusharonselva/mobilerobot-openloopcontrol/assets/119405600/e16908ec-5366-4254-9381-6608bf75ec9e)

![movement](https://github.com/Anusharonselva/mobilerobot-openloopcontrol/assets/119405600/e6c68f15-9481-48e5-bf1a-71bd317dc0ed)


![endpoint](https://github.com/Anusharonselva/mobilerobot-openloopcontrol/assets/119405600/be5849cf-57df-43e3-8601-59d4d9112247)





## MobileRobot Movement Video:

https://youtu.be/rN-k7TI7Vco


[![IMAGE ALT TEXT HERE](https://img.youtube.com/vi/YOUTUBE_VIDEO_ID_HERE/0.jpg)](https://www.youtube.com/watch?v=YOUTUBE_VIDEO_ID_HERE)


## Result:
Thus the python program code is developed to move the mobilerobot in the predefined path.




```
Mobile Robotics Laboratory
S.ANUSHARON
212222240010
Department of Artificial Intelligence and Data Science/ Machine Learning
Saveetha Engineering College
```
