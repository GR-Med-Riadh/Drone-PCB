# Drone-PCB

JLCPCB is a company that constructs PCBs and prints 3D mechanical designs, they give us great offers with cheap prices for high quality precision PCBs. I would like to thank JLCPCB for their sponsorship and for supporting me in creating and innovating schematics, and improving my PCBs designs.

This is the latest PCB design that I have received from JLCPCB, this PCB is for a version 1 drone that is controlled using an ESP32 microcontroller since it uses both wifi & bluetooth communication so we have a choice on the remotes controller.
Thanks to these means of communication, we can connect our drone to the internet and track it, we can also control it using bluetooth or using esp-now a communication protocol of espressif.

It consists of 2 cores to create a RTOS (real-time operating system). That means we can control it, receive data and localisation from our drone in real time.
The first core is used for communication with the remote and for regulation of the sensors with PID (proportional, integrator and derivative) methods, and the second core is used for controlling the motors and their synchronization. 
PID type controllers are used in various industries for machines, robots and systems to control the stability of their systems.

ESP32 has an MCPWM peripheral (motor control pulse width modulation), this functionality helps us to synchronize the motors by using a timer for each motor. 

In this PCB we use a mpu6050 which contains a gyroscope and accelerometer. The accelerometer is used to measure acceleration forces and the gyroscope is for measuring rotation forces. We also use a QMC5883L magnetometer to measure the magnetic force. These sensors control the stability of the drone and help to detect the direction in which it is located.

The PCB contains a motor driver that uses a mosfet transistor as a switch to convert our pwm signal to a speed motor. It also contains an opto-coupler which works as a bridge between the ESP32 and the mosfet to eliminate any reverse current.

JLCPCB link: https://jlcpcb.com/HAR 

