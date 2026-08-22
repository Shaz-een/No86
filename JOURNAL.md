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


**Total Time Spent 4 hours**


# August 6 : Gait and Movement
To most effectively maximise the power of the motors and the design the final piece of the mimicry of the tiger beetle has to come together to construct a 
machine built for speed the movement. By analysing footage of the movement of tiger beetle i have determined the way in which they move ,it uses an 
alternating tripod gait to ensure stability under high speeds they have two groups of limbs which operate inversely Group A (Consisting of the Front Left 
,Rear Left and Middle Right) and group B (Front Right ,Rear Right and Middle Left) When group a touches the ground group b lifts and swings forward the 
beetle alternates between these two tripods at fractions of a second (a full stride cycle occurs in as little as 30–50 milliseconds).Standard hobby servo 
motors cant reach the torque or speed needed for a 30Hz movement so Brushless motors with planetary gear box would be needed. At High Speeds rigid parts 
will shatter under the load so flexible carbon fibre would be used and Just as the beetle runs "blind" during its sprint, high-speed robots cannot rely on 
slow visual camera pipelines mid-step. Instead, they use Central Pattern Generators (CPGs)—pre-programmed, high-frequency mathematical gait cycles—and rely 
on fast onboard IMUs and tactile switches for rapid trajectory adjustments.

<img width="1538" height="743" alt="Screenshot 2026-08-12 002559" src="https://github.com/user-attachments/assets/99753a35-8af3-4612-95d3-81416ae8624e" />
<img width="1537" height="705" alt="Screenshot 2026-08-12 002531" src="https://github.com/user-attachments/assets/01751403-f68a-4268-9d1e-e1029b410ce0" />
<img width="1536" height="751" alt="Screenshot 2026-08-12 002638" src="https://github.com/user-attachments/assets/4f5121cf-4459-427a-a932-6e2c357c4a02" />


**Total Time Spent 3 hours**

# August 14 : Inverse Kinematics Part 1

I have progressed to the point where I need to stat the equation and code behind the systems of the hexapod. I started with watching a couple of YouTube 
videos for research and recapping basic trigonometric equation and learning why inverse kinematics exists I then started drawing and mapping out the 
equations. I drew a set of axis in accordance to the right hand set of axis commonly used in inverse kinematics i first labelled the lengths of the segments 
of the leg in the diagram then drew lines to connect the position where the servos will be placed to and then created equation to calculate theoretical 
angles and lengths needed to precisely move the legs where they needed to be it was a series of basic cosine and Pythagoras theorem that had to be 
implemented with a different context in mind. This is only the first section of kinematics and as it stands it is all theoretical equation with no real unit 
or measurements a true full 3D model of the hexapod will have to be constructed in order to produce any valuable and programmable data 


<img width="641" height="855" alt="image (1)" src="https://github.com/user-attachments/assets/ec58e01b-f6a0-4430-a112-dc82e6d28fe3" />

<img width="641" height="855" alt="image (2)" src="https://github.com/user-attachments/assets/3ca41998-c578-4b11-8267-b59d58276eb9" />

**Total Time Spent 3 hours**

# August 18 : Parts Assignment and List

To construct and build a high speed hexapod that mimics the movement and proportions of a tiger beetle we need to find part that can operate abos 30Hz and high spec hardware that is capable of delivering speed and movement without sacrificing structural integrity all whilst being lightweight.
The part required for full functionality are : Servo Motors with appropriate torque , An IMU to monitor pitch and roll and position during high speed movement , A microcontroller to control the 18 joint and the inverse kinematics of each of the six legs  
This is a list of item that i have put together that I believe fit the criteria 


| Part Name |  Function | Key Specifications | Quantity | Est. Unit Price (USD) | Total Price (USD) |
|---|---|---|---|---|---|
| **Waveshare ST3215 Servo** | Actuation (Coxa, Femur, Tibia) | **Torque:** 30 kg·cm @ 12V Encoder: 12-bit Magnetic (360° position feedback) Control: TTL Serial (1Mbps) Operating Voltage: 6V–12.6V | 18 | ~$18.00 | $324.00 |
| **Teensy 4.1 Microcontroller** | Master Logic & Trajectory Engine | CPU: 600 MHz ARM Cortex-M7 Memory 8MB Flash / 1MB RAM Calculates 18-joint Inverse Kinematics   | 1 | ~$31.50 | $31.50 |
| **Waveshare Bus Servo Adapter (A)** | Serial Communication Interface | Converts Teensy Hardware UART (TX/RX) to half-duplex single-wire bus; distributes 12V battery power directly. | 1 | ~$5.00 | $5.00 |
| **MPU-9250 / MPU-6050** | IMU (Orientation & Balance) |  Gyro + Accelerometer to detect pitch/roll and slight wiggles during sprint gaits. | 1 | ~$4.00 | $4.00 |
| **3S LiPo Battery** | Main Power Source | **Voltage:** 11.1V (12.6V peak) Capacity:** 2200mAh – 3000mAh Discharge Rating:** 50C–75C Direct power to ST3215 servos.* | 1 | ~$22.00 | $22.00 |
| **DC-DC Buck Converter (5V/3A)** | Logic Power Regulation | Step-down converter from 3S LiPo (~12V) down to 5V to power the Teensy 4.1 MCU cleanly. | 1 | ~$3.50 | $3.50 |
| **Aluminum Servo Arms (25T)** | Joint Coupling | High-strength metal servo horns matching the ST3215 25T spline output. | 18 | ~$0.75 | $13.50 |


