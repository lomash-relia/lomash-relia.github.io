---
layout: single
title: "Projects"
permalink: /projects/
---

My projects focus on **end-to-end autonomous system development**, spanning **mechanical fabrication, perception, control, learning, and real-world deployment**.  
The emphasis is on **building complete robotic systems**, validating them in simulation, and deploying them under real hardware and power constraints.

---

# 🤖 Eye-in-Hand Image-Based Visual Servoing (SO-101 Robot Arm)

**MuJoCo · OpenCV · Python · Embedded Servo Control**

This project implements a **robust eye-in-hand Image-Based Visual Servoing (IBVS)** pipeline for a 5-DoF SO-101 robotic arm, integrating **mechanical fabrication, actuator control, perception, and closed-loop visual control**.

---

## Physical Fabrication & Hardware Integration

![SO-101 hardware validation setup](/assets/images/projects/so101-hardware-lab.jpg)
*Custom-fabricated SO-101 robotic arms assembled and validated in the NanoR Group Lab, Dept. of EEE, ABV-IIITM Gwalior.*

- 3D printed structural components in-house at the **NanoR Group Lab**
- Independently assembled dual-arm configuration
- Integrated **Waveshare ST3215 serial bus servos** for all joints
- Configured half-duplex UART-based daisy-chain communication
- Designed dual-arm power architecture using a **12V SMPS**
- Managed stable current distribution for simultaneous actuation
- Performed mechanical alignment and joint calibration
- Validated perception-to-actuation response prior to IBVS deployment

This stage ensured mechanical reliability and actuator stability before deploying vision-based control.

---

## System Simulation & Camera Modeling

![SO-101 robot arm in MuJoCo simulation](/assets/images/projects/ibvs-mujoco-setup.png)
*SO-101 robot arm simulated in MuJoCo for perception-driven manipulation.*

- Modeled full robot–camera system in MuJoCo
- Mounted calibrated eye-in-hand camera with offset compensation
- Implemented forward/inverse kinematics validation
- Used **ArUco marker detection** for feature extraction
- Applied **lever-arm compensation** for camera displacement correction

Simulation enabled safe validation of the control pipeline prior to hardware testing.

---

## IBVS Approach Phase (Large Initial Error)

![IBVS approach phase with large feature error](/assets/images/projects/ibvs-approach-phase.png)
*Initial IBVS phase with large feature error (~482 px).*

- Visualized raw image-space feature geometry
- Estimated depth using **marker size–based approximation**
- Scaled interaction matrix using real-time depth estimates
- Transitioned from high-error approach to stable convergence

This phase tested robustness under severe pose misalignment.

---

## Eye-in-Hand Visual Servoing (Convergence)

![Eye-in-hand camera view with feature convergence](/assets/images/projects/ibvs-eye-in-hand.png)
*Feature alignment during closed-loop convergence.*

- Implemented **Chaumette’s pixel-based control law**
- Designed a **damped pseudo-inverse controller** to avoid singularities
- Used **radial multi-depth search** for robustness
- Enforced minimum gripper height safety constraint
- Implemented automatic restart on tracking failure

The controller maintained stability across both translational and rotational components.

---

## Control Behavior & Stability

![Camera velocity during IBVS](/assets/images/projects/ibvs-camera-velocity.png)
*Linear and angular velocity components during convergence.*

- Observed smooth velocity decay profiles
- Avoided oscillatory behavior during rotational alignment
- Maintained consistent convergence rate across test conditions

---

## End-Effector Trajectory Validation

![End-effector 3D trajectory](/assets/images/projects/ibvs-ee-trajectory.png)
*3D trajectory from initial pose to final alignment.*

- Demonstrated smooth monotonic convergence
- Achieved final alignment within **30–40 px feature error**
- Validated repeatability across multiple initial conditions

---

### Outcome

A **simulation-validated and hardware-deployed eye-in-hand IBVS pipeline**, demonstrating tight integration of:

- Mechanical fabrication  
- Actuator-level control  
- Perception-driven feedback  
- Safety-constrained closed-loop control  
- Real-world robotic execution  

🔗 GitHub: https://github.com/lomash-relia/vision_mujoco

---

# 🚀 AI-Powered Planetary Rover (Pragyan-Inspired)

**PyTorch · OpenCV · Raspberry Pi · Edge AI Deployment**

This project involved designing and deploying a **low-cost autonomous planetary rover prototype**, emphasizing **edge AI inference, perception-driven navigation, and simulation-to-real transfer**.

---

## Simulation & Perception Validation

![Planetary rover simulation with perception overlays](/assets/images/projects/rover-sim-perception.png)
*Simulated lunar terrain used for navigation validation.*

- Developed obstacle detection and terrain perception pipelines
- Compared stereo-based simulation with monocular deployment
- Analyzed perception failures and depth uncertainty

---

## Onboard Edge AI (Raspberry Pi 4B)

![Real-time object detection and depth estimation on Raspberry Pi](/assets/images/projects/rover-rpi-gui.png)
*Real-time detection and monocular depth estimation running on edge hardware.*

- Integrated YOLO-based object detection
- Deployed monocular depth estimation under constrained compute
- Optimized models for near real-time inference
- Maintained system temperature below **65°C**
- Supported autonomous and manual control via remote GUI (VNC)

Demonstrated practical trade-offs between inference latency and depth accuracy.

---

## Physical Rover Prototype

![Planetary rover hardware prototype](/assets/images/projects/rover-hardware.png)
*Low-cost rover prototype with onboard compute and actuation.*

- Designed modular chassis and drivetrain
- Integrated motor drivers and power management
- Enabled end-to-end perception-to-actuation testing

---

### Outcome

A full **simulation-to-real autonomous rover pipeline**, highlighting:

- System-level optimization under hardware constraints  
- Edge AI feasibility for planetary-style navigation  
- Trade-offs between perception accuracy and real-time performance  

---

# 🌪 Deep Learning for Tropical Cyclone Intensity Estimation

**PyTorch · TensorFlow**

- Designed a **4-channel satellite imagery pipeline**
- Implemented image-to-intensity regression models
- Replicated rotation-blended CNN architectures
- Benchmarked performance against published results
- Published in the **WGNE Blue Book**

This project emphasized reproducibility and scientific benchmarking in applied computer vision research.

---

# 🧠 LLM-Based Knowledge Extraction System

**FastAPI · LangChain · Retrieval-Augmented Generation**

- Built a pipeline for transforming unstructured text into structured knowledge graphs
- Implemented **Retrieval-Augmented Generation (RAG)**
- Developed REST APIs for system interaction
- Improved factual grounding and response reliability

---

# Notes

- Code repositories and additional technical details are linked where applicable.
- Extended experimental results and demos are available upon request.
- Ongoing robotics and autonomous system work continues under my M.Tech thesis.
