# Al-Jazari | Autonomous Rescue Hexapod 🕷️

**Al-Jazari** is an autonomous hexapod search and rescue robot team developed by the Robotic Development Community of Ahmad Dahlan University, representing the institution in the Indonesian SAR Robot Contest (KRSRI). Designed to navigate unstructured disaster environments, the robot autonomously detects targets and executes complex locomotion to assist in simulated rescue missions.

### ⚙️ System Architecture & Technology Stack

Our robotic system relies on a distributed architecture, separating high-level cognitive processes from low-level hardware control:

*   **High-Level Control & Simulation (ROS 2):** The core navigation and mapping systems are built upon the Robot Operating System 2 (ROS 2). We utilize Gazebo and RViz for comprehensive kinematic simulations and environment tracking prior to physical deployment.
*   **AI Vision Pipeline:** Environmental perception is driven by a custom computer vision stack. We deploy **YOLOv8** on a **Jetson Nano** for real-time, on-device object recognition, complemented by OpenCV for precise spatial tracking and aspect ratio calculations.
*   **Low-Level Execution & Firmware:** Precise leg articulation and sensory polling are handled by embedded microcontrollers. The firmware implements **FreeRTOS** to guarantee deterministic task scheduling, running on a custom-designed PCB layout engineered for structural power distribution and signal isolation.
