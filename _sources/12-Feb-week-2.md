# 2/8/22-2/10/22
## 2/8/22 
### Attendance: &#9744;  Brody, &#9745; Derek, &#9745; Jack
### Goals:
- Improve match autons.
- Continue Driver practice.

### Accomplished:
- &#9745; Continue Driver practice.
- &#9745; Improve Elim auton.

#### How:
- Today Derek continued driver practice and is more consistently getting the 310 skills run completed. Since he was unable to achieve it at the last tournament he is focusing even harder to ensure that this weekend he gets it.
- Jack improved the elim auton by using the rest of the 15 seconds to better manuever the neutral goals so driving is easier for Derek. Now the robot grabs the smaller neutral goal with the front lift instead of the back lift and the robot drops the tall neutral goal into the corner and then finishes by grabbing the alliance goal with the back lift.

<iframe width="560" height="315" src="https://www.youtube.com/embed/8gFYpVJGHPw" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

#### Why:
- This improves the autonomous because it gives Derek a much easier starting position once the driver phase starts. Before he would have to drop both goals and grab the small neutral goal and the alliance goal. Now Derek can just start driving and scoring rings onto the goal since the robot will start with the goals he needs to hold.

### Plans for next Practice:
- Improve AWP auton. 
- Improve skills auton.
- Continue Driver practice.


```{important}
Last Edited on 2/8/22.
```

## 2/9/22 
### Attendance: &#9744;  Brody, &#9745; Derek, &#9745; Jack
### Goals:
- Improve AWP auton. 
- Improve skills auton.
- Continue Driver practice.

### Accomplished:
- &#9745; Improve AWP auton. 
- &#9745; Design new skills route.
- &#9745; Continue Driver practice.

#### How:
- Today Jack improved the AWP routine by fixing the PID constants for a couple turns so the robot turns more accurately throughout the run as well as changing how it grabs the two neutral mobile goals to mimic the new elim auton. Now the robot grabs the smaller neutral goal with the front and the tall neutral goal with the back. 

- Jack and Derek designed a new auton skills routine today that will score 200 points. We accomplish this by elevating 5 goals onto the platforms. We will start by scoring two on the opposing platform and then will score 3 more on the second platform. We are pursuing this autonomous as it will be less complicated then if we try to replicate the driver skills run and it will also allow us to build upon it for the state championship.

- Derek set a new record for himself with a driver score of 336 today in practice. The extra points from the planned 310 are from the rings that he picks up while driving through the field. 

<iframe width="560" height="315" src="https://www.youtube.com/embed/m3LACAv-gm8" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

#### Why:
- Jack changed the way the AWP routine grabs the two neutral goals because it will give Derek a better starting position and allow him to quickly begin scoring points.

- We redesigned the skills routine because this new routine should be easier to achieve as well as expand upon later since there will only be two goals left to elevate for a total of 280 points.

- Derek is continuing to improve every practice and will be more than ready for the tournament this weekend.

### Plans for next Practice:
- Tune intake and intake hood.
- Strengthen 4 bar.
- Continue driver practice.
- Improve skills auton.

```{important}
Last Edited on 2/9/22.
```

## Robot Release 2.1
- Today is the last entry before the February 12th Polaris Tech competition so below here we will explain everything we are bringing to the tournament. To get a full view of the code we are bringing to the tournament you can visit our github repo [here.](https://github.com/PSASchool/9447H-TippingPoint)
> Since last week we released the 2.0 version of our robot and code we are marking this release as 2.1 since only minor changes have happened through this week.

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
1. Absolute Position Tracking from Odom AND the GPS Sensor.
2. PID and Slew control for all moving mechanisms.
3. Threads and State machines to properly manage every mechanism independently.
4. Pure Pursuit for absolute position based movement.

### Auton Routines
1. Full Auton Win Point routine that grabs 2 neutral mobile goals.
2. Elim Auton that grabs 2 neutral mobile goals in 4 seconds.
3. 200 point Skills auton.