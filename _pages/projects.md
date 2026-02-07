---
layout: single
title: "Projects"
permalink: /projects/
---

My projects focus on **end-to-end autonomous system development**, spanning **perception, control, learning, and real-world deployment**.  
The emphasis is on **building complete robotic systems**, validating them in simulation, and deploying them under practical constraints.

---

## 🤖 Eye-in-Hand Image-Based Visual Servoing (SO-101 Robot Arm)

**MuJoCo, OpenCV, Python**

This project implements a **robust eye-in-hand Image-Based Visual Servoing (IBVS)** pipeline for a 5-DoF SO-101 robotic arm, integrating perception, control theory, and safety constraints.

---

### System Setup
![SO-101 robot arm in MuJoCo simulation](/assets/images/projects/ibvs-mujoco-setup.png)
*SO-101 robot arm simulated in MuJoCo for vision-based manipulation.*

- Simulated the complete robot–camera system in MuJoCo
- Mounted an eye-in-hand camera with calibrated offset
- Used **ArUco marker detection** for feature extraction
- Applied **lever-arm compensation** to account for camera displacement

---

### IBVS Approach Phase (Initial Error)
![IBVS approach phase with large feature error](/assets/images/projects/ibvs-approach-phase.png)
*Initial IBVS approach phase showing large feature error (~482 px), depth estimation, and image-space geometry.*

- Visualized raw image-space feature configuration during large initial misalignment
- Estimated depth using **marker size–based approximation**
- Used depth to correctly scale the interaction matrix
- Transitioned from high-error approach to stable convergence phase

---

### Eye-in-Hand Visual Servoing (Convergence)
![Eye-in-hand camera view with feature convergence](/assets/images/projects/ibvs-eye-in-hand.png)
*Eye-in-hand camera view showing feature alignment during convergence.*

- Implemented **Chaumette’s pixel-based control law**
- Used **radial multi-depth search** for robustness
- Enforced safety constraints including minimum gripper height
- Implemented automatic restart on divergence or tracking failure

---

### Control Behavior (Camera Velocity)
![Camera velocity during IBVS](/assets/images/projects/ibvs-camera-velocity.png)
*Linear and angular camera velocity components during visual servoing.*

- Designed a **damped pseudo-inverse controller** to avoid singularities
- Observed smooth velocity profiles during convergence
- Maintained stability across translational and rotational components

---

### End-Effector Trajectory
![End-effector 3D trajectory](/assets/images/projects/ibvs-ee-trajectory.png)
*3D end-effector trajectory from initial pose to target alignment.*

- Demonstrated smooth, monotonic convergence in task space
- Achieved final alignment within **30–40 px feature error**
- Validated repeatability across multiple initial conditions

---

**Outcome:**  
A complete **simulation-validated eye-in-hand IBVS pipeline**, demonstrating tight integration of perception, control theory, safety, and system diagnostics.

🔗 GitHub: https://github.com/lomash-relia/vision_mujoco

---

## 🚀 AI-Powered Planetary Rover (Pragyan-Inspired)

**PyTorch, OpenCV, Raspberry Pi**

This project involved the design and deployment of a **low-cost autonomous planetary rover prototype**, emphasizing **edge AI, perception-driven navigation, and simulation-to-real transfer**.

---

### Simulation & Perception Pipeline
![Planetary rover simulation with perception overlays](/assets/images/projects/rover-sim-perception.png)
*Simulated lunar terrain with perception overlays used for algorithm validation.*

- Developed obstacle detection and terrain perception pipelines
- Validated navigation logic in a simulated lunar environment
- Analyzed perception failures and depth uncertainty prior to deployment

---

### Onboard Edge AI (Raspberry Pi)
![Real-time object detection and depth estimation on Raspberry Pi](/assets/images/projects/rover-rpi-gui.png)
*Real-time object detection and monocular depth estimation running on Raspberry Pi.*

- Integrated **YOLO-based object detection** and **monocular depth estimation**
- Optimized models for **near real-time inference** under compute constraints
- Maintained system temperature below **65 °C** during sustained operation
- Supported autonomous and manual control via remote GUI (VNC)

---

### Physical Rover Prototype
![Planetary rover hardware prototype](/assets/images/projects/rover-hardware.png)
*Low-cost planetary rover prototype with onboard compute and motor control.*

- Designed and assembled a modular rover platform
- Integrated power management, motor drivers, and onboard compute
- Enabled end-to-end testing from perception to actuation

---

**Outcome:**  
Demonstrated a full **simulation-to-real autonomous rover pipeline**, highlighting practical trade-offs between perception accuracy, inference latency, and hardware limitations.

---

## 🌪 Deep Learning for Tropical Cyclone Intensity Estimation

**PyTorch, TensorFlow**

- Engineered a **4-channel satellite imagery pipeline** for image-to-intensity regression
- Replicated and validated **rotation-blended CNN architectures** from published research
- Benchmarked performance against reported results
- Published results in the **WGNE Blue Book**

---

## 🧠 LLM-Based Knowledge Extraction System

**FastAPI, LangChain, Retrieval-Augmented Generation (RAG)**

- Built a pipeline for transforming unstructured text into structured knowledge graphs
- Implemented **Retrieval-Augmented Generation (RAG)** for improved factual grounding
- Exposed system functionality through REST APIs using FastAPI

---

## Notes
- Code repositories and additional details are linked where applicable
- Further experimental results and demos are available upon request
