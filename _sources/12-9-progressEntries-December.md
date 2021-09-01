---
jupytext:
  cell_metadata_filter: -all
  formats: md:myst
  text_representation: {extension: .md, format_name: myst, format_version: 0.12, jupytext_version: 1.6.0}
kernelspec: {display_name: Python 3, language: python, name: python3}
---

# December 2020 Progress Entries
## 12/1/20 
### Attendance: &#9744; Brody, &#9745; Derek, &#9744; Dylan, &#9745; Ian, &#9745; Jack
#### Goals: 
- practice on autonomous routine and driver skills routine. get as close as possible to 106 for autonomous and 126 for driver

When working on our autonomous routine, we noticed that the robot would act in a weird way when doing very small turns. The problem was that when it started using the slew rate acceleration it would turn the wrong way and begin speeding up until hitting the PD loop after that it would then settle perfectly and turn the right way. To combat this problem we added a new member function to the Chassis class that allows us to enable or disable the slew rate acceleration portion in driving or turning. This is the perfect fix for this problem since in reality we do not even need slew rate acceleration when the turn is so small because the robot is already going very slow with the PD loop so to use slew rate acceleration is unnecessary. With our autonomous we encountered a problem with the robot not settling when approaching a goal because the goal was restricting it's movement forward. To fix this problem we added a V5 distance sensor to the front of our robot that is at the same height of the rings of the goals. What this distance allows us to do is break the robot from the `Chassis::drive` member function and continue with the run. This will be extremely helpful as it will now enable us to not worry about hitting the goal at one specific spot but to continue going forward until the distance sensor determines that we are close enough to the goal to begin scoring.  

### Competition Goals
Our goal for this competition is to score at least 150 points total. With our current autonomous routine and our driver routine we think this is more than feasible. We want to score at least 150 points because at this point in the season we should be able to have more than half of the maximum skills score (which is 126) and 150 points is a solid starting point.

## 12/5/20 The VRC Phoenix Skills Only Challenge (Blended MS/HS, In-Person or Remote, Live, Remote Judging)
### Attendance: &#9745; Brody, &#9745; Derek, &#9744; Dylan, &#9745; Ian, &#9745; Jack
### Tournament Results
| Rank | Team   | Driver Highscore | Programming Highscore | Total Highscore |
|------|--------|------------------|-----------------------|-----------------|
| 1    | 10955M | 126              | 52                    | 178             |
| 2    | 61317A | 111              | 52                    | 163             |
| 3    | 9447H  | 111              | 45                    | 156             |
| 4    | 3859W  | 100              | 26                    | 126             |
| 5    | 9447B  | 82               | 19                    | 101             |
| 6    | 1223Y  | 80               | 19                    | 99              |
| 7    | 79267A | 69               | 19                    | 88              |
| 8    | 1711A  | 65               | 13                    | 78              |
| 9    | 9623Z  | 55               | 19                    | 74              |
| 10   | 9623X  | 41               | 19                    | 60              |
| 11   | 1711B  | 57               | 0                     | 57              |
| 12   | 61317D | 48               | 0                     | 48              |
| 13   | 9447Z  | 41               | 0                     | 41              |
| 14   | 3859D  | 35               | 0                     | 35              |
| 15   | 61317B | 0                | 0                     | 0               |

In Our skills tournament, we placed 3rd with a total score of 156. We then went on to win the excellence award. The highlight of this tournament for us, was that this was by far our best skills performance. We did much better in both driver and autonomous and our time practicing them really helped. Since our next competition is not until January we are going to start making the changes to our intakes. We are going to be building and testing out the fully static flex wheel intakes design first since we already have the exact layout for it and we are very interested to see how effective fully static intakes will be. As of 12/5/2020 we are currently ranked 88th in the world, 61st in the United States, and  second place in SC for skills.

### Goals for Next Comp 1/23/20
Although our next comp is not for a while we want to begin readying ourselves for it. For our next comp we want to get a score of at least 200 points in skills. To do this will we be aiming for a 106 point auton and a 126 point driver.

+++

## December Timeline
Between now and our next compeition we have 7 practices and a total of 21 hours to work with the field. Since we want to get our skills score to 200+ points we know that we will need to spend a lot of time practicing both autonomous and driver skills. Since we have a limited amount of time available at the field, we are planning out all of our practices between now and the tournament on January 23rd to ensure that we are able to meet our goals. In addition to our skills score goal we also want to revisit our 15 second autonomous and perfect it so it can more reliably score and own our home row since it was not able to do that at our first competition.

<img src="././_images/12-December/12-6-20/december_calendar.png" alt="december_calendar.png"/>

### Goals
#### 15 second autonomous Created on 12/08/20
Since we already have the run programmed all we need to do is finetune each move individually so it is as accurate and consitent as possible. Since this is a relatively simple task we will only be alloting one practice to working on this. 

#### 60 second autonomous Created on 12/08/20
To make the 106 autonomous routine we are planning on expanding on our 45 point auton to get the remaining goals. Due to the time it takes for us to be able to perfect each move in autonomous we are going to alloting 9 hours of practice time to accomplishing this task since it is very important to us.

#### Driver Skills Created on 12/08/20
We will be alloting the other 9 hours to practicing our driver skills run. We want to allot this much time to practicing driver skills because the difference between 111 driver score and 126 driver score even though it isn't much in points is a lot in the actual driving since we will need to descore all the blue balls as well as score every red ball. This will require us to design a new driving strategy to be able to do this as efficiently as possible with our robot.  

## 12/8/20
### Attendance: &#9744; Brody, &#9745; Derek, &#9744; Dylan, &#9744; Ian, &#9744; Jack 
### Goals 
- Perfect the 15 second autonomous routine 
- Add new flex wheel intakes to the robot, and fix the ball-idle issue with middle rollers
### What we Accomplished
Today we built and added the new flex wheel intakes to the robot. We changed the design slightly from the one in the CAD models so it has better spacing and less friction. (the axle was moved from a side hole on the c-channel to the middle hole, idk how exact you want to be when documenting this). When we first started testing the new intakes we quickly noticed that instead of bringing the balls up into the robot, the intakes would bring the balls towards the motors and the balls would get stuck. To fix this issue, we added zip ties to the bottom rubber band structure to help guide the balls upwards. The zip ties are stronger than the rubber bands and help the intakes a lot. To make the intakes even better we cut a piece out of the cross brace of the robot as the balls were scraping against it and slowing down.
The ball-idle issue was also fixed today, the problem is that instead of being pulled up the intake rollers, the balls get forced into the rubber bands of the back roller, then bounce backwards losing a lot of energy and slowing down until the rollers regain friction with the ball and continue to move it upwards. The way we fixed this problem was by adjusting the number of rubber bands on each roller. The back top roller that the balls were bouncing off of now has less bands to prevent balls bouncing off it, and the middle front roller has more rubber bands to maintain more constant grip with the ball. We also began working on perfecting the 15 second autonomous since that was the main goal for today. While working on it, we decided that we wanted to improve upon the autonomous by descoring the enemy's balls in the two corner goals. To do this we run our GoalSort function while at the goal which will send the enemy's ball out the back of our robot upon sensing it with the optical sensor. Adding this to our 15 second autonomous though made the process of perfecting the run take longer than we had expected since we now need more time to descore so all of the movements will need to be sped up so we have enough time to sort the goals.

<img src="././_images/12-December/12-8-20/intakeAngledView.JPG" alt="intakeAngledView.JPG" style="width: 200px;"/>
<img src="././_images/12-December/12-8-20/intakeSideView.JPG" alt="intakeSideView.JPG" style="width: 200px;"/>
<img src="././_images/12-December/12-8-20/robotFrontView.jpg" alt="robotFrontView.JPG" style="width: 200px;height: 200px;"/>
<img src="././_images/12-December/12-8-20/robotSideView.JPG" alt="robotSideView.JPG" style="width: 200px;"/>

## 12/15/20
### Attendance: &#9744; Brody, &#9744; Derek, &#9744; Dylan, &#9744; Ian, &#9745; Jack
Today while working on the 15 second autonomous program we noticed that our lateral movements were getting more and more inaccurate. To figure out the problem we printed the encoder values to ensure that the encoders were reading properly. Unfortunately our encoders had broken and were no longer correctly tracking the robot's movement. After replacing the encoders with new ones the robot now more accurately then ever before tracks the robot's movement through it's wheels. Finding this problem was extremely important as we were confused why our lateral movements were less accurate then our turning movements. Now that we have this fixed our movement during autonomous will be a lot more consistent. After fixing this problem we finished perfecting our 15 sec autonomous routine. A normal match starts with Red and Blue tied at 15-15 but our autonomous causes a 23 point swing bringing our total to 30 points and the enemy's to 7 points. The reason we needed to add the descoring of the blue balls is because even if the enemy team gets their home row, we will win by two points since we also descore the balls from the goals. Although we are now finished with the 15 second autonomous routine we will be running it every practice at least once to make sure it is truly consistent. 

## 12/22/20
### Attendance: &#9744; Brody, &#9744; Derek, &#9744; Dylan, &#9744; Ian, &#9745; Jack
We began working on our skills auton today and have made many improvements from our skils auton we used at our last comp. Currently we have a skills auton with a maximum of 85 points which we achieve by scoring 10 red balls and descoring 9 blue balls and also owning 7 of the nine goals. To help with consistency we have created a couple new member functions to make sure we can be as efficient and consistent as possible during our skills auton. Two new member functions we made are `Intake::goalSort(int allinaceColor, int time, bool state = SHOOTBALL);` and `Intake::dropBall();`. The reason we made another goalSort function was we wanted the ability to run `Intake::goalSort` for a set amount of time and also decide if we wanted to hold onto the blue balls or shoot them out the back of our robot. During the beginning half of the autonomous if we shoot the balls out the back of the robot it creates a chance that the blue ball might hit a red ball that we use or get in our future path and so to solve this problem we now are able to score our red balls and then hold onto the blue balls from the goal and then whenver we want to all we need to do to get rid of the blue balls is call the `Intake::dropBall();` function which just spits them out the back. In practice what this looks like is after we score our red balls and pull the blue ball(s) out we will turn and then before continuing on through our autonmous routine we will shoot the blue ball(s) out the back of the robot into a place that will not effect the autonomous routine. A problem we began noticing was that balls would sometimes not be able to flow through our robot well and either not make it up to the top of the robot or just fall out the back when they were not supposed to. Our fix for this is we are going to replace our two bottom rubber band rollers with 3in. flex wheels so the balls are controlled better through our robot. We know this will solve our problem since the cause is that we are having trouble with consistent compression which can not be achieved by rubber bands since they deteriorate so quickly. Since the flex wheels that we have on our robot currently have been very good we are confident that replacing more rollers with flex wheels is the right move in making our robot more efficient. 

``` cpp
void Intake::goalSort(int allianceColor, int time, bool state){
  if(state){
    for(int i=0; i<time;i++){
      goalSort(allianceColor);
      pros::delay(15);
    }
  }else{
    for(int i=0; i<time;i++){
      runAutoIndexer();
      pros::delay(15);
    }
  }
  intakeStop();
  middleStop();
  indexerStop();
  blueBall = 0;
  holdComplete =0;
}

void Intake::dropBall(){
  indexerSpinVelocity(-200);
  pros::delay(250);
  middleSpinVelocity(600);
}
```
## 12/29/20
### Attendance: &#9745; Brody, &#9744; Derek, &#9744; Dylan, &#9744; Ian, &#9745; Jack
For our tournament on January 23rd we want to be fully prepared for every aspect of it. To do this we are trying out a lot more tactics then we have never done in the past. In addition to practicing our skills runs to get the highest possible skills score we also want to do well in the qualifier and elimination bracket. Looking back at our first tournament in Greenville at JL Mann we did really well in qualifiers by winning 6 of our 7 auton phases and tieing the last one. But in finals, we lost both the auton phase and the match. For our tournament at West Ashley we have been working on our 15 second auton a lot and it is a lot more consistent than the one we brought to JL Mann. The final preparation we are doing to ensure that we are ready for our next tournament is that we have started working with another team. We decided on doing this because it will allow us to begin practicing and strategizing with them so during the tournament we are more prepared then we would be normally. We talked with 3859W and together we designed an autonmous routine where we will control 6 goals during the autonmous phase. Our routine will set the match score to 61-7 asssuming the opposing alliance does not score any points. If the opposing alliance scores their home row and descores all of our balls from their home row we will still win by 9 points. Today is the day that we are officialy saying that we finished our 15 second autonomous routine. We are very happy with and think it will do very well at our upcoming tournament. We are also happy with our skills auton but believe it can be improved upon. 

%%HTML
<div align="middle">
<video width="80%" controls>
      <source src="././_images/1-January/1-5-21/15-sec-auton.mp4" type="video/mp4">
</video></div>

## West Ashley Pre-Tournament Scouting
| Category             | 3859W    | 61317A   | 1223Y    | 9447B    | 9623X    | 79267A   |
|----------------------|----------|----------|----------|----------|----------|----------|
| Auton                | &#10003; | &#10003; | &#9746;  | &#9746;  | &#9746;  | &#9746;  |
| Driver Skill         | &#10003; | &#10003; | &#10003; | &#10003; | &#10003; | &#10003; |
| Skills Score         | &#10003; | &#10003; | &#9746;  | &#10003; | &#9746;  | &#10003; |
| Synergy              | &#10003; | &#10003; | &#10003; | &#10003; | &#10003; | &#10003; |
| Highest Skills Score | 126      | 176      | 99       | 101      | 60       | 88       |

There are 6 teams that we think will most likely do quite well at the next tournament that we want to keep track of. Between Turning Point, Tower Takeover and Change Up we have been able to get to know all of these teams pretty well and know what their strengths are generally. 3859W is a good team that is proven since at our last tournament they won the design award. 61317A is also a good team as they have both a high skills score as well as they normally have good autonomous routines. 1223Y is another quality team as they have a very competent driver. 9447B is a very special team to us because they are our sister team and this year they have proven to be a very capable team. 9623X started late compared to everyone else this year so it makes sense that they did not do as well as everyone else at our last tournament but over the winter break they most likely have improved a lot more since our last tournament. 79267A was the team we partnered with at states last year in Tower Takeover. They are a very nice team and also have a good robot, so we are looking forward to see how they will do at the West Ashley tournament. 

### Our Expectations
Overall we are very excited for our next tournament. This will definetely be the most competitive tournament so far.