# ERC-WarehouseRobot_TeamROSe
Hi, we are students from BITS Pilani Goa Campus Participating in ERC Hackathon 2025.

Mechanical Objective:
Design a robust, reliable, and efficient mechanical structure for an autonomous warehouse management robot capable of navigating through warehouse environments, lifting and transporting boxes of various weights, and organising inventory on shelves.
Specifications:
Robot Parameters (Given):
Weight of boxes: 800 g.
Dimensions of boxes: 30cm x 30cm x 20cm
Height of shelves: 0.4m, 0.75m, 1.1m, 1.4m (approximately)
Required operating speed: 0.5 m/s traversal, 0.2 m/s lifting/lowering
Workspace dimensions: 15m x 9m
Chassis Design:
  Dimensions: As per your requirements (should be able to justify your choice)
  Mobility: Differential drive system with 4 DC motors for navigation
  Ground Clearance: Ensure sufficient clearance for navigating warehouse floors
  Camera Mounts: Include a front-facing camera for navigation and barcode scanning
CAD and Analysis:
  Use Fusion 360, OnShape to design the robot
  Sketch the forklift mechanism to determine appropriate dimensions and gear ratios
  Conduct static structural analysis using Ansys for both the chassis and the forklift mechanism
Torque Calculations: Perform detailed torque calculations for:
  Traversal system
  Manipulator system
Bonus:
● Detailed Engineering: Show comprehensive torque calculations and safety factors
● Safety Integration: Advanced safety features and emergency systems
● New creative mechanisms, apart from ground vehicles, our welcome


2. Electronics
Objective:
Design the complete electronics system for an autonomous warehouse robot using
TinkerCAD simulation. The system should be efficient, reliable, and capable of controlling
the robot's movement and functions.
Requirements:
TinkerCAD Simulation:
● Design the entire electronics system using TinkerCAD
● Assume the components in TinkerCAD have sufficient torque, power, and other features
● Use 2 Arduino UNOs:
○ Master Arduino: Communication and decision making
○ Slave Arduino: Motor control and sensor interfacing
System Functions:
The circuit you design should perform these three main functions:
1. Differential Drive Movement: Control 4 DC motors for robot navigation
2. Forklift Control: Control 2 DC motors with encoders for vertical movement
3. Conveyor Belt Control: Control 2 DC motors with encoders for the prong conveyor
system
Sensing Systems:
● Ultrasonic Sensor: Position detection for objects on a conveyor belt
● Limit Switches: Stop forklift at upper and lower limits (use pushbuttons in TinkerCAD)
● Encoders: Position feedback for precise motor control
Power System:
● Power Calculations: Calculate total power requirements for the robot
● Component List: Provide a realistic part list based on power and torque calculations
PCB Design:
● Design Arduino UNO shield (slave) using KiCad
● Include all required footprints and components (motor drivers, encoders, etc.)
● Use screw terminals for external wire connections
● Calculate and justify the track thickness for power distribution
● Minimise wiring complexity through proper shield design
Code Requirements:
● Master-Slave Communication: Implement serial communication I2C between Arduinos
● Comprehensive Comments: Include thorough code documentation
● Control Logic: Implement proper control algorithms for all subsystems
● Safety Features: Include emergency stop and limit protection
General Instructions:
● Document all assumptions made during the design
● Ensure PCB design matches actual component specifications
● Note the differences between TinkerCAD and real-world components

3. Automation
Objective:
Design and implement the automation system for an autonomous warehouse management
robot using ROS2 and Gazebo simulation. The robot needs to navigate through a
warehouse environment, detect and organise misplaced packages, and avoid obstacles as
well.
Task Instructions:
Setup:
● Use ROS2 Humble and Gazebo Fortress Ignition for simulation, with the provided
world file and the robot files.
● The robot starts at a designated home position in the warehouse
● The warehouse contains multiple colour-specific shelves
● Obstacles include pallets, trolleys, people(static) and trash bins.
Primary Tasks:
1. Inventory Management:
○ Detect boxes on shelves and verify correct placement
○ Identify company affiliation through colour (RGBY) detection, and locate the shelf
and rack number from the ARUCO marker ID 5x5 (range 0-19).
○ Reorganise misplaced boxes to correct the shelves 
○ Create an optimal path for reorganisation tasks
2. Floor Priority System:
○ Detect boxes randomly placed on the warehouse floor
○ Be creative in your solution to this [For example, you may choose to complete an
ongoing task or end it to finish this floor box]
○ Resume the previous task after floor clearance
Technical Requirements:
Path Planning:
● Implement a sampling-based algorithm (RRT, RRT*) or a graph-based algorithm (A*)
● Navigate through the maze-like warehouse with multiple shelves
● Dynamic Obstacle Avoidance: Account for moving people
● Multi-objective Planning: Optimise for both task completion and safety
Control System:
● Collision Avoidance: Prevent collisions with shelves, boxes, and people
● Emergency Stop: Immediate halt capability for safety
Computer Vision:
● OpenCV Implementation: Use OpenCV for all vision tasks
● Real-time Processing: Process camera feed for navigation and detection
● Colour Recognition: Distinguish between different colored boxes (RGBY)
● AruCo Reading: Read the aruco marker to determine the shelf and rack position from
the ARUCO ID.
General Instructions:
● Document all assumptions and design decisions
● Implement robust error handling and recovery mechanisms
● Provide comprehensive code comments and documentation
● Test the system thoroughly in the simulation environment
Bonus Points:
● Custom Messages: Define specialised ROS2 messages for warehouse operations
● Advanced Planning: Implement multi-robot coordination capabilities
● Machine Learning: Use ML for improved box detection and classification
