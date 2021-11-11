# 11/9/21-11/11/21
## 11/9/21
### Attendance: &#9745; Brody, &#9745; Derek, &#9745; Jack
### Goals:
- Continue Driver Practice.
- Continue Skills Auton.
### Accomplished:
- &#9745; Continue Driver Practice.
- &#9745; Continue Skills Auton.
- &#9745; Improve Ring Blockers
#### How:
- Today Jack continued working the skills auton. The third goal we are scoring is the tallest neutral goal. To score this goal though, Jack had to change the scoring of the first two goals. After scoring the third goal the robot will pick up the blue alliance goal that on the AWP line. 
- Derek began practicing the 313 auton route. The route is the same as before except for that we now park with the two blue alliance goals as opposed to just elevating them.
#### Why:
- Jack had to change the first two goals scoring because for the platform to balance the tall middle goal we have to offset the first two goals to one side and then score the tall middle goal on the other. 
- To help with parking Derek cut down the size of the ring blockers to make sure that they do not dig into the ground like before. With the new small ring blockers, we have enough clearance to properly park on the platform with two goals.
### Plans for next Practice:
- Continue Skills Auton.
- Continue Driver Practice.

```{important}
Last Edited on 11/9/21.
```
## 11/10/21
### Attendance: &#9745; Brody, &#9745; Derek, &#9745; Jack
### Goals:
- Continue Skills Auton.
- Continue Driver Practice.
### Accomplished:
- &#9745; Continue Driver Practice
- &#9745; Fixed Auton Turning.

#### How:
- Jack fixed the turning problem by correcting the calcDir function. Before it would add 360 when the target or current heading was 0 but this did not work properly. Now when the inital turn is greater than 180 degrees it will reverse it and find the opposite angle. 
- Derek continued practicing driving and is very close to being able to get 313 in one minute. His current best run is 1 minute 3 seconds. 
#### Why:
- Jack fixed the calcDir function by inputting the turnError into the arctan function which will return the opposite angle if the turnError is greater than 180.
- Derek's practice of the new route is going well and he is on pace to achieve 313 in under a minute. 

```c++
void Chassis::calcDir(){
    turnComplete ? turnError = target.thetaTwo - *theta : turnError = target.theta - *theta;
    
    turnError = macro::toRad(turnError);
    turnError = atan2( sin( turnError ), cos( turnError ) );
    turnError = macro::toDeg(turnError);
    
    turn_output = turn_PID.calculate(turnError);
}
```
### Plans for next Practice:
- Continue Auton Skills.
- Continue Driver Practice.



