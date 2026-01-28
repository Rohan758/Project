# Enchanted Maze Quest:
A Magical Garden AdventureThis project was developed for the UMIC (Unmesh Mashruwala Innovation Cell) and involves designing and simulating an autonomous robotic companion capable of navigating a mystical garden maze. The robot must overcome "dangerous plants" (obstacles) and follow "magical signs" (Aruco markers) to find a hidden treasure.

# Project Overview
The mission is to navigate a $13 \times 13$ maze environment in Gazebo without the use of GPS for localization. The system uses a combination of an overhead camera for global positioning and an on-bot camera for local sign detection and interaction.

# Key Features
Autonomous Navigation: The robot calculates optimal paths using the $A^*$ algorithm.

Sign Detection: Real-time detection of Aruco markers (QR codes) that provide movement instructions (Left, Right, Straight) which override existing paths.

Dynamic Re-planning: Each time a sign is encountered, the robot recomputes its path to the destination.

Overhead Localization: An overhead camera provides continuous image data to the path planning and control subsystems to track the bot's position.

# System Architecture
1. Bot Design
   Mechanism: Differential drive.
   
   Dimensions: $50 \times 50 \times 70 \text{ cm}$.
   
   Sensors: Equipped with an optical camera for Aruco detection and various advanced sensors for obstacle avoidance.
  
3. Software Stack
   Simulation: Gazebo (using Building Editor for the maze).
   
   Communication: ROS (Robot Operating System).
   
   Path Planning: $A^*$ Algorithm, NumPy, and OpenCV (to convert maze images into a $0/1$ matrix).
   
   Control: Proportional (P) controller from the PID framework for aggressive and precise movement within tight maze walls.
