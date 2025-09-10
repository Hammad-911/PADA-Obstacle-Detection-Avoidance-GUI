#PADA Obstacle Detection & Avoidance GUI
This project is a real-time Graphical User Interface (GUI) developed for the Lycans PADA (Powered Autonomous Delivery Aircraft) project. The application uses a webcam to detect obstacles of different shapes and colors, and visualizes the aircraft's corresponding avoidance maneuvers in a simulated "Airplane POV" panel.

Developed by Ahmed Hammad.

Features
Real-Time Video Processing: Captures and processes a live feed from a webcam using OpenCV.

Object Detection: Detects three types of objects based on color and shape:

Red Triangles (Dangerous Obstacles): Highest priority.

Blue Squares (Boundary Markers): Medium priority.

Green Circles (Safe Zones): Lowest priority.

Dynamic Visualization: Displays a 2D airplane model that animates its roll and pitch based on the position of detected objects.

Priority-Based Logic: Implements a control system where dangerous obstacles are reacted to first, followed by boundaries.

Interactive UI: Built with Streamlit, featuring Start/Stop controls and a clean, two-column layout for the camera feed and visualization.

Installation & Setup
To run this project, you need to have Python installed along with several libraries.

Clone or download the repository.

Install the required Python libraries:
Open your terminal or command prompt and run the following command:

pip install streamlit opencv-python numpy Pillow

Add Asset Files:
Make sure you have the following image files in the same directory as the Python scripts:

airplane.png: The image for the aircraft visualization.

sky.png: The background image for the visualization panel.

How to Run the Application
Once the setup is complete, navigate to the project directory in your terminal and run the following command:

streamlit run trial.py

This will start a local web server, and your default browser will open with the application running.

Project Structure
The project is organized into two main Python files for better modularity:

Visualization.py: This is the main application script. It handles the Streamlit user interface, manages the application state, and contains the visualization logic using the Pillow library. You run this file to start the app.

LycansOpenCV.py: This is a dedicated module that contains all the computer vision logic. It processes the camera frames to detect shapes and colors and returns the processed frame and the final avoidance command.
