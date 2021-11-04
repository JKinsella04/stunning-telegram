# 10/19/21-10/21/21
## 10/19/21
### Attendance: &#9745; Brody, &#9745; Derek, &#9745; Jack
### Goals:
- Begin working on skills autonomous.
- Continue driver practice.
### Accomplished:
- &#9745; Begin working on skills autonomous.
- &#9745; Continue driver practice.
#### How:
- Jack began programming the skills routine by mapping out the whole routine. For our routine we will be going for a 220 point auton routine. We will do this by elevating 4 goals and scoring 3 in the home zones. 
- For our skills autonomous we will be using absolute point to point movments to ensure its accuracy. We will be using the coordinates from the GPS sensor to get our robot's position.
- Derek continued practicing driving by running more driver skills runs. Currently his best run is a 1.5 minute run so he is getting close to being in the minute time frame since last week he was averaging 2 minute runs.
- In addition to the GPS sensor Jack also has implemented Odometry for our robot. We use the robot's wheel movements to get its position in (x,y) coordinates.
```c++
switch (PositionTrackerState) {
    case PositionTracker::RELATIVE: {
      thetaDeg = ( lf_Imu.get_heading() + lb_Imu.get_heading() + rf_Imu.get_heading() + rb_Imu.get_heading() )/4;
      thetaRad = macro::toRad(thetaDeg);

      rotation = ( LF.get_position() + LB.get_position() + RF.get_position() + RB.get_position() ) /4;
      
      break;
    }
    case PositionTracker::GPS: {
      gpsData = gps.get_status();
      
      thetaDeg = abs(gps.get_heading() - 360);
      thetaRad = macro::toRad(thetaDeg);
      
      posX = gpsData.x * 1000;
      posY = gpsData.y * 1000;

      // GPS Error
      error = gps.get_error();
      break;
    }
    case PositionTracker::ODOM: {
      thetaRad = abs(lf_Imu.get_heading() - 360) * (PI / 180);
      thetaDeg = macro::toDeg(thetaRad);

      currentL = ( LF.get_position() + LB.get_position() ) / 2;
      currentR = ( RF.get_position() + RB.get_position() ) / 2;

      deltaL = currentL - lastL;
      deltaR = currentR - lastR;

      posX = posX + ((deltaL + deltaR) / 2) * cos(thetaRad);
      posY = posY + ((deltaL + deltaR) / 2) * sin(thetaRad);

      lastL = ( LF.get_position() + LB.get_position() ) / 2;
      lastR = ( RF.get_position() + RB.get_position() ) / 2;
      
      break;
    }
}
```
#### Why:
- Jack plans for a 220 auton routine because we want to win skills at each competition this year and with a high scoring auton like this we will most likely be able to consistently win skills.
- We are using point to point movements because in 60 seconds error can build up a lot so to mitigate it we will be using point to point to fix any error that accumulates.
- Currently all Derek needs to improve himself is just to keep on practicing, he understands what he wants to achieve and just needs to spend ample time doing it to get it under a minute.

### Plans for next Practice:
- Continue coding the skills autonomous.
- Continue driver practice.

```{important}
Last Edited on 10/19/21.
```

## 10/20/21
### Attendance: &#9745; Brody, &#9745; Derek, &#9745; Jack 
### Goals:
- Continue coding the skills autonomous.
- Continue driver practice.
### Accomplished:
- &#9745; Continue coding the skills autonomous.
- &#9745; Continue driver practice.
#### How:
- Jack continued working on the autonomous routine and can score 60 of the 220 points consistently. Currently we score one red alliance goal on the red platform and one neutral goal in the red home zone. After we score these two we will begin moving to score a blue alliance goal and another neutral goal for 120 points.
- Derek continued driver practice and now is able to finish in 1.25 minutes. This is solid improvement from yesterday as he was only 15 seconds over instead of 30 seconds over. Since tomorrow is just a driver practice day we plan on reaching our goal of finishing the run in 60 seconds.
#### Why:
- Jack continued programming the autonomous and spent the day improving the consistency of scoring the first two goals as opposed to trying to score the other goals. It is important that we consistently score the first two goals and move on once those are consistent.
- Derek has been solidly increasing his driver skill by completing the same task in shorter and shorter time intervals. With the extra time tomorrow for him we plan on him being able to reach the 60 second requirement. 
### Plans for next Practice:
- Continue coding the skills autonomous.
- Continue driver practice.

```{important}
Last Edited on 10/20/21.
```
## 10/21/21
### Attendance: &#9744; Brody, &#9745; Derek, &#9744; Jack 
### Goals:
- Continue driver practice.
### Accomplished:
- &#9745; Continue driver practice.
#### How:
- Derek continued practicing driving today by running driver skills runs.
- To best use our time during driver practice days, we are using a new analyzing in which Derek drives for one minute then we set a timer for one minute to analyze what was good and bad in the run. Then once the timer goes off, we reset the field and Derek does another practice run. 
#### Why:
- We started timing our analyzing period because we have a problem of spending too much time analyzing what was wrong instead of actually practicing. This new routine is helpful for us since it forces us to be more aware of the time we are using during driver practice, to maximize the amount of actual driver practice Derek gets.
### Plans for next Practice:
- Continue coding the skills autonomous.
- Continue driver practice.

## Robot Release 1.0
- Today will be the last entry for our first tournament, so below here we will explain everything we are bringing to our first competition.

### Robot Features
1. 333 RPM drive base. 
> We will be faster then most of the teams there.
2. 4 bar lift + Pneumatic clamp.
> A fast Lift with PID + Slew to make it move efficiently and accurately.
3. Small mobile goal lift.
> Can carry a mobile goal the entire match while fighting over other goals.
4. Angled c-channels
> With our two 45 degree c-channels we will be able to tip the enemy's platform if goals are elevated on it.

#### Code Features
1. Absolute Position Tracking from Odom AND the GPS sensor.
2. PID and Slew control for all moving mechanisms.
3. Threads and State machines to properly manage every mechanism independently.

#### Auton Routines
1. Full Auton Win Point routine that also grabs one yellow goal.
2. Elim Auton that grabs all three yellow mobile goals.
3. Skills auton that scores at least 120 points.

```{important}
Last Edited on 10/21/21.
```