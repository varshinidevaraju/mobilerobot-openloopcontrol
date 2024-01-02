# MobileRobot-Openloopcontrol
## Aim:

To develop a python control code to move the mobilerobot along the predefined path.

## Equipments Required:
1. RoboMaster EP core
2. Python 3.7

## Procedure

## Step1:
Define the robots kinematics.
## Step2:
Design a Control Input Profile.
## Step3:
Implement the Control Algorithm.
## Step4:
Upload the Control Inputs to the Robots.
## Step5:
Execute the Open_Loop Control.

## Program
```
#DEVELOPED BY: VARSHINI D
#REGISTER NUMBER: 212223230234

from robomaster import robot
import time
from robomaster import camera
if _name_ == '_main_':
ep_robot = robot.Robot()
ep_robot.initialize(conn_type="ap")
ep_chassis = ep_robot.chassis
ep_led = ep_robot.led
ep_camera = ep_robot.camera
print("Video streaming started.....")
ep_camera.start_video_stream(display=True, resolution = camera.STREAM_360P)
ep_chassis.move(x=2.5, y=0, z=0, xy_speed=1.5).wait_for_completed()
ep_led.set_led(comp = "all",r=255,g=0,b=0,effect="on")
ep_chassis.move(x=0.4, y=0, z=80, xy_speed=1.5).wait_for_completed()
ep_led.set_led(comp = "all",r=0,g=255,b=255,effect="on")
ep_chassis.move(x=1, y=0, z=0, xy_speed=1.5).wait_for_completed()
ep_led.set_led(comp = "all",r=255,g=204,b=0,effect="on")
ep_chassis.move(x=0, y=-1.5, z=0, xy_speed=1.5).wait_for_completed()
ep_led.set_led(comp = "all",r=255,g=255,b=0,effect="on")
ep_chassis.move(x=0, y=0, z=60, xy_speed=1.5).wait_for_completed()
ep_led.set_led(comp = "all",r=255,g=0,b=255,effect="on")
ep_chassis.move(x=1.5, y=0, z=0, xy_speed=1.5).wait_for_completed()
ep_led.set_led(comp = "all",r=204,g=255,b=255,effect="on")
ep_chassis.move(x=0, y=0, z=43, xy_speed=1.5).wait_for_completed()
ep_led.set_led(comp = "all",r=255,g=128,b=128,effect="on")
ep_chassis.move(x=1.4, y=0, z=0, xy_speed=1.5).wait_for_completed()
ep_led.set_led(comp = "all",r=255,g=128,b=128,effect="on")
ep_chassis.move(x=0, y=0, z=-85, xy_speed=1.5).wait_for_completed()
ep_led.set_led(comp = "all",r=255,g=0,b=255,effect="on")
ep_chassis.move(x=-2, y=0, z=0, xy_speed=1.3).wait_for_completed()
ep_led.set_led(comp = "all",r=0,g=255,b=255,effect="on")
ep_chassis.move(x=0, y=0, z=-98, xy_speed=1.5)wait_for_completed()
ep_led.set_led(comp = "all",r=153,g=51,b=0,effect="on")
ep_chassis.move(x=0.6, y=0, z=0, xy_speed=1.3).wait_for_completed()
ep_led.set_led(comp = "all",r=153,g=51,b=153,effect="on")
ep_chassis.move(x=0, y=0, z=0, xy_speed=1.3)wait_for_completed()
ep_led.set_led(comp = "all",r=51,g=102,b=255,effect="on")
    
time.sleep(4)
ep_camera.stop_video_stream()
print("Stopped video streaming.....")
ep_robot.close()
```

## MobileRobot Movement Image:

![robo](./img/robomaster.png)

Insert image here

![](car_ss.jpg)

## MobileRobot Movement Video:

Upload your video in Youtube and paste your video-id here

https://www.youtube.com/watch?v=Lfw8zWgJ2QU

## Result:
Thus the python program code is developed to move the mobilerobot in the predefined path.

```
Mobile Robotics Laboratory
Department of Artificial Intelligence and Data Science/ Machine Learning
Saveetha Engineering College
```
