# ArUco-Based Bolt Tightening Sequence Monitoring System

⚠️ This project was developed during an industrial internship. Due to confidentiality, only high-level details are shared.

## Overview
This project focuses on developing a computer vision–based system to monitor and validate bolt tightening sequences in an automotive assembly environment. The system ensures that bolts are tightened in the correct order by integrating vision data with industrial tool feedback.

## Problem Statement
Manual verification of bolt tightening sequence is error-prone and may lead to incorrect assembly, safety risks, and quality failures. There is a need for an automated system that validates both sequence and tool feedback in real time.

## Solution Approach
A hybrid system was designed combining:
- ArUco marker-based visual tracking
- Nut runner feedback data
- PLC-based communication

The system correlates bolt position (vision) with tightening confirmation (tool feedback) to validate the sequence.

## System Architecture
- Industrial Camera → Captures bolt positions
- Edge Device (Jetson Nano) → Runs ArUco detection
- ArUco Markers → Identify each bolt uniquely
- Siemens PLC → Acts as central controller
- Nut Runner Tool → Sends tightening feedback
- Validation Logic → Matches sequence + tool confirmation
- Display Interface → Shows OK / NG status

## Workflow
1. Camera captures real-time assembly area  
2. ArUco markers are detected and mapped to bolt positions  
3. Operator tightens bolts using nut runner tool  
4. Nut runner sends tightening confirmation via PLC  
5. PLC provides:
   - Engine model information  
   - Tool feedback data  
6. System validates:
   - Correct bolt sequence  
   - Correct tightening confirmation  
7. Output:
   - Correct sequence + valid feedback → OK  
   - Wrong sequence / missing feedback → NG alert  

## Technologies Used
- Python  
- OpenCV (cv2.aruco)  
- Edge AI (Jetson Nano)  
- Siemens PLC (Industrial Communication)  
- GUI / HMI  

## Key Contributions
- Integrated computer vision with industrial PLC signals  
- Designed sequence validation logic combining vision and tool data  
- Enabled real-time operator feedback for assembly correctness  

## Disclaimer
This repository presents a conceptual and high-level overview of the project.  
All industrial data, images, implementation details, PLC configurations, and performance metrics are excluded due to confidentiality agreements.
