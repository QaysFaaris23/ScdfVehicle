# EA TANK PROJECT
Joshua's Journal~

<img src="https://github.com/QaysFaaris23/ScdfVehicle/blob/master/JoshuaJournal/Tank.jpeg" width ="300"> 



### Hi welcome to my  blog on this project that will be named Tank Brigrade

When i was first introduced to this project my team and i were tasked to brainstorm on what we wanted our
project to do and its functions. We came up with the idea of assisting Firefighters to fight fire and it was something that could be implemented in singapore.
 <img src="https://github.com/QaysFaaris23/ScdfVehicle/blob/master/JoshuaJournal/Auzzie%20fire.png" width ="300">
###### Other rough ideas we had
- Food delivery
- mine sweeping
- personal assitant (tank that follows you around
But all these ideas were not practical or not relatable to singapore


 


##### About the project~
When we decided on the project my team and i have decided on the workload of the project
and my job will be to handle the electronics part of the project and have to work very closely with both mechanical and software side of my teammates.
 
#### Getting started~
First brainstorming we decided the function of the tank will be firefighting and started to list down the Parts will be needed to build this project...
Parts i have decided (electrical)
- Esp 32
- FPV camera
- Camera monitor
- 2 18650 Lithium Batteries (3.7v each)
- 5V boost converter
- 2 Fs5106B servo motors
- Dual throw switch
- 2 12v DC motors
- stripboard
- 2 TP4056 charging modules
- 12 V water pump

I suggested placing a temperature sensing equipment such as a thermal camera but thought twice and decided that our vehicle have enough equipment and would be an overkill.



###### Power system

<img src="https://github.com/QaysFaaris23/ScdfVehicle/blob/master/JoshuaJournal/Power%20chematic.png" width ="300">
First thing i did was the Power systems as to me it was the most essential part of the project. Above is a schematic that i had planned out. This design was assisted by the Tso of EA lab and had helped multiple groups with this design. With this deisign both batteries can be charged with 1 micro Usb plugged into it.
But it had several problems with it as it short circuited the moment it was connected until a switched was placed in the positive input of the DC converter.

<img src="https://github.com/QaysFaaris23/ScdfVehicle/blob/master/JoshuaJournal/Editing%20tank%20track%20length.jpeg" width ="300">
When we first got our tank from the lectuerers we realised that the tank track were a little to large and had no tension of any sort to grip onto the wheels. From the image above you could see me removing part of the tracks to fit snugly into the wheels.

After realising that the parts i had planned was not sufficient i had requesting for the following in order to go through with my plans for the project.
<img src="https://github.com/QaysFaaris23/ScdfVehicle/blob/master/JoshuaJournal/Parts%20list%20REQ.png" width ="300">

###### L298N Motor Drivers
Next step was to test the L298N motor driver and recreate the schematic shown below and see if it works. In the end it did work but however i did not manage to capture a video of it. We used an external power source (not the one i planned) as it had not finished connecting yet.
<img src="https://github.com/QaysFaaris23/ScdfVehicle/blob/master/JoshuaJournal/L298N%20schematic.png" width ="300"> <img src="https://github.com/QaysFaaris23/ScdfVehicle/blob/master/JoshuaJournal/Testing%20L298N%20with%20motors.jpeg?raw=true" width ="300">

###### Power calculations
Following this we had tested the current draw for the components to calculate the power needed for the enitire circuit
<img src="https://github.com/QaysFaaris23/ScdfVehicle/blob/master/JoshuaJournal/Power%20calculation.png" width ="300">
Total of 38.7w needed to power everything.

##### servo motors
Now on to the servo motors. In order to control X-Y-Z axis we require 2 servo motors and ALOT of power. We realise the power draw from the 2 servo mmotors are way too much for the 2 18650 lithium batteries given to us. We had to use an seperate battery for it.
<img src="https://github.com/QaysFaaris23/ScdfVehicle/blob/master/JoshuaJournal/servo%20motors.png" width ="300">
Here is the newly planned and final schematic for the servo motors and ofcoures still connected to the same Esp32.


##### Esp 32
<img src="https://github.com/QaysFaaris23/ScdfVehicle/blob/master/JoshuaJournal/esp32.png" width ="300">
The power for the Esp will be taken from the L298N 5v output and will be sufficient to power the Esp and have stable voltage. Pin 12/13 will e used to control

###### Water Pump
Coming to our most important component of the project, the water pump. This is a 12v DC water pump. In order to draw water, the pump has to be fully submerge into the water which the reason for our water tank in the final product.
here is an image of the circuit for the water pump.
<img src="https://github.com/QaysFaaris23/ScdfVehicle/blob/master/JoshuaJournal/Water%20pump%20circuit.png" width ="300">

###### Putting everything together
After much planning of eqipment and the electronics, we have came up with the final schematic. Here are the images from the planning stage as compared to the final product.<img src="https://github.com/QaysFaaris23/ScdfVehicle/blob/master/JoshuaJournal/Planning%20circuit%20for%20Tank.jpeg" width ="300"> <img src="https://github.com/QaysFaaris23/ScdfVehicle/blob/master/JoshuaJournal/Overal%20schematic.png" width ="300"> 
With that i end the electrical journey of the project~ 

What i learnt the most important was that the circuits may work in the schematic but will not work in real life due to unforeseen circumstances such as a lose wire or bad solder which will lead to a short circuit of the components.
