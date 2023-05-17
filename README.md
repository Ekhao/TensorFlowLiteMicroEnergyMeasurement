# TensorFlowLiteMicroPowerMeasurement
This repository contains a changed version of the Arduino Nano 33 BLE Sense TensorFlow Lite Micro "Hello World" example for the purpose of creating a program that can be used to measure the power consumption of machine learning inference using TensorFlow Lite Micro.
The "Hello World" example has been stripped of unnecessary code for measuring the energy consumption of a device running the code - this, e.g., includes removing input and output handling for the machine learning model.
A 10-second delay has also been added to identify breaks between inference runs and let MBEDos handle operating system tasks during this time.
To make the timing of model inference easier, the neural network model has been replaced with the neural network model from the "Person Detector" example.
Timers have also been added to allow for simulating/calculating the energy consumption of the program using datasheet values for power consumption during work and low power modes.

Note that it has not been the objective of this project to create a power efficient program, so power consuming peripherals have not been turned off. 
See the following link for information on how to reduce power consumption on the Arduino Nano 33 BLE Sense: https://support.arduino.cc/hc/en-us/articles/4402394378770-How-to-reduce-power-consumption-on-the-Nano-33-BLE