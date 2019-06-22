# Programming Exercise 1: Quadrotor Simulator and PD Controller

# 1 Introduction
The goal of this programming exercise is to get you familiar with working with the quadrotor simulator and implementing a Proportional Derivative (PD) controller. In Week 1, we provided you with a quadrotor GUI in which to tune PD control gains. In this exercise, you will have to implement your own PD controller to control the height of a quadrotor, as well as tune its gains.

# 2 PD Controller
As you have seen in the lecture, the dynamic equation for the motion of the quadrotor in the z direction is ¨ z = u m −g
Figure 1: 1D quadrotor model.
Hence, the control input for a PD controller is
u = m(¨ zdes + Kpe + Kv ˙ e + g)
where e and ˙ e can be calculated from the current and desired states (z,zdes, ˙ z, ˙ zdes).

# 3 Quadrotor Simulator
We utilize one of MATLAB’s ODE solvers, called ode45, to simulate the behavior of the quadrotor.You can read more details at Mathworks or other online resources. We then use the function plot/plot3 to help visualize the current state of the quadrotor at each time step. You may take a look at ﬁle height_control.m for the simulation code.

# 4 Tasks
You will need to ﬁrst implement a PD controller for height control of the quadrotor. Then, tune the proportional gain (Kp) and derivative gain (Kv) in the ﬁle controller.m until the quadrotor converges quickly and smoothly to a step response input.
