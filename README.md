Robotics Intern Assignment
This project addresses the requirements of the Robotics Intern Assignment, focusing on
two key problems: 3D grid pathfinding and drone waypoint mission planning. The code
is written in Python and includes visualization and GUI enhancements.
Problem 1: 3D Grid Shortest Path
Features
• 3D Grid Generation:
o Creates a grid with specified dimensions.
o Randomly assigns weights to certain points to simulate obstacles or
challenges.
• Pathfinding Algorithm:
o Uses the A* algorithm to compute the shortest path between two points.
o Ensures no two paths share a point at the same time.
• Visualization:
o Displays the 3D paths using matplotlib.
o Integrated with a GUI to dynamically adjust grid size, start/end points, and
velocity.
How to Use
1. Run the script.
2. A GUI window will open, allowing input for:
o Grid size.
o Velocity (m/s).
o Start and end points (x, y, z).
3. Click Generate Path to compute and visualize the shortest path.
Problem 2: Waypoint Mission Planning
Features
• Waypoint Generation:
o Automatically generates 15 waypoints with latitude, longitude, and
altitude.
o Adds a new waypoint after the 10th point, 100m perpendicular to the
current direction.
• Mission Planning:
o Implements pymavlink for communication with a drone.
o Sends the waypoints to the drone for autonomous execution.
• Telemetry:
o Fetches real-time telemetry data, displaying:
▪ Current position.
▪ Distance and estimated time to next waypoint.
• Visualization:
o Generates a 2D map using folium.
o Displays waypoints and the drone's trajectory on an interactive map.
How to Use
1. Ensure you have a drone simulation or real connection ready.
2. Configure the connection string in the code (e.g., udp:127.0.0.1:14550).
3. Run the script to:
o Send waypoints to the drone.
o Monitor telemetry data.
o Save the mission map as mission_map.html.
Requirements
Python Libraries
Install the following Python libraries before running the code:
• numpy
• networkx
• matplotlib
• tkinter
• pymavlink
• folium
Command:
pip install numpy networkx matplotlib pymavlink folium
File Structure
• robotics_assignment.py: Main script containing all functionalities.
• mission_map.html: Generated map file showing waypoints and trajectory.
Results and Visualizations
1. 3D Grid Pathfinding:
o Visualizes paths avoiding conflicts in both space and time.
o GUI allows dynamic adjustment of inputs.
2. Waypoint Mission:
o 2D map visualization of the drone's planned mission.
o Real-time telemetry updates and trajectory tracking.
Submission
• The code is available in a private GitHub repository.
• Includes:
o Detailed documentation in this README.
o Results and visualizations
