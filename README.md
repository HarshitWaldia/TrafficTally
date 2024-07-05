# 🚗 TrafficTally : Vehicle Detection and Counting Notebook 🚙

This project is a Jupyter notebook application designed to detect and count vehicles in a video stream. It uses OpenCV for image processing and a background subtractor algorithm to identify moving vehicles. The application draws bounding boxes around detected vehicles and counts them as they cross a predefined line in the video frame.

## Features

- **🚘 Vehicle Detection**: Identifies and draws bounding boxes around moving vehicles.
- **📊 Vehicle Counting**: Counts vehicles as they cross a specified line in the video frame.
- **⏱️ Real-Time Processing**: Processes video frames in real-time for live counting.

## Requirements

- 🐍 Python 3.x
- 🖼️ OpenCV
- 🔢 NumPy
- 📓 Jupyter


## Installattion
### Setting Up the Environment

It's recommended to use a virtual environment to manage the dependencies for this project. Follow the steps below to set up the environment using `conda`.

1. Install [Miniconda](https://docs.conda.io/en/latest/miniconda.html) or [Anaconda](https://www.anaconda.com/products/distribution) if you haven't already.

2. Create a new conda environment:

    ```bash
    conda create --name vehicle_counter python=3.8
    ```

3. Activate the environment:

    ```bash
    conda activate vehicle_counter
    ```

4. Install the required packages:

    ```bash
    pip install -r requirements.txt
    ```
## Usage
To run the vehicle detection and counting notebook, follow these steps:

1. Ensure you have a video file named `video3.mp4` in the same directory as your notebook, or modify the code to use a different video file.

2. Launch Jupyter Notebook:
```bash
jupyter notebook
```
3. Open the [`main.ipynb`](main.ipynb) notebook and run all cells to start the vehicle detection and counting process.

4. Run all the cells in the notebook to start the vehicle detection and counting process.

## Explanation of Key Components
- **🔍 Background Subtraction**: Uses cv2.bgsegm.createBackgroundSubtractorMOG() to segment moving objects (vehicles) from the background.<br>
- **✏️ Contour Detection**: Detects contours in the segmented frames and draws bounding boxes around the detected vehicles.<br>
- **🔢 Vehicle Counting**: Defines a counting line and increments the vehicle count whenever a detected vehicle crosses this line.<br>
- **📍 Center Function**: Calculates the center of the bounding box for each detected vehicle.<br>

## Customization
- **Change Count Line Position**:
Modify the count_line_position variable to change the position of the counting line.

- **Adjust Rectangle Size**:
Modify the min_width_rectangle and min_height_rectangle variables to adjust the minimum size of detected vehicles.

- **Use Different Video Source**:
Change the path in cv2.VideoCapture("video3.mp4") to use a different video file or a webcam.

## Code Explanation
The script performs the following steps:

- Imports necessary libraries and initializes video capture.
- Sets parameters for vehicle detection and counting.
- Defines a background subtraction algorithm and contour detection.
- Implements real-time processing to count vehicles crossing a designated line.

## Contributions
Contributions are welcome! If you have any suggestions or improvements, please create a pull request or open an issue on GitHub.
