# Autonosky-GCS-drone_fleet_map

A full-stack web application for real-time visualisation and control of an autonomous drone fleet.  
The system provides a scalable, interactive map interface that tracks live drone telemetry, supports mission-based navigation, and allows operators to monitor and control individual drones in real time.

---

## Key Features

- Real-time drone telemetry streaming via WebSockets
- Interactive, zoomable, and scrollable map built from mission NED coordinates
- Dynamic drone icons with flight-status-based visual indicators
- Automatic viewport tracking of the selected drone
- Click-to-select drone interaction with integrated control panel
- Scalable map rendering designed for multi-drone operations

---

## System Overview

The platform consists of a Python backend responsible for telemetry streaming and a React-based frontend for visualisation and control.


Mission waypoints are defined in North-East-Down (NED) coordinates and rendered onto a 2D map.  
Live drone positions are streamed from the backend and rendered in real time on the frontend.

---

## Map and Visualisation

- Mission markers are generated from NED coordinates using Python and Matplotlib
- The map supports constrained zooming and panning to prevent invalid view states
- Drone icons are rendered dynamically and update position in real time
- When a drone is selected, the viewport follows the drone to keep it centered during flight
  
https://github.com/Ryan-McRae/Autonosky-GCS-drone_fleet_map/tree/main/Autonosky-fleetmanager/OverallG.mp4

---

## Drone Interaction

- Each drone icon is selectable
- Selecting a drone:
  - Highlights the drone visually
  - Locks the viewport to follow its movement
  - Enables control via the adjacent control panel
- Drone icon colour reflects current flight status (e.g. idle, active, error)

https://github.com/Ryan-McRae/Autonosky-GCS-drone_fleet_map/tree/main/Autonosky-fleetmanager/autopanG.mp4
https://github.com/Ryan-McRae/Autonosky-GCS-drone_fleet_map/tree/main/Autonosky-fleetmanager/autofollowG.mp4

---

## Tech Stack

### Backend
- Python
- WebSockets
- Real-time telemetry streaming

### Frontend
- React (TypeScript / TSX)
- Tailwind CSS
- SVG / Canvas-based rendering

---

## Design Considerations

- Optimised for desktop and large displays
- Scalable with viewport dimensions
- Not intended for small-screen or mobile use
- Designed for operator situational awareness and control stability

---
