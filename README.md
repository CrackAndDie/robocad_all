# gitcad_robot
My project with mine idle for visual robot
## robocad
**robocad** includes important functions for programming visual (or real) robot with 3 omni wheels.  
At first you need to open IDLE in the folder called **"gui"** and start **"gui.exe"**  
To open viewer you need to go to the folder called **"view"** and then start **"view.exe"**   

![](https://github.com/CrackAndDie/gitcad_python_private/blob/master/Yandex/cad_low_d.png)
## all available functions  
#### robotino.drive_to_point(tup, self_speed=False, speed=5)
Driving to needed point  

:param tup: Tuple of X, Y and Omega  
:param self_speed: If True you can set your speed to robot, else robot will drive smooth  
:param speed: Speed to drive if self_speed == True  
:return: None  
  
### robocad.position_reached
Returns True if position reached  
   
### robocad.drive_system(tuple)
Drive system includes 3 motors
Program will be faster if you use this but not each motors (drive_m1-3)  
  
:param tup: Tuple of speeds to motors (range from -300 to 300)  
:return: None  

### robocad.get_coords()  
Function that returns tuple of coordinates (not sure that they are correct)  

### robocad.center_sensor()
Function that returns distanse from robot's center to the red tetragon  


