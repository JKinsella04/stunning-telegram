# 2/22/22-2/24/22
## 2/22/22 
### Attendance: &#9745;  Brody, &#9745; Derek, &#9745; Jack
### Goals:
- Make 3 new autons (Left 1/2AWP, Right 1/2AWP, One goal Elim).
- Continue driver practice.

### Accomplished:
- &#9745; Make 3 new autons (Left 1/2AWP, Right 1/2AWP, One goal Elim).
- &#9745; Continue driver practice.
- &#9745; Change controller mapping.

#### How:
- Today Jack remapped the controller to make it easier for Derek to toggle the front and back clamps. The new controls have the front clamp toggle its clamp just with R1 and toggle the back clamp with R2. This is different from the previous controls in which R1 and R2 were used to toggle between the two states for the front clamp and the UP arrow and X were used to toggle the back lift.

```{code}
void FrontLift::updateClamp(){ // Update front clamp state if new state inputted.
    if( clampState != lastClampState ) {
        frontClamp.set_value( clampState );
        lastClampState = clampState;
    }
}

void BackLift::updateClamp(){ // Update back clamp state if new state inputted.
    if( clampState != lastClampState ) {
        backClamp.set_value( clampState);
        pros::delay( delay ); // Custom delay from user input. Default 100ms.
        conveyer::spin(600); // Spin intake for ring scoring.
        lastClampState = clampState;
    }
}
```
- Jack also programmed the routes for the new autons. These new autons all will go for a neutral mobile goal first and then after grabbing the goal they will score rings on the nearest alliance goal for the AWP bonus.

- Derek continued practicing driving today by testing out these new controls since he will have to get accustomed to them quickly.

#### Why:
- Jack remapped the controller buttons because this will give derek much more control when driving since before he had to move his thumbs off the joysticks to toggle the back lift. Now with the backlift on R2 he will be able to move and toggle the back liftt's state.

- We are making 1/2 AWP bonus routines because at state most teams will probably be able to score half of the AWP bonus. Since teams will be able to score half of the AWP that means that we can now grab neutral mobile goals at the beginning of the matches for qualifiers which will help us win more matches.

- Since the controls changed Derek had to get used to the new controls before practicing skills again since he needs to rebuild his muscle memory.

### Plans for next Practice:
- Finish Left + Right + Full AWP autons.
- Continue driver practice.
- Practice judges interview.


```{important}
Last Edited on 2/22/22.
```

## 2/23/22 
### Attendance: &#9745;  Brody, &#9745; Derek, &#9745; Jack
### Goals:
- Finish Left + Right + Full AWP autons.
- Continue driver practice.
- Practice judges interview.

### Accomplished:
- &#9745; Finish Left + Right + Full AWP autons.
- &#9745; Continue driver practice.
- &#9745; Prepare for judges interview.

#### How:
- Today Jack worked on tuning the three AWP match autons. We have three different autonomous programs for the AWP in case our teammate can score half of the AWP bonus themselves. The two new autons grab a neutral mobile goal first and then score points on the closest alliance goal.

<iframe width="560" height="315" src="https://www.youtube.com/embed/heiZHq42zrU" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

<iframe width="560" height="315" src="https://www.youtube.com/embed/qHcCD9EXvqc" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

- Derek started running full driver skills runs today and scored 334 points on his second run. With the recent changes to the lift, clamps and button mapping, it should be easier for Derek to score over 310 points in driver skills.

- Instead of running through mock judge interviews like we originally planned, we instead all took time to reflect on the judge interview rubric and practice properly answering the rubric. Tomorrow we will begin running through mock judge interviews to get ready for our CREATE interview as well as for states.
#### Why:
- Jack tuned the AWP autons today because it is very important that we will be able to get the AWP bonus every match since it will be impossible to get first without getting the AWP bonus. Tomorrow he will work on the elim bracket autons that just focus on grabbing the neutral mobile goals. Which will be vital for winning the elimination bracket.

- Tomorrow Jack will finetune the turns of both autons as they approach the alliance goals since the turns currently overshoot the goals too much which can cause inaccuracy and possibly not score the AWP bonus.

- Now that Derek is comfortable with the new button mapping, he will continue practicing driver skills runs as well as general driving practice to get ready for states.

- We are practicing our judges' interview because just like every other part of robotics we need to practice and improve on it. By practicing the interview we will be more capable of explaining the most important features our team has developed through this season and how we have evolved over the season.
### Plans for next Practice:
- Finetune Left + Right AWP autons.
- Create Elim Bracket Autons (Old Elim + Middle Goal).
- Continue driver practice.
- Practice judges interview.

```{important}
Last Edited on 2/23/22.
```

## 2/24/22 
### Attendance: &#9744;  Brody, &#9745; Derek, &#9744; Jack
### Goals:
- Continue driver practice.

### Accomplished:
- &#9745; Continue driver practice.
- &#9745; Smooth air release for back lift.

#### How:
- Unexpectedly Brody and Jack were unable to go to practice today so instead of working on the judge interview and the autonomous Derek spent the entire practice driving.

- Derek also added speed controllers to the pneumatics that power our back lift so when we disengage the pistons the mobile goal will be dropped slowly so no rings get descored from it falling.

<iframe width="560" height="315" src="https://www.youtube.com/embed/645WDYbrap4" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

- Derek scrimmaged against our sister team 9447N. Practicing normal matches is also very important since the majority of his driving will be in the match format.
#### Why:
- Since Brody and Jack were unable to make it to practice Derek was able to focus on his driving today allowing him time to improve his driving skill. Because of this the initial goals for today will be rescheduled to next Tuesday.

- Adding the speed controller to the penumatics is very important since before when we would drop alliance mobile goals with the backlift we would lose 1-3 rings depending on how many were scored on the post. Having the slower back lift will be very useful since we will no longer lose rings after scoring them.

### Plans for next Practice:
- Finetune Left + Right AWP autons.
- Create Elim Bracket Autons (Old Elim + Middle Goal).
- Continue driver practice.
- Practice judges interview.