# Chassis and Drivetrain
*go back to [/r/FTC wiki](/r/FTC/wiki)*

__This article is up to date as of Dec 08, 2017.__


Chassis and drivetrain is the foundation of the robot. While it might seem a relatively simple construction, its importance can nto be overestimated. Most of problems plaguing new teams comes from the desing of their drivetrain.

Instead of making your own chassis and drivetrain, you can buy a ready kit. Most popular such kit is AndyMark's [TileRunner](http://www.andymark.com/TileRunner-p/am-tilerunner.htm), available in different configurations. This is the easiest solution, 
recommended for new teams. 

The information below is for teams that are building their own drivetrain rather than using a kit. 

## Drivetrain type

Below is the list of the most common types of drivetrain used in FTC.

* *Tank drive*: wheels/tracks on the left and right side of the robot are controlled independently. To turn, 
wheels/tracks on one side rotate forward, and on the other, backwards. This is by far the most common type of design. 

To reduce the friction when turning, some teams use one pair of high-traction wheels such as AndyMark stealth wheels and one pair of omni wheels (see discussion of different wheels below). Another common solution is using 3 wheels on each side, mounting the center wheel so that it is slightly lower (usually about 2mm) than the front and rear wheels and thus carries most of the weight. This design is popular in FRC, where it is sometimes called _west coast drive_ . This design is also used in AndyMark's TileRunner.

* *Mecanum drive*: using special mecanum wheels  allows the robot to move sideways.  This gives more manuevrability, but is more complicated to build and program. This design discussed in detail in a [separate article](TODO).

* *Holonomic drive*: using four omniwheels mounted at the corners of the frame at 45 degree angle allows the robot to move sideways. This gives more manuevrability, but less powerful robot. This design  is more complicated to build and program; it is discussed in detail in a [separate article](TODO). (Strictly speaking, name _holonomic design_ covers  all designs that allow sideways motion, including mecanum drive; however, in FTC world, _holonomic design_ usually refers to the design with four omni wheels.)


* *Swerve drive*: each of the four wheels is mounted on a special module which can be turned in any direction using an auxiliary servo or motor. This allows great maneuvrability and speed without sacrificing power. This drive is probably the most complex and difficult to build and is rarely used. You can see an example of such a drive used in 2017-18 season by team Hanks Tanks in their [reveal video](https://www.youtube.com/watch?v=TnkryF89va4).


## Wheels 

Most teams use 4 in diameter wheels. Different options include

* Regular wheels from [Actobotics](https://www.servocity.com/4-heavy-duty-wheel) and [Tetrix](https://www.tetrixrobotics.com/wheels/TETRIX-Wheels). These wheels offer decent traction on soft tiles, but might not be enough for climbing ramps and other inclined surfaces.

* [Stealth wheels](https://www.andymark.com/Stealth-Wheels-p/am-stealthwheel.htm) from AndyMark. These wheels provide much higher traction than the regular Actobotics or Tetrix wheels. They come in different variants, with different traction and durability and with different bores. For drive wheels, use black (Durometer 60); if you need really high traction, use blue (Durometer 50), but be prepared that turning might be difficult.  Select 8mm bore for easy attachment to Tetrix parts; to attach to Actobotics, use Actobotics to Tetrix [adapter](https://www.servocity.com/hub-adaptor-b). 

* Omni wheels have rollers along the outer edge of the wheel, which allow them  to roll freely perpendicular to the drive direction. 
They can be used in tank drive design or in holonomic drive. Such wheels are available from [Actobotics](https://www.servocity.com/4-omni-wheel) and [Tetrix](https://www.tetrixrobotics.com/TETRIX-Omni-Wheel-Packs).

* Mecanum wheels are discussed in the section on [mecanum drive](TODO).

## Mounting the wheels

The easiest way to mount the wheels is direct mount, putting the wheels on the output shaft of the motors. However, this is not recommended except for lightest robots: lateral load on motor shaft puts more stress on the motor and might eventually damage the motor gearhead. Instead, it is recommended to mount the wheels on axles  supported by ball bearings (for Actobotics) or bushings (for Tetrix) and power them using chains, timing belt, or gear transmission. 

If you are using Tetrix axles (4.7 mm), it is highly advised to support the axle on both sides of the wheel. When using 1/4" axle (Actobotics), supporting on both sides of the wheel is recommended for heavier robots. 


## Motors 

Common choices for the motors are AndyMark's [Neverest 40](http://www.andymark.com/NeveRest-40-Gearmotor-p/am-2964a.htm) or [Neverest Orbital 20](http://www.andymark.com/NeveRest-20-12V-Planetary-Gearmotor-p/am-3637.htm). Teams using REV Robotics building system can also use their [HD Hex Motor](http://www.revrobotics.com/rev-41-1301/).  Most teams use 2 motors on each side, for more power; however, it is also possible to use one motor per side. 

Using Neverest 40 with 4 inch wheels without any reduction gives a slightly slow but powerful robot; using Neverest 20 gives a very  fast robot (maybe too fast), but not as powerful. You can also use gearing up/down (or chain trasnsmission with ration different form 1:1, such as 3:2) for the combination of speed and power which works best for your design.

## Chains, gears, belts
Unless you are directly mounting wheels on motors, you need a way of transferring power from motors to the wheels. It can be done using gear trains, chain transmission, or timing belt. Here are some hints on best ways to do it:
 
* In all situations, avoid using set screw hubs for drivetrain. Instead, use AndyMark's [nubs](http://www.andymark.com/AndyMark-Nub-p/am-nub.htm) for Tetrix systems, Actobotics D-profile hubs [1](https://www.servocity.com/0-770-set-screw-d-hubs), [2](https://www.servocity.com/0-770-clamping-d-hubs), or REV Robotics hex hubs. If you must use set screw hubs, use thread locker such as [Loctite Blue](https://www.amazon.com/dp/B000I1RSNS). 

* When using chain (most FTC teams use #25 chain), pay attention to alignment of the sprockets. The chain shoudl have very little slack, but should not be taut. 

* If using timing belt (such as Andy Mark's [HTD](http://www.andymark.com/Belt-Pulley-s/502.htm) or Actobotics [XL](https://www.servocity.com/0-375-3-8-wide-timing-belts), the belt should have no slack. It is advised to use idle pulleys as belt tensioners. 






## Programming 
TODO

*All content on this wiki is licensed under the [Creative Commons Attribution-ShareAlike 4.0](https://creativecommons.org/licenses/by-sa/4.0/) liscense.*
/r/FTC thanks you for reading this article and asks you to [contribute](https://github.com/GeekyStudios/rFTC-wiki) soon.