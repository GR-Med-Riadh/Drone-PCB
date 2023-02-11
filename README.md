# Drone-PCB

I would like to share one of my latest PCB designs that I have just received from jlcpcb
First of all, I'd like to thank jlcpcb for their sponsorship and for supporting young tech
enthusiasts like myself in being able to create quality PCBs with greater precision.

This PCB is for  a version 1 drone that is controlled using an  ESP32  microcontroller since it uses both  wifi & bluetooth communication so we have a choice on remotes controllers. It consists of 2 cores to create a RTOS ( real-time operating system ), the first core is used  for communication and PID ( proportional, integrator and derivater) regulation of the sensors, and the second core is used  for controlling motors and their synchronization.
ESP32 has MCPWM (motor control pulse width modulation),this functionality helps to control the  synchronization of the motors because it uses a timer for each motor.
This PCB contains a mpu6050 (gyroscope & accelerometer ) and magnetometer to control stability of the Drone.
We also use a  motor driver that uses a mosfet transistor to control the motors speed. As well as  an opto-coupler which works as  a bridge between the ESP32 and the mosfet to eliminate any reverse current.
link of jlcpcb: https://jlcpcb.com/HAR
