# 9/28/21 - 9/30/21
## 9/28/21
### Attendance: &#9745; Brody, &#9745; Derek, &#9745; Jack
### Goals:
- Create the Preload scoring mechanisms.
- Fix the dragger mechanism.
### Acomplished:
- &#9745; Create Preload scoring mechanisms.
#### How:
- Since our robot does not have ability to manipulate rings we have to add a special mechanism to allow for us to score our three preload rings during the autonomous phase to win the AWP. 
- Derek added two l-channels on top of the small mobile goal lift so when we drive into the goal it drops two rings into the goal. 
- To score the third ring we place it on top of the clamp's pneumatic that is on the 4 bar, so when we toggle the pneumatic it launches the ring forward into the second goal that we need to score into for the AWP.
- We swapped out the pneumatic that toggles the dragger from a single-acting to a double-acting piston so both extending and retracting are powered, but this still is not enough to make the dragger function properly.
- Jack added a new feature to our autonmous movment called two angle correction. Previously the robot would correct its angle to the requested while moving laterally. Now though we can tell the robot to correct to one angle and then correct to a second angle allowing us to create more advanced movements that allow the robot to move around obstacles more efficiently.

<iframe width="560" height="315" src="https://www.youtube.com/embed/T3CEADUJybk" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

<iframe width="560" height="315" src="https://www.youtube.com/embed/i2RTYuKQQCM" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

<iframe width="560" height="315" src="https://www.youtube.com/embed/eax42Kk5JLk" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

#### Why:
- Derek created created this simple mechanism because we decided that being able to achieve the AWP will be crucial to our success this season.
- We launch the third ring into the goal because adding more pieces to either lift would be redundant when placing the ring ontop of the clamp scorest the ring very well.
- Since swapping to a double-acting piston did not solve the problem completely, we will start tomorrow off by changing the base point the piston is secured onto the robot. This should help so it has a better movement profile since currently the piston lacks the proper positioning to be able to extend.
- Jack added this feature because to be able to complete the AWP by ourselves we will need to move quickly from one side of the field to the other. Below is the addition to ChassisState::DRIVE.
```c++
if(turnComplete && target.thetaTwo != nullptr){
    turn_output = turn_PID.calculate(*target.thetaTwo, *theta);
}else {
    turn_output = turn_PID.calculate(target.theta, *theta);
}if(fabs(turn_PID.getError()) <= turn_tol){
    turnComplete = true;
    turnSlew.reset();
}
```
### Plans for next Practice:
- Fix the draggers.

```{important}
Last Edited on 9/28/21.
```
## 9/29/21
### Attendance: &#9745; Brody, &#9745; Derek, &#9745; Jack
### Goals:
- Fix the draggers.
### Accomplished:
- &#9745; Increase drive base clearance.
- &#9745; Add ring blockers.
- &#9745; Fix the draggers.
#### How:
- With the added weight of the lifts on the robot, we were unable to drive up the platforms since our drive base contacts the screws on the platform. To solve this problem we cut the c-channels on the drive base that touch the platform so they no longer contact it.
- To help with the autonmous and driving we added two polycarbonate pieces in front of the wheels so the rings get blocked and cannot get under the wheels. 
- While testing different positions with the draggers Derek and Jack determined that currently the only way to make the draggers work is if we use double acting pistons instead of single acting, but we only have one more double acting piston so we would be limited to only having one dragger. From this we are putting them on the backlog and will not worry much about them since we do not need them to perform well.

<script src="https://cdn.jsdelivr.net/npm/publicalbum@latest/embed-ui.min.js" async></script>
<div class="pa-gallery-player-widget" style="width:100%; height:480px; display:none;"
  data-link="https://photos.app.goo.gl/rMWvvQfaq98HZe8HA"
  data-title="9/29/21"
  data-description="2 new photos added to shared album"
  data-delay="2">
  <object data="https://lh3.googleusercontent.com/j3uDFU0hlnigUAWUkmKHI9XPc7SR_8TkQSg-gEphNEU-HnwDvVtRCVh3VQPvnXVrnPaUWYJTxmhQCoRbTPfxu8VkZCQLzAco-L2YS2fnVkM84hx58y5jHR8u5g70PwoQH_LyTLXWEg=w1920-h1080"></object>
  <object data="https://lh3.googleusercontent.com/7KhCd3piQEge11DFcDXauEQy-tMo1Z3ZMvv8h9YWiejGeqv1NChu3yMfPUAxJ_mWsAabqB3fAbfV0L5TJHQrTSvZuXhyZnvakK-NUWcTWW8sV5UFdLbTQlQbGRrvtQx2TBlYUO0dsA=w1920-h1080"></object>
</div>

#### Why:
- Since we do not have enough double acting pistons we are putting the draggers on hiatus because we do not want to waste a lot of time for a mechanism that will only be used during one 15 second autonous routine. Instead of grabbing two mobile goals and dragging them, we will grab one and score it in our zone and then go back to grab a second goal. 
- Once we get another double acting piston, we will recontinue the draggers because they will be very useful in securing the autonomous bonus in  elimination matches.

### Plans for next Practice:
- Secure the 4 bar tower.
- Ensure the robot is able to pass inspection.
- Begin working on the AWP auton routine.