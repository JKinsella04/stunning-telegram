---
jupytext:
  cell_metadata_filter: -all
  formats: md:myst
  text_representation: {extension: .md, format_name: myst, format_version: 0.12, jupytext_version: 1.6.0}
kernelspec: {display_name: Python 3, language: python, name: python3}
---
# July 2020 Progress Entries
## 7/11/20
### Attendance: &#9744; Brody, &#9744; Derek, &#9744; Dylan, &#9744; Ian, &#9745; Jack
Created the buttons for the third tab on the GUI. The third tab is the Reset page, it has 4 buttons that all reset different sensors or motors. There is the “Reset IMUs” which resets the three inertial sensors, “Reset Odom” which resets the tracking wheels, “Reset Vision” which resets the vision sensor, and finally “Reset Chassis” which resets the drive base motors. This page is to help debug and will not be needed to be used in competitions since all the motors and sensors get reset at the beginning of the program so this will mainly be used to debug the robot during practice.

<img src="././_images/7-July/7-11-20/reset.jpg" alt="reset.jpg" style="width: 400px;"/>


## 7/24/20
### Attendance: &#9744; Brody, &#9744; Derek, &#9744; Dylan, &#9744; Ian, &#9745; Jack
We remade the loading screen and added our alliance logos above our team number. We also optimized the screen by using less objects. Before we had the background galaxy image and then another image that was “9447H” but now we put everything on one image and display that instead. This is better than before because we are using less memory by having less objects.
We finished the CAD model today so we can start building in the future. The odometry tracking wheels were changed to be stronger, and the robot's height was increased so we can get closer to the top of the goals. Nothing should be affected by this change as the intakes were not moved.


%%HTML
<div align="middle">
<video width="80%" controls>
      <source src="././_images/7-July/7-24-20/loadingscreen.mp4" type="video/mp4">
</video></div>


## 7/25/20
### Attendance: &#9744; Brody, &#9745; Derek, &#9744; Dylan, &#9744; Ian, &#9744; Jack
Today we started to build the front intakes, they are generally the same shape as the CAD model but we added extra support to the insides to reduce friction. Currently the right side intake spins a bit slower than the left and we are working to fix it. One other improvement that might come in the future is replacing the standoff chain tensioner with spacers to reduce friction on the chain. 

### Pictures of Changes
<img src="././_images/7-July/7-25-20/intakeSideViewBack.JPG" alt="intakeSideViewBack.JPG" style="width: 200px;"/>
<img src="././_images/7-July/7-25-20/intakeSideViewFront.JPG" alt="intakeSideViewFront.JPG" style="width: 200px;"/>
<img src="././_images/7-July/7-25-20/intakeTopView.JPG" alt="intakeTopView.JPG" style="width: 200px;"/>


## 7/26/20
### Attendance: &#9745; Brody, &#9745; Derek, &#9745; Dylan, &#9745; Ian, &#9745; Jack
We completed building the middle intakes and indexer system today. There were not many problems when building it as we had already designed it in cad. Because we now have this piece of the robot we have started to test out our driver control programs. Initially the motors were reversed but after we fixed that, the intakes pick up balls very quickly. We may slow this down the in the future but for now it seems to be working well.

### Middle Intakes and Indexer
<img src="././_images/7-July/7-26-20/towerFrontView.JPG" alt="towerFrontView.JPG" style="width: 200px;"/>
<img src="././_images/7-July/7-26-20/towerLeftSideView.JPG" alt="towerLeftSideView.JPG" style="width: 150px; -webkit-transform: rotate(270deg);"/>
<img src="././_images/7-July/7-26-20/towerRightSideView.JPG" alt="towerRightSideView.JPG" style="width: 200px;"/>
<img src="././_images/7-July/7-26-20/towerTopView.JPG" alt="towerTopView.JPG" style="width: 200px;"/>