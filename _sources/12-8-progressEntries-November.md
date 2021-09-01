---
jupytext:
  cell_metadata_filter: -all
  formats: md:myst
  text_representation: {extension: .md, format_name: myst, format_version: 0.12, jupytext_version: 1.6.0}
kernelspec: {display_name: Python 3, language: python, name: python3}
---

# November 2020 Progress Entries
## 11/3/20
### Attendance: &#9745; Brody, &#9745; Derek, &#9745; Dylan, &#9745; Ian, &#9745; Jack
### Goals for today
- Begin practicing! 

### What we did today
- Noticed a problem with scoring balls into goal, a lot of speed loss, indexer meets polycarbonate hood. wanted to combat this by pulling back the hood. Rebanded robot. 
- Our first real tournament is coming up really soon. It is on the 21st and is a saturday. Unfortunately only three members are allowed to go so we had to decide who 3 were going. Due to Dylan and Ian already having plans for that weekend, we didn’t have too much of a problem deciding since only Brody, Derek and Jack are able to go anyways.

### Auto Sort Function
Last thursday (10/29/20) PROS pushed a new kernel update that supported the optical and distance sensors so we were able to port over our code we created in VEXcode to our actual program. When we ported it over, we also increased the speed at which the intakes and rollers run so it is much faster now. We also created a new function for sorting when we are interacting with the goals. The code is a simplified version of the normal auto sorting but with a few differences. The main one is that it no longer checks to see if it found the right color, it only checks for the enemy color. Upon finding the enemy color it will reverse the top indexer to send the enemy ball out the back of the robot. Another change to it is that instead of stopping the ball at the top line sensor, it spins is all rollers to score the balls in the goals. The way this works is that it will be scoring all the balls and upon finding the enemy color it will eject that out the back of the robot and then immediately continue scoring.

### Goals for next week’s Practice
- Make sure the robot is in size requirements with the hood deployment.
- Fine tune auto sorting
- Begin Practicing!

```cpp
void Intake::goalSort(int allianceColor){ //The sorting code when we are cycling balls at a Goal.
  switch (allianceColor){
    case REDBALL:{
      LOptical.set_led_pwm(ledLevel);
      ROptical.set_led_pwm(ledLevel);
      intakeSpin(200);
      indexerSpin(600);
      middleSpin(600);
      double currentHue = (LOptical.get_hue() + ROptical.get_hue())/2;
      printf("currentHue %F\n", currentHue); //debug code
      if(currentHue >= blueHue){indexerSpin(-600);pros::delay(250);} //If there is a blue ball it will send it out back.
      break;
    }
    case BLUEBALL:{
      LOptical.set_led_pwm(ledLevel);
      ROptical.set_led_pwm(ledLevel);
      intakeSpin(200);
      indexerSpin(600);
      middleSpin(600);
      double currentHue = (LOptical.get_hue() + ROptical.get_hue())/2;
      printf("currentHue %F\n", currentHue); //debug code
      if(currentHue <= redHue){indexerSpin(-600);pros::delay(250);} //If there is a red ball it will send it out back.
      break;
    }
  }
}
```

## 11/10/20
### Attendance: &#9745; Brody, &#9745; Derek, &#9744; Dylan, &#9745; Ian, &#9745; Jack
### Goals for today
- Begin practicing! 

### What we did today
- Practice!
- Minor tweaks to slew and autosort code.

### Auto Sort Fine tuning
With the auto sorting, we had a problem with the ball going past the top line sensor. We had been trying to fix it by lowering the speed of the top indexer but this just made the problem worse. The actual problem wasn’t the timeframe to sense the ball but actually the speed difference between the top and middle rollers. Since the middle ones were faster than the top, it would cause a weird anomaly where the ball would idle for a little bit and move backwards and then when it would go up to the line sensor it would not be able to sense the ball. To fix this all we had to do was make both the middle and top rollers spin the same rpm. 
We also had an issue with the enemy ball cycling all the way through in both the auto sorting and the goal sorting. To fix this we added a second optical sensor and lowered both of them to be right behind the back of the intakes. This now allows the balls to be read very early and more accurately since both sensors are very close to the balls when they enter. Even if a ball comes in a little astray to one side the second optical sensor will be able to still read the ball.

### Practice Runs
We spent the whole day practicing Driver Skills. Throughout the practice Derek was making constant improvements. This was a very successful day today since Derek got to begin practicing and with even more practice theres no doubt that we can get a max score of 126 points.
|Run #| Points Scored|Run #| Points Scored|
|-----|--------------|-----|--------------| 
|1. |53 points|7. |83 points|
|2. |77 points|8. |74 points|
|3. |82 points|9. |81 points|
|4. |59 points|10. |106 points|
|5. |93 points|11. |109 points|
|6. |81 points|12. |107 points|

<img src="././_images/11-November/11-10-20/driver_runs_graph.PNG" alt="driver_runs_graph.png" style="width: 500px;"/>

### Goals for next week’s Practice
- Begin programming the autonomous routines. Focus on the 15 sec Home Row auton first then the 60 sec auton.
- Continue Drive Practice.

## 11/14/20
### Attendance: &#9745; Brody, &#9745; Derek, &#9744; Dylan, &#9744; Ian, &#9745; Jack
Today we hosted a scrimmage that consisted of 4 teams, 9447B, 9447Z, 3859W, and 9447H(us). The scrimmage went from 2:30 to 4:00. We did 10 qualification matches and then did a best of three for finals. We paired with 3859W for finals and won the best of three with them. This scrimmage was very good in helping us learn about what we need to practice. The main thing we have to do is continue practicing both driving and programming. The auto sorting could use a little bit more tuning but the robot is good and all we need to do now is become good at driving and programming it. 

## 11/17/20
### Attendance: &#9744; Brody, &#9745; Derek, &#9744; Dylan, &#9745; Ian, &#9745; Jack
Today we focused on practicing. We spent most the day just working on the autonomous phase and spent the last thirty minutes practicing driving. In this time we were able to create an autonomous routine that scores scores a ball in every goal in our home row in the 15 seconds. With this autonomous we are confident that we will be able to do well in our first tournament.

## 11/21/20
### Attendance: &#9744; Brody, &#9745; Derek, &#9744; Dylan, &#9745; Ian, &#9745; Jack
This competition was a very good one. We won all of our qualifier matches and won every auton except one which we tied. We ended qualifiers with 14WP/39AP/70SP. We also won the excellence award since we placed high in qualifications, high in skills, made it to finals, and did well in our interview.
The only things we want to improve about our robot is the intakes as they had some inconsistencies and just more autonomous and driver practice. We are very happy with how our robot performed today and will spend our time between this and our next competition practicing as much as we can.

| Rank | Team Number | W-L-T | WP | AP | SP |
|------|-------------|-------|----|----|----|
| 1    | 61317A      | 7-0-0 | 14 | 42 | 66 |
| 2    | 9447H       | 7-0-0 | 14 | 39 | 70 |
| 3    | 1223Y       | 6-1-0 | 12 | 30 | 59 |
| 4    | 9447B       | 5-2-0 | 10 | 33 | 71 |
| 5    | 3796E       | 5-2-0 | 10 | 24 | 71 |
| 6    | 97671A      | 3-4-0 | 6  | 24 | 82 |
| 7    | 97671C      | 3-4-0 | 6  | 21 | 68 |
| 8    | 3796F       | 3-4-0 | 6  | 18 | 78 |
| 9    | 3796B       | 3-4-0 | 6  | 18 | 47 |
| 10   | 9880A       | 3-4-0 | 6  | 15 | 76 |
| 11   | 9880C       | 3-4-0 | 6  | 12 | 70 |
| 12   | 3796A       | 2-5-0 | 4  | 18 | 67 |
| 13   | 3796D       | 2-5-0 | 4  | 15 | 70 |
| 14   | 3796C       | 2-5-0 | 4  | 15 | 59 |
| 15   | 97671B      | 1-6-0 | 2  | 9  | 64 |
| 16   | 9880D       | 1-6-0 | 2  | 3  | 66 |

| Our Matches | Red Alliance    | Blue Alliance  | Auton Winner | Score   |
|-------------|-----------------|----------------|--------------|---------|
| Q1          | 9447B & 97671C  | **9447H** & 3796E  | Tie          | 11 - **26** |
| Q7          | **9447H** & 3796A   | 3796B & 3796D  | Red          | **14** - 8  |
| Q11         | **9447H** & 61317A  | 9447B & 3796F  | Red          | **24** - 16  |
| Q16         | 9880A & 9880D   | **9447H** & 3796D  | Blue         | 12 - **25** |
| Q20         | 3796C & 3796B   | **9447H** & 97671B | Blue         | 6 - **67**  |
| Q23         | 97671A & 97671B | **9447H** & 3796C  | Blue         | 6 - **42**  |
| Q27         | **9447H** & 1223Y   | 9880C & 9880D  | Red          | **30** - 6  |
| QF 1-1      | **9447H** & 61317A  | 3796C & 97671B | Red          | **66** - 3  |
| SF 1-1      | **9447H** & 61317A  | 97671A & 3796B | Red          | **24** - 7  |
| F 1-1       | **9447H** & 61317A  | 9447B & 3796F  | Blue         | 8 - **30**  |

## 11/24/20
### Attendance: &#9744; Brody, &#9745; Derek, &#9744; Dylan, &#9744; Ian, &#9745; Jack
Today we spent our practice fixing the problems we noticed with our robot and our code from the tournament. We decided that since the traction wheels in the drive base were not very effective at stopping us from getting pushed that we would remove the traction wheels entirely and just have 4 omni wheels. While doing this does leave us susceptible to be being pushed from the side we are able to move the front motors on the drive base back and connect the two motors together. This change is worth being able to be pushed because now we will have a stronger drive base and with the motors being farther back we can improve on the path that the balls take so the balls will move through our robot much smoother. Today we also made changes to our code. At the competition we noticed our slew code in our `Chassis::turn();` and `Chassis::drive();` was not performing how we wanted it to so we altered the member functions to now work in a specific way. The robot will use the slew rate acceleration code until the speed it gets to from the slew code reaches the same output as the PD loop. Upon that happening it will use the PD loop to determine the speed of the motors. This allows for a steady acceleration from the slew code which then perfectly transitions into the steady decceleration of the PD loop. We also added a few more features into the code such as allowing us to run the `Intake::autoSort();` member function while calling `Chassis::drive();` or `Chassis::turn();`. The final change we made to our code was we also fixed the `Chassis::withHeading();` member function. Whenever we call `Chassis::drive();` we can also call `Chassis::withHeading();` which will tell the robot what degree it should be facing. This will allow us to either keep the robot straight while driving or we can tell it to go to any other degree and then it will begin to curve while driving to it's target. This capability will allow us to drive in a curve-like manner if we need to for the autonomous phases. The last thing we did today was we also designed a new intake design. The new design uses fully static intakes and instead of track and a wheel it uses two flex wheels on each intake. They will be connected by 12 tooth sprockets with chain. Our reasoning for making them completely static is that the flex wheels will flex as much as they need to, to allow the balls to enter the robot. The design is very simple and since they are completely static they are very strong which was a problem with our current intakes. We are very exicted to try and test out these intakes since from what we saw at the competition in Greenville no one in our state seems to be using the new flex wheels.

```cpp
switch (drive_theta){
  case 0: {
    if(abs(headDifference) < 180){
      LOutput -=correction_rate;
      ROutput +=correction_rate;
    }else{
      LOutput +=correction_rate;
      ROutput -=correction_rate;
    }
  break;
  }
  default:{
    if(averageheading < drive_theta && averageheading!=0){
      LOutput +=correction_rate;
      ROutput -=correction_rate;
    } else if(averageheading > drive_theta && averageheading!=0){
      LOutput -=correction_rate;
      ROutput +=correction_rate;
    }
    if(headDifference >180 && averageheading ==0){
      LOutput -=correction_rate;
      ROutput +=correction_rate;
    }else if(headDifference <180 && averageheading ==0){
      LOutput +=correction_rate;
      ROutput -=correction_rate;
    }
  break;
  }
}
```

<img src="././_images/11-November/11-24-20/intake_alone.png" alt="intake_alone.png" style="width: 200px;"/>
<img src="././_images/11-November/11-24-20/intake_on_robot.png" alt="intake_on_robot.png" style="width: 200px;"/>
<img src="././_images/11-November/11-24-20/intake_other_angle.png" alt="intake_other_angle.png" style="width: 200px;"/>
<img src="././_images/11-November/11-24-20/intake_top.png" alt="intake_top.png" style="width: 200px;"/>