---
jupytext:
  cell_metadata_filter: -all
  formats: md:myst
  text_representation: {extension: .md, format_name: myst, format_version: 0.12, jupytext_version: 1.6.0}
kernelspec: {display_name: Python 3, language: python, name: python3}
---

# September 2020 Progress Entries
## 9/1/20
### Attendance: &#9745; Brody, &#9745; Derek, &#9745; Dylan, &#9745; Ian, &#9745; Jack
Today we spent the day ensuring the integrity of every part of the robot. We spent a whole day on this because it is very important that the robot does not have any screws missing or parts about to fall off. Through this integrity check we decided that the drive base was not secure enough and added a new brace going accross the drive base at the bottom. The brace is a 5 long c-channel. Other than this addition to the drive base, no other problems where identified during the integrity check

<img src="././_images/9-September/9-1-20/driveBaseBracing.jpg" alt="driveBaseBracing.jpg" style="width: 300px;"/>

## 9/8/20
### Attendance: &#9745; Brody, &#9745; Derek, &#9745; Dylan, &#9745; Ian, &#9745; Jack

We created more member functions of the Intake class since we realized we needed more control over our intakes. We realized that we wanted to be able to control the intakes and each set of rollers separetely during the autonomous, so we had to create more member functions so we could actually control them since currently we could only control all of them in one member function.

```cpp
    /*
    Sets intakes to 0 RPM.
    */
    void intakeStop();

	/*
    Spins indexer for the given amount of encoder counts in RPM.

    @param ecount encoder counts
    @param speed rpm
    */
    void indexerSpin(int ecount, int speed);

    /*
    Sets indexer to 0 RPM.
    */
    void indexerStop();

    /*
    Spins middle intake at given RPM.
    @param speed RPM
    */
    void middleSpin(int speed);


    /*
    Spins middleIntake for the vien amount of encoder counts in RPM.
    @param ecount encoder counts
    @param speed rpm
    */
    void middleSpin(int ecount, int speed);

    /*
    Sets middleIntake to 0 RPM. 
    */
    void middleStop();

    /*
    Runs the intakes for driver control.
    */
    void runIntakes();
```

## 9/15/20
### Attendance: &#9745; Brody, &#9745; Derek, &#9745; Dylan, &#9745; Ian, &#9745; Jack
Today we worked on finetuning our new intake functions. We now have the ability to input the precise rpm that we want the motors to spin at and the ability to control each motor independently of the others. Originally we had added a delay in every intake movement but this caused problems with slowing down everything since it kept on making the robot stop constantly. We now have it where the are no delays and they spin until they are told to stop. We also created more functions, so we can either enable the intakes to spin until stopped or to spin to a set rotation. 

```cpp
void Intake::intakeSpin(int speed){
  leftIntake.move(speed);
  rightIntake.move(speed);
}

void Intake::intakeSpin(double ecount, int speed){
  leftIntake.move_relative(ecount, speed);
  pros::delay(50);
  rightIntake.move_relative(ecount, speed);
}
```

## 9/22/20
### Attendance: &#9745; Brody, &#9745; Derek, &#9745; Dylan, &#9745; Ian, &#9745; Jack

With the scrimmage only a few days away, We began practicing as much as we could with the restrictions we have with only being able to be at the school one day a week. That being said, we were able to get a 45 point autonomous up and below is a recording of it working. Unfortunately Derek was unable to practice driving since we took up the whole time programming the autonomous, but we will be able to go to the school early in the morning and spend plenty of time practicing before it is our turn to compete. To be able to run the skills run, we also created a new member function in the Auton class called runSkills();. As well the GUI has a third option in the dropdown that allows the user to choose `skills`. We plan on keeping this feature as well, since it will be useful for all competition where we want to run our autonomous skills run.

### 45 Point Auton

%%HTML
<div align="middle">
<video width="50%" controls>
      <source src="././_images/9-September/9-22-20/45pointAutonRun.mp4" type="video/mp4">
</video></div>

## 9/29/20
### Attendance: &#9745; Brody, &#9745; Derek, &#9745; Dylan, &#9745; Ian, &#9745; Jack

The scrimmage results are finally in, unfortunately we did not do as well as we hoped but we did learn a lot and we now have a clear plan for what improvements we want to make to our robot and code to make us do better for our first real tournament which is on November 21.

### List of Improvements
- 1 button auto sorting and auto sorting when cylcing goals.
- Improve intakes to intake balls easier.
- Re-build hood to make the balls always make it into the goal.
- Spend more time practicing both Auton and Driving.
> All of these goals will be achieved by November 21st.

<img src="././_images/9-September/9-29-20/firstComp.jpg" alt="firstComp.jpg" style="width: 300px;"/>