# 11/23/21-11/25/21
## 11/23/21
### Attendance: &#9745; Brody, &#9745; Derek, &#9745; Jack
### Goals:
- Continue skills auton.
- Continue driver practice.

### Accomplished:
- &#9745; Continue skills auton.
- &#9745; Continue driver practice.

#### How:
- Today Jack continued working on the skills auton and has gotten the 4th goal scored as well as picked up the 5th and 6th goals. After picking them up the robot will score the two on the platform with the three other goals already elevated. After scoring those two goal we will have a skills score total of 220 leaving only the 7th goal and parking left to accomplish.
- Derek continued practicing driving by running the skills runs a couple more times and also getting some basic driver practice in to hone in his elevating skills.
#### Why:
- Derek spent time just elevating goals instead of running the skills run over and over because it is important for Derek to practice just specific motions so he can become more efficient in the movements he makes while driving in both skills and normal matches.
- Jack continued working on the auton since today is the only practice day we have this week.

### Plans for next Practice;
- Continue skills auton.
- Continue driver practice.



## Robot Release 1.1
- Today is the last entry before the December 4th JP2 competition so below here will explain everything we are bringing to the tournament.
> This release is 1.1 because not much has changed from our last tournament other than minor building improvements and a new auton routine.

### Robot Features
1. 333 RPM drive base.
> Based off scouting from the JL Mann tournament and general knowledge we know we will be the fastest robot at this next tournament.

2. 4 bar lift + Pneumatic clamp.
> A fast lift with PID + Slew to make it move efficiently and accurately.

3. Small mobile goal lift.
> Can carry a mobile goal the entire match while fighting over other goals with the 4bar lift.

4. Angled c-channels
> With our two 45 degree c-channels we will be able to tip the enemy's platform if goals are elevated on it.

5. Ring blockers
> We updated our ring blockers to allow us to be able to park as well as never get stuck in rings.

### Code Features
1. Absolute Position Trackign from Odom AND the GPS Sensor.
2. PID and Slew control for all moving mechanisms.
3. Threads and State machines to properly manage every mechanism independently.

### Auton Routines
1. Full Auton Win Point routine that also grabs a neutral mobile goal.
2. Elim Auton that grabs 2 neutral mobile goals in 6 seconds.
3. Skills auton that can score up to 290 points.

```{important}
Last Edited on 11/23/21.
```