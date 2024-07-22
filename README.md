# Robotic Arm Control Using LLMs
Author: Curran Flanders
Program: Wolfram Summer School
Completion Date: 07/09/2024

## Project description
The use of large language models (LLMs) can add natural language comprehension and reasoning abilities to a robot control system. This project uses the capabilities of large 
language models to enable a robotic arm to follow natural language instructions. The arm is simulated in Mathematica in an environment containing other objects. First, a 2D 
model of the arm is constructed. Then, the model is extended into 3D. Functions are added to create environment datasets and to allow the LLM and the graphics simulation to 
access the datasets. Finally, functions are added to allow the LLM to guide the movement of the arm by specifying a list of sequential target positions. 

## Purpose
The purpose of this project is to create a workflow and code that allows a user to control a simulated 
robot arm with natural language instructions. The natural language instructions will be passed to a 
large language model (LLM) which will interpret the instructions and determine the positions to which 
the arm will be moved. The LLM specifies points in space for the arm to move to, but the inverse 
kinematics must be handled in a separate process. 

## I/O and implememtation
The inputs to the LLM are a prompt from the user, a string description of the arm's environment, and a
template string to enclose this data. The LLM returns a path of points whose trajectory the arm should 
follow. Inverse kinematics is used to determine the joint angles the robot arm must have to reach these 
positions. An interpolation function is created between the sets of joint angles corresponding to the 
points along the path. This leads to a continuous path between the sets of points.  A graphic showing 
the arm travelling along its path is displayed. 

## Extendability
This process should work in a similar manner for any LLM whose API is directly accessible by Wolfram, 
but testing has been performed exclusively with GPT-4 by OpenAI.


