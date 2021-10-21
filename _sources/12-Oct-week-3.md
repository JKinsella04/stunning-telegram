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