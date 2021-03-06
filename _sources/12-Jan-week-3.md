# 1/25/22-1/27/22
```{Note}
Due to COVID our school went virtual last week causing us to skip practice on 1/18/22-1/20/22.
And the tournament on 1/22/22 was also rescheduled due to COVID for 2/12/22. So now our next tournament is 2/5/22.
```

## 1/25/22 
### Attendance: &#9745;  Brody, &#9745; Derek, &#9745; Jack
### Goals:
- Continue AWP routine.
- Continue driver pratice.

### Accomplished:
- &#9745; Continue AWP routine.
- &#9745; Continue driver pratice.
- &#9745; Reinforce drive base.

#### How:
- Today Derek reinforced the drive base by adding another cross bar to it. Due to the scoring mechanisms on our robot we only had one cross bar. While adding the second cross brace to the robot Derek also noticed that the spacing on our back lift was incorrect and was forcing the back of the drive base to expand and the front to contract. 

- Jack continued working on the AWP routine and now the robot can consistently score the AWP bonus but still needs tuned to score neutral mobile goals. Tomorrow he will begin working on the elim auton since that auton is also very important.

- Derek continued practicing driving today and will start doing skills runs tomorrow.
#### Why:
- Derek added another cross bar because it is important that our robot is strong enough to be able to get hit by other robots during matches and not break. Adding another cross bar will strengthen us against match defense as well as make the robot less malleable altogether.

- Jack will start on the Elim auton tomorrow because it is very important that we have an autonomous that grabs yellow goals quickly since most matches are determined by who has ownership of the neutral goals after the autonomous phase.


### Plans for next Practice:
- Start Elim auton.
- Continue Driver practice.

```{important}
Last Edited on 1/25/22.
```

## 1/26/22 
### Attendance: &#9745;  Brody, &#9745; Derek, &#9745; Jack
### Goals:
- Start Elim auton.
- Continue Driver practice.

### Accomplished:
- &#9745; Finish Elim auton.
- &#9745; &#9745; Continue Driver practice.

#### How:
- Derek continued practicing driving and has changed the routine slightly. After elevating the first two goals Derek will grab the blue alliance goal and then grab the tall neutral goal. 
 
- Today Jack made the elim auton. It is the same route that our old robot used just finetuned to our new robot. Since our robot is faster than before Jack was able to save 2 seconds on the autonomous bringing the run time down to 4 seconds. This is very good as it will help ensure that we get both goals before the opposing team gets either. 

<iframe width="560" height="315" src="https://www.youtube.com/embed/CXj9izmbvUM" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

#### Why:
- Derek does this because grabbing a goal with the front lift shifts our center of gravity and can cause us to tip. If we grab a goal with the back lift our center of gravity stays at the center of the drive base allowing us to move quickly without tipping.

- Jack finetuned our old autonomous routine because it is the quickest auton for grabbing two neutral goals. He was able to save time by tuning the auton to not overshoot the goals by having the drive base stop before the middle line. This makes the autonomous quicker since it is driving less distance and also will lower the chances of the opposing alliance being able to grab the goal.

### Plans for next Practice:
- Finish AWP routine.
- Continue Driver practice.

```{important}
Last Edited on 1/26/22.
```

## 1/27/22 
### Attendance: &#9744;  Brody, &#9745; Derek, &#9745; Jack
### Goals:
- Finish AWP routine.
- Continue Driver practice.

### Accomplished:
- &#9745; Finish AWP routine.
- &#9745; Continue Driver practice.

#### How:
- Today Jack finished the AWP routine by finetuning the movements that grab the two neutral mobile goals. This auton now scores 3-7 rings between the two alliance goals and then grabs two yellow neutral goals for a maximum total of 61 points. This is a major improvement from the previous auton which could only score 23 points. The main point increase here is that we are now grabbing two neutral goals instead of just one.

<iframe width="560" height="315" src="https://www.youtube.com/embed/1lpFz1eV82Y" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

- Derek continued practicing driving today and is close to scoring a 310 driver score like before. With more practice Derek will get used to the new robot since it is very different from the last build. 
#### Why:
- Jack finetuned the autonomous by tweaking the turning angles as well as the PID + Slew values for each movement. With these constants properly tuned the autonomous is much more consistent than before.
- Our primary goal is for Derek to get back to being able to score 310 points in skills since the scoring method in that routine is the most effective still. 

### Plans for next Practice:
- Begin skills auton
- Continue driver practice.

```{important}
Last Edited on 1/27/22.
```

## Robot Release 2.0
- Today is the last entry before the February 5th PSA competition so below here we will explain everything we are bringing to the tournament. To get a full view of the code we are bringing to the tournament you can visit our github repo [here.](https://github.com/PSASchool/9447H-TippingPoint)
> Since this is a turning point in our season with the new robot we are marking this as our 2.0 release.

```{figure} ././_images/january/robotSide.PNG
---
width: 500
name: robotSide.PNG
---
Side view of our current robot.
```

### Robot Features
    1. 6 motor 280 RPM drive base.
> Most teams in South Carolina either have 2 or 4 motor drive bases so ours being 6 motor will give us more speed as well as more strength so we will be able to fight for goals better than ever before.

    2. 4 bar lift + Pneumatic clamp.
> A fast lift with PID + Slew to make it move efficiently and accurately.

    3. Pneumatic Tilt + Clamp.
> We are able to tilt and clamp onto a goal holding it securely while also being able to score rings on it.

    4. Ring Conveyer Belt.
> With our 2.0 robot release we are now able to score rings on the alliance mobile goal posts. This will give us a major advantage since most teams in South Carolina currently can not score rings at all.

    5. Ring Blockers.
> Our robot has ring blockers to enure we do not get stuck on any rings while driving.

### Code Features
1. Absolute Position Trackign from Odom AND the GPS Sensor.
2. PID and Slew control for all moving mechanisms.
3. Threads and State machines to properly manage every mechanism independently.
4. Pure Pursuit for absolute position based movement during the skills autonomous.

### Auton Routines
1. Full Auton Win Point routine that grabs 2 neutral mobile goals.
2. Elim Auton that grabs 2 neutral mobile goals in 4 seconds.
3. Skills auton.

```{important}
Last Edited on 1/27/22.
```
