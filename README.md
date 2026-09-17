# Smart India Hackathon Workshop

## Date: 17.9.26
## Register Number: 212223040182
## Name: Sanjay Kumar H
## Problem Title
SIH 1710: Enhancing Navigation for Railway Station Facilities and Locations
## Problem Description
Background: Railway stations are complex environments with numerous facilities and locations such as ticket counters, platforms, restrooms, food courts, and waiting areas. Passengers often face difficulties in navigating these spaces, especially in large or unfamiliar stations. Efficient and user-friendly navigation systems are crucial for improving passenger experience, reducing congestion, and ensuring timely travel connections. Description: The problem involves developing a comprehensive navigation solution for railway stations that assists passengers in locating various facilities and destinations within the station premises. This includes creating detailed maps, providing real-time directions, and integrating features such as accessibility options for individuals with disabilities. The solution should be intuitive, easy to use, and accessible via multiple platforms, including mobile devices and digital kiosks. Key challenges include updating navigation information in real-time, ensuring accuracy, and accommodating the diverse needs of all passengers. Expected Solution: The expected solution is a multi-platform navigation system that provides detailed, real-time directions to all facilities and locations within a railway station. This system should include: A mobile application with 3D interactive maps and step-by-step navigation. Digital kiosks located throughout the station with touch-screen interfaces. Voice-guided navigation for visually impaired passengers. Regular updates to reflect changes in station layout and facility locations. Integration with existing railway apps and services for seamless user experience. The solution should enhance the overall passenger experience by reducing confusion, saving time, and improving accessibility within the station.

## Problem Creater's Organization
Ministry of Railway

## Idea
RailNav AI – Smart Indoor Railway Station Navigation System

RailNav AI is an intelligent indoor navigation system designed to help passengers easily navigate large railway stations and locate important facilities such as platforms, ticket counters, restrooms, food courts, waiting areas, lifts and escalators.

The system provides navigation through a mobile application and digital kiosks. Passengers can select their current location manually or scan a QR code at designated locations and then choose their destination. The system calculates an optimal route using a graph-based navigation engine.

The solution also supports accessibility-aware navigation by considering lifts, ramps and accessible pathways. For visually impaired passengers, the system provides voice-based step-by-step guidance.

Railway authorities can use an Admin Dashboard to update facility information, platform details, blocked pathways and lift/escalator status. These updates are used by the navigation engine to provide alternative routes when required.

## Proposed Solution / Architecture Diagram
## System Architecture

The system consists of the following major components:

1. User Access Layer

Mobile Application

Digital Kiosk

Supports general passengers, elderly passengers and differently-abled/visually impaired users.

2. Real-Time Station Data

Lift and escalator status

Blocked paths and maintenance 

Train schedule integration

Facility updates

3. Backend Server

Built using Spring Boot

Provides REST APIs

Handles user requests and navigation requests

Manages real-time station information

Provides admin management APIs

4. Database Layer

PostgreSQL database

Stores station layout and map data

Facility information

Nodes and pathways required for graph navigation

Real-time status logs

User preferences

5. Navigation Engine

Converts the station map into a graph of nodes and pathways.

Uses A* / Dijkstra algorithms to calculate routes.

Applies accessibility preferences.

Performs dynamic rerouting when a pathway is blocked.

6. Navigation Output

Interactive 2D/3D map

Step-by-step 

Distance and estimated travel time

Voice guidance using Text-to-Speech

7. Admin Dashboard

Update facility locations

Mark paths as blocked/under maintenance

Update platform information

View logs and analytics

## Working Flow
```
Passenger / Kiosk
       ↓
Scan QR / Select Location
       ↓
Select Destination
       ↓
Set Accessibility Preference
       ↓
Backend Server
       ↓
Station Database + Real-Time Data
       ↓
Navigation Engine
       ↓
A* / Dijkstra + Accessibility Filtering
       ↓
Optimal Route
       ↓
Interactive Map + Voice Guidance
```

## Use Cases

1. Platform Navigation

Passengers can select a platform and receive the best route from their current location.

2. Facility Navigation

Users can search and navigate to:

Ticket counters, Restrooms, Food courts, Waiting areas, Lifts, Escalators, Other station facilities

3. Accessible Navigation

The system can generate routes that:

Avoid stairs, Prefer lifts and ramps, Consider accessibility requirements

4. Voice-Guided Navigation

Visually impaired passengers can receive step-by-step voice instructions through Text-to-Speech.

5. QR-Based Location Detection

QR codes placed at important locations can help identify the passenger's current position inside the station.

6. Real-Time Rerouting

If a pathway is blocked or a lift is unavailable, the system uses updated information and calculates an alternative route.

7. Digital Kiosk Navigation

Passengers without the mobile application can use touch-screen kiosks to find facilities and routes.

8. Railway Administration

Administrators can update station information and monitor facility/pathway status through the dashboard.

## Technology Stack

Mobile/Web - Frontend	React.js, HTML, CSS

Digital Kiosk -	React.js / Web Interface

Backend Server - Spring Boot

API	- REST APIs

Database - PostgreSQL

Navigation Engine - A* / Dijkstra Graph Algorithm

Station Map	SVG / Leaflet, 2D/3D Map

AI/NLP - Natural Language Processing for destination search

Voice Assistance - Speech Recognition, Text-to-Speech

Indoor Positioning - QR Codes, optional BLE

Real-Time Updates - REST APIs / Webhooks

Testing - Postman

Version Control - GitHub

Deployment - AWS / Render / Vercel

## Dependencies

Railway station layout and floor-plan data

Platform and facility location information

Station nodes and pathway/graph data

QR codes installed at important station locations

Real-time lift and escalator status

Blocked-path and maintenance information

Train schedule information/API, if integrated

Smartphone camera for QR scanning

Microphone and speaker for voice navigation

Internet connectivity for real-time synchronization

PostgreSQL database

Railway authority/admin access for updating station information

## Expected Outcome

The proposed system aims to reduce passenger confusion and navigation time, improve accessibility for elderly and differently-abled passengers, provide reliable indoor directions, and dynamically adapt routes according to real-time station conditions. The architecture can also be extended to multiple railway stations by adding their respective maps, facilities and pathway data.
