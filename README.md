# Forward and Inverse Kinematics for a 3-DOF Robot

This project explains the forward and inverse kinematics for a 3-DOF planar robot. It includes detailed calculations and an example to illustrate the concepts.

![3-DOF Robot](https://github.com/justRuba/Forward-and-Inverse-Kinematics-for-a-3-DOF-Robot/assets/134620937/d40005b8-c36b-48cf-8213-4d36e81bb1a4)

*Image source: [Example Source](https://www.youtube.com/watch?v=LpYf_hJPN70)*

## Forward Kinematics

Forward kinematics involves determining the position and orientation of the end-effector given the joint parameters (angles for revolute joints).

### 3-DOF Planar Robot

Consider a planar robot with three revolute joints, denoted as \(\theta_1\), \(\theta_2\), and \(\theta_3\). Each joint connects to a link of length \(L_1\), \(L_2\), and \(L_3\), respectively.

The position \((x, y)\) of the end-effector is given by:

\[ 
x = L_1 \cos(\theta_1) + L_2 \cos(\theta_1 + \theta_2) + L_3 \cos(\theta_1 + \theta_2 + \theta_3)
\]
\[ 
y = L_1 \sin(\theta_1) + L_2 \sin(\theta_1 + \theta_2) + L_3 \sin(\theta_1 + \theta_2 + \theta_3)
\]

### Example Calculation

Let:
- \(L_1 = 1\)
- \(L_2 = 1\)
- \(L_3 = 1\)
- \(\theta_1 = 30^\circ\)
- \(\theta_2 = 45^\circ\)
- \(\theta_3 = 60^\circ\)

Convert angles to radians:
- \(\theta_1 = \frac{\pi}{6}\)
- \(\theta_2 = \frac{\pi}{4}\)
- \(\theta_3 = \frac{\pi}{3}\)

Calculate \(x\) and \(y\):

```math
x = 1 \cos\left(\frac{\pi}{6}\right) + 1 \cos\left(\frac{\pi}{6} + \frac{\pi}{4}\right) + 1 \cos\left(\frac{\pi}{6} + \frac{\pi}{4} + \frac{\pi}{3}\right)
