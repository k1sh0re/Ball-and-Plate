
# Ball And Plate System

## Objective

To balance a ball at the center of a plate using PID control.

## PID Controller
PID control stands for proportional integral derivative control and is one the most popular control method used in robotics as it is relatively simple and can achieve control over almost any sort of disturbance created in a system.

Working of the PID controller:

Proportional (P) part : Applies correction proportional to the current error. A proportional control alone can not stabilize a system but instead it brings the system to an equilibrium wherein the ball occilates between the desired position with a steady error.

Integral (I) part: It takes into account the past values of error and applies correction as a proportional integral of it. The integral part can be used to remove constant errors in the system.

Derivative (D) part: This part provides an estimate on how the error may change in the future and accordingly applies correction as a derivative of error.

The overall equation for a pid controller is given by:

u(t) = $K_pe(t) + K_i \int_{0}^{t} e(t) dt\ + K_d \dfrac{de(t)}{dt}$

## Workflow
### 1. Cruise Control
In order to familiarize ourselves with the working of a PID controller, we first developed a Cruise Control for a car which needs to move at a fixed set-point velocity.
The system was implemented using python and the following results were obtained.

![cruise](https://user-images.githubusercontent.com/109210914/196035804-36c04ede-36d8-4b54-bc71-bb0aad3f6c71.png)

The rise time for this system is 1.09 seconds with a maximum overshoot of 1.35%

# 

### 2. Ball and Beam
Next we built a Ball and Beam system in which the ball needs to be balanced in one dimension. An ultrasonic sensor was used to get the position of the ball and a sigle servo was used to control the inclination of the beam.
The system was first implemented as code using Python and the following results were obtained.

![babs](https://user-images.githubusercontent.com/109210914/196035822-4ff42dd6-65d2-43a9-8a1d-1faabdf6e566.png)

The rise time for this system is 1.71 seconds with a maximum overshoot of 3.57%
 
The system was then implemented using an Arduino and we were able to get the desired results.

![ball_and_beam](https://user-images.githubusercontent.com/109210914/196095834-43c094b6-9f8e-4d77-b6de-a9d98c597ba4.gif)

#

### 3. Ball and Plate

In our next step we implemented ball and plate system as code using Python and the following results were obtained.

![bap1](https://user-images.githubusercontent.com/109210914/196409465-f74777ee-7f4e-4404-b855-240165e4a5ff.png)

![bap2](https://user-images.githubusercontent.com/109210914/196409503-cc0d28aa-3f67-4aa6-98da-6dec8ec10c6a.png)

The rise time for this system is 1.86 seconds in x direction and 1.22 in y direction.

The trajectory the ball will follow can be seen below.

![bap3](https://user-images.githubusercontent.com/109210914/196409553-19f59c7b-14b8-4831-a710-97be6a6b4acf.png)










