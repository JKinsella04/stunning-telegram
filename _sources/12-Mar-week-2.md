# 3/8/22 - 3/10/22
## 3/8/22 
### Attendance: &#9745;  Brody, &#9745; Derek, &#9745; Jack
### Goals:
- Fix back clamp.
- Switch to okapi Units

### Accomplished:
- &#9745; Fix back clamp.
- &#9745; Switch to okapi Units

#### How:
- Today Derek worked on fixing the back clamp because during states, there were many instances where when grabbing the second alliance goal we were unable to hold it properly and score rings effectively. Derek has fixed this issue by manipulating the connection points and the angle at which the pneumatics push the clamp to more efficiently tilt the goal. 

- Jack switched the code to use the okapi units today meaning that instead of inputting encoder values we now can input distances in either the imperial or metric system. We also now can input our acceleration in terms of units/sec^2 and for turns we now work with rad/sec^2 and rad/sec. While this does not exactly increase our accuracy it will majorly improve our readability and ease of use since our auton program lines have become more descriptive than before.

```{code}
BEFORE:
chassis.turn(90, 900, 12000).withTurnTol(5).waitUnitlSettled();
NEW:
chassis.turn(90_deg, 2.2_radps2, 27.6_radps).withTurnTol(1_deg).waitUntilSettled);
```
#### Why:
- Derek spent the day tuning the back clamp because it is very important that we grab the alliance goals properly since scoring rings on the pole will be crucial to winnign matches at CREATE.

- Jack has switched to using the okapi units because in addition to increasing readability it also will uses dimensional analysis at compile time to check the units values. This helps the code run quickly and efficiently.  

### Plans for next Practice:
- Redesign ring hood.


## 3/9/22 
### Attendance: &#9745;  Brody, &#9745; Derek, &#9745; Jack
### Goals:
- Redesign ring hood.

### Accomplished:
- &#9745; Redesign ring hood.

#### How:
- Today Derek completely redesigned the ring hood by using a piece of polycarbonate bent in a semi-circle to guide the rings. The new design also uses standoffs above the polycarbonate to stop any rings from launching upward.

```{figure} ././_images/march/newHood.jpg
---
width: 500px
name: newHood.png
---
A side view of the new ring hood.
```

#### Why:
- We changed the hood to a single piece of polycarbonate because this design is much more efficient at controlling the rings' movement since the semi-circle is just slightly larger than the rings themselves so there is no extra space for them to go off course. The design currently is not scoring 100% of the rings but is slightly better than the previous design meaning with a couple slight changes over tomorrow and these 2 weeks we should be able to create a very consistent ring hood.
### Plans for next Practice:
- Retune autons to use okapi units.
- Test and tune ring hood.

## 3/9/22 
### Attendance: &#9745;   Brody, &#9745; Derek, &#9745; Jack
### Goals:
- Retune autons to use okapi units.
- Test and tune ring hood.
- CAD Worlds robot.

### Accomplished:
- &#9745; Retune Left + Right 1/2 AWP autons.
- &#9745; Fix air leaks.
- &#9745; Continue driver practice.

#### How:
- Today Jack tuned the the two 1/2 AWP autons today to use the okapi units. The movements have a tolerance range of 0.5 inches - 2 inches and the turns have a tolerance of 1 degree. Jack tuned these two autonomous programs first since they are the simplest as well as the most important autonomous programs since we will most likely only run these at CREATE since most robots will be able to score half of the AWP bonus.

```{code}
void leftAWP() { // One yellow + left AWP
  frontLift.toggleClamp();
  chassis.setBrakeType(COAST);
  backLift.setState(BackLiftState::AUTON);
  frontLift.withTol(10).setState(FrontLiftState::DOWN);
  chassis.drive(42_in, 2.5_ftps2).withAngle(355_deg, 28_radps2).withGains(3.5, 0, .5).withTurnGains(30).withTol(2_in).withTurnTol(10_deg).waitUntilSettled();
  frontLift.toggleClamp().setState(FrontLiftState::UP, 50).waitUntilClamped();
  chassis.drive(-52_in).withAngle(15_deg).withTol(3_in).withTurnTol(5_deg).withTurnGains(30).waitUntilSettled();
  chassis.turn(95_deg, 1.1_radps2, 14_radps).waitUntilSettled();
  chassis.drive(-30_in, .2_ftps2, .2_ftps2, -2.75_ftps).withAngle(90_deg).withTol(1_in, true).waitUntilSettled();
  backLift.toggleClamp();
  chassis.drive(27_in, 0.05_ftps2, 0.05_ftps2, 1.5_ftps).withGains(3).withAngle(105_deg).withTol(2_in).waitUntilSettled();
  chassis.drive(-20_in, 0.05_ftps2, 0.05_ftps2, -1.5_ftps).withGains(3).withAngle(105_deg).withTol(2_in).waitUntilSettled();
  chassis.drive(19_in, 0.05_ftps2, 0.05_ftps2, 1.5_ftps).withGains(3).withAngle(105_deg).withTol(2_in).waitUntilSettled();
  chassis.drive(-20_in, 0.05_ftps2, 0.05_ftps2, -1.5_ftps).withGains(3).withAngle(105_deg).withTol(2_in).waitUntilSettled();
  chassis.drive(19_in, 0.05_ftps2, 0.05_ftps2, 1.5_ftps).withGains(3).withAngle(105_deg).withTol(2_in).waitUntilSettled();
  chassis.drive(-20_in, 0.05_ftps2, 0.05_ftps2, -1.5_ftps).withGains(3).withAngle(105_deg).withTol(2_in).waitUntilSettled();
}
```

- Derek continued practicing driving by running through the skills route repeatedly. Derek also found a broken tubing connection on our solenoid which caused us to lose air quickly. Derek remedied this by replacing the faulty one and checked all the other connections to ensure no other parts were damaged.

- Derek began working on the design of our worlds robot. We want to build a new robot for worlds that will be faster and lighter while not losing any functionality. To do this we have to cut down and minimize the amount of metal we use.

<script src="https://cdn.jsdelivr.net/npm/publicalbum@latest/embed-ui.min.js" async></script>
<div class="pa-gallery-player-widget" style="width:100%; height:480px; display:none;"
  data-link="https://photos.app.goo.gl/84dJ7ne9evvwg1kt6"
  data-title="3/10/22"
  data-description="4 new items added to shared album"
  data-delay="2">
  <object data="https://lh3.googleusercontent.com/7aggNwhQPQb8Ayk6R49aFX2qM2rHu1kgHIKqPTTJr2iOs05LyMexYc9JKNS8vrIyGTLsMJBcd7xU2h0_Nw51sMgk21B3YbTTDdJ6zxMMS3a20STmEFm5WdBph4YaOCEYo1MvEuJJBw=w1920-h1080"></object>
  <object data="https://lh3.googleusercontent.com/plo-G665i7Kk2_V5gZ3ffH-BM3k0uGK4geyDeWfTYVzmN0yVUDN5cWbv0_WWWGxIsK72ZZyHMBdOyIt5nazRJiYWD_Wu7COIJmchMN798xcUt1gz3qT5nS2icPO6CU8WEkVaCZEJ5w=w1920-h1080"></object>
  <object data="https://lh3.googleusercontent.com/u0ggK59Xy7Hb-zkNugX4ZqBQtOec7RTR_NzOVO-N3LYVfk_oYlhKM3q0t1vBe4SivoWl846Vg1y_44pzxKG52xNRDF64p5Tq89qfhu-8ewILAxbfG-Nj_il5-GYngxloPSZ87-sDGA=w1920-h1080"></object>
  <object data="https://lh3.googleusercontent.com/VOqdiQ7yK8jb2wg7zFfiZXx7m22MOH9TA4BYefTYeTwTCtHTodWVNXmUBIdlPhlCF59h6QPA6kPTrXgqCUxqwAiS0O9sAOnK0dmzKdSdsk7eVSCOR0Q8aXqJCr5ZZ7AraU_zIr23uw=w1920-h1080"></object>
</div>

#### Why:
- Since most robots will likely be able to hold two goals and score rings on alliance goals at CREATE, we are expecting to be running our 1/2 AWP autons that grab a neutral goal first since ownership of the neutral goals will be highly contested. After changed the units our two autons work efficiently and are more accurate than before.

- Derek is continuing driver practice since he wants to be able to score over 330 points in driver skills at CREATE. We believe that if Derek continues practicing the driver route that he will be able to score over 330 at CREATE.

- Derek noticed that the robot was losing too much air after each run and after fixing the broken piece had stabilized our air loss. Since the pneumatics serve such an important role on our robot is is very important that they are optimized to use the least amount of air.

- Derek has begun working on the new design since we will only have a month after CREATE to build this new robot. We are doing this now so we will have enough time to build and test and practice before the world championship. Derek is planning on having the design finished by next wednesday. So we will be ready to build after returning from Iowa.

### Plans for next Practice:
- Convert middle goal auton + Full AWP auton to okapi units.
- Continue driver practice.
- Finish CAD.