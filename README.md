# Flying Car Controller

In this project I have implemented a Cascade PID Drone Controller and tested for multiple scenarios as described below:

## Rubric

|Task | Status|
|----|---|
|Implemented body rate control in C++.| Implemented in lines 111-115|
|Implement roll pitch control in C++. | Lines 146-163|
|Implement altitude controller in C++.| Lines 194-209|
|Implement lateral position control in C++.| Lines 246-267|
|Implement yaw control in C++.| Lines 288-302|
|Implement calculating the motor commands given commanded thrust and moments in C++.| Lines 78-87|





## Performance Metrics

### 1: Intro
Tuned the mass parameter so that the drone starts to hover without falling.  


[![Intro task](https://img.youtube.com/vi/XK1lUQUWUyg/0.jpg)](https://www.youtube.com/watch?v=XK1lUQUWUyg)

### 2: RollPitchControl 
 In this test scenario, the drone is expected to meet following two criteria:

> 1. roll should be less than 0.025 radian of nominal for 0.75 seconds (3/4 of the duration of the loop)
> 2. roll rate should be less than 2.5 radian/sec for 0.75 seconds


[![Intro task](https://img.youtube.com/vi/LN1lWt7Gq_c/0.jpg)](https://www.youtube.com/watch?v=LN1lWt7Gq_c)

The simulator prints success message: 

> PASS: ABS(Quad.Roll) was less than 0.025000 for at least 0.750000 seconds
> PASS: ABS(Quad.Omega.X) was less than 2.500000 for at least 0.750000 seconds

### 3:Position Control 
 In this, the Drone is expected to satisfy following constraints:

> 1. X position of both drones should be within 0.1 meters of the target for at least 1.25 seconds
> 2. Quad2 yaw should be within 0.1 of the target for at least 1 second


The simulator prints success message:
> PASS: ABS(Quad2.Pos.X) was less than 0.100000 for at least 1.250000 seconds
> PASS: ABS(Quad2.Yaw) was less than 0.100000 for at least 1.000000 seconds

### 4:
In this scenario, there are 3 drones which have to satisfy following constraint:

> 1. position error for all 3 quads should be less than 0.1 meters for at least 1.5 seconds


> PASS: ABS(Quad2.PosFollowErr) was less than 0.250000 for at least 3.000000 seconds







