---
title: "6-DOF Robot Arm"
description: "A multi-version robotic arm project exploring different control systems, materials, and capabilities through iterative design improvements."
cover: "./cover.png"

startDate: "2023-01"
endDate: "2024-06"
status: "in-progress"
featured: true
tags: ["robotics", "mechanical-design", "control-systems", "3d-printing", "arduino", "raspberry-pi", "python", "cad"]
githubUrl: "https://github.com/matt-nolan11/robot-arm"
versionsTitle: "Project Versions"

sections:
  - columns:
    - type: "content"
      title: "Project Overview"
      content: |
        This project represents my journey through multiple iterations of robotic arm design and control, spanning over 18 months of development. Each version built upon the lessons learned from the previous iteration, resulting in increasingly sophisticated capabilities.

        The goal was to create a fully functional 6-degree-of-freedom robotic arm capable of performing complex manipulation tasks. Starting from basic servo control, the project evolved through stepper motor precision, ROS integration, and now incorporates artificial intelligence for autonomous operation.

    - type: "gallery"
      gallery:
        - src: "./cover.png"
          alt: "6-DOF Robot Arm - Current Version"
          caption: "Latest iteration of the robot arm showing improved joint design and control system"
        - src: "./cover.png"
          alt: "Project Evolution"
          caption: "Evolution from basic servo control to AI-powered autonomous operation"
      galleryOptions:
        size: "medium"
        autoplay: true
        autoplayInterval: 4000

  - columns:
    - type: "content"
      title: "Technical Architecture"
      content: |
        The project follows a modular architecture that allows for easy component upgrades and testing different approaches.
        
    - type: "sections"
      sections:
        - columns:
          - type: "content"
            title: "Hardware Components"
            content: |
              Core hardware elements that form the foundation of each version:
              
              - High-torque servo motors for main joints
              - Precision stepper motors for end-effector control
              - Custom-designed 3D printed brackets and joints
              - Integrated sensor systems for position feedback
          - type: "content"
            title: "Software Stack"
            content: |
              Evolving software architecture across versions:
              
              - Arduino firmware for low-level motor control
              - Python control interface with inverse kinematics
              - ROS integration for modular robot control
              - AI/ML pipeline for autonomous task learning
        - columns:
          - type: "sections"
            sections:
              - columns:
                - type: "content"
                  title: "Control Theory"
                  content: |
                    Mathematical foundations underlying the robot's movement:
                    
                    - Forward and inverse kinematics calculations
                    - PID control loops for smooth motion
                    - Trajectory planning algorithms
                - type: "content"
                  title: "Vision System"
                  content: |
                    Computer vision capabilities for object recognition:
                    
                    - OpenCV-based object detection
                    - Depth perception using stereo cameras
                    - Real-time path adjustment based on visual feedback

  - columns:
    - type: "content"
      title: "Design Philosophy"
      content: |
        Each version focused on specific aspects of robotic systems:

        - **Version 1**: Mechanical fundamentals and basic control
        - **Version 2**: Precision and computer vision integration  
        - **Version 3**: Professional control systems and path planning
        - **Version 4**: Autonomous learning and AI integration

        ## Technical Challenges

        Throughout the project, several key challenges emerged:

        1. **Mechanical Precision**: Balancing cost, precision, and durability in mechanical design
        2. **Control Systems**: Evolving from simple position control to advanced trajectory planning
        3. **Software Architecture**: Building maintainable, extensible control software
        4. **Integration Complexity**: Managing the increasing complexity of multi-system integration

  - columns:
    - type: "content"
      title: "Impact and Applications"
      content: |
        This project has applications in:
        - Educational robotics demonstrations
        - Automated manufacturing processes
        - Research in human-robot interaction
        - Open-source robotics community contributions

        The iterative approach has proven valuable not just for the technical outcomes, but for the learning process and documentation of design evolution in robotics projects.

versions:
  - version: "v0.5"
    title: "Early Breadboard Prototype"
    description: "Very first experiments with servo control and basic positioning using Arduino."
    startDate: "2022-11"
    endDate: "2022-12"
    status: "completed"
    images:
      - "./cover.png"
      - "./cover.png"
      - "./cover.png"

  - version: "v1.0"
    title: "Basic Gripper Prototype"
    description: "Initial proof-of-concept with simple servo-driven gripper and basic positioning. Focus was on learning fundamentals of robotic kinematics and control."
    startDate: "2023-01"
    endDate: "2023-04"
    status: "completed"
    githubUrl: "https://github.com/matt-nolan11/robot-arm/tree/v1.0"
    achievements:
      - "Successfully implemented basic forward kinematics"
      - "Created modular 3D-printed joint system"
      - "Achieved 3-DOF movement with acceptable precision"
    learnings:
      - "Servo backlash significantly affects precision"
      - "PLA not ideal for load-bearing joints"
      - "Need better cable management system"
    sections:
      - columns:
        - type: "content"
          title: "Design Overview"
          content: |
            This first iteration served as my introduction to robotics fundamentals. The primary goal was to understand the basics of **forward kinematics** and create a working prototype that could demonstrate basic pick-and-place operations.
            
            ## Design Decisions
            
            I chose servo motors for their simplicity and cost-effectiveness, though this decision would later prove limiting for precision applications. The mechanical design focused on:
            
            - **Modular joints** using 3D-printed components
            - **Simple cable routing** through the arm structure  
            - **Basic end effector** with parallel jaw gripper
        - type: "gallery"
          gallery:
            - src: "./cover.png"
              alt: "V1.0 Full Assembly"
              caption: "Complete v1.0 robot arm with servo-driven joints"
            - src: "./cover.png"
              alt: "Gripper Mechanism"
              caption: "Parallel jaw gripper with basic position feedback"
            - src: "./cover.png"
              alt: "Control Electronics"
              caption: "Arduino-based control system with servo driver board"
          galleryOptions:
            size: "medium"
            autoplay: true
            showThumbnails: true
      - columns:
        - type: "content"
          title: "Control System Implementation"
          content: |
            The control system was deliberately simple, using an Arduino Uno with basic position commands. I implemented:
            
            ```arduino
            // Basic forward kinematics for 3-DOF positioning
            void moveToPosition(float x, float y, float z) {
              // Calculate joint angles
              float theta1 = atan2(y, x);
              float r = sqrt(x*x + y*y);
              // ... additional calculations
            }
            ```
            
            This version taught me the importance of **mechanical precision** and **backlash compensation** in robotic systems.

  - version: "v2.0"
    title: "Stepper Motor Upgrade"
    description: "Complete redesign using stepper motors for improved precision and repeatability. Added computer vision for object detection and automated pick-and-place operations."
    startDate: "2023-05"
    endDate: "2023-11"
    status: "completed"
    githubUrl: "https://github.com/matt-nolan11/robot-arm/tree/v2.0"
    liveUrl: "https://youtube.com/watch?v=demo-v2"
    achievements:
      - "10x improvement in positioning accuracy"
      - "Implemented inverse kinematics solver"
      - "Added camera-based object detection"
      - "Created custom end effector with force feedback"
    learnings:
      - "Stepper motor heat management is critical"
      - "Computer vision lighting requirements"
      - "Importance of rigid base construction"
    images:
      - "./cover.png"
      - "./cover.png"
      - "./cover.png"
      - "./cover.png"
    sections:
      - columns:
        - type: "content"
          title: "Major Improvements"
          content: |
            The second iteration represented a major leap in capability and complexity. Frustrated by the precision limitations of servo motors, I completely redesigned the arm around **stepper motors** and added **computer vision** capabilities.
            
            ### Precision Control System
            The move to stepper motors required learning about:
            - **Microstepping** for smooth motion
            - **Acceleration profiles** to prevent missed steps  
            - **Thermal management** for continuous operation
        - type: "gallery"
          gallery:
            - src: "./cover.png"
              alt: "Stepper Motor Assembly"
              caption: "High-precision stepper motors with microstepping control"
            - src: "./cover.png"
              alt: "Computer Vision Setup"
              caption: "OpenCV-based object detection and tracking system"
          galleryOptions:
            size: "medium"
            autoplay: true
      - columns:
        - type: "content"
          title: "Computer Vision Integration"
          content: |
            Adding OpenCV-based object detection opened up autonomous operation possibilities:
            
            ```python
            def detect_objects(frame):
                # HSV color filtering for object detection
                hsv = cv2.cvtColor(frame, cv2.COLOR_BGR2HSV)
                
                # Define color ranges for different objects
                red_range = [(0, 50, 50), (10, 255, 255)]
                blue_range = [(100, 50, 50), 130, 255, 255)]
                
                # Find contours and calculate centroids
                # ... object detection logic
                return object_positions
            ```
            
            ### Mechanical Redesign
            
            This version featured:
            - **PETG construction** for improved durability
            - **Integrated cable management** with internal routing
            - **Force-sensing gripper** with basic feedback
            - **Rigid aluminum base** for stability
            
            The combination of precise stepper control and computer vision enabled **automated sorting tasks** that demonstrated the arm's growing capabilities.

  - version: "v3.0"
    title: "ROS Integration & Advanced Control"
    description: "Professional-grade control system using ROS, with trajectory planning, collision avoidance, and multi-arm coordination capabilities."
    startDate: "2023-12"
    endDate: "2024-06"
    status: "completed"
    githubUrl: "https://github.com/matt-nolan11/robot-arm/tree/v3.0"
    liveUrl: "https://robot-arm-controller.example.com"
    achievements:
      - "Full ROS integration with MoveIt! planning"
      - "Real-time collision detection and avoidance"
      - "Smooth trajectory execution with velocity profiling"
      - "Web-based control interface"
      - "Simulated twin in Gazebo"
    learnings:
      - "ROS learning curve is steep but worthwhile"
      - "Simulation-to-real transfer challenges"
      - "Importance of proper system architecture"
    gallery:
      - src: "./cover.png"
        alt: "ROS Control System"
        caption: "Complete ROS-based control system with real-time monitoring"
      - src: "./cover.png"
        alt: "MoveIt! Planning"
        caption: "MoveIt! trajectory planning interface showing collision-free paths"
      - src: "./cover.png"
        alt: "Gazebo Simulation"
        caption: "High-fidelity Gazebo simulation for safe algorithm development"
      - src: "./cover.png"
        alt: "Web Interface"
        caption: "Browser-based control interface for remote operation"
    galleryOptions:
      size: 500
      autoplay: false
      showThumbnails: true
    sections:
      - columns:
        - type: "content"
          title: "ROS Architecture"
          content: |
            Version 3.0 marked the transition from hobby project to **professional-grade robotics system**. The integration of ROS (Robot Operating System) brought industry-standard capabilities and opened up advanced functionality.
            
            The system architecture leveraged ROS's modular design:
            
            ```yaml
            # ROS Node Structure
            /robot_arm_controller      # Main control node
            /trajectory_planner        # MoveIt! integration
            /collision_detector        # Real-time safety
            /gripper_controller       # End effector control
            /camera_processor         # Vision pipeline
            /web_interface            # User control
            ```
        - type: "image"
          src: "./cover.png"
          alt: "ROS System Architecture"
          caption: "Complete ROS system showing node connections and data flow"
      - columns:
        - type: "content"
          title: "MoveIt! Integration & Simulation"
          content: |
            ### MoveIt! Integration
            
            [MoveIt!](https://moveit.ros.org/) provided professional path planning capabilities:
            - **OMPL planners** for optimal trajectory generation
            - **Collision checking** with environment models
            - **Velocity profiling** for smooth execution
            - **Joint constraints** enforcement
            
            ### Simulation Environment
            
            Gazebo simulation enabled safe development and testing:
            
            ```xml
            <!-- URDF model with physics simulation -->
            <robot name="robot_arm">
              <link name="base_link">
                <inertial>
                  <mass value="2.5"/>
                  <inertia ixx="0.1" ixy="0" ixz="0" iyy="0.1" iyz="0" izz="0.1"/>
                </inertial>
                <!-- ... geometry and collision definitions -->
              </link>
              <!-- Additional joints and links -->
            </robot>
            ```
            
            ## Advanced Features
            
            This version introduced:
            - **Real-time trajectory execution** with feedback control
            - **Web-based control interface** for remote operation
            - **Digital twin simulation** for testing and validation
            - **Multi-arm coordination** framework (future-ready)
            
            The **simulation-to-real transfer** proved challenging but valuable for validating control algorithms before physical testing.

  - version: "v4.0"
    title: "AI-Powered Autonomous Operation"
    description: "Current development focusing on machine learning for autonomous task learning and execution. Implementing reinforcement learning for pick-and-place optimization."
    startDate: "2024-07"
    status: "in-progress"
    githubUrl: "https://github.com/matt-nolan11/robot-arm/tree/v4.0-dev"
    achievements:
      - "Implemented basic RL training pipeline"
      - "Created custom simulation environment"
      - "Initial autonomous sorting demonstrations"
    learnings:
      - "Sim-to-real gap requires careful domain adaptation"
      - "Data collection for robotics is challenging"
      - "Edge computing constraints affect model complexity"
    sections:
      - columns:
        - type: "gallery"
          gallery:
            - src: "./cover.png"
              alt: "AI Training Setup"
              caption: "Robot arm in training environment with multiple objects for reinforcement learning"
            - src: "./cover.png"
              alt: "Neural Network Visualization"
              caption: "Real-time visualization of the neural network decision-making process"
            - src: "./cover.png"
              alt: "Edge Computing Hardware"
              caption: "NVIDIA Jetson Nano integration for real-time ML inference"
          galleryOptions:
            size: "medium"
            autoplay: true
            autoplayInterval: 5000
        - type: "content"
          title: "Reinforcement Learning Pipeline"
          content: |
            The current iteration explores the frontier of **autonomous robotics** through machine learning integration. This represents a shift from programmed behaviors to **learned capabilities**.
            
            The RL system uses a custom environment built on top of the existing ROS infrastructure:
            
            ```python
            import gymnasium as gym
            from stable_baselines3 import PPO
            
            class RobotArmEnv(gym.Env):
                def __init__(self):
                    # Define action and observation spaces
                    self.action_space = gym.spaces.Box(
                        low=-1, high=1, shape=(6,), dtype=np.float32
                    )
                    self.observation_space = gym.spaces.Box(
                        low=-np.inf, high=np.inf, shape=(15,), dtype=np.float32
                    )
                    
                def step(self, action):
                    # Execute action and return observation, reward, done, info
                    # ...
            ```
      - columns:
        - type: "content"
          title: "Edge Computing & Current Capabilities"
          content: |
            ## Edge Computing Integration
            
            Running ML inference on **NVIDIA Jetson Nano** presents unique challenges:
            - **Model optimization** for limited compute resources
            - **Real-time inference** requirements
            - **Power consumption** considerations
            - **Thermal management** during continuous operation
            
            ### Training vs. Inference
            
            The approach separates training and deployment:
            - **Cloud training** using high-performance GPUs
            - **Model quantization** and optimization for edge deployment
            - **Transfer learning** for rapid adaptation to new tasks
            
            ## Current Capabilities
            
            The system currently demonstrates:
            - **Autonomous object sorting** based on color and shape
            - **Adaptive grip force** based on object properties
            - **Basic task learning** from demonstration
            - **Safe exploration** with collision avoidance
            
            ## Research Challenges
            
            Key areas of ongoing development:
            - **Sim-to-real transfer** for robust deployment
            - **Sample efficiency** in physical robot training
            - **Multi-task learning** for versatile operation
            - **Human-robot collaboration** safety protocols
            
            The goal is to create a system capable of **learning new tasks** through demonstration and **adapting to environmental changes** autonomously.

---
