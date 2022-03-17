# 3/15/22 - 3/17/22
## 3/15/22 
### Attendance: &#9744;  Brody, &#9745; Derek, &#9745; Jack
### Goals:
- Build locking clamp prototype.
- Retune middle goal auton and Full AWP.
- Continue driver practice.

### Accomplished:
- &#9745; Build locking clamp prototype.
- &#9745; Retune middle goal auton.
- &#9745; Continue driver practice.

#### How:
- Today Jack tuned the middle goal auton to use the okapi units. He also expanded it to score rings on the goal to accomplish half of the AWP bonus in case we run the autonomous in a qualifier match. He began tuning the full AWP auton but was unable to finish it today.

<iframe width="560" height="315" src="https://www.youtube.com/embed/UrIk4cloqbs" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

- Derek built a prototype of a locking clamp for the Worlds robot. This clamp is more advanced than our current clamp since it uses a halfcut that will lock the clamp making it impossible for another robot to steal a goal from the clamp.

<script src="https://cdn.jsdelivr.net/npm/publicalbum@latest/embed-ui.min.js" async></script>
<div class="pa-gallery-player-widget" style="width:100%; height:480px; display:none;"
  data-link="https://photos.app.goo.gl/32zCVU1ySiFNo2gR6"
  data-title="3/15/22"
  data-description="2 new items added to shared album"
  data-delay="2">
  <object data="https://lh3.googleusercontent.com/usGt1fV-Po-zosjxPcA35lbB9M36Utzx_GxJmbNk0uDpDpf2LdO1oll20_Ch2oHfPWWZ48PWWB-htZ4hCz5dGTcIr-CUdsOjNcaZzCrWqfWCJiMgq-w_3uMoO9fslDLY9eqwrCPJgw=w1920-h1080"></object>
  <object data="https://lh3.googleusercontent.com/aEdaq5Aa1UvOL8gXQBj6JTunQz4IcLX1flbHcmnwkcwIkl-BHnbbOUwqGdS1PN2RfuJ3GywW3B2iCB8ig7ow60c7ZYXkt1nroDY2FUt0D03Q-EUmBvF896GB7GdJEnSaqyit534z9w=w1920-h1080"></object>
</div>


- Derek continued practicing driving and is becoming more consistent at finishing the route before 60 seconds.

#### Why:
- Jack added the AWP bonus to the middle goal auton since there was about 11 seconds left and it will allow us to use this auton during qualifiers and still score the AWP bonus.

- We are going to use a locking clamp for worlds because it will be vital that we ensure no one can steal goals from us since all the robots at worlds will be very competitive. This design uses a 4 bar to lock the bottom bars in place and the only way for it to unlock is if the pneumatic releases and pulls the top bars down.

### Plans for next Practice:
- Finish tuning Full AWP auton and begin tuning skills auton.
- Finish the locking clamp prototype.
- Continue driver practice.

```{important}
Last Edited on 3/15/22.
```

## 3/16/22 
### Attendance: &#9745;  Brody, &#9745; Derek, &#9745; Jack
### Goals:
- Finish tuning Full AWP auton and begin tuning skills auton.
- Finish the locking clamp prototype.
- Continue driver practice.

### Accomplished:
- &#9745; Finish the locking clamp prototype.
- &#9745; Continue driver practice.

#### How:
- Today Jack continued tuning the Full AWP auton but was unable to finish it since getting the long curve movement converted proved to be very complex. He will finish it tomorrow.

- Derek finished building the prototype of the locking clamp and is going to update the CAD of the robot to this exact design. In addition to the front clamp being finished Derek also has finished the CAD of the worlds robot and we will begin building the new robot once we are back from CREATE.

- Derek continued practicing driving today and hit a new personal record of 342.

<iframe width="560" height="315" src="https://www.youtube.com/embed/0S-x855mgXI" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

#### Why:
- Since we will only have a month to rebuild and practice for worlds, getting the CAD to be accurate and complete now is very important so when Derek starts building the new robot he can finish it quickly.

- Since the last couple tournaments we have been unable to score over 300 points in driver skills, Derek has been practicing driving every day to ensure that at CREATE we score over 300 points. 

### Plans for next Practice:
- Finish Full AWP routine and start tuning skills auton.
- Continue driver practice.

```{important}
Last Edited on 3/16/22.
```

## Robot Release 3.0
- Since this is the last entry before we submit the notebook for the World Championship we are making a release for our soon to be worlds robot.

```{figure} ././_images/march/worldRobot.PNG
---
width: 400
name: 
---
A front view of our worlds robot.
```
```{figure} ././_images/march/worldRobotBack.PNG
---
width: 400
name: 
---
A back view of our worlds robot.
```
```{figure} ././_images/march/worldRobotAngle.PNG
---
width: 400
name: 
---
An angled view of our worlds robot.
```

### Robot Features
    1. 6 motor 600 RPM drive base with 3.25" wheels.
> With this new high speed drive base we have a maximum speed of 8.51 ft/s which will give us an advantage over the majority of teams since to date the fastest robot revealed has a maximum speed of 7.2 ft/s.

    2. 1 Motor 4 bar lift + Pneumatic Locking clamp.
> A fast lift with PID + Slew to make it move efficiently and accurately and a locking clamp that will only release a goal when we retract the pneumatic piston.

    3. Pneumatic Tilt + Clamp.
> A pneumatic tilter that keeps a very strong grip on the goals preventing other teams from stealing our goal.

    4. 1 Motor 600 RPPM Ring Conveyer Belt.
> A fast intake to quickly and reliably score rings on the alliance goals.

    5. Ring Blockers.
> Esnure we do not get stuck on any rings while driving.

    6. Kickstand.
> Allows us to start closer to the neutral goals by holding half of our robot over the starting line to get an advantage over the other teams.

### Code Features
1. Absolute Position Tracking from Odom AND the GPS Sensor.
2. PID and Slew control for all moving mechanisms.
3. Okapi Units for verbose code that can accept many different units.
4. Threads and State machines to properly manage every mechanism independently.
5. Pure Pursuit for absolute position based movement.

### Auton Routines
1. Full Auton Win Point routine that grabs 1 neutral mobile goal.
2. 3 1/2 AWP routines that grab 1 neutral goal and score half of the AWP bonus.
3. Elim Auton that grabs 2 neutral mobile goals in 3 seconds.
4. 550-600 point Skills auton.

```{important}
Last Edited on 3/17/22.
```