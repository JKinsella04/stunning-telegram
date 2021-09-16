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
#### Why:
- Derek focused only on connecting the clamp to the lift today because it is very important that the spacing is correct because of how close the clamp will be to the drive base when lowered. Derek has taken today to ensure that the spacing is perfect and that the clamp is on the lift as securely as possible.
### Plans for next Practice:
- Finish the lifts.

```{important}
Last Edited on 9/15/21.
```