---
title: N086
author: Shazeen Feroz
description: Mobile Dynamic Hexapod
created_at: "2026-05-23"
---

# May 23 : Reasearch

Spent Time Learning the Basic of Kinematics and calculus behing hte movement of the robot
and how i would make it dynamicalyy react to it enviroment

**Total time spent: 2 hours**


# June 11 : Main Body Model

Spent time planning and designing the main body fro the robot using onshape
this is the prototype model and will be improved but with the skills i have now
i created the main chassy for all other components to fit inside and on 

**Total time spent 4 hours**

# July 28 : Design choice

In order to differentiate myself and innovate in the space of hexapod construction i have opted towards a special design that takes inspiration from nature
.The tiger beetle is the fastest known land invertebrate and with six legs it fits perfectly and inspiration to a build a fast compact hexapod.
I calculated in relation to its body the length of a tiger beetles legs are that the front legs must be about 0.9 body lengths and the middle legs should be around 1.1 body length and the back legs 1.3 body lengths with the total stance being 2.2 body lengths.
The ratio of segments for each legs lies at roughly in the ratio 1:4:5 -> Coxa, Femur and Tibia Respectively so that means if i wanted a body length of 20 cm this means that my leg length would be  18cm for the front legs 22cm for the centre and 26cm for the hind legs with femur and tibia lengths of 8cm and 10cm for the front and 10cm and 12cm for the centre and 12cm and 14cm for the hind respectively 
To match the efficiency of a tiger beetle it also has a ground Clearance of 4-5cm 

<img width="576" height="1024" alt="IMG_0411" src="https://github.com/user-attachments/assets/73364fa6-c141-40d7-9ce1-c7f94c17c134" />

**Total Time Spent 4 hours**

# August 5 : Servo Requirements

In order to assign part i first have to calculate the forces and condition under which the parts will operate under.
First number to be calculated was the estimated length of the leg which i had previously determined to be 18cm 22cm and 26cm now with appropriate length 
calculated i only need one more factor in order to calculate the moment of force and total torque experienced by the motor.
I will be using a special carbon fiber filament known as PA12-CF to maintain a low weight profile as the legs of the robot have to account for a maximum of 
30% of the hexapods weight. Each set of legs have varying weights to most efficiently maximise thrust from the motors
---
Part: Weight(g)
Front: 112.5
Centre: 157.5
Rear: 180
---
With the chosen filament having a density of 1.06g/cm^3 this provide adequate working volume for the legs.
Now to calculate the moment i simply multiple the length of the leg by the weight of the leg in kilos and i end up with calculation that require a 
servo that can handle 2-4.5kg of torque. However these calculation may be exaggeration as in no instance does the movement of the hexapod require the leg to 
be fully extended out ward. In light of this i chose to make more realistic calculations for the torque by first figuring out the nominal stance moment of the arm at a 4.5cm ground clearance √(.10)^2-(0.045)^2) = 0.174m then i can simply multiply this by mass*g to give me an estimate of the torque that each leg is under to get the final value of 8kg with saftey factor taken into account

<img width="576" height="1024" alt="image" src="https://github.com/user-attachments/assets/82cd7169-1c1f-4e51-9f2c-de49d3dcc18d" />

**Total Time Spent 3 hours**


**Total Time Spent 5 Hours**
