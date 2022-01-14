# 1/11/22-1/13/22
## 1/11/22 
### Attendance: &#9744; Brody, &#9745; Derek, &#9745; Jack
### Goals:
- Lengthen the ring hood.

### Accomplished:
- &#9745; Reroute AWP routine.

#### How:
- Jack rerouted the AWP routine and now it consistently scores rings in both goals and moves the alliance goal across the line to get us the Auton Win Point bonus. Tomorrow Jack will work on grabbing two yellow goals after scoring the Auton Win Point bonus. After scoring the preload rings, scoring 5 more rings and grabbing two yellow goals this auton will score a total of 64 points. Which is an increase from our old AWP routine which scored 23 points.

<iframe width="560" height="315" src="https://www.youtube.com/embed/T4OxbI9OJ6Q" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

#### Why:
- Jack changed the AWP routine pathing because we deemed it more important to ensure that we score the Auton Win Point bonus before going for yellow goals since the extra win point is more important than securing one or two yellow goals in qualifier matches. 
- Since qualifier matches are 4 random teams it is safe to say that worst case scenario we will be able to fight for the yellow goals if our auton does not get them.
- We put extending the ring hood on hold for tomorrow because Jack wanted to restart the AWP routine since we were scraping the progress we made last week. 

### Plans for next Practice:
- Lengthen the ring hood.
- Fix air leak.

```{important}
Last Edited on 1/11/22.
```

## 1/12/22 
### Attendance: &#9745; Brody, &#9745; Derek, &#9745; Jack
### Goals:
- Lengthen the ring hood.
- Fix air leak.
### Accomplished:
- &#9745; Lengthen the ring hood.
- &#9745; Fix air leak.

#### How:
- Today Derek fixed the air leak by replacing the air tubes that connect the backlift pistons to the resevoirs. These tubes when originally cut were slanted and not straight so their connection to the resevoirs and pistons were not secure which causes significant air loss.
- Derek also added a new piece of polycarbonate to the ring hood which helped with the problems of the intake where the rings would not contact the hood and fly by. Even though this hood is not 100% accurate it is much better than before and is competition ready. 

<iframe width="560" height="315" src="https://www.youtube.com/embed/h3Vae3nkBfo" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

#### Why:
- It is acceptable for a not 100% success rate on scoring rings because our ring intake is very fast which makes up for the inaccuracy. We will most likely be the only ring intake robot at this next tournament so the consistency it is at currently will be adequate.
- We took today to fix the ring hood and the air leak because these were the final two problems with our robot that were preventing it from being competition ready. Starting tomorrow our robot will be fully competition ready and we can just focus on our autonomous programs as well as driver practice.

### Plans for next Practice:
- Finish AWP routine.
- Begin driver practice.

```{important}
Last Edited on 1/12/22.
```

## 1/13/22 
### Attendance: &#9745; Brody, &#9745; Derek, &#9745; Jack
### Goals:
- Finish AWP routine.
- Begin driver practice.

### Accomplished:
- &#9745; Begin driver practice.

#### How:
- Derek started practicing driving today. He is not focusing on skills runs yet, as he needs to get used to driving the new robot before running the routine. Since our new robot can score rings our goal for driver skills will be 337 points. These new points are from scoring 9 rings on a goal. Due to time we will stick with the same original route that Derek drove with the old robot but now he can drive through rings since we can now score them on goals.
- Jack continued trying to optimize the AWP routine but was unable to finish it today. He will have to continue next week. The autonomous is nearly complete but needs just a little more finetuning. Below is the current AWP routine.

```c++
void awp(){
  backLift.setState(BackLiftState::UP);
  pros::delay(300);
  // Score Preload rings
  backLift.setState(BackLiftState::DOWN);
  chassis.drive(1050,75,450).withGains(15, 0, 6.25).withAngle(90).withTurnGains(133, 0, 66).withTol(50, 5).waitUntilSettled();
  chassis.turn(0).withTurnGains(133,0,66).withTol(0,5).waitUntilSettled();
  chassis.drive(-5000, 900, 450, 12000).withGains(15, 0, 6.25).withAngle(358).withTurnGains(266, 1, 133).withTol(50, 10).waitUntilSettled();
  backLift.setState(BackLiftState::UP);
  frontLift.setState(FrontLiftState::UP);
  chassis.drive(400).withGains(15, 0, 6.25).withTol(50).waitUntilSettled();  
  chassis.turn(85).withTurnGains(133,0,33).withTol(0,5).waitUntilSettled();
  chassis.drive(1500).withGains(15, 0, 6.25).withTol(50).waitUntilSettled();
  frontLift.setState(FrontLiftState::DOWN);
  chassis.drive(-1000).withGains(15, 0, 6.25).withTol(50).waitUntilSettled();
  backLift.setState(BackLiftState::DOWN);
  // Grab second alliance goal and score rings. AWP COMPLETE
  chassis.turn(75).withTurnGains(266, 0, 66).withTol(0, 5).waitUntilSettled();
  chassis.drive(1750).withGains(15, 0, 6.25).withTol(50).waitUntilSettled();
  frontLift.setClamp(true).setState(FrontLiftState::MIDDLE).waitUntilSettled();
  // Grab first yellow goal
 }
 ```
#### Why:
- Derek will only score rings on the goal that starts on the AWP line and as he drives over to the platform to park he will be able to drive through rings to fill the goal.
- We are keeping the same driver routine because Derek really likes this routine and even though it is a new robot he should be able to easily complete the routine in under a minute just like before.

### Plans for next Practice:
- Finish AWP routine.
- Continue driver practice.
- Begin Elim auton.
- Begin Skills auton

```{important}
Last Edited on 1/13/22.
```
