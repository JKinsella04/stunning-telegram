# 2/15/22-2/17/22
## 2/15/22 
### Attendance: &#9745;  Brody, &#9745; Derek, &#9745; Jack
### Goals:
- Redesign back lift.

### Accomplished:
- &#9745; Redesign back lift.

#### How:
- Today Derek redesigned the back lift to make it more consistent and stronger. The new design also uses two piston as opposed to 3 pistons. This will lower our air consumption and allow us to also allocate another piston to the front clamp to make it stronger as well.

<iframe width="560" height="315" src="https://www.youtube.com/embed/fr6I8mDJP_k" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

<iframe width="560" height="315" src="https://www.youtube.com/embed/UA4QNE6z-Gs" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

#### Why:
- We rebuilt our back lift since our previous design used a lot of air and was not lifting goals consistently. Enemy teams could also steal our goal easily which caused us to lose the advantage in matches. Now with this new clamp we will be able to more consistently score rings.

- With this new design no robot will be able to steal the goal from us because of how the clamp reaches into the bottom of the goal base causing it to have a very strong grip on it.

### Plans for next Practice:
- Strengthen 4 bar.
- Test back lift and tune ring hood.


```{important}
Last Edited on 2/15/22.
```

## 2/16/22 
### Attendance: &#9745;  Brody, &#9745; Derek, &#9745; Jack
### Goals:
- Strengthen 4 bar.
- Test back lift and tune ring hood.

### Accomplished:
- &#9745; Strengthen 4 bar.
- &#9745; Test back lift and tune ring hood.
- &#9745; Active Brake code.

#### How:
- Today Jack added active brake to our driver control code. After the robot stops moving, it gets it current position and uses PID to hold that position. If a robot tries to push us from this position the robot will fight and ensure that we hold that spot. This also has the extra benefit of holding our position in case the platform becomes unbalanced as the robot will not drift down.

- Today we tested and tuned our intake by analyzing slow motion footage of the rings being scored onto the goal and added a half-cut c-channel to help guide the rings even more so then consistently score on the post. This new addition in tandem with the new back clamp now allows us to better score rings onto the alliance goals as intended.

<iframe width="560" height="315" src="https://www.youtube.com/embed/B_v57Ze4Ark" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

- Derek also reinforced the 4 bar today by replacing the standoffs with half-cuts. What this allows us to do is add tension between the bars on both sides to more efficiently lift up the goals.

```{code}c++
if( fabs( leftJoystick ) < 1 && fabs( rightJoystick ) < 1 ){
    lastRot = *rotation; 
    braking = true;
    // If no controller input get current position and set braking to true.
}
if( braking ){ 
    leftJoystick = rightJoystick = drive_PID.set(30,0,0).calculate(lastRot, *rotation);
} // PID from current position to last known position.
```

#### Why:
- Jack added this feature because it is important for our robot to be able to hold its position on the platform even if it becomes unbalanced since this will help Derek when driving in skills and normal matches. The active brake will also help us combat defense from other robots since the opposing robot will not be able to move us.

### Plans for next Practice:
- Build front clamp.

```{important}
Last Edited on 2/16/22.
```
## 2/17/22 
### Attendance: &#9745;  Brody, &#9745; Derek, &#9745; Jack
### Goals:
- Build front clamp.

### Accomplished:
- &#9745; Build front clamp.
- &#9745; Add Kickstand.

#### How:
- Today Derek built the front clamp. Since the clamp is very different from our previous design he had to rebuild the whole front clamp structure. With this new clamp design we have gained 1 inch of larger clamping range as well as a much stronger grip on the goals. This design has a similar grab to the back clamp since it reaches far into the mobile goal base. This will make it very hard for any robot to steal a goal from us.

```{figure} ././_images/february/frontClamp.PNG
---
width: 250px
name: frontClamp.PNG
---
An angled view of our new clamp holding a mobile goal.
```

- Derek also added a kickstand to our robot. Having a kickstand on our robot allows us to start closer to the neutral goals by having the front half of the robot float above the starting line. By starting closer to the goals we will be able to reach them before any other team does.

<iframe width="560" height="315" src="https://www.youtube.com/embed/9CwBLLlmC1U" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

#### Why:
- We rebuilt our front clamp because possessing mobile goals is crucial to winning a match and these new clamp designs ensure that no one will take a goal from us once we grab it.

- Since the new clamps ensure that we never lose a goal the next important step is getting to the goals first. With our fast drive base and the kickstand we will be able to reach the goals before anyone else. These paired with our new clamp designs will allow us to reach the goals first and ensure that no teams steal our goals.
### Plans for next Practice:
- Make 3 new match autons (Left 1/2AWP, Right 1/2AWP, One goal Elim).
- Continue driver practice.


```{important}
Last Edited on 2/17/22.
```