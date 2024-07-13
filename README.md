# Forward and Inverse Kinematics for a 3-DOF Robot

This project explains the forward and inverse kinematics of a 3-DOF planar robot. It includes calculations.

## Forward Kinematics

Forward kinematics involves determining the position and orientation of the end-effector given the joint parameters.

### Example: 3-DOF Planar Robot

Consider a planar robot with three revolute joints, Each joint connects to a link of length.

The end-effector's position can be found by summing the contributions of each link.

The position (x,y) of the end-effector is given by:

![WhatsApp Image 2024-07-14 at 00 58 18_498a66df](https://github.com/user-attachments/assets/15b8d9be-36a0-49fc-9ad1-9daae7aa0b0b)

Let:
L1, L2 and L3 = 1
theta1 = 30, theta2 = 45 and theta3 = 60

Then calculate x and 𝑦:

![WhatsApp Image 2024-07-14 at 01 04 24_564d56a0](https://github.com/user-attachments/assets/adaaf3c1-b845-44f7-b3b0-7350e67c19af)

The Result:

x ≈ 0.418 and y ≈ 2.173

## Inverse Kinematics

Inverse kinematics determines the joint parameters that achieve a given end-effector position and orientation.

### Example: 3-DOF Planar Robot

Given the end-effector position and Finding the joint angles

Let:
(x,y) = (0.418, 2.173)
L1, L2 and L3 = 1

Solve for theta1:

![WhatsApp Image 2024-07-14 at 01 14 06_a8155bae](https://github.com/user-attachments/assets/7427b1e8-217c-4ad6-86c9-60763a5b887b)

![WhatsApp Image 2024-07-14 at 01 18 17_d7c6b50a](https://github.com/user-attachments/assets/64a08a1c-48e8-49cd-b385-702a37b94cac)

Solve for theta2:

![WhatsApp Image 2024-07-14 at 01 15 49_c1b486dd](https://github.com/user-attachments/assets/5b62f700-5d6e-48ad-8925-6ca2dcf611f8)

![WhatsApp Image 2024-07-14 at 01 19 56_79bb7b98](https://github.com/user-attachments/assets/8f2c6230-56c3-4167-89c8-5f6191d5b7f6)

Solve for theta3:

![WhatsApp Image 2024-07-14 at 01 16 23_5c085980](https://github.com/user-attachments/assets/b12deb96-aedd-430d-9630-279075d03ab0)

![WhatsApp Image 2024-07-14 at 01 21 48_af81d75f](https://github.com/user-attachments/assets/c268e14e-91f7-4764-8bdf-01571b7d6631)

![WhatsApp Image 2024-07-14 at 01 22 28_236863f0](https://github.com/user-attachments/assets/ae537639-245f-4b0d-97ed-f0170cbba463)

