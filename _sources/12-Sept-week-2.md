# 9/7/21 - 9/9/21
## 9/7/21
### Attendance: &#9745; Brody, &#9745; Derek, &#9745; Jack
### Goals:
- Begin building the lifts.
- Begin desigining the code structure.

### Accomplished:
- &#9745; Begin building the lifts.
- &#9745; Begin desiging the code structure.

#### How:
- Derek and Brody added the supports to the drive base that will hold the lifts. 
- Jack began working on the code by creating classes and namespaces for the required actions of the robot. This includes the Chassis, Lifts, GUI, Auton Selector, Odometry, Intakes, Mobile Goals, and even frequently used equations in the code such as PID, and Slew. 
- Jack also implemented finite state machines. We are using state machines for mechanisms such as the the chassis and the lifts.
- Jack plans to create threads for each class so we can run each mechanism on its own while being able to still command the ther mechanisms.
```c++
class Chassis{};
enum class ChassisState{
    DRIVE, POINT, TURN, OPCONTROL, BALANCE, IDLE
};
class Lift{};
enum class LiftState{
    ZERO, UP, IDLE
};
class Display{};
class Auton{};
class Odometry{};
namespace intake{};
namespace mobileGoal{};
namespace macro{
    class Slew{};
    class PID{};
}
```
```{admonition} Github Repository!
Here is a link to our [Github Repo](https://github.com/PSASchool/9447H-TippingPoint).
```
#### Why:
- By using a state machine we are able to ensure that the robot will always be in one of our defined states, and that by changing it's state we are able to tell it to do specific actions. This helps our robot be more consistent as well as make our code easier to read.
- Using threads for each class is important because it allows us to run asynchronously so we can drive somewhere while also moving the lift if needed. This will also allow the GUI to continue running throughout the entire program unlike last year where after the init phase our GUI would become frozen.
### Plans for next Practice:
- Continue building the lifts.
- Design and integrate the GUI.

```{important}
Last Edited on 9/7/21.
```

## 9/8/21
### Attendance: &#9745; Brody, &#9745; Derek, &#9745; Jack
### Goals:
- Continue building the lifts.
- Design and integrate the GUI.
### Accomplished:
- &#9745; Continue building the lifts.
- &#9745; Design and integrate the GUI.

#### How:
- Derek and Brody continued building the lifts by making the clamp that will go on the end of the lift.
- The focus of our GUI this year is all about being simple, informative and looking nice. To make it simple we have chosen to go for an auton selector where we have buttons that each correlate to an specific auton routine. 
- When an auton routine is selected a photo on the right of the screen is updated showing off the path and as well the name of the selected auton is printed on the top of the screen.
- The final aspect of our GUI is the look of it. This is just as important as everything else because we wanted something that would be nice to look at. To do this we used a photo from this [website](https://destinyemblemwallpapers.com). Jack also added a GIF to the GUI that Derek created of our team logo. 

<iframe width="560" height="315" src="https://www.youtube.com/embed/CETrG6-x1uw" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

#### Why:
- Since we have not received the needed HS axles for the robot we are unable to continue making the base of the lifts and have shifted over to the other parts of the lifts in the meantine.
- We wanted to accomplish these three goals because these were the main aspects that our previous GUI lacked. Our old GUI was very complicated because you had to press buttons in an exact order or else it would not work unlike now where it does not matter what order the buttons are pressed.
- Our old GUI was also lacking in information since it was unable to show any data and also did not explicitly show what auton was chosen, but now the GUI prints the name and a photo of the path.
- The Change Up GUI was slow and ugly but now we have a fast, and elegant GUI that anyone could use. 
### Plans for next Practice:
- Build the pneumatic clamp and pneumatic grabbers.

```{important}
Last Edited on 9/8/21.
```

## 9/9/21
### Attendance: &#9745; Brody, &#9745; Derek, &#9745; Jack
### Goals:
- Finish the pneumatic clamp and build the pneumatic grabbers.

### Accomplished:
- &#9745; Build the pneumatic clamp and pneumatic grabbers.

### How:
- Today Derek finished building the pneumatic clamp we began building yesterday. He also built the pneumatic grabbers which will be used during the auton phase to grab multiple mobile goals quickly.
- The pneumatic clamp will be attached to the 4bar and will be used to clamp onto mobile goals and place them onto the platform without having to drive up onto the platform.

<iframe width="560" height="315" src="https://www.youtube.com/embed/CSSgKQJZfv0" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

<iframe width="560" height="315" src="https://www.youtube.com/embed/naGsXneXLC8?start=10" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

### Why:
- We built these two mechanisms because we are still waiting for the HS axles and other parts to arrive. S while we cannot connect the clamp to the robot yet we have built it and tuned the pneumatics firing range so it works how we want.
- We need the pneumatic grabbers because during the autonomous phase we need to be able to drive to the middle of the field and grab as many mobile goals as possible to make sure we can win the autonomous phase. With our pneumatic grabbers we will be able to grab two scoring us 40 points.
### Plans for next Practice:
- Continue building the lifts.
- Code all class member functions.

```{important}
Last Edited on 9/9/21.
```