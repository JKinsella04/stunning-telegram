# 3/8/22 - 3/10/22
## 3/8/22 
### Attendance: &#9745;  Brody, &#9745; Derek, &#9745; Jack
### Goals:
- Fix back clamp.
- Switch to okapi Units

### Accomplished:
- &#9745; Fix back clamp.
- &#9745; Switch to okapi Units

#### How:
- Today Derek worked on fixing the back clamp because during states, there were many instances where when grabbing the second alliance goal we were unable to hold it properly and score rings effectively. Derek has fixed this issue by manipulating the connection points and the angle at which the pneumatics push the clamp to more efficiently tilt the goal. 

- Jack switched the code to use the okapi units today meaning that instead of inputting encoder values we now can input distances in either the imperial or metric system. We also now can input our acceleration in terms of units/sec^2 and for turns we now work with rad/sec^2 and rad/sec. While this does not exactly increase our accuracy it will majorly improve our readability and ease of use since our auton program lines have become more descriptive than before.

```{code}
BEFORE:
chassis.turn(90, 900, 12000).withTurnTol(5).waitUnitlSettled();
NEW:
chassis.turn(90_deg, 2.2_radps2, 27.6_radps).withTurnTol(1_deg).waitUntilSettled);
```
#### Why:
- Derek spent the day tuning the back clamp because it is very important that we grab the alliance goals properly since scoring rings on the pole will be crucial to winnign matches at CREATE.

- Jack has switched to using the okapi units because in addition to increasing readability it also will uses dimensional analysis at compile time to check the units values. This helps the code run quickly and efficiently.  

### Plans for next Practice:
- Redesign ring hood.


## 3/9/22 
### Attendance: &#9745;  Brody, &#9745; Derek, &#9745; Jack
### Goals:
- Redesign ring hood.

### Accomplished:
- &#9745; Redesign ring hood.

#### How:
- Today Derek completely redesigned the ring hood by using a piece of polycarbonate bent in a semi-circle to guide the rings. The new design also uses standoffs above the polycarbonate to stop any rings from launching upward.

```{figure} ././_images/march/newHood.jpg
---
width: 500px
name: newHood.png
---
A side view of the new ring hood.
```

#### Why:
- We changed the hood to a single piece of polycarbonate because this design is much more efficient at controlling the rings' movement since the semi-circle is just slightly larger than the rings themselves so there is no extra space for them to go off course. The design currently is not scoring 100% of the rings but is slightly better than the previous design meaning with a couple slight changes over tomorrow and these 2 weeks we should be able to create a very consistent ring hood.
### Plans for next Practice:
- Retune autons to use okapi units.
- Test and tune ring hood.




