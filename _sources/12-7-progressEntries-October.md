---
jupytext:
  cell_metadata_filter: -all
  formats: md:myst
  text_representation: {extension: .md, format_name: myst, format_version: 0.12, jupytext_version: 1.6.0}
kernelspec: {display_name: Python 3, language: python, name: python3}
---

# October 2020 Progress Entries
## 10/6/20
### Attendance: &#9745; Brody, &#9745; Derek, &#9745; Dylan, &#9745; Ian, &#9745; Jack
### Intake Changes
- Static intakes (dont fold out)
- Geared intakes instead of connected by track
- A mechanism to push the goal up a bit to help the ball leave the goal

Today we solely focused on improving our intakes. We began by redoing the core design of them and building something similar to the design we had in Tower Takeover. This new design is better because it encompases all of the criteria above which were all pitfalls of the last design. 

### New Intakes
<img src="././_images/10-October/10-6-20/intakesFrontView.jpg" alt="intakesFrontView.jpg" style="width: 200px;"/>
<img src="././_images/10-October/10-6-20/intakesSideView.jpg" alt="intakesSideView.jpg" style="width: 200px;"/>
<img src="././_images/10-October/10-6-20/intakesWithBall.jpg" alt="intakesWithBall.jpg" style="width: 200px;"/>
<img src="././_images/10-October/10-6-20/goalLifter.jpg" alt="goalLifter.jpg" style="width: 200px;"/>

## 10/13/20
### Attendance: &#9745; Brody, &#9745; Derek, &#9745; Dylan, &#9745; Ian, &#9745; Jack
### Problems with scoring

#### Description
- The ball indexed at the top of the robot has trouble scoring itself because it doesn’t have enough speed.

#### Attempt to fix it 
We tried increasing gear ratio to 2:1 to make the ball faster. While increasing it to have more speed, the ball was not able to move at all.To help this, we are going from a 2:1 to a 1:2 gear ratio. While making the gear ratio 1:2, it was the worst out of the three. Our next approach was changing the curve of our hood. We tried having the hood bend upward at the end of it which turned out to fix the problem we were having. TWhile this hood does do a good job at scoring the balls, it does have a hard time supporting itself and also starting in the size requirements. Next week we are going to redesign the hood so it meets all of these requirements.

<img src="././_images/10-October/10-13-20/hoodSCurve.jpg" alt="hoodSCurve.jpg" style="width: 200px;"/>

## 10/20/20
### Attendance: &#9745; Brody, &#9745; Derek, &#9745; Dylan, &#9745; Ian, &#9745; Jack

### Hood Changes
- Near flat piece of polycarbonate.
- Easy and consistent starting postition.
- Secure position for the top line sensor.

Today we solely focused on improving our hood. We began by redoing the way it connected to the robot as the old design was weak and in the way. The new design has the hood connect to the two c-channels that create the back tower of our robot. Since we mounted it this way, it also able to fit inside the top roller for an easy and consistent starting position. Our new hood is almost completely flat. To help with keeping constant pressure on the ball, we put 1.5" spacers at the end of it to give it just enough of an arc that would give the ball just the right amount of pressure.

### New Hood

%%HTML
<div align="middle">
<video width="80%" controls>
      <source src="././_images/10-October/10-20-20/hoodUnfolding.mp4" type="video/mp4">
</video></div>

## 10/27/20
### Autosort Function
Since we got VEX’s new optical sensor that can sense the color of objects, we decided that we wanted to use that instead of the vision sensor since the sensor is more compact and is more efficient at detecting color than the vision sensor. Since the sensor currently does not have support in PROS we began testing it in VEXCODE. Since we implemented the sensor we are able to now remove the bottom line sensor since now when we index balls we can use the optical sensor to stop the ball and the bottom line sensor is redundant. Since the optical sensor might not be supported in PROS by the time of our first competition on 11/21/20 we will probably not be using this feature and stick with normal auto indexing. But we will continue developing and perfect it so when it becomes supported we will be ready to implement it fully. Below is the current working autosort function.

```cpp
void calculateSort(int goodBall){ //This function is run by autoSort() AutoSort inputs the value for goodBall goodBall tells the robot if red or blue is good
 switch (goodBall){
   case 1:{
     if(Optical2.hue() <= 10){ //Sees RED Ball //If there is a ball at the top already it will stop this ball at the Optical Sensor
       middleIntake.setVelocity(50, rpm);
       indexer.setVelocity(80, rpm);
       indexer.spin(forward);
       redBall=1;
       if(topLine.value(pct)<=60)middleIntake.stop();
     }
     if(Optical2.color() == blue){middleIntake.setVelocity(50, rpm); middleIntake.spin(forward); if(topLine.value(pct) >=60){indexer.spin(reverse);}}
    
     if(topLine.value(pct) <=60){
       indexer.stop();
     }
 
     redBall=0;
     break;
   }
   case 2:{
     if(Optical2.hue() == blue){ //Sees BLUE Ball
         middleIntake.setVelocity(100, rpm);
         indexer.setVelocity(100, rpm);
         middleIntake.spin(forward);
         indexer.spin(forward);
         if(topLine.value(pct) <=60){
           indexer.stop(); //Intake until it reaches top Line Sensor
           if(midLine.value(pct) <=60)middleIntake.stop();
         }
     }else if(Optical2.hue() <= 10)middleIntake.spin(forward);
     break;
   }
 }
}
```

### Finalizing the Robot for the 11/21 Competition
We are very happy with the way our robot is right now, so we decided that today was our last editing day and that starting next tuesday we will begin practicing again in preparation for our competition. Our goals for this competition are to win Tournament Champion, Skills, and Excellence if possible. We are confident that if we practice enough that we will be more than able to do this with our current robot. 

#### Practice Goals
For Pre-auton, we want a program that will be able to fill our home row. We want this because if we can fill the home row in every match we will get a lot of extra Win Points which will help us rank high. 
For Autonomous Skills, if time allows, we will improve upon our home row pre-auton by either trying to fill the rest of the goals or by filling only a couple rows but also removing the blue balls from them.
For Driving Skills, Our goal is to get at least 100 points and then begin trying to get the max score by descoring all the blue balls too