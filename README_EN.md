![logo1](https://raw.githubusercontent.com/sugawara-system/tutoring-work-schedule/main/docs/images/user_32.png)



[日本語版 README はこちら](https://github.com/sugawara-system/tutoring-work-schedule/blob/main/README.md)




## Summary

This project runs on the paid software, Schedule Nurse, and solves the problem of creating shifts for tutors.
The original problem is an article on Qiita, [Introduction to Optimization Project with Google OR-Tools](https://qiita.com/yukiopt/items/dab6bc76d9ff41d551f5) written in Japanese.

<br><br>


## Install Schedule Nurse

Schedule Nurse is a paid software that runs on Windows 10/11. Around 4.09USD/month,4.09EUR/month (as of December 2024).

Install at [installation site](https://apps.microsoft.com/store/detail/9N94ZPBTB0RL).

<br><br>

## How to use


1. Open GithubViewer. 


<div align="center"><img src="https://raw.githubusercontent.com/sugawara-system/tutoring-work-schedule/main/docs/images/user_33.png" width="1200"/></div>
.

2. Press Next until this site comes up.

<div align="center"><img src="https://raw.githubusercontent.com/sugawara-system/tutoring-work-schedule/main/docs/images/user_34.png" width="1200"/></div>

3. Download this project. 

<div align="center"><img src="https://raw.githubusercontent.com/sugawara-system/tutoring-work-schedule/main/docs/images/user_35.png" width="1200"/></div>

4. Name and save the project.

<div align="center"><img src="https://raw.githubusercontent.com/sugawara-system/tutoring-work-schedule/main/docs/images/user_36.png" width="1200"/></div>

5. Press the Solve button.


<br><br>

## Modeling

### I want to minimize the number of empty frames as much as possible.

Turn off the Attendance Penalty(Shift Penalty,Row Constraint: 3), which is unrelated to the constraint in question. (Uncheck the relevant soft constraint and solve for it.)
Also, weight the schedule heavily so that the work shift preference does not change.

<div align="center"><img src="https://raw.githubusercontent.com/sugawara-system/tutoring-work-schedule/main/docs/images/user_48.png" width="1200"/></div>


### I want to minimize my shift as much as possible.

From the subject, we turn off all soft shift requests. We also turn off the penalty for free frames instead of adding the penalty for the shift to solve the problem.

<div align="center"><img src="https://raw.githubusercontent.com/sugawara-system/tutoring-work-schedule/main/docs/images/user_47.png" width="1200"/></div>



<br><br>


## Implementation

### Shift form

The shift pattern is not specified, but it is assumed that there are all possible patterns: four frames, three frames, and two frames in a row. (Single frame is assumed to be prohibited.)


<div align="center"><img src="https://raw.githubusercontent.com/sugawara-system/tutoring-work-schedule/main/docs/images/user_46.png" width="1200"/></div>

<br>


The constraints of the part that generates the desired penalty are as follows.

### Free frame time



<div align="center"><img src="https://raw.githubusercontent.com/sugawara-system/tutoring-work-schedule/main/docs/images/user_45.png" width="1200"/></div>


<br>

### Attendance (negation of day-off)



<div align="center"><img src="https://raw.githubusercontent.com/sugawara-system/tutoring-work-schedule/main/docs/images/user_44.png" width="1200"/></div>


<br>

## Enter Preferred schedule

All cells, constrained to level 1.


<div align="center"><img src="https://raw.githubusercontent.com/sugawara-system/tutoring-work-schedule/main/docs/images/user_43.png" width="1200"/></div>

<br>

### Number of tutors

Each week and each day of the week, the required number of tutors will change, which is defined in the following table.


<div align="center"><img src="https://raw.githubusercontent.com/sugawara-system/tutoring-work-schedule/main/docs/images/user_42.png" width="1200"/></div>

<br>

## Algorithms

The following algorithms can be selected.



<div align="center"><img src="https://raw.githubusercontent.com/sugawara-system/tutoring-work-schedule/main/docs/images/user_41.png" width="1200"/></div>

<br>

The developer and summary of each algorithm is below.



<div align="center"><img src="https://raw.githubusercontent.com/sugawara-system/tutoring-work-schedule/main/docs/images/user_40.png" width="1200"/></div>

<br><br>


## Shift solution example


<div align="center"><img src="https://raw.githubusercontent.com/sugawara-system/tutoring-work-schedule/main/docs/images/user_39.png" width="1200"/></div>


## Task solution example


<div align="center"><img src="https://raw.githubusercontent.com/sugawara-system/tutoring-work-schedule/main/docs/images/user_37.png" width="1200"/></div>

## Example of Shift Task Solution

<div align="center"><img src="https://raw.githubusercontent.com/sugawara-system/tutoring-work-schedule/main/docs/images/user_38.png" width="1200"/></div>

