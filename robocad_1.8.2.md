# gitcad_robot
My project with mine idle for visual robot
## robocad
**robocad** includes important functions for programming visual (or real) robot with 3 omni wheels.  
At first you need to open IDLE in the folder called **"gui"** and start **"gui.exe"**  
To open viewer you need to go to the folder called **"view"** and then start **"view.exe"**   

![](https://github.com/CrackAndDie/robocad_all/blob/master/pics/cad_low_d.png)
## at first it is a specific syntax
You need to write **do-while** sentences like  
```python 
do {
    your program
} while (condition)
```  
<h2 align="center">VIEW</h2> 
  
### robocad.drive_to_point(tup, self_speed=False, speed=5)
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
  
:param tup: Tuple of speeds to motors  
:return: None  

### robocad.get_coords()  
Function that returns tuple of coordinates 

### robocad.center_sensor()
Function that returns distanse from robot's center to the red tetragon  

### robocad.front_sensor()
Function that returns distance from the front of robocad to one of the red wall

:return: Distance (Float)

### robocad.reset_coords()
Zeroing coordinates

:return: None

### robocad.reset_gyro()
Zeroing gyro

:return: None

### robocad.reset_all()
Zeroing gyro and coordinates

:return: None

### robocad.drive_m1-3(speed)
Speed to the right, left and back motors

:param speed: Needed speed (range from -300 to 300)  
:return: None  

### now_time
Variable that stores now time

:return: Now time    

### time_of_start
Variable that stores time of start program

:return: Start time    

### robocad.get_image_path(im_name: str, start_x: int, start_y: int, infelicity=14, dispersion=3, is_start=True, power=3, reverse_x=False, reverse_y=True, number_in_arr=10, start_dis=3, slowly=True)  

Getting b/w image with black line by which it will drive

:param im_name: Image name (image needs to be in the same folder as program)  
:param start_x: X position of pixel on the image from which robot will drive  
:param start_y: Y position of pixel on the image from which robot will drive  
:param infelicity: Distance of return to last pixel that has more than one path  
:param dispersion: Dispersion of search nearest pixels  
:param start_dis: Start dispersion of search nearest pixels  
:param is_start: If True start_X and start_Y will be (0, 0)  
:param power: Coefficient to multiple to coords  
:param reverse_x: Reverses X coord  
:param reverse_y: Reverses Y coord  
:param number_in_arr: Last number to return in arr that has more than one path  
:param slowly: If True start_dis will go to dispersion by adding 2  
:return: Path includes array of tuples coords like [(0, 0), (9, 18), (4, 82)]  

### robocad.drive_by_image(arr: array)

Func to drive by image

:param arr: Path array  
:return: None  

### robocad.drive_by_axis(tup: tuple)

Func to drive by axis X, Y and rotate

:param tup: Tuple of X, Y and rot  
:return: None  

### robocad.save_cam_image(st='robocadcam.png')  

Saving image like image from robocad camera  
  
:param st: Name of image  
:return: None  

#### check this one  
![](https://github.com/CrackAndDie/robocad_all/blob/master/pics/bez_ugla.png)  
#### and one more image that show you how is robocad sees field  
![](https://github.com/CrackAndDie/robocad_all/blob/master/pics/where_1.6.png)  

### robocad.left_sharp()  

Distance from left infrared sensor  

:return: Distance (float)  

### robocad.right_sharp()  

Distance from right infrared sensor  

:return: Distance (float)  

### robocad.left_us()  

Distance from left ultrasonic sensor  

:return: Distance (float)  

### robocad.right_us()  

Distance from right ultrasonic sensor  

:return: Distance (float)  

#### and the sensors seems like... jedi(?) (shakaled 30%)  
![](https://github.com/CrackAndDie/robocad_all/blob/master/pics/sensors.jpg)  

### rcadout(st, end='')  

Print to console in IO panel  

:param st: String to print  
:param end: end of string for example \n or \t  
:return: None  

### rcadin()  

Returns input from IO panel  

You need to write code like this:  

```python 
do {
    robocad.inp = rcadin()
} while(glob_input is None)
do {
    rcadout(robocad.inp)
} while(False)
``` 

<h2 align="center">GUI</h2> 
  
<h2>Functions</h2> 

<h3>File</h3> 

#### New
create new file

#### Open
open file

#### Save
save file

#### Save as copy
save the file as copy

<h3>Edit</h3> 

#### Output terminal
terminal to print output (do not use it, use ctrl+b)

#### Right border
changes text field's width from 79 simbols to size of window

<h3>Robocad</h3> 

#### Run module
run your program

#### Default scale
return view window scale to default

#### Open map
open your txt file with description of your objects  
for example: https://github.com/CrackAndDie/robocad/blob/available_1.8.2/gui/self_map1.txt

#### EMS (Pause)
off power of robocad's motors

#### Stop program
stop your program

#### Reset robocad
restart robocad (view)

<h2>Robocad inforamtion</h2>

#### view_scale
view window scale

#### robocad_x
X coordinate of robocad

#### robocad_y
Y coordinate of robocad

#### rotation
robocad' rotation

#### pos_reached
True if position reached

#### fps_view
view window' fps

#### right_us
right ultrasonic' distance

#### left_us
left ultrasonic' distance

#### right_psd
right sharp' distance

#### left_psd
right sharp' distance

#### output_var_1-3
you can pass the value of a variable and see it

<h2>Program Panel</h2>  

![](https://github.com/CrackAndDie/robocad_all/blob/master/pics/prog_panel.jpg)  
Label with name of your file (if name is red - file is not saved)  
Backlight known words  
Auto adding close brackets  

<h2>Front Panel</h2>  

![](https://github.com/CrackAndDie/robocad_all/blob/master/pics/front_panel.jpg)  
Open with ctrl+e  
Information like in program panel  
3 buttons: Pause, Start, Stop  

<h2>IO Panel</h2>  

![](https://github.com/CrackAndDie/robocad_all/blob/master/pics/io_panel.jpg)  
Open with ctrl+b  
Output text field  
Slider to change sizes of fields  
Input text field  
  
<h2 align="center">FUNCAD</h2> 
  
### funcad.transfunc_vitality(array, value)
Not moronic transfer function powered by Coda (Vitality)

:param array: Input 2D array (1D array includes input and output values) like: [[1, 11], [2, 12], [3, 13]]  
:param value: Input of value to conversion by transfer function  
:return: Output is conversed input  

### funcad.in_range(val, min_v, max_v)
Func that checks that value in range min and max

:param val: Value that needs to check  
:param min_v: Min limit  
:param max_v: Max limit  
:return: Value in range  

### funcad.sign(val)
Retuns sign of val

:param val: Input value  
:return: Sign of input value  

### funcad.sigmoid(val)
Simple rational sigmoid

:param val: Input value  
:return: Sigmoided (?) value  

### funcad.transfunc(arr: list, val: float)  
Not moronic transfer function  
Powered by Coda (Vitality)  

:param arr: Input 2D array (1D array includes input and output values) like: [[1, 11], [2, 12], [3, 13]]  
:param val: Input of value to conversion by transfer function  
:return: Output is conversed input 

### robocad.cutter(val: float, min_v: float, max_v: float)  
Cuts value to range  

:param val: Value  
:param min_v: Minimal value  
:param max_v: Maximum value  
:return: Cut value  

