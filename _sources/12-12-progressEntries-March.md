# March 2021 Progress Entries

## 3/2/21
### Attendance: &#9745; Brody, &#9745; Derek, &#9745; Dylan, &#9745; Ian, &#9745; Jack
#### Today's Goals
- Retune 15 second autons
- Begin retuning skills auton
- Replace the track and flaps with 2in. flex wheels
- Driver practice

#### Auton Retuning
Today we spent the majority of practice retuning our autonomous routines. Jack retuned all of our lateral movements so instead of halting at the end of every movement we now slow down smoothly. This will help with improving consistency since the tracking wheels no longer slip off the ground since before the back wheels including the tracking wheels would lose contact to the mats when the robot stopped. 

#### Building Improvements
The only building improvement Dylan and Derek made today was replacing the track and flaps with our flex wheels. Having flex wheels in replace of the track and flaps is better because the robot now has more consistent contact with the balls which allows the robot to descore from the goals much quicker. 

#### Driver Practice
Since the robot descores much quicker, Derek is now able to reliably descore all but 4 of the blue balls during driver skills while scoring 12-14 red balls for a total of 120-122 points. 

## March Timeline
<img src="././_images/3-March/mar_calendar.png" alt="mar_calendar.png"/>

### Goals Created
- 106-119 skills auton
- 120-126 driver 

### Goals Accomplished
- retuned 15 second auton
- replaced track and flaps with 2in flex wheels

## Pre-State Championship 
### Our Robot
- For the State Championship, we decided to make our github repository of our code public. In there is all of our code as well as our README and wiki that explain some concepts of our robot in more depth. [Our Code.](https://github.com/PSASchool/9447H-ChangeUp)
- The repository for this jupyter-book can be found [here.](https://github.com/PSASchool/OperationPheasant/tree/gh-pages)

<iframe width="560" height="315" src="https://www.youtube.com/embed/e2y2DPhcRHE" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

### Drive Strategy
- We will mainly be using the circle strategy this Saturday as well believe it to be the best for us generally. Depending on the matchups we may switch to the hourglass strategy or possibly the 17-16 win if needed.
<img src="././_images/1-January/1-12-21/circle_Strategy.PNG" alt="circle_Strategy.PNG" style="width: 200px;"/>


### Auton Strategy
- We will be using our home row auton with descoring as our default auton phase. We will also create an auton to score in either the middle goal or the middle right goal. 

### Skills Strategy
- We are going for a 200+ pt skills score for this tournament as we believe that 1st place will be around 200-210. To Achieve a score in this range we are going to be attempting a max driver skills run and will be going for a 106-120 auton run. The big range in auton score is based on how many blue balls we are able to descore while we go to each goal.  

### Robot feature list
#### Mechanical Features
- 333 RPM Drive Base.
- 600-600-840 RPM (intakes - middle rollers - top rollers).
- 5 Roller setup with hole in back for ejecting enemy's balls.
- Expanding section of intakes to allow for easier intaking and descoring in all goals including the middle goal.
- 4 VEX Pulleys (2 on each side) to help the robot glide on the walls.
- Velcro license plates for easy swapping. 
#### Sensor List
- 2 Tracking wheels with V5 Rotation Sensors to track lateral movement of the robot.
- 3 V5 Inertial sensors to get accurate absolute angle of the robot.
- 1 V5 Distance sensor to index balls at the top of the robot
- 1 V5 Distance sensor to detect the prescence of a goal in front of the robot.
- 2 V5 Optical sensors to detect the color of the balls.
#### Software Features
- Fully Automated Autosorting
    - split into two types, one for picking up balls and the other for when scoring at a goal.
- Slew code for smooth accerleration in both driver and autonomous phases.
- PD loops for both turning and lateral movements for autonomous.
- Loading Screen that restricts us from interacting with the robot before it finishes running setup functions.
- Select alliance color through GUI.
- Select starting position and autonomous routine through GUI.
     - The Auton builder allows us to run parts of home row autonomous if needed in case we do not need to score in all three goals. Being able to manipulate our autonomous before the match without having to actually change any code gives us more control than a conventional auton selector.
     
 
## Post States Reflection
Our states experience was very informative. It helped us see our strongpoints as well as seeing what we need to improve on for 2021 worlds and other future events. In states we ranked 3rd in skills and went 2-4-0 in qualifications and we won excellence. Our strongest points are our build quality and our autonomous and our weakest point is our driving. 

### Plan moving forward
- Robot design specifically for LRT format
- 15 second auton routine for LRT format
- Driver practice

## 3/16/21
### Attendance: &#9745; Brody, &#9745; Derek, &#9744; Dylan, &#9745; Ian, &#9745; Jack
#### Today's Agenda
- Finish CAD for new robot
- Begin planning our strategies for LRT

<img src="././_images/3-March/3-16-21/new_robot_2nd_angle.PNG" alt="new_robot_2nd_angle.PNG" style="width: 200px;"/>
<img src="././_images/3-March/3-16-21/new_robot_side.PNG" alt="new_robot_side.PNG" style="width: 200px;"/>
<img src="././_images/3-March/3-16-21/new_robot_3rd_angle.PNG" alt="new_robot_3rd_angle.PNG" style="width: 200px;"/>
<img src="././_images/3-March/3-16-21/new_robot_angle.png" alt="new_robot_angle.png" style="width: 200px;"/>
<img src="././_images/3-March/3-16-21/robot_front_close_up.PNG" alt="robot_front_close_up.PNG" style="width: 200px;"/>
<img src="././_images/3-March/3-16-21/second_drive_base_close_up.PNG" alt="second_drive_base_close_up.PNG" style="width: 200px;"/>

#### Major Changes 
- Removed the ability to eject balls out the back.
- Increased drive base speed from 333 rpm to 360 rpm.

#### Sensor changes
- Added another distance sensor to detect goal
- Move 1 optical sensor towards top of the robot for indexing.

#### Initial LRT Strategy
- AutoIndex instead of autoSort
> Since LRT requires us to score all balls not just our alliance color's we need to swap from autoSorting them out to now taking in all colors.
- 6 ball Middle Goal
> In LRT balls can touch our robot and still be scored so we can use this to score more than three balls in a goal which is very important.
- 15 second autonmous routine
> We need to figure out a path in which we can score the middle goal as well as the whole home row. Since we do not need to descore this should be possible. 

#### Goals Created
- Research past LRTs to see what kinds of strategies teams employ and begin developing 3-5 different strategies that we can test before worlds. 

## 3/23/21
### Attendance: &#9744; Brody, &#9745; Derek, &#9745; Dylan, &#9745; Ian, &#9745; Jack
#### Agenda for today
- Begin building new robot

#### Worlds Preparations
- This will be our last meeting before we submit our notebook for the worlds competition. To make sure we do not break any rules with the notebook submission, we will continue logging our progress but we will not push the updates to the notebook until after worlds so we do not manipulate our notebook past the submission phase. 

#### Parts of the Robot
 1. &#9745; Drive base 
 
 2. &#9745; Front intakes 
 
 3. &#9745; Roller tower & Bottom Roller
 
 4. &#9744; Middle & Top Roller
 
 5. &#9745; Primary hood
 
 6. &#9744; Secondary hood
 
 7. &#9744; Backboard 
 
 - Today Derek and Dylan began working on the new robot design. They began by building the new 360 rpm drive base. When building it they made sure that it was as low friction as possible. Each wheel indepently can free spin for around 15 seconds and even with all of the gears connected they still have low friciton. 
 - Derek mounted the front intakes onto the robot. We transfered the intakes from the old robot over to the new robot since they worked very well for us.  
 - We also began working on the roller tower and got the tower and the bottom roller built.
 - The robot currently weighs 10.2 lbs and when it is completed it should weigh no more than 12lbs. The robot should drop about 4lbs from our old robot which will help with not burning out our drive base motors. 
 - One minor design change we made was the cortex placement. To make interacting with the GUI easier we moved the cortex to the side so in case we start with the back of the robot near a goal we do not have any trouble picking our alliance and autonomous routine.

<img src="././_images/3-March/3-23-21/new_robot_side.PNG" alt="new_robot_side.PNG" style="width: 200px;"/>
<img src="././_images/3-March/3-23-21/new_robot_angle.PNG" alt="new_robot_angle.PNG" style="width: 200px;"/>

#### Upcoming Schedule 
<img src="././_images/3-March/3-23-21/schedule.PNG" alt="schedule.PNG"/>

- Goals Created
    * Complete 1st half of new Robot by 3/23/21
    * Complete 2nd half of new Robot by 3/30/21
    * Robot ready for first LRT on 4/10 by 4/6/21
- Goals Accomplished
    * Complete 1st half of new Robot by 3/23/21
    
The second half of April is not fully planned out yet, because we do not know when our next LRT tournament will be. Depending on how well our robot performs at our first LRT on 4/10 we may do our second LRT also in April. For now we have just planned out what our next couple weeks will be since we need to focus on completing the robot and getting enough practice to have a consistent auton as well as have Derek, our driver, fully adjust to the game format.  

## 3/30/21
### Attendance: &#9745; Brody, &#9745; Derek, &#9744; Dylan, &#9745; Ian, &#9745; Jack

#### Goals For Today
- Finish second half of the robot
 
#### Goals Accomplished
 1. &#9745; Middle & Top Roller
 
 2. &#9745; Secondary hood
 
 3. &#9745; Backboard

<img src="././_images/3-March/3-30-21/robot_angle.PNG" alt="robot_angle.PNG" style="width: 200px;"/>
<img src="././_images/3-March/3-30-21/robot_front.PNG" alt="robot_front.PNG" style="width: 200px;"/>

Today Derek finished the rest of the robot by attaching the secondary hood and adding the top roller and the middle roller's flex wheels. For the backboard we decided to split it into two parts, a rubber band ramp and a polycarbonate plate with foam. The ramp is to help guide the balls up into the first roller in the tower and then the polycarbonate plate is the back wall of the robot that applies enough compression to let the rollers move the balls quickly.

<iframe width="560" height="315" src="https://www.youtube.com/embed/_9fPEe7zsto" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>


#### Timelime Changes
The LRT scrimmage that was on 4/10 has been cancelled so now we have signed up for two other tournaments, one on 4/22 and one on 5/1. With this extra time before our first tournament we will have ample time to perfect the robot's cycle time and develop our autonomous routine as well as multiple driver strategies. 