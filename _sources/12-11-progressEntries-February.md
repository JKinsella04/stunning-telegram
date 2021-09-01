# February 2021 Progress Entries

## 2/2/21
### Attendance: &#9745; Brody, &#9745; Derek, &#9745; Dylan, &#9744; Ian, &#9745; Jack
Since the West Ashley tournament was cancelled we signed up for a Remote Skills Only No Judging tournament for this weekend. Today we spent the majority of the day practicing driver skills. To help with descoring balls from the middle goal, we added a deployable pusher on the back of the robot that allows us to more easily descore from the middle goal. When creating this pusher we wanted it to meet two criteria, be efficent at descoring the middle and also be non-invasive to the majority of the run. To satisfy the effeciency we developed a strategy that we employ with this pusher where we put the pusher into the goal and then turn left and right, this movemenet will without fail remove at least one ball from the goal. To make it non-invasive, we made it work like a lever. To do this we added tension where in its starting position it would stay up and out of the way, to activate the lever, we back up into a goal and when the bottom of the mechanism hits the goal it will reposition the tension making it want to become parallel with the ground. 

<iframe width="560" height="315" src="https://www.youtube.com/embed/r7A88vzF-zk" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

## Pre-Tournament Entry 2/8/21
### Current Robot

<img src="././_images/2-February/2-8-21/robot_angle.png" alt="robot_angle.png" style="height: 300px;"/>
<img src="././_images/2-February/2-8-21/robot_side.png" alt="robot_side.png" style="height: 300px;"/>
<img src="././_images/2-February/2-8-21/robot_other_angle.png" alt="robot_other_angle.png" style="height: 300px;"/>

### Core Mechanical Concepts
#### Expanding intakes
To increase our reach into the goals, we added a new section to our intakes, which start folded into the robot and expand outward. Currently they have intake rollers since we do not have any extra of the smallest flex wheels. This new intake expansion now lets our robot enter halfway into the middle goal and 

### Core Programming Concepts
#### 2 Controller Setup
For this competition we have increased our automatic controls to a more advanced configuration. Our old controller scheme had used 5 buttons on one controller but now we use 4 buttons on two controllers. Derek our main driver, uses our master contrller which controls the drive base and has one button (R1), which when pressed runs `goalSort()`. Jack is our second driver who uses the partner controller, which has 3 buttons (R1, R2, and L1). The partner controller is mainly just used to update our `ballsLeft` variable which controls how the intakes spin when we run `goalSort()`. When we run `goalSort()` it will subtract one from `ballsLeft` every time the enemy's ball is sorted through our robot, and once `ballsLeft` reaches 0 it reverses the intakes so we do not intake our own balls. L1 on the partner controller adds one to this variable so we can manually tell the robot how many balls to expect before it reaches the goal. R1 sets the variable to 0 so we have the ability to reset the variable in the event anything unexpected happens and we need to reset the variable manually. R2 on the partner controller reverses the intakes. We have this so when we go to descore the middle goal we can spin the intakes in reverse without spinning any of the rollers. 

## 2/9/21 
Today is our last practice before our next tournament. The only change we had to make to our robot is that we removed our front hood for this tournament since we can not get it to fit in size and we want to use our last practice practicing instead of trying to fit the hood. We are pretty confident that we will get around 84 points in our autonomous and should range anwhere from 190-200 points total for skills. 

### February Timeline
<img src="././_images/2-February/feb_calendar.PNG" alt="feb_calendar.png"/>

#### Completed Goals
- 85-94 Autonomous skills run 

#### Remaining goals for February
- Reimplement front hood before JL Mann tournament
- 106-119 point auton

## Post-Tournament 2/14/21
### Tournament Stats
| Rank | Team   | Name                      | W-L-T | WPs / APs / SPs | OPR   | DPR   | CCWM   |
|------|--------|---------------------------|-------|-----------------|-------|-------|--------|
| 1    | 9447H  | ¯\_(ツ)_/¯                | 7-0-0 | 18 / 39 / 32    | 27.97 | -5.72 | 33.69  |
| 2    | 79267A | Swamp Bots                | 6-1-0 | 13 / 24 / 63    | 11.51 | -0.13 | 11.64  |
| 3    | 9623Z  | WARP Drive - Zulu         | 4-2-1 | 12 / 30 / 44    | 3.87  | 9.42  | -5.55  |
| 4    | 9447B  | Wild Cards                | 5-2-0 | 12 / 24 / 44    | 24.75 | 7.55  | 17.2   |
| 5    | 61317A | JP2 S.H.I.E.L.D.          | 5-2-0 | 11 / 30 / 41    | 24.66 | 5.07  | 19.59  |
| 6    | 9623X  | WARP Drive - BotX         | 4-2-1 | 9 / 30 / 55     | 17.82 | 1.19  | 16.62  |
| 7    | 9447Z  | GoofTroop                 | 4-2-1 | 9 / 21 / 46     | 6.49  | 0.77  | 5.72   |
| 8    | 61317B | JP2 S.H.I.E.L.D. Robotics | 3-3-1 | 8 / 30 / 50     | 3.8   | 17.2  | -13.4  |
| 9    | 3859W  | Astrobots                 | 4-3-0 | 8 / 27 / 51     | 16.07 | 1.5   | 14.57  |
| 10   | 29073A | Robophobia                | 3-3-1 | 8 / 21 / 77     | 6.08  | 6.2   | -0.12  |
| 11   | 3859D  | Dystopia                  | 4-3-0 | 8 / 18 / 60     | 16.65 | 20.18 | -3.53  |
| 12   | 3859B  | Vortex                    | 3-3-1 | 8 / 15 / 77     | 9.55  | 13.68 | -4.13  |
| 13   | 1711A  | Mighty Lions HS           | 3-3-0 | 7 / 24 / 62     | 16.67 | 4.29  | 12.38  |
| 14   | 61317D | JP2 S.H.I.E.L.D.          | 3-4-0 | 6 / 15 / 39     | 7.54  | 9.27  | -1.73  |
| 15   | 1711B  | MLRC B                    | 3-4-0 | 6 / 6 / 63      | 2.95  | 7.34  | -4.39  |
| 16   | 79267F | Swamp Bots 2.0            | 2-5-0 | 5 / 15 / 43     | 10.47 | 17.05 | -6.59  |
| 17   | 44252A | LexTech                   | 2-5-0 | 4 / 0 / 44      | 2.98  | 20.49 | -17.52 |
| 18   | 29073B | Rust in Pieces            | 1-5-1 | 3 / 18 / 61     | 2.64  | 20.32 | -17.67 |
| 19   | 88458A | Hawthorne Robotics        | 1-6-0 | 2 / 18 / 62     | 0.87  | 19.04 | -18.17 |
| 20   | 1711W  | The Third Wheel           | 1-6-0 | 2 / 12 / 49     | -1.04 | 29.39 | -30.43 |
| 21   | 3859X  | Flying Lawnmowers         | 1-6-0 | 2 / 9 / 37      | -0.13 | 10.42 | -10.55 |

### Our matches
| Our Matches | Red Alliance        | Blue Alliance      | Auton Winner | Score |
|-------------|---------------------|--------------------|--------------|-------|
| Q-3          | **9447H** & 613171B | 61317D & 1711B     | Tie          | **16**-6  |
| Q-7         | 61317D & 29073B     | **9447H** & 9623Z  | Blue         | 4-**34**  |
| Q-14        | **9447H** & 79267A  | 3859X & 84458A     | Red          | **28**-5  |
| Q-18        | 88458A & 9447B      | **9447H** & 61317A | Blue         | 5-**50**  |
| Q-26        | 1711A & 29073B      | **9447H** & 79267F | Blue         | 3-**38**  |
| Q-31        | **9447H** & 29073A  | 9447Z & 44252A     | Red          | **44**-6  |
| Q-34        | **9447H** & 61317B  | 3859B & 3859X      | Red          | **50**-3  |
| QF 1.1      | **9447H** & 3859W   | 61317D & 1711B     | Blue         | **19**-11 |
| SF 1.1      | **9447H** & 3859W   | 9447B & 9623X      | Blue         | 9-**18**  |


### Tournament Evaluation
Overall we are very happy with our performance this tournament. In this tournament we won Excellence and Robot Skills. Our autonomous worked quite well with an exception of our first match in which we tied the autonomous phase. We placed first place this tournament because we won all of our qualifier as well as getting the autonomous win point 4 times. Unfortunately one of our tracking wheels got damaged in our Quaterfinal match which caused our autonomous to run incorrectly causing us to drive too much backward. Our skills score this tournament was 193, 82 autonomous and 111 driver. This tournament helped us determine what parts of our robot work well and what does not. For this tournament we had to remove our front hood since with the new intakes we could not fit in size, but because we removed our hood the balls spent a lot of extra time spinning at the top of the goals and sometimes just entirely fell out of the goals while they spun around. This caused us to end us spending more time than we wanted when cycling as well as hurting our autonomous routines. To fix this we began working on a new hood that will fit in size with our new intakes. Our other biggest problem is that because of different light and the distance between our line sensor to the balls we hold we were having problems with the ball not indexing properly during both autonomous and driver. To fix this we swapped out our top line sensor with a v5 distance sensor. Replacing the line sensor with the distance sensor helps us since now we checking to find a change in distance instead of a difference in light. 

## 2/16/20
### Needed changes before next tournament
- Reinforce tracking wheels
- Redesign + add front hood

#### Reinforced tracking wheels
To help reinforce our tracking wheels, we supported them on both sides instead of just one screw joing on the side. Doing this allows us to have be tensioned while not pulling the wheels to the side so we will more accurately track the robot's movement as well as making them more resistant to defensive play from other robots.

<iframe width="560" height="315" src="https://www.youtube.com/embed/1Ov_rHwna9A" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

#### New hood
To have the hood be able to fit with the new intakes we had to shorten the overall length of the hood which means the hood goes farther forward from the robot than it does upward. This is not a problem for us since the goal of the hood for us is not to guide the ball down towards the goal but to make the ball go down into the goal faster.

<iframe width="560" height="315" src="https://www.youtube.com/embed/RJeTpzs-vcM" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

## Post Tournament  2/21/20
We are pretty happy with our performance yesterday at the JL Mann tournament. We went 5-1-0 with 11 11 Win Points, 27 Auton Points and 46 Strength Points. We paired with 94999E Yokai-Independent who is from Georgia. We unfortunately lost in quarterfinals


### Tournament Stats
| Rank | Team   | Name                      | W-L-T | WPs / APs / SPs | OPR   | DPR   | CCWM   |
|------|--------|---------------------------|-------|-----------------|-------|-------|--------|
| 1    | 61317A | JP2 S.H.I.E.L.D.          | 5-0-1 | 11 / 30 / 57    | 32.22 | 0.75   | 31.47  |
| 2    | 9447H  | ¯\_(ツ)_/¯                | 5-1-0 | 11 / 27 / 46    | 25.05 | -1.58 | 26.63  |
| 3    | 3796B  | Some Assembly Required    | 5-1-0 | 10 / 15 / 56    | 17.41 | -1.38 | 18.78  |
| 4    | 3796F  | Pay Respects              | 4-2-0 | 9 / 24 / 60     | 16.66 | 0.59  | 16.07  |
| 5    | 1102X  | M'Aiken Magic             | 4-1-1 | 9 / 21 / 71     | 15.2  | 8.65  | 6.55   |
| 6    | 89878E | The Thingies              | 4-2-0 | 9 / 18 / 65     | 9.9   | 11.42 | -1.52  |
| 7    | 61317D | JP2 S.H.I.E.L.D.          | 4-1-1 | 9 / 12 / 73     | 18.14 | 7.33  | 10.81  |
| 8    | 9880C  | 3 Guys                    | 4-2-0 | 8 / 27 / 47     | 14.86 | 9.28  | 5.58   |
| 9    | 94999E | Yokai - Independent       | 4-2-0 | 8 / 21 / 55     | 11.34 | 14.92 | -3.58  |
| 10   | 97735X | Techno Crankers           | 4-2-0 | 8 / 18 / 70     | 15.53 | 3.58  | 11.95  |
| 11   | 9880D  | Valkyries                 | 4-2-0 | 8 / 12 / 57     | -0.05 | 4.06  | -4.12  |
| 12   | 3796E  | Caution! Student Drivers! | 4-2-0 | 8 / 12 / 50     | 19.04 | 11.82 | 7.21   |
| 13   | 40994F | Obsidian Outlaws          | 3-2-1 | 7 / 27 / 62     | 12.52 | 2.43  | 10.08  |
| 14   | 42748C | Cougars Renegades         | 3-2-1 | 7 / 24 / 76     | 11.87 | 4.61  | 7.26   |
| 15   | 29073A | Robophobia                | 3-3-0 | 7 / 24 / 52     | 12.94 | 15.83 | -2.88  |
| 16   | 86400A | ADHD                      | 3-3-0 | 7 / 24 / 46     | 15.1  | 11.0  | 4.09   |
| 17   | 9880A  | Rebel Circuits            | 2-3-1 | 6 / 24 / 51     | 10.45 | 14.87 | -4.42  |
| 18   | 8686Z  | Akanda and Friends        | 3-3-0 | 6 / 18 / 49     | 5.79  | 14.5  | -8.7   |
| 19   | 3796A  | Mann Made                 | 3-3-0 | 6 / 12 / 51     | 15.8  | 13.33 | -2.47  |
| 20   | 61317B | JP2 S.H.I.E.L.D. Robotics | 3-3-0 | 6 / 9 / 47      | 17.29 | -0.18 | 17.46  |
| 21   | 42748A | Cougar Crushers           | 3-3-0 | 6 / 6 / 70      | 5.26  | 17.17 | -11.91 |
| 22   | 8686Y  | League of Villians        | 2-3-1 | 5 / 18 / 61     | 13.34 | 6.91  | 6.43   |
| 23   | 86400C | Sprocketeers              | 2-3-1 | 5 / 15 / 73     | 1.72  | 10.33 | -8.61  |
| 24   | 86400D | The Spartans              | 2-4-0 | 4 / 18 / 46     | 1.21  | 6.53  | -5.32  |
| 25   | 97671C | Costco Hotdogs            | 2-4-0 | 4 / 15 / 59     | 9.41  | 26.49 | -17.08 |
| 26   | 8686S  | Giant Salamander          | 1-5-0 | 2 / 21 / 74     | -0.37 | 17.85 | -18.22 |
| 27   | 29073B | Rust in Pieces            | 1-5-0 | 2 / 12 / 55     | 6.1   | 18.97 | -12.86 |
| 28   | 3796D  | Oops, We Did It Again!    | 1-5-0 | 2 / 9 / 69      | 7.83  | 21.09 | -13.26 |
| 29   | 86400B | The Orbiters              | 1-5-0 | 2 / 9 / 47      | 1.57  | 8.45  | -6.88  |
| 30   | 3796C  | Don't Forget To Breathe   | 1-5-0 | 2 / 6 / 56      | -0.37 | 28.45 | -28.83 |
| 31   | 40994A | Peak Performers           | 0-6-0 | 0 / 0 / 41      | -4.12 | 31.48 | -35.6  |

### Our Matches
| Our Matches | Red Alliance       | Blue Alliance      | Auton Winner | Score     |
|-------------|--------------------|--------------------|--------------|-----------|
| Q-4         | 3796D & 86400B     | **9447H** & 94999E | Blue         | 2-**66**  |
| Q-10        | **9447H** & 8686S  | 86400C & 1102X     | Tie          | **12**-11 |
| Q-22        | **9447H** & 97735X | 3796C & 9880C      | Red          | **44**-5  |
| Q-26        | 3796E & 9880D      | **9447H** & 86400D | Blue         | **15**-12 |
| Q-37        | 40994F & 29073B    | **9447H** & 42748C | Red          | 12-**24** |
| Q-42        | **9447H** & 86400A | 61317D & 40994A    | Red          | **47**-4  |
| QF-3-1      | **9447H** & 94999E | 97735X & 40994F    | Blue         | 7-**35**  |

This tournament our weakest point was our skills score. Since we did not practice enough between the tournament our driver score was not as high as we normally score. Our skills total was 122, 66 Driver and 56 autonomous. We ranked 4th place total in the skills portion. We also the design award. 

## 2/23/20
Since State Championship is in three weeks, we do not want to make any more changes to the robot and instead we will only focus on practicing to improve our driving and programming routines. We are very happy with our robot and our code and now all we need to do is practice driving and tune all of our movements in the various autonomous routines. 