# 9/21/21 - 9/23/21
## 9/21/21
### Attendance: &#9745; Brody, &#9745; Derek, &#9745; Jack
### Goals:
- Finish the small lift.
- Ensure code works.
### Accomplished:
- &#9745; Finish the small lift.
- &#9745; Ensure code works.
#### How:
- Today Derek and Brody finished building the small lift. Since the small lift is very simple and compact we left it to be the last mechanism to build since it is only 7 c-channels total. The mechanism has two small c-channels that wrap around the bottom of a mobile goal and then lifts up allowing us to grab and move a mobile goal around.
- Once the small lift was built we tested the code for both lifts. For the most accurate control of the lifts we are using PID and slew code in tandem to accelerate and deccelerate from point to point. 

<iframe width="560" height="315" src="https://www.youtube.com/embed/tvxJO8-eGb0" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

<script src="https://cdn.jsdelivr.net/npm/publicalbum@latest/embed-ui.min.js" async></script>
<div class="pa-gallery-player-widget" style="width:560px; height:315px; display:none;"
  data-link="https://photos.app.goo.gl/Gu7LYcHmsdCzmFz66"
  data-title="9-21-21"
  data-description="6 new photos added to shared album"
  data-delay="2">
  <object data="https://lh3.googleusercontent.com/a5IGXNj0KmmlxhyDLaVbbFlN2p9j08kMRVhihzhdbFrKHN0sDYy-OcBBjgXRp9AvzZMesWbMe_QfVfT0EKki225JayWpgl4uI-fs4VbH7E1hmsyaorPMM48LOl6lAdOR7RHdi7qtQA=w640-h480"></object>
  <object data="https://lh3.googleusercontent.com/h49FzeqRcxL3-ttjqxOF-9JTpEx6ze6BFxseZNFG1nXt4VpQufzaWEAwG06e38FZV6XvRdf-rS068b_OpMpaJb9VcgIHwGJ4XThpka10xVwEd0UllYYKnj3HqLCUBKMGz1NYcpc9vQ=w640-h480"></object>
  <object data="https://lh3.googleusercontent.com/40F9Y0b_Jy0OUDCeWkjCmiJIJrzrzxwFDuptokWx0mdVe7n192AbmxhYa-yKV_noGb50sVJAJgyf7Y1I9AqHIuRA81lslo85u6r7BwWTYU2DNlGSLpDkHSLKurt45I5K6Goa3rUGkg=w640-h480"></object>
  <object data="https://lh3.googleusercontent.com/9XeFQntGYhauIarhR5UF85mxRe6Dvwyb7ko5GbSGMbcoyvIVoPrHXjAoPVeiHgrwEKXe5ZFpNDiKnM0tQKYO7VaurcIf9DkWBx3uO5Uh79MwgRAFIph2V_ED4pzyhgPZqGS4cNpkTw=w640-h480"></object>
  <object data="https://lh3.googleusercontent.com/cwQ-tKl0R5AO1gXFI_Mu_elyNFATgLDQgnukxXy3aTkYaUoSQjx5uG9EipZ3CfORqqB14EepgE2isgZzs007HjEDJMj87A6dYACNv5w44v5SHL-S9K8u3xU6Mf9Ih8PWs1h_LOqRZA=w640-h480"></object>
  <object data="https://lh3.googleusercontent.com/L8-MtncY1KVvImZXDuStkMGL8BjqrH4HdxFCY69T3VWWhDOcZqRcjncNF1ALGj7og_zM-HnevYx8K3zjOmqcGszwWcMsK_rTWubmiCry-Bdk4R2bmRQYUwGCdAOT09n5Td3aICpFiA=w640-h480"></object>
</div>


#### Why:
- The point of the small lift is to allow us to control more goals at once and also to be able to carry a goal while driving up the ramp in case we need to do so. Even though it can not reach heights like the 4 bar lift it is still very useful as we will be able to grab a goal and hold onto it for the entire match.
- We use PID and Slew to control the two lifts because they both have physical points that they can not go past or the robot will break. The PID and Slew help with this because they allow us to still move both mechanisms quickly while also still having the precise control we need to make sure we do not damage the robot at all.
- To accurately evaluate the small lift we are using the V2 potentiometer since the small lift does not make a full rotation. Since the 4 bar lift rotates more than 2 full rotations we are unable to use a potentiometer and until we order a new rotation sensor we will be using an average of the two motors position that move the 4 bar.
> Below is the code for both lifts. The logic is the exact same except the small lift takes the potentiometer value while the 4 bar takes the average of motor positions and the phrase MobileGoal is replaced with Lift (Lift_PID, Lift_Slew, etc).

```c++
void MobileGoal::move(double target){
  // Update current position.
  current = mobileGoalPos.get_value();
  // Lift position 
  // current = ( leftArm.get_position + rightArm.position )/2;
  
  // PID calculation.
  output = MobileGoal_PID.calculate(target, current);
  
  // Slew calculation.
  slewOutput = MobileGoal_Slew.calculate(output);
  
  // Send slew output to motors.
  leftMobileGoal.move_voltage(-slewOutput);
  rightMobileGoal.move_voltage(-slewOutput);
  
  // If within tolerance stop movement.
  if(fabs(MobileGoal_PID.getError()) < tol){
    if (!pros::competition::is_autonomous()) {
        mobileGoalMode = MobileGoalState::OPCONTROL;
    } else{
        mobileGoalMode = MobileGoalState::IDLE;
    }
    isSettled = true;
  }
}
```
### Plans for next Practice:
- Test the robot.
- Begin strategizing the 15 second auton routine.

```{important}
Last Edited on 9/21/21.
```

## 9/22/21
### Attendance: &#9745; Brody, &#9744; Derek, &#9745; Jack
### Goals:
- Test the robot.
- Begin strategizing the 15 second auton routine.
### Accomplished:
- &#9745; Test the robot.
- &#9745; Begin strategizing the 15 second auton routine.
#### How:
- Today we tested the robot by driving around the field and scoring goals by carrying them into the home zones and placing them onto the platforms. In our tests we have learned of a couple needed changes in the code and extra parts to strengthen the robot.
- Brody and Jack began planning how we will accomplish the autonomous win point since doing that will be very important to do well in competitions.
#### Why:
- We needed to redo the code for the small lift because the current code did not account for the starting position. The new code now does by having a setup function that moves the small lift into the potentiometer range so the robot can accurately move the small lift after setup. We decided to do this instead of abandoninig the potentiometer because we need to have exact value readings to make sure we do not move the lift into the drive base and if we only use the motor encoders their error build-up could be problematic. 
- For our first competition we want to be able to do the entire auton win point challenge by ourselves. This will allow us to not worry about our qualification partner's autonomous routines and just run our own consistent autonomous. Ensuring the AWP will allow us to place high in the qualification rankings which is very important.
```c++
// Moves small lift into the potentiometer range. Run before opcontrol/auton.
void mobileGoal::setup(){
    leftMobileGoal.move_absolute(-800, 127);
    rightMobileGoal.move_absolute(-800, 127);
}
```

### Plans for next Practice:
- Add support structure to 4 bar.
- Begin strategizing about the skills routines. 

```{important}
Last Edited on 9/22/21.
```

## 9/23/21
### Attendance: &#9745; Brody, &#9744; Derek, &#9745; Jack
### Goals:
- Add support structure to 4 bar.
- Begin strategizing about the skills routines.

### Accomplished:
- &#9745; Add support structure to 4 bar.
- &#9745; Begin strategizing about the skills routines.

#### How:
- Today Derek added a cross bar onto the 4 bar to secure it so both sides of the 4 bar move in unison.
- Brody and Jack began desiging skills strategies by determining what scoring objectives we need to focus to maxmimmize our score. Since our robot is built to manipulate the mobile goals, we want to elevate all seven goals onto the two platforms in both driver and autonomous. Scoring seven elevated goals would be a skills score of 280 and as of 9/23/21 the highest drive skills score is 260. 
- Jack continued working on Pure pursuit by developing the point to point drive state.
```c++
case ChassisState::POINT: {
      distToTarget = hypot(target.x - *posX, target.y - *posY);

      absAngleToTarget = atan2(target.y - *posY, target.x - *posX);

      double thetaRad = macro::toRad(*theta);

      relAngleToTarget = macro::angleWrap(absAngleToTarget - (thetaRad - macro::toRad(90)));

      double relAngleDeg = macro::toDeg(relAngleToTarget);

      relXToPoint = sin(relAngleToTarget) * distToTarget;
      relYToPoint = cos(relAngleToTarget) * distToTarget;

      double xPower = relXToPoint / (fabs(relXToPoint) + fabs(relYToPoint));
      double yPower = relYToPoint / (fabs(relXToPoint) + fabs(relYToPoint));

      // Drive PID calc
      drive_PID.setError(relXToPoint);
      drive_output = drive_PID.calculate();
  
      // Turn PID calc.
      turn_PID.setError(relYToPoint);
      turn_output = turn_PID.calculate();

      // Find quickest turn.
      // calcDir();
      
      // Slew Calcs.
      TslewOutput = turnSlew.withGains(target.rateTurn, target.rateTurn, true).withLimit(target.speedTurn).calculate(turn_output);
      LslewOutput = leftSlew.withGains(target.rateDrive, target.rateDrive, true).withLimit(target.speedDrive).calculate(drive_output);
      RslewOutput = rightSlew.withGains(target.rateDrive, target.rateDrive, true).withLimit(target.speedDrive).calculate(drive_output);

      // std::cout << "Angle:" << drive_PID.getError() << std::endl; //<< "AngleDeg:" << turn_output << std::endl;
      std::cout << "relX: " << relXToPoint << " relY: " << relYToPoint << std::endl;
      // std::cout << "xPower: " << xPower << " yPower: " << yPower << std::endl; 
      // std::cout << "Drive: " << drive_output << " Turn: " << turn_output << std::endl;

      left(LslewOutput + TslewOutput );
      right(RslewOutput - TslewOutput);

      // double relTurnAngle = relAngleToTarget - macro::toRad(180) + target.theta;
      // double turnPower = macro::clip(relTurnAngle/macro::toRad(30), -1, 1); 

      // std::cout << "turn: " << turnPower << " rel:" << relTurnAngle << std::endl;

      if(fabs(drive_PID.getError()) <= tol && fabs(turn_PID.getError()) <= 0.75){
        left(0);
        right(0);
        withGains().withTurnGains().withTol();
        reset();
        isSettled = true;
        mode = ChassisState::IDLE;
        goto end;
      }

      break;
    }
```
    
#### Why:
- We needed the extra support on the 4 bar because the left side of the 4 bar would lag behind the right side which caused the robot to not be able to reach it's maximum height.
- We are not worrying about parking during the skills routines because we do not expect to have enough time to score seven goals and park at the same time so we are just planning on elevating the mobile goals. 
- Jack is developing point to point motion control because it will be very useful for moving in the autonomous phase. We will be able to use either odom/dead reckoning or the GPS sensor values as input  for this movement since all three options will return (x,y) coordinates. 
### Plans for next Practice:
- Fix the draggers.
- Build the ring preload mechanism.

```{important}
Last Edited on 9/23/21.
```
