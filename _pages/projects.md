---
layout: single
title: "Projects"
permalink: /projects/
---

This page presents a selection of my **research-oriented and applied engineering projects** in robotics, autonomous systems, and artificial intelligence.  
The projects emphasize **end-to-end system development**, covering **perception, control, learning, and deployment**.

---

## Eye-in-Hand Image-Based Visual Servoing for SO-101 Robot Arm  
**MuJoCo, OpenCV, Python**  
*Dec 2025 – Jan 2026*

I developed a robust **eye-in-hand Image-Based Visual Servoing (IBVS)** pipeline for the open-source **SO-101 5-DoF robotic arm** in a MuJoCo-based simulation environment.

**Key contributions:**
- Implemented layered IBVS using **ArUco marker detection** and **pixel-space control** based on Chaumette’s formulation  
- Designed a **damped pseudo-inverse control law** with joint and velocity limits for stability  
- Integrated safety mechanisms including **minimum gripper height constraints** and **automatic divergence recovery**  
- Built real-time visualization with feature overlays and a **JSON-based feature teaching tool**

**Outcome:**  
Achieved reliable convergence to **30–40 pixel feature error**, demonstrating stable and repeatable visual servoing under initialization noise and partial failures.

🔗 GitHub: https://github.com/lomash-relia/vision_mujoco

---

## AI-Powered Planetary Rover (Pragyan-Inspired)  
**PyTorch, OpenCV, Raspberry Pi**  
*Jan 2025 – Jul 2025*

This project involved the design and deployment of a **low-cost autonomous planetary rover prototype**, inspired by real-world space exploration constraints.

**Key contributions:**
- Designed a complete rover system running on **Linux Bookworm OS** with onboard edge AI  
- Implemented **monocular metric depth estimation** and **real-time object detection** for navigation  
- Optimized deep learning models to maintain **near real-time inference** while keeping system temperature below **65°C**  
- Developed **dual control modes** supporting autonomous navigation and manual remote operation via VNC  

**Outcome:**  
Demonstrated practical trade-offs between perception accuracy and real-time feasibility on **resource-constrained embedded hardware**, bridging simulation and deployment.

---

## Deep Learning for Tropical Cyclone Intensity Estimation  
**PyTorch, TensorFlow**  
*Sep 2024 – Oct 2024*

As part of a research collaboration with the **Indian Institute of Tropical Meteorology (IITM), Pune**, I worked on deep learning models for cyclone intensity prediction.

**Key contributions:**
- Engineered a **4-channel satellite imagery pipeline** for image-to-intensity regression  
- Replicated and validated **rotation-blended CNN architectures** from published research  
- Benchmarked model performance against reported results to evaluate robustness and generalization  

**Outcome:**  
Strengthened understanding of **remote sensing data**, **model evaluation**, and **scientific benchmarking** in applied deep learning research.

---

## LLM-Based Knowledge Extraction System  
**FastAPI, LangChain, Retrieval-Augmented Generation (RAG)**  
*Apr 2024*

This project focused on building a backend system for **structured knowledge extraction from unstructured text** using large language models.

**Key contributions:**
- Developed a **knowledge graph generation pipeline** using LLMs and LangChain  
- Implemented a **Retrieval-Augmented Generation (RAG)** workflow for improved factual grounding  
- Exposed system functionality through REST APIs using FastAPI  

**Outcome:**  
Delivered a scalable backend capable of converting large text corpora into structured, queryable knowledge representations.

---

## Mobile Application for Brain Tumor Detection (Proof of Concept)  
**Flutter, TensorFlow Lite**  
*May 2023 – Jun 2023*

Developed a mobile proof-of-concept application integrating on-device machine learning for medical image analysis.

**Key contributions:**
- Integrated a **TensorFlow Lite-based brain tumor detection model** into a Flutter application  
- Optimized the model for **real-time inference on mobile devices**  
- Designed application components using **Bloc state management** and efficient network handling  

**Outcome:**  
Demonstrated feasibility of deploying deep learning models on mobile platforms with strict performance constraints.

---

## Notes
- Detailed code repositories and experimental results are linked where applicable.  
- Additional projects and ongoing work are available upon request.
