# 12/7/21-12/9/21
## 12/7/21
### Attendance: &#9745; Brody, &#9745; Derek, &#9745; Jack
### Goals:
- Test central gear box of drive base works.
- Rebuild Tipping Point Field.
- Implement Pure Pursuit.

### Accomplished:
- &#9745; Test central gear box of drive base works.
- &#9745; Rebuild Tipping Point Field.
- &#9745; Implement Pure Pursuit. 

#### How:
- Jack implemented pure pursuit into the code today by combining bezier curve generation and the point to point code we already had. From the bezier curve generation we can get a smooth curve with either 1 or 2 control points that will form the curve to the final point. We use this in tandem with the point to point to accurately move along the curve in very small increments. 
- We had to bring our Tipping Point Field to the tournament last weekend so the first thing we had to do today was rebuild the field.
- Today Derek wanted to make sure his drive base design from CAD worked properly, so he replicated the center part where all three drive base motors will connect to make sure the spacing of the 84 tooth gears was correct.

<iframe width="560" height="315" src="https://www.youtube.com/embed/hVbQ1-pnL5w" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>


<script src="https://cdn.jsdelivr.net/npm/publicalbum@latest/embed-ui.min.js" async></script>
<div class="pa-gallery-player-widget" style="width:100%; height:480px; display:none;"
  data-link="https://photos.app.goo.gl/g17PCe8UAXKrdnp19"
  data-title="12/7/21"
  data-description="2 new items added to shared album"
  data-delay="2">
  <object data="https://lh3.googleusercontent.com/YYr_lCXIco0XborbedL3BYCXNASEPOlUta4LaKnWilojDABmImuZUXbwd2KYECISeeMCpuVwcKpBm3sFZ92Xg184z4-NeGl2i4rSr8XwmC1uxwTJRU8q7GrD9ht1ml6nnx_69VKYpA=w1920-h1080"></object>
  <object data="https://lh3.googleusercontent.com/HprnI5wEvkEoMkpVHcvDvOPlMQHWsAdZKtW0NdqXpv54kAlUbd71xi7u9D4JOhM8LIVzTpC-E7MYmdvQJTLIswGeFOjeo9Tklq2eyRdkwz44Gqp8WjzKFr-LQOIu9EIGsvDDVCpsHQ=w1920-h1080"></object>
</div>


#### Why:
- Since our skills auton failed at the last tournament and because of how long it took to create Jack has implemented a new algorithm to allow for consistent autonomous movement. This new movement will be more accurate since we will be using absolute position as opposed to relative and following a bezier curve will be more accurate then creating a path by hand.
- The spacing Derek designed works so no changes are required and once we create a full parts list and order the new parts we will be able to begin building the new robot. Until we get new parts though, we will build any mechanisms we can with our current parts. 

### Plans for next Practice:
- Continue the CAD of the new robot.

```{important}
Last Edited on 12/7/21.
```

## 12/8/21
### Attendance: &#9744; Brody, &#9745; Derek, &#9744; Jack
### Goals:
- Continue the CAD of the new robot.
### Accomplished;
- &#9745; Continue the CAD of the new robot.
#### How:
- Derek continued desiging the robot and has mostly finished the back mobile goal lift. Since the robot will have a conveyer belt for rings, our back lift has to be entirely powered by pneumatics sine we already use 8 motors on our robot. Our new back lift design is very different from our old robot since now it uses two pistons to tilt backward and a third one to clamp onto the goal.
#### Why:
- Derek designed the new back lift like thise so we can efficently grab and position the alliance goals to be able to score rings from the conveyer belt onto the post. With the new design the robot will have a secure grip on the alliance goal to not allow other robots to steal the goal from us while also allowing us to park and manuever with it easily.

```{figure} ././_images/december/backlift.png
---
width: 1000px
name: backlift.png
---
A view of the backlift
```

### Plans for next Practice:
- Continue the CAD of the new robot.

## 12/9/21
### Attendance: &#9744; Brody, &#9745; Derek, &#9744; Jack
### Goals:
- Contine the CAD of the new robot.

### Accomplished;
- &#9745; Continue the CAD of the new robot.

#### How:
- Derek is nearly finished with the new robot design. The final part to complete is the front clamp's piston placement. The conveyer belt placement is not exact but is designed to be easily tuned when building the robot.
- New robot features
    1. 6 motor drive
    2. 1 motor lift + 1 piston clamp
    3. 1 motor ring conveyer
    4. 2 piston tilter + 1 piston clamp
- This robot utilizes 8 motors and 4 pneumatic pistons. We can possess 2 mobile goals at a time and score rings on the alliance goal posts.
```{figure} ././_images/december/newRobot.PNG
---
width: 1000px
name: newRobot.png
---
```

#### Why:
- Since designing the precise angle and placement of the conveyer belt is very difficult in CAD, Derek instead designed the rest of the robot to allow the conveyer belt a lot of space to be easily fintuned when we physically build the robot so we can test to find the best spot for it.
### Plans for next Practice:
- Finalize front lift in CAD
- Begin building components of the new robot.
