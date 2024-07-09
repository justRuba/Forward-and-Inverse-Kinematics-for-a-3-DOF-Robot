# Forward and Inverse Kinematics for a 3-DOF Robot

This project explains the forward and inverse kinematics for a 3-DOF planar robot. It includes detailed calculations and an example to illustrate the concepts.

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

\[ 
x = 1 \cos\left(\frac{\pi}{6}\right) + 1 \cos\left(\frac{\pi}{6} + \frac{\pi}{4}\right) + 1 \cos\left(\frac{\pi}{6} + \frac{\pi}{4} + \frac{\pi}{3}\right)
\]
\[ 
y = 1 \sin\left(\frac{\pi}{6}\right) + 1 \sin\left(\frac{\pi}{6} + \frac{\pi}{4}\right) + 1 \sin\left(\frac{\pi}{6} + \frac{\pi}{4} + \frac{\pi}{3}\right)
\]

Let's compute these step by step:

1. Calculate individual cosine and sine terms:
   - \(\cos\left(\frac{\pi}{6}\right) = \frac{\sqrt{3}}{2}\)
   - \(\cos\left(\frac{\pi}{6} + \frac{\pi}{4}\right) = \cos\left(\frac{5\pi}{12}\right)\)
   - \(\cos\left(\frac{\pi}{6} + \frac{\pi}{4} + \frac{\pi}{3}\right) = \cos\left(\frac{3\pi}{4}\right) = -\frac{\sqrt{2}}{2}\)

2. Combine these to find \(x\):
   \[ 
   x = 1 \cdot \frac{\sqrt{3}}{2} + 1 \cdot \cos\left(\frac{5\pi}{12}\right) + 1 \cdot -\frac{\sqrt{2}}{2} 
   \]

3. Calculate \(y\):
   - \(\sin\left(\frac{\pi}{6}\right) = \frac{1}{2}\)
   - \(\sin\left(\frac{\pi}{6} + \frac{\pi}{4}\right) = \sin\left(\frac{5\pi}{12}\right)\)
   - \(\sin\left(\frac{\pi}{6} + \frac{\pi}{4} + \frac{\pi}{3}\right) = \sin\left(\frac{3\pi}{4}\right) = \frac{\sqrt{2}}{2}\)

4. Combine these to find \(y\):
   \[ 
   y = 1 \cdot \frac{1}{2} + 1 \cdot \sin\left(\frac{5\pi}{12}\right) + 1 \cdot \frac{\sqrt{2}}{2} 
   \]

## Inverse Kinematics

Inverse kinematics involves determining the joint parameters that will achieve a given end-effector position and orientation.

### Example: 3-DOF Planar Robot

Given the end-effector position \((x, y)\), we need to find the joint angles \(\theta_1\), \(\theta_2\), and \(\theta_3\).

Let's assume:
- End-effector position: \((x, y) = (2, 1.5)\)
- Link lengths: \(L_1 = 1\), \(L_2 = 1\), \(L_3 = 1\)

1. **Solve for \(\theta_3\):**
   \[
   \cos(\theta_3) = \frac{x - L_1 \cos(\theta_1) - L_2 \cos(\theta_1 + \theta_2)}{L_3}
   \]
   \[
   \sin(\theta_3) = \frac{y - L_1 \sin(\theta_1) - L_2 \sin(\theta_1 + \theta_2)}{L_3}
   \]

2. **Solve for \(\theta_2\):**
   \[
   \cos(\theta_2) = \frac{x - L_1 \cos(\theta_1)}{L_2}
   \]
   \[
   \sin(\theta_2) = \frac{y - L_1 \sin(\theta_1)}{L_2}
   \]

3. **Solve for \(\theta_1\):**
   \[
   \theta_1 = \tan^{-1}\left(\frac{y}{x}\right)
   \]
