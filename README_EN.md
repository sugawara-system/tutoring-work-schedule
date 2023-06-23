![logo1](https://raw.githubusercontent.com/sugawara-system/tutoring-work-schedule/main/docs/images/user_13.png)


[“ú–{Œê”Å README ‚Í‚±‚¿‚ç](https://raw.githubusercontent.com/sugawara-system/tutoring-work-schedule/main/README.md)




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

<div align="center"><img src="https://raw.githubusercontent.com/sugawara-system/tutoring-work-schedule/main/docs/images/user_31.png" width="1200"/></div> 2.

Press Next until this site comes up.

<div align="center"><img src="https://raw.githubusercontent.com/sugawara-system/tutoring-work-schedule/main/docs/images/user_27.png" width="1200"/></div> 3.

3. Download this project. 

<div align="center"><img src="https://raw.githubusercontent.com/sugawara-system/tutoring-work-schedule/main/docs/images/user_30.png" width="1200"/></div>

4. Name and save the project.

<div align="center"><img src="https://raw.githubusercontent.com/sugawara-system/tutoring-work-schedule/main/docs/images/user_28.png" width="1200"/></div> 5.


5. Press the Motome button.

<br><br>

## Modeling

### I want to minimize the number of empty frames as much as possible.

Turn off the Attendance Penalty Generation section (Row Constraint: 3), which is unrelated to the constraint in question. (Uncheck the relevant soft constraint and solve for it.)
Also, weight the schedule heavily so that the work shift preference does not change.

<div align="center"><img src="https://raw.githubusercontent.com/sugawara-system/tutoring-work-schedule/main/docs/images/user_21.png" width="1200"/></div>


### I want to minimize my attendance as much as possible.

From the subject, we turn off all soft attendance requests. We also turn off the aforementioned penalty for free frames to solve the problem.

<div align="center"><img src="https://raw.githubusercontent.com/sugawara-system/tutoring-work-schedule/main/docs/images/user_22.png" width="1200"/></div></div

<br><br>


## Implementation

### Shift form

The shift pattern is not specified, but it is assumed that there are all possible patterns: four frames, three frames, and two frames in a row. (Single frame is assumed to be prohibited.)

<div align="center"><img src="https://raw.githubusercontent.com/sugawara-system/tutoring-work-schedule/main/docs/images/user_18.png" width="1200"/></div></div


The constraints of the part that generates the desired penalty are as follows.

### Free frame time


<div align="center"><img src="https://raw.githubusercontent.com/sugawara-system/tutoring-work-schedule/main/docs/images/user_20.png" width="1200"/></div>


### Attendance (negation of day-off)


<div align="center"><img src="https://raw.githubusercontent.com/sugawara-system/tutoring-work-schedule/main/docs/images/user_19.png" width="1200"/></div>

## Enter Preferred schedule

All cells, constrained to level 1.

<div align="center"><img src="https://raw.githubusercontent.com/sugawara-system/tutoring-work-schedule/main/docs/images/user_17.png" width="1200"/></div>



### Number of tutors

Each week and each day of the week, the required number of tutors will change, which is defined in the following table.

<div align="center"><img src="https://raw.githubusercontent.com/sugawara-system/tutoring-work-schedule/main/docs/images/user_29.png" width="1200"/></div></div

<br><br><br

## Algorithms

The following algorithms can be selected.


<div align="center"><img src="https://raw.githubusercontent.com/sugawara-system/tutoring-work-schedule/main/docs/images/user_16.png" width="1200"/></div></div


The developer and summary of each algorithm is below.


<div align="center"><img src="https://raw.githubusercontent.com/sugawara-system/tutoring-work-schedule/main/docs/images/user_23.png" width="1200"/></div>

<br><br>


## Shift solution example

<div align="center"><img src="https://raw.githubusercontent.com/sugawara-system/tutoring-work-schedule/main/docs/images/user_25.png" width="1200"/></div></div


## Task solution example

<div align="center"><img src="https://raw.githubusercontent.com/sugawara-system/tutoring-work-schedule/main/docs/images/user_26.png" width="1200"/></div>


## Example of Shift Task Solution
<div align="center"><img src="https://raw.githubusercontent.com/sugawara-system/tutoring-work-schedule/main/docs/images/user_24.png" width="1200"/></div>
