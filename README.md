# Hand Gesture Volume Control

This Python project allows you to control your computer's system volume using hand gestures captured in real-time through your webcam. It uses computer vision to track hand landmarks and maps the distance between the thumb and index finger to a specific volume level.

## Features

- Real-time Gesture Recognition: Controls system volume instantly based on hand gestures.
- Visual Feedback: An on-screen volume bar and percentage display provide clear, intuitive feedback.
- Hand Landmark Visualization: Overlays the detected hand skeleton on the video feed.
- Performance Monitoring: Displays the current FPS (Frames Per Second).

## How It Works

1.  Camera Input: The script captures video feed from the webcam using 'OpenCV'.
2.  Hand Tracking: It uses the 'MediaPipe' library to detect and track 21 different landmarks on the hand in real-time.
3.  Gesture Analysis: The script specifically isolates the coordinates of the thumb tip (Landmark 4) and the index finger tip (Landmark 8).
4.  Distance Calculation: It calculates the Euclidean distance between these two points.
5.  Volume Mapping: This distance is linearly mapped to the system's volume range (e.g., 0% to 100%).
6.  System Volume Control: The 'pycaw' library is used to set the master volume of the operating system.
7.  Visualization: OpenCV is used to draw the volume bar, percentage text, and the line connecting the thumb and index finger onto the video frame.

## Setup and Installation

Follow these steps to get the project running on your local machine.

#### Prerequisites
- Python 3.8 - 3.11
- A connected webcam

#### **Installation Steps**

1.  **Clone the repository (replace with your details):**
    ```bash
    git clone [https://github.com/your-username/your-repository-name.git](https://github.com/your-username/your-repository-name.git)
    cd your-repository-name
    ```

2.  **(Recommended) Create and activate a virtual environment:**
    - For Windows:
      ```bash
      python -m venv venv
      .\venv\Scripts\activate
      ```
    - For macOS/Linux:
      ```bash
      python3 -m venv venv
      source venv/bin/activate
      ```

3.  **Install the required dependencies from `requirements.txt`:**
    ```bash
    pip install -r requirements.txt
    ```

## Usage

Once the setup is complete, run the main Python script:
```bash
python volume_project.py
