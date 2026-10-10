# **TASK 1:UAV ASSEMBLY & FLIGHT CONTROLLER CONFUGIRATION**
##### **OBJECTIVE :**
To collaboratively assemble and configure a fully functional quadcopter with GPS, receiver, and flight controller integration.
##### **OUTCOMES & LEARNING :**
  - This task will help me to learn how a quadcopter done is really built.
  - And also with the help of this task I will learn the assmebly of each components which are required for quadcopter,
  - And overall this task became bridge between level 2 and level 3 task.
  

  


# **TASK 2 : Autonomous Flight Planning & Execution**
##### **OBJECTIVE :**
 To understand and practice autonomous flight mission planning using Mission Planner and the ArduPilot simulator.

##### **OUTCOMES & LEARNING :**
- In this task I learnt about bascis struture of **Mission planner**.
- And also about Heads Up Display (HUD) used in mission planner.
- This task helped me to learn about **GEO - FENCING & SURVEYING(GRID)**.
- Finally I tried to do the Geo - fencing and surveying of UVCE.
  
 #### **About Heads Up Display (HUD) :**
  The image below shows the main “Heads-up Display (HUD)” view of the Mission Planner Ground Station. Once we have connected to a vehicle this screen will display the telemetry sent by ArduPilot.

![image alt](https://github.com/sujan935/sujan_level-1--images/blob/main/Screenshot%202026-06-12%20204406.png?raw=true)

##### **Detailed Image Shows the Struture and Use of HUD :**
  ![image alt](https://github.com/sujan935/sujan_level-1--images/blob/main/Screenshot%202026-06-12%20204954.png?raw=true)

1) Airspeed (Groundspeed if no airspeed sensor is fitted)

2) Crosstrack error and turn rate (T)

3) Heading direction

4) Bank angle

5) Telemetry connection link quality (averaged percentage of good packets)

6) GPS time

7) Altitude (Blue bar is the rate of climb)

8) Airspeed

9) Groundspeed

10) Battery status

11) Artificial Horizon

12) Aircraft Attitude

13) GPS Status

14) Distance to Waypoint > Current Waypoint Number

15) Current Flight Mode
  
#### **Geofencing & Surveying** :

Geofencing is a hardware-enforced safety protocol used to establish virtual boundaries for unmanned vehicles. If a vehicle crosses a defined boundary, a fence breach occurs, prompting the autopilot to override manual inputs and execute a preconfigured fail-safe maneuver.

#### **Core Architecture**

• **Inclusion Zones:** The primary operational airspace. The vehicle is permitted to fly only within this boundary.

• **Exclusion Zones:** Specific restricted areas located inside the inclusion zone (e.g., buildings, power lines, public roads) that the vehicle is strictly forbidden to enter.

• **Boundary Types:**
	• Cylindrical (TinCan): A radial boundary centered around the vehicle's Home or Takeoff point.

	• Polygonal: A custom multi-point geometric shape drawn directly on the telemetry map.
	• Altitude Limits: Rigid ceilings (maximum height) and floors (minimum height) to prevent regulatory airspace violations.

#### **Operational Actions upon Breach**

When a fence is breached, the autopilot triggers a user-defined emergency protocol:
• **RTL (Return-to-Launch):** The vehicle automatically flies back to its original takeoff point.

• **Land:** The vehicle immediately terminates flight and descends safely at its current coordinates.

• **Smart RTL / Hold:** The vehicle retracts its path safely or hovers in place to await operator intervention.

 #### **Autonomous Surveying (Aerial Mapping & Data Collection)**

Surveying is an automated mission planning utility used for photogrammetry, 3D modeling, and remote sensing. Instead of manually mapping individual waypoints, the operator defines a boundary, and Mission Planner algorithmically computes the optimal back-and-forth grid pattern required to capture uniform sensor data.

#### **Key Calculation Parameters**

• **Ground Sampling Distance (GSD):** The spatial resolution of the data (measured in centimeters per pixel). Mission Planner dynamically shifts flight altitude based on the required GSD.

• **Camera Sensor Profiles:** The system calculates the camera’s focal length, sensor width, and image resolution to accurately time photo intervals.

• **Image Overlap:** Crucial for image stitching software. It requires adjusting two distinct vectors:

	• Frontal Overlap: The percentage of photographic overlap between successive images along the same flight line.
	• Lateral (Side) Overlap: The percentage of overlap between adjacent parallel flight rows.

#### **Workflow Execution :**

1. **Polygon Delineation:** The operator traces the target geographical area on the map.
2. **Grid Generation:** The operator opens the Auto WP -> Survey (Grid) interface to input camera specifications, cruise speed, and overlap requirements.
3. **Waypoint Synthesis:** Mission Planner converts the calculated grid into sequential commands (e.g., WAYPOINT, DO_DIGICAM_CONTROL) and writes the complete autonomous mission sequence to the vehicle’s flight controller.
   
[click here](https://youtu.be/WK1bsJM3Tbc?si=6WsMllZhMlkMPY2d) to watch the geofencing and surveying using mission planner


    
# **TASK 3 : INTRODUCTION TO MATLAB**
 ##### **OBJECTIVE :**
 To gain foundational knowledge of MATLAB and Simulink.
 ##### **OUTCOMES & LEARNING :**
 - With the help of this task I learnt basic syntax and expressions of matlab .
 - And also I am at the finishing line of completing MATLAB course .
 - Overall this task helped me to know about imporatnce of MATLAB in aviation.
  
  #### **About MATLAB & SIMULINK:**

   MATLAB and Simulink are core platforms in aviation for Model-Based Design (MBD), allowing engineers to simulate, test, and build safety-critical flight systems before touching physical hardware

#### **Importance of MATLAB & Simulink in Aviation**

• **Guidance, Navigation, and Control (GNC):** Engineers use MATLAB and Simulink to design and test flight control laws, autopilot routines, and six-degrees-of-freedom (6DoF) aircraft dynamics models.

• **Automated Flight Code Generation:** Tools like Embedded Coder convert visual Simulink models directly into production-ready ANSI/ISO C, C++, or HDL code for deployment on aircraft microcontrollers and digital signal processors (DSPs).

• **Safety & Regulatory Certification:** The software integrates with specialized packages (such as the DO Qualification Kit) to streamline compliance with strict aviation safety and systems engineering standards like DO-178C (software), ARP4754B (aircraft/systems), and ARP4761A (safety assessments).

• **Verification and Testing (SIL/PIL/HIL):** Teams can run automated software-in-the-loop (SIL), processor-in-the-loop (PIL), and hardware-in-the-loop (HIL) tests, as well as Monte Carlo simulations to stress-test flight software across thousands of failure scenarios.

• **Flight Test Data Analysis:** Flight test engineers use MATLAB to ingest, process, and visualize gigabytes of time-stamped telemetry and data-bus records gathered during live test flights.

• **Specialized Domain Toolsets:** Add-ons like the Aerospace Blockset and Aerospace Toolbox provide pre-built atmosphere, gravity, terrain, and pilot-behavior models to speed up system design.

#### **My  MATLAB Completion Certificate :**


![image alt](https://github.com/sujan935/sujan_level-1--images/blob/main/Screenshot%202026-10-10%20132648.png?raw=true)

#### **My  Simulink Completion Certificate :**

![image alt](https://github.com/sujan935/sujan_level-1--images/blob/main/Screenshot%202026-10-10%20193221.png?raw=true)    
    
# **TASK 4 : Advanced PID Tuning**

##### **OBJECTIVE :**
To develop a strong understanding of PID controllers and their application in UAV stability and autonomous control systems.

##### **OUTCOMES & LEARNING :**
- This task help me to learn about **PID** in detail . And also this is continuation of Level 1 task.
- And also I learnt why PID is very important in Aviation and also other control system.
- And also I saw the video of making **Self balancing robot**.

#### **Basics of PID control and it's importance**

A PID (Proportional-Integral-Derivative) controller is the primary control loop feedback mechanism that governs drone flight stabilization. Drones are inherently unstable aerodynamic platforms that cannot maintain flight without automated assistance. The PID loop continuously calculates an error value—the difference between the pilot's intended command (setpoint) and the vehicle's actual orientation (process variable measured by the IMU gyroscopes)—and applies a mathematical correction by adjusting individual motor speeds thousands of times per second.
* **Proportional (P - Present Error):** 
  * Generates a corrective force directly proportional to the size of the current error. If the drone is tilted 10° off-target, P pushes the motors twice as hard as it would for a 5° error.
  * Determines the primary responsiveness and stiffness of the drone. If P is too low, the vehicle feels sluggish; if it is too high, the vehicle will violently oscillate.
* **Integral (I - Past Error):** 
  * Sums up the duration and magnitude of environmental errors over time. It continuously ramps up motor power until the persistent error is completely neutralized.
  * Governs attitude retention. I counteracts constant external forces like aerodynamic drag, steady crosswinds, or physical center-of-gravity offsets caused by asymmetrical payloads.
* **Derivative (D - Future Error):** 
  * Analyzes the rate of change of the error. It acts as a predictive dampener or brake, fighting against rapid angular accelerations.
  * Smooths out the flight envelope. D dampens the aggressive overshoot tendencies caused by the P term, eliminating wobbles when the drone finishes a sharp maneuver.

#### **Importance of PID in Drone Systems**

* **Dynamic Flight Stabilization:** Multi-rotor aircraft lack mechanical surfaces (like flaps or rudders) to glide or self-stabilize. The PID loop acts as an artificial stabilization layer, allowing the drone to maintain a crisp hover or continuous trajectory without manual pilot micro-corrections.
* **Environmental Disturbance Rejection:** When exposed to sudden wind shears or thermal drafts, the PID controller registers the unauthorized angular displacement and spins up opposing motors within milliseconds to counteract the forces, preserving spatial positioning.
* **Predictable Linear Control:** The PID loop translates abstract pilot inputs (joystick deflections) into concrete angular targets. This ensures that a specific stick movement yields an exact, repeatable flight response, regardless of standard aerodynamic turbulence.
* **Adaptive Payload Management:** Drones frequently operate under changing physical dynamics—such as carrying variable camera gimbals, deploying delivery packages, or emptying liquid tanks on agricultural aircraft. The PID loop dynamically scales its motor output to balance the aircraft as its mass distribution shifts mid-flight.


##### **Detailed Information About PID Control From Level 1 Report**


![image alt](https://github.com/sujan935/sujan_level-1--images/blob/main/PID%201.jpg?raw=true)
![image alt](https://github.com/sujan935/sujan_level-1--images/blob/main/PID%202.jpg?raw=true)
![image alt](https://github.com/sujan935/sujan_level-1--images/blob/main/PID%203.jpg?raw=true)
![image alt](https://github.com/sujan935/sujan_level-1--images/blob/main/PID%204.jpg?raw=true)

#### **PID Of  Self Balancing Robot**
  In a self-balancing robot, PID stands for Proportional, Integral, Derivative. It is a mathematical control algorithm that calculates the error between the robot's desired vertical position (setpoint) and its current tilt, adjusting the motors in real-time to keep the robot upright.

  #### **Planning of Self -Balancing Robot :
  ![image alt](https://github.com/sujan935/sujan_level-1--images/blob/main/self%20balancing.jpg?raw=true)

##### **Circuit Daigram Of Self Balancing Robot :**
  ![image alt](https://github.com/sujan935/sujan_level-1--images/blob/main/self%20balncing%20robot.jpg?raw=true)

  # **TASK 5 : Rules in the Rule Book Written by Blood**
##### **OBJECTIVE :**
To explore the methodology behind air crash investigations and learn how aviation safety evolves from past incidents.
##### **OUTCOMES & LEARNING :**
- This task helped me to learn how to make report of a air crash.
- With the help of this task I did report of Air India Express 812 .
  
##### **Detailed Report on Air India Express 812 , Mangalore**
Air India Express Flight 812 was a scheduled international flight from Dubai International Airport, Dubai, to Mangalore International Airport, Mangalore. On 22 May 2010, the Boeing 737-800 passenger jet operating the flight crashed on landing at Mangalore. 
Click the below link to view full report.


[click here](https://github.com/sujan935/Task_5-level-2/blob/main/Sujan%20final%20ppt.pdf) to view detailed report on Air crash of **Air India Express 812 , Mangalore**.


# **TASK 6 :FLIGHT DATA LOGGING & ANALYSIS**
##### **OBJECTIVE:** 
To explore the methodology behind air crash investigations and learn how aviation safety evolves from past incidents.
##### **OUTCOMES & LEARNING :**
- This task helped me to learn how to extract log files using mission planner .
- With the help of this task I am able to analyse three different log files which were given in marvel website .
- And also with the help of this task I could able to identify the problems in the system by analysing each graphs.
  
#### **Importance of Flight Data Logging & Analysis**

1. **Air Crash Investigation & Forensic Reconstruction**
   Telemetry logs act as the digital "black box" during an anomaly or accident. Microsecond-level timestamps allow investigators to reconstruct exact timeline sequences, isolate component failures, and map 3D flight paths in software like Google Earth.

2. **System Health & Pre-Flight Verification**
   Logs record sensor calibration baselines, battery discharge performance, and internal power module health. Reviewing these parameters ensures power supplies remain stable and hardware operates safely before mission execution.

3. **Flight Control Tuning & PID Optimization**
   Comparing target control commands against actual vehicle responses allows engineers to fine-tune Proportional, Integral, and Derivative (PID) control loops for optimal attitude and altitude stability.

4. **Vibration Analysis & Structural Diagnostics**
   Raw motor output and accelerometer data reveal mechanical frame flex, propeller imbalances, or failing bearings, allowing teams to identify mechanical issues before structural fatigue leads to in-flight failure.

5. **Failsafe & Autonomous System Validation**
   Telemetry logs provide quantitative verification of Extended Kalman Filter (EKF) sensor fusion, GPS position accuracy, and automated failsafe responses (such as radio loss or low battery Return-to-Launch triggers).

   [click here](https://github.com/sujan935/Sujana_report_pdf/blob/main/flight_controller_log_analysis.pdf) to read detailed analysis of 3 different log files which was given in marvel website.

  # **TASK 7 : INTRODUCTION TO ROS 2 FOR UAVs**
  ##### **OBJECTIVE :**
  To get started with the Robot Operating System (ROS) 2 ecosystem and understand its application in UAV communication through node-based architecture.
  ##### **OUTCOMES & LEARNING :**
  - With the help of this task I got an complete overview of ROS 2.
  - And also I learnt about basic syntax which were used in ROS 2 .
  
  ### **Briefy Introduction to ROS 2 Humble Hawksbill**
  

**ROS 2 Humble Hawksbill** is a Long-Term Support (LTS) release of the Robot Operating System (ROS 2), officially released in **May 2022** and supported through **May 2027**. Built primarily for **Ubuntu 22.04 LTS (Jammy Jellyfish)** and Tier-1 operating systems (Windows, macOS, RHEL 9), Humble serves as one of the most widely adopted and stable distributions for robotics development in academia and industry.

---

### **1. Core Architecture & Key Upgrades**

* **Native Middleware (DDS):** Uses **eProsima Fast DDS** as its default middleware vendor, providing robust Data Distribution Service (DDS) standards for real-time, peer-to-peer communication without a single point of failure (no central master node).
* **Language Support:** Features full support for **C++17** and **Python 3.10**, enabling high-performance node development alongside flexible scripting.
* **Security (SROS 2):** Native support for DDS-Security standard, allowing encrypted communication, node authentication, and access control out of the box.

---

### **2. Key Features & Ecosystem Improvements**

1. **Type Adaptation (ros2_type_adapter):** Allows custom user types to be passed directly through pipeline interfaces, reducing unnecessary data serialization/deserialization overhead.
2. **Improved Execution & Launch:** Enhanced Launch system diagnostic feedback and optimized multi-threaded executors for better CPU core usage.
3. **Maturity of Core Tooling:**
   * **Rviz2:** Enhanced 3D visualization stability.
   * **ros2bag:** Improved storage backend support (MCAP & SQLite3) for efficient logging and playback.
   * **Nav2 & MoveIt 2:** Mature release versions fully targeted at production autonomous navigation and robotic arm manipulation.

---

### **3. Core Communication Concepts**

| Feature | Description |
| :--- | :--- |
| **Nodes** | Modular processes executing specific computational tasks. |
| **Topics** | Asynchronous many-to-many publish-subscribe message transport. |
| **Services** | Synchronous request-response interaction pattern. |
| **Actions** | Asynchronous goal-oriented requests with continuous feedback loops. |
| **Parameters** | Dynamic per-node configuration values configured at runtime. |

---

### **4. Why Choose Humble Hawksbill?**

* **Long-Term Stability:** 5-year support lifecycle makes it ideal for enterprise products and commercial deployment.
* **Large Community Ecosystem:** Supported by major hardware manufacturers, simulation tools (Gazebo Fortress/Ignition), and open-source packages.
* **Determinism & Performance:** Enhanced real-time capability suitable for safety-critical robotic applications.

[click here](https://github.com/sujan935/Sujana_report_pdf/blob/main/ROS2_Report%20.pdf) to view complete docuementaion of task 7.
  









   

