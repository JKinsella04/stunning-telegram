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

#### Why:
- Derek created created this simple mechanism because we decided that being able to achieve the AWP will be crucial to our success this season.
- We launch the third ring into the goal because adding more pieces to either lift would be redundant when placing the ring ontop of the clamp scorest the ring very well.
- Since swapping to a double-acting piston did not solve the problem completely, we will start tomorrow off by changing the base point the piston is secured onto the robot. This should help so it has a better movement profile since currently the piston lacks the proper positioning to be able to extend.
- Jack added this feature because to be able to complete the AWP by ourselves we will need to move quickly from one side of the field to the other.
### Plans for next Practice:
- Fix the draggers.

```{important}
Last Edited on 9/28/21.
```