# Object Detection with YOLOv5 and OpenCV

This project demonstrates real-time object detection using YOLOv5 and OpenCV with a webcam.

## Features

- Real-time object detection using a pre-trained YOLOv5s model.
- Utilizes OpenCV for webcam access and frame processing.
- Visualizes detection results directly on the webcam feed.

## Prerequisites

Before you begin, ensure you have the following installed:

- Python 3.x
- pip (Python package installer)

## Setup

1.  **Clone the repository (if you haven't already):**

    ```bash
    git clone https://github.com/SHAIK-ARSHAD191/object-detection.git
    cd object-detection
    ```

2.  **Install dependencies:**

    The project relies on `ultralytics` (which includes `YOLO`) and `opencv-python`. Although `requirements.txt` might be empty, you can install them manually:

    ```bash
    pip install ultralytics opencv-python
    ```

3.  **Download YOLOv5s weights:**

    The model expects `yolov5s.pt` to be in the project root. It should be present in the repository, but if not, you can usually find it from the official Ultralytics YOLOv5 repository or it might be downloaded automatically by the `ultralytics` package.

    *Note: There is also `yolov5su.pt` which may be another variant of the YOLOv5 model.*

## How to Run

1.  **Ensure your webcam is connected and recognized by your system.**

2.  **Run the detection script:**

    ```bash
    python test_webcam_opencv.py
    ```

    A window titled 'YOLOv5 Webcam Detection' will appear, displaying the live feed from your webcam with detected objects highlighted.

3.  **To quit the application, press the 'q' key.**

## Troubleshooting

### `Cannot open webcam` error

-   Ensure your webcam is properly connected and drivers are installed.
-   Check if another application is using the webcam.
-   On some systems, you might need to grant camera permissions to your terminal or IDE.

### OpenCV not working / `ModuleNotFoundError: No module named 'cv2'`

-   Make sure you have `opencv-python` installed:
    ```bash
    pip install opencv-python
    ```
-   If you encounter issues, try reinstalling it:
    ```bash
    pip uninstall opencv-python
    pip install opencv-python
    ```

### `ultralytics` related errors / `ModuleNotFoundError: No module named 'ultralytics'`

-   Make sure you have `ultralytics` installed:
    ```bash
    pip install ultralytics
    ```
-   If you encounter issues, try reinstalling it:
    ```bash
    pip uninstall ultralytics
    pip install ultralytics
    ```

### Model loading issues (`yolov5s.pt` not found)

-   Ensure `yolov5s.pt` is in the same directory as `test_webcam_opencv.py`.
-   Verify the file name is exactly `yolov5s.pt`.

## Project Structure

-   `test_webcam_opencv.py`: The main Python script for webcam object detection.
-   `yolov5s.pt`: Pre-trained YOLOv5s model weights.
-   `yolov5su.pt`: Another variant of YOLOv5 model weights.
-   `requirements.txt`: Lists project dependencies (currently appears empty or minimal).
-   `runs/`: Directory containing output from detection runs (e.g., `predict`, `predict2`, `predict3` with `zidane.jpg`, `0.avi`). These are often generated during testing or initial runs.

