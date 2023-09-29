<a name="br1"></a> 



<a name="br2"></a> 

**Safety Verification of Autonomous Vehicles**

**based on Signal Temporal Logic (STL)**

**constraints**

\- Aditya Parameshwaran & Yue Wang

*DISTRIBUTION STATEMENT A. Approved for public*

*release: distribution unlimited. OPSEC #*7375



<a name="br3"></a> 

Formal Verification of Off-road Autonomous Vehicles

**GOAL:**

§Formally verify the safety of an off-road autonomous vehicle and develop an autonomous

controller based on the safety specifications

**RESEARCH OBJECTIVE:**

§Develop safety verification tools and Model Predictive Control (MPC) with Signal Temporal

Logic (STL) constraints

§Conduct offline formal verification of the computed traces to determine the robustness of the

controller

**SAE International®**

SAE 2023 WCX

Paper 2023-01-0113

*DISTRIBUTION STATEMENT A. Approved for public release:*

*distribution unlimited. OPSEC #7375*

3



<a name="br4"></a> 

Outline

• Research Goal and Objectives

• Motivation

• Signal Temporal Logic

• Cost Function Formulation

• Vehicle Model

• STL Parser

• Mixed Integer Linear Programming

• Receding Horizon Control

• Results

• Future Work

**SAE International®**

SAE 2023 WCX

Paper 2023-01-0113

*DISTRIBUTION STATEMENT A. Approved for public release:*

*distribution unlimited. OPSEC #7375*

4



<a name="br5"></a> 

STL Constraint based Mobile Robot Navigation

**Mixed Integer Linear**

**Programming (MILP)**

**solver**

**Constraints**

**Objective Function**

Vehicle Dynamics

*Optimal Control*

*Input:*

*Wheel Velocities*

Input and State

Bounds

**2D Navigation**

*Feedback*

**+**

*Offline*

*Verification*

Signal Temporal Logic

**Safety**

**Region**

**Unsafe Region**

**SAE International®**

SAE 2023 WCX

Paper 2023-01-0113

*DISTRIBUTION STAT*

*distribution unlimite*



<a name="br6"></a> 

Signal Temporal Logic

Introduction

Logic

“AND”

“NOT”

“OR”

Domain

Knowledge

Signal

<sub>Temporal</sub>T mpo~~ra~~l

Logic

Applicatio

n

“Natural Language Rules”

Signal

**SAE International®**

SAE 2023 WCX

Paper 2023-01-0113

*DISTRIBUTION STATEMENT A. Approved for public release:*

*distribution unlimited. OPSEC #7375*

6



<a name="br7"></a> 

Overview of STL

STL Grammar and Semantics

Predicate

Not

And

Or

Implies

Eventually

Always

Until

**SAE International®**

SAE 2023 WCX

Paper 2023-01-0113

*DISTRIBUTION STATEMENT A. Approved for public release:*

*distribution unlimited. OPSEC #7375*

7



<a name="br8"></a> 

Overview of STL

Graphical Example

PROPERTY

SATISFIED

AN

D

Alway

s

PROPERTY VIOLATED

Eventuall

y

PROPERTY SATISFIED

**SAE International®**

SAE 2023 WCX

Paper 2023-01-0113

*DISTRIBUTION STATEMENT A. Approved for public release:*

*distribution unlimited. OPSEC #7375*

8



<a name="br9"></a> 

Properties of Signal Temporal Logic

Robustness Semantics combined with Safety

And

c

c

c

**SAE International®**

SAE 2023 WCX

Paper 2023-01-0113

*DISTRIBUTION STATEMENT A. Approved for public release:*

*distribution unlimited. OPSEC #7375*

9



<a name="br10"></a> 

Vehicle Model

2D Simplified Kinematic Model

• Kinematic model for simplicity and to test validity of method

• Feedback linearized kinematics model for faster computation

[1]

Simplified Vehicle Kinematics

(Unicycle Model)

Feedback Linearized Vehicle

Model

Discrete-time Linear Vehicle

Model

0

0

0

0

0

1

0

0

0

0

1

0

0

0

0

1

0

0

0

0

1

0

*A* =

*, B* =

0

0

[1] De Luca et al., Stabilization of the Unicycle Via Dynamic Feedback

Linearization,

IFAC Proceedings Volumes, Vol 33, 2000

**SAE International®**

SAE 2023 WCX

Paper 2023-01-0113

*DISTRIBUTION STATEMENT A. Approved for public release:*

*distribution unlimited. OPSEC #7375*

10



<a name="br11"></a> 

Feedback Linearization

Converting the linear control inputs back to nonlinear kinematics

Linear Vehicle Model

Transformation Matrix

Simulate Non-Linear

Dynamics

Computed Optimal Control

Inputs

**SAE International®**

SAE 2023 WCX

Paper 2023-01-0113

*DISTRIBUTION STATEMENT A. Approved for public release:*

*distribution unlimited. OPSEC #7375*

11



<a name="br12"></a> 

Cost Function Formulation

Robustness

Cost Function

The aim is to compute *optimal*

*control inputs* (**u\***) that maintain

positive robustness for the

prediction horizon

System Kinematics

Control Bounds

State Bounds

The *optimal control inputs* will be

applied to the system model

following the linearized system

kinematics explained earlier

**SAE International®**

SAE 2023 WCX

Paper 2023-01-0113

*DISTRIBUTION STATEMENT A. Approved for public release:*

*distribution unlimited. OPSEC #7375*

12



<a name="br13"></a> 

STL Parser

From Natural Language to Inequality Equations

User Input format:

Go-To-Goal

Multi-Waypoint Navigation

**SAE International®**

SAE 2023 WCX

Paper 2023-01-0113

*DISTRIBUTION STATEMENT A. Approved for public release:*

*distribution unlimited. OPSEC #7375*

13



<a name="br14"></a> 

Mixed Integer Linear Programming (MILP) Problem

MILP Formulation

Goal Region L.I.E.

Obstacle Region

L.I.E.

Get *Goal Coordinates* from STL parser •

Get *Obstacle Coordinates* from STL

parser

•

e.g.

•

Like the Goal region, we define an

obstacle region polytope as

• Set of Linear Inequality Equations

(L.I.E.)

1

0

0

1

0

0

0

0

0

0

0

0

• STL Constraints

• System Dynamics

• State and Input Bounds

\-

1

**G** =

**, b** =

0

0

\-

1

**SAE International®**

SAE 2023 WCX

Paper 2023-01-0113

*DISTRIBUTION STATEMENT A. Approved for public release:*

*distribution unlimited. OPSEC #7375*

14



<a name="br15"></a> 

Receding Horizon Control

Obstacle

Goal Region

**SAE International®**

SAE 2023 WCX

Paper 2023-01-0113

*DISTRIBUTION STATEMENT A. Approved for public release:*

*distribution unlimited. OPSEC #7375*

15



<a name="br16"></a> 

Example Simulation 1

"alw ((ev\_[04,05] (X(1:2,t) > [0.3;0.5] and X(1:2,t) < [0.5;0.7]))

and X(1:2,t) >~ [1.0;1.2] and X(1:2,t) <~ [1.2;1.7])"

STL Specification

Robustness

“alw (min\_d[t] > 0.05)

*Offline*

*Verification*

Robustness plot

Go-To-Goal

**Safety**

**Region**

**Unsafe Region**

**SAE International®**

SAE 2023 WCX

Paper 2023-01-0113

*DISTRIBUTION STATEMENT A. Approved for public release:*

*distribution unlimited. OPSEC #7375*

16



<a name="br17"></a> 

Example Simulation 2

**Safety**

**Region**

**Unsafe Region**

**SAE International®**

SAE 2023 WCX

Paper 2023-01-0113

*DISTRIBUTION STATEMENT A. Approved for public release:*

*distribution unlimited. OPSEC #7375*

17



<a name="br18"></a> 

**Contact Info**

Thank you

Acknowledgment

This work was supported by the

Simulation Based Reliability and

Safety Program for modeling and

simulation of military ground

vehicle systems, under the

technical services contract No.

W56HZV-17-C-0095 with the U.S.

Army DEVCOM Ground Vehicle

Systems Center (GVSC).

Aditya Parameshwaran, Yue Wang

Clemson University

Clemson, South Carolina

+1 7654186709

[aparame@clemson.edu](about:blank)

yue6@clemson.edu

**SAE International®**

SAE 2023 WCX

*DISTRIBUTION STATEMENT A. Approved for public release:*

*distribution unlimited. OPSEC #7375*

Paper 2023-01-0113

18

