# System Overview

## Project Name

**VAJRA - AI-Based Intelligent Video Analytics Platform for Border Surveillance**

## Problem Statement

**SIH 26187 - AI-Based Intelligent Video Analytics Platform for Border Surveillance using Existing CCTV Infrastructure**

## Primary Goal

Improve border surveillance by using existing CCTV infrastructure with AI-based video analytics to detect important activities, generate alerts and provide useful information through a single surveillance dashboard.

## Core Capabilities

### CCTV Video Monitoring

The system uses existing CCTV infrastructure for surveillance and provides a centralized interface where operators can view camera feeds and recorded surveillance videos.

### Human Detection

AI-based video analysis can identify people in surveillance footage and help operators monitor movement in important or restricted areas.

### Vehicle Analytics

The platform provides vehicle-focused analysis to detect and monitor vehicles appearing in CCTV footage.

### Face Detection

The system provides a dedicated face-detection capability for identifying detected faces in surveillance footage.

### ANPR

Automatic Number Plate Recognition (ANPR) is included to support the detection and display of vehicle number-plate information from surveillance footage.

### Virtual Fence Monitoring

Virtual Fence helps monitor movement across defined or restricted areas.

### Suspicious Activity Detection

The platform provides a dedicated section for suspicious activity so that unusual or important events can be highlighted for operator attention.

### Night Movement Monitoring

Night Movement focuses on monitoring movement during low-light or night-time conditions using available surveillance footage.

### Alerts and Event Logs

Detected events can be presented as alerts and recorded in event logs with information such as detection time and camera/source information.

## Technical Architecture

The system combines:

- Existing CCTV video sources
- React-based surveillance dashboard
- Node.js and Express backend services
- AI-based video analytics concepts
- Event and alert processing
- Camera and surveillance data
- Reports and visualization components

## System Workflow

```text
Existing CCTV
      ↓
Video Monitoring
      ↓
AI Video Analysis
      ↓
Detection
      ↓
Event / Alert
      ↓
VAJRA Dashboard
      ↓
Operator Situational Awareness
```
