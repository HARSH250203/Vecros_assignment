# Robotics Intern Assignment

This project addresses the requirements of the Robotics Intern Assignment, focusing on two key problems: **3D grid pathfinding** and **drone waypoint mission planning**. The code is written in Python and includes features for visualization and GUI enhancements.

---

## Problem 1: 3D Grid Shortest Path

### Features
- **3D Grid Generation:**
  - Creates a grid with specified dimensions.
  - Randomly assigns weights to certain points to simulate obstacles or challenges.

- **Pathfinding Algorithm:**
  - Uses the A* algorithm to compute the shortest path between two points.
  - Ensures no two paths share a point at the same time.

- **Visualization:**
  - Displays the 3D paths using Matplotlib.
  - Integrated with a GUI to dynamically adjust grid size, start/end points, and velocity.

### How to Use
1. Run the script.
2. A GUI window will open, allowing input for:
   - **Grid size**
   - **Velocity (m/s)**
   - **Start and end points (x, y, z)**
3. Click **Generate Path** to compute and visualize the shortest path.

---

## Problem 2: Waypoint Mission Planning

### Features
- **Waypoint Generation:**
  - Automatically generates 15 waypoints with latitude, longitude, and altitude.
  - Adds a new waypoint after the 10th point, 100m perpendicular to the current direction.

- **Mission Planning:**
  - Implements `pymavlink` for communication with a drone.
  - Sends the waypoints to the drone for autonomous execution.

- **Telemetry:**
  - Fetches real-time telemetry data, displaying:
    - Current position
    - Distance and estimated time to the next waypoint

- **Visualization:**
  - Generates a 2D map using `folium`.
  - Displays waypoints and the drone's trajectory on an interactive map.

### How to Use
1. Ensure you have a drone simulation or real connection ready.
2. Configure the connection string in the code (e.g., `udp:127.0.0.1:14550`).
3. Run the script to:
   - Send waypoints to the drone.
   - Monitor telemetry data.
   - Save the mission map as `mission_map.html`.

---

## Requirements

### Python Libraries
Install the following Python libraries before running the code:
```bash
pip install numpy networkx matplotlib pymavlink folium
```

---

## File Structure
- **`robotics_assignment.py`:** Main script containing all functionalities.
- **`mission_map.html`:** Generated map file showing waypoints and trajectory.

---

## Results and Visualizations

### 1. 3D Grid Pathfinding
- **Visualization:**
  - Displays paths avoiding conflicts in both space and time.
  - GUI allows dynamic adjustment of inputs like grid size, velocity, and start/end points.

### 2. Waypoint Mission
- **Visualization:**
  - Displays a 2D map showing waypoints and the drone's planned mission.
  - Tracks real-time telemetry updates and trajectory.

---

## Submission
- The code is available in a private GitHub repository.
- Includes:
  - Detailed documentation in this README.
  - Results and visualizations.
  
---

**For questions or feedback, please contact via the repository's collaboration request feature.**

