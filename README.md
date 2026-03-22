# ArUco-Based Bolt Tightening Sequence Monitoring System

⚠️ This project was developed during an industrial internship. Due to confidentiality, only high-level details are shared.

## Overview
This project focuses on a computer vision–based system designed to monitor and validate bolt tightening sequences in an automotive assembly environment. The system ensures that bolts are tightened in the correct order by integrating visual tracking with industrial tool feedback.

## Team Context
This system was developed as part of an industrial team during my internship, where core system development was handled by full-time engineers.

My role focused on supporting system testing, validation, and fine-tuning to ensure reliable performance in a real production environment.

## Project Context
At the time of joining the internship, this system was already in the testing and validation phase. My primary contribution was supporting system testing, validation, and fine-tuning to ensure reliable performance in a real production environment.

## Problem Statement
Manual verification of bolt tightening sequences is error-prone and can lead to incorrect assembly, safety risks, and quality issues. An automated system is required to validate both the tightening sequence and tool feedback in real time.

## Solution Approach
The system combines:
- ArUco marker-based visual tracking for bolt identification
- Nut runner feedback for tightening confirmation
- PLC-based communication for centralized control

By correlating vision data with tool feedback, the system validates whether bolts are tightened in the correct sequence.

## System Architecture
- Industrial Camera → Captures bolt positions  
- Edge Device (Jetson Nano) → Runs ArUco detection  
- ArUco Markers → Unique identification of each bolt  
- Siemens PLC → Central control and data exchange  
- Nut Runner Tool → Provides tightening feedback  
- Validation Logic → Matches sequence with tool confirmation  
- Display Interface → Shows real-time OK / NG status  

## Workflow
1. Camera captures real-time assembly area  
2. ArUco markers are detected and mapped to bolt positions  
3. Operator tightens bolts using nut runner tool  
4. Nut runner sends tightening feedback via PLC  
5. PLC provides:
   - Engine model information  
   - Tool feedback signals  
6. System validates:
   - Correct bolt tightening sequence  
   - Proper tightening confirmation  
7. Output:
   - Correct sequence + valid feedback → OK  
   - Incorrect sequence / missing feedback → NG alert  

## Technologies Used
- Python  
- OpenCV (cv2.aruco)  
- Edge AI (Jetson Nano)  
- Siemens PLC (Industrial Communication)  
- GUI / HMI  

## Key Contributions
- Supported system testing and validation in a real industrial environment  
- Assisted in fine-tuning ArUco detection for stable performance  
- Helped identify and troubleshoot edge-case issues in sequence validation  

## Disclaimer
This repository presents a conceptual and high-level overview of the project.  
All industrial data, images, implementation details, PLC configurations, and performance metrics are excluded due to confidentiality agreements.
