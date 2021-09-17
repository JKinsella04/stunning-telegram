# 9/14/21 - 9/16/21
## 9/14/21
### Attendance: &#9745; Brody, &#9745; Derek, &#9745; Jack
### Goals:
- Continue building the lifts.
- Code all class member functions.
### Accomplished:
- &#9745; Continue building the lifts.
- &#9745; Code all class member functions.
#### How:
- Derek has to quarantine for two weeks, but has the robot and parts to continue building. Today Derek worked on the lift since the HS axles arrived. The HS axle connection spot and one of the two lift motors have been built. Derek also tweaked the clamp that will connect to the lift tuning its rotation point to make it stronger and smoother.

<script src="https://cdn.jsdelivr.net/npm/publicalbum@latest/embed-ui.min.js" async></script>
<div class="pa-gallery-player-widget" style="width:100%; height:480px; display:none;"
  data-link="https://photos.app.goo.gl/rqtToydVLAXtxUAf8"
  data-title="9/14/21"
  data-description="3 new photos added to shared album">
  <object data="https://lh3.googleusercontent.com/RU9oEuv82qDGVwg2aGOPEPHHiGbEtIGZCl2wSFr4hbSmDkME6OO2juu9vyX50Zg_het-r81QJP3sqOTynFqSuPpOxPLBNh-cyT6pPQJjJWVDeS50vZiSzfmkIBFnl9uE5CzoTbUJng=w1920-h1080"></object>
  <object data="https://lh3.googleusercontent.com/x4O16U5d-dB0VpslUVOwztREwBrZi6KL_jY_0MQNTSW0ntpmYZOiuqG3eaT2xu04nQGtZd2XIka6-H9r3bGAI4rsa4UH1S7qyoB4JH_AbQebVt9uYnZqXNfxN5qEddllBCGqFOa5KA=w1920-h1080"></object>
  <object data="https://lh3.googleusercontent.com/rT2cgtxMu0D1G_8fhAwlB-D4DseYTtaRhhWozuh86BLFDTlzLBd-3Z9nyokO-K5MlX9Qr15e7AnKJh-TudWOrzBQui-Cfbe39HmEn9Mh-PMU32mtrRV8bzxibBWSsmqbnfqbbBNXag=w1920-h1080"></object>
</div>

- Instead of showing all the classes here we will explain the layout and formatting of the code since all classes follow the same format. [Github Repo.](https://github.com/PSASchool/9447H-TippingPoint)
- Classes that need special data inputted such as the chassis have overloaded constructors to store values such as x, y, angle, and wheel travel distance. To use PID throughout our code we create an object in our custom PID class where we give it all the values needed and then can run a calculate member function to return the PID output. We do the same for our Slew class as well. Currently we have 3 PID objects being, drive_PID, turn_PID, and lift_PID. We also have 4 Slew objects being leftSlew, rightSlew, turnSlew and, liftSlew.

```c++
Slew(double accel_, double decel_, bool reversible);
PID(double kP_ = 0, double kI_ = 0, double kD_ = 0);
```
- Below is how we set the values for turning and then how those are taken and used by PID and Slew objects to make the chassis turn. This is a part of the chassis state machine. 
```c++
Chassis &Chassis::withTurnGains(double kP_, double kI_, double kD_) {
    turn_PID.set(kP_, kI_, kD_);
    return *this;
}

Chassis &Chassis::turn(double theta, double rate, double speed) {
    target.theta = theta;
    target.rateTurn = rate;
    target.speedTurn = speed;
    reset();
    isSettled = false;
    mode = ChassisState::TURN;
    return *this;
```

```c++
case ChassisState::TURN:{
    // Turn PID Calc
    turn_output = turn_PID.calculate(target.theta, *theta);
     
     // Find quickest turn.
     calcDir();
     
     // Slew Calc
     TslewOutput = turnSlew.withGains(target.rateTurn, target.rateTurn, true).withLimit(target.speedTurn).calculate(turn_output);
     
     left(TslewOutput);
     right(TslewOutput);
     
     if(fabs(turn_PID.getError()) < tol){
         left(0);
         right(0);
         withTurnGains(0).withTol(0);
         reset();
         isSettled = true;
         mode = ChassisState::IDLE;
         goto end;
     }
break;
}
```
#### Why:
- Derek tuned the clamp because the most important aspect of the robot is its quality and consistency. With the improved clamp we are confident that we will not run into problems with the pneumatic piston getting stuck or moving in an unwanted way since it is now very secure and is not twisted or slanted in any direction.
- The GUI, Lift and, Chassis classes all follow the same format, there is a start function which is called when we create the threads that run the class. The start member function sets the boolean isRunning to true and calls the run member function which is then where the while loop that controls the chassis state, GUI buttons, or Lift state. 
### Plans for next Practice:
- Continue building the lifts.

```{important}
Last Edited on 9/14/21.
```

## 9/15/21
### Attendance: &#9744; Brody, &#9745; Derek, &#9744; Jack
### Goals: 
- Continue building the lifts
### Accomplished:
- &#9745; Continue building the lifts
#### How:
- Derek continued building the lifts today and connected the clamp to the 4 bar. The plan is to use 2 motors on the lift and have the pneumatic clamp hold the goal but the robot is already able to lift and hold the goal with only one motor and the clamp holds the goal even without air pressure. This is good because it shows that even if the pneumatics or a motor give out we will still be able to perform well.

<script src="https://cdn.jsdelivr.net/npm/publicalbum@latest/embed-ui.min.js" async></script>
<div class="pa-gallery-player-widget" style="width:100%; height:480px; display:none;"
  data-link="https://photos.app.goo.gl/HEbaLC9DSVskm9Fy7"
  data-title="9/15/21"
  data-description="2 new photos added to shared album">
  <object data="https://lh3.googleusercontent.com/d99ufZLhoVul3G5dD7xr1YXjykLmXjRDEdn3vMIo9jHVAOlt5oX675TG8GPmWQ2NOTu_VlRP3kSmhkIsQ1VlQAfcpB6apx3Ib1udqo3buK0dCLlWmROa32wxiy_cj-lSkUVbealAiA=w1920-h1080"></object>
  <object data="https://lh3.googleusercontent.com/aRFGdpOQC8Kgk43JwiBphuIRZb6rEEP6gYkAQnYCfhbmDosVXJJjaqZj2h0ATy_crezVSHb9_OJoIH7D6ebusbRhryo-PK3lQZ0j4FydvCrpXVb9zo6HvKWYoPBhVV-pNIDxYDC7iQ=w1920-h1080"></object>
</div>


#### Why:
- Derek focused only on connecting the clamp to the lift today because it is very important that the spacing is correct because of how close the clamp will be to the drive base when lowered. Derek has taken today to ensure that the spacing is perfect and that the clamp is on the lift as securely as possible.
### Plans for next Practice:
- Finish the lifts.

```{important}
Last Edited on 9/15/21.
```

## 9/16/21
### Attendance:  &#9745; Brody, &#9745; Derek, &#9745; Jack
### Goals:
- Finish the lifts.
### Accomplished:
- &#9745; Finish the lifts.
#### How:
- Derek finished building the lift today by adding the finishing touches to it. The completed lift is a 4 bar that uses 2 200rpm motors with a 1:7 gear ratio geared for torque. Since we use 2 200rpm motors our lift is very fast so to compensate for this we will be using PID to safely move the lift between its maximum height and its start position so we do not cause strain on the motors by going past the lift's physical limits. 
- We are using the new V5 potentiometer to get and accurate value of the lift's movement.
- Derek also has fully planned out the pneumatic layout. We will be using two resevoirs each with 100psi that supply air to two single acting solenoids and one double acting solenoid.

<iframe width="560" height="315" src="https://www.youtube.com/embed/nZzrLr_bpgY" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

#### Why:
- We decided to use three solenoids instead of just two because we want to be able to control each dragger indepent of the other in case we only need to use one during the autonomous routine.
- To make sure the robot does not break itself we are using PID in our most important mechanisms, such as the lift and the chassis. Below is the PID calculation that runs when we call ```PID.calculate();```
```c++
double calculate(double target, double current){
// Proportional Calculation
if ( error == 0) {
    error = target - current;
}

// Integral Calculation
integral += error;
if (error == 0){
    integral = 0;
}if (integral > 12000){
    integral = 12000;
}

// Derivative Calculation
derivative = error - prevError;
prevError = error;

// Ouput Calculation
output = error * kP + integral * kI + derivative * kD;
error = 0
return output;
}
```
### Plans for next Practice:
- Begin building the second mobile Goal lift.

```{important}
Last Edited on 9/16/21.
```