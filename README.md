# Real-Time Vehicle Detection and Tracking with YOLOv8

![Project Demo GIF](https://i.imgur.com/gC582Vo.gif)
*Example of the model tracking vehicles on a highway.*

An AI-powered computer vision project that detects, tracks, and logs various types of vehicles and other objects from video footage. Built using Python and the powerful YOLOv8 object detection model.

## About The Project

This project provides a robust foundation for analyzing traffic flow, monitoring road activity, and gathering vehicle data. It takes a video file or a live camera stream as input, processes it frame by frame to identify objects, and assigns a unique tracking ID to each object, allowing for analysis of its movement over time.

The primary goal is to create a simple yet powerful tool that can be extended for various real-world applications, from traffic management in cities like Brahmapur to simple security monitoring.

### Key Features

* **Real-Time Object Detection:** Identifies 80 common object classes (cars, trucks, buses, pedestrians, etc.) using the pre-trained YOLOv8 model.
* **Multi-Object Tracking:** Assigns and maintains a unique ID for each detected object across frames.
* **Data Extraction:** Outputs structured data for each object, including its class, position, and unique tracker ID for every frame.
* **High Performance:** Optimized for speed to enable real-time processing on a capable GPU.
* **Customizable:** Can be easily fine-tuned on a custom dataset to detect new types of objects.

### Built With

* [Python](https://www.python.org/)
* [PyTorch](https://pytorch.org/)
* [Ultralytics YOLOv8](https://github.com/ultralytics/ultralytics)
* [OpenCV](https://opencv.org/)

## Getting Started

Follow these instructions to get a copy of the project up and running on your local machine for development and testing.

### Prerequisites

* Python 3.8 or later
* An NVIDIA GPU is highly recommended for real-time performance.

### Installation

1.  **Clone the repository:**
    ```sh
    git clone [https://github.com/your_username/your_repository_name.git](https://github.com/your_username/your_repository_name.git)
    cd your_repository_name
    ```

2.  **Create a virtual environment (recommended):**
    ```sh
    python -m venv venv
    source venv/bin/activate  # On Windows, use `venv\Scripts\activate`
    ```

3.  **Install the required packages:**
    A `requirements.txt` file should be included in your repository with the following content:
    ```txt
    # requirements.txt
    ultralytics
    opencv-python-headless
    ```
    Install it using pip:
    ```sh
    pip install -r requirements.txt
    ```

### Usage

The script is designed to be run from the command line and can process both video files and live webcam streams.

1.  **To process a video file:**
    ```sh
    python track.py --source "path/to/your/video.mp4"
    ```

2.  **To use a live webcam feed:**
    ```sh
    python track.py --source 0
    ```

The script will generate two outputs:
* An annotated video file named `output.mp4`.
* A detailed data log printed directly to the console.

*(Note: You will need to slightly modify the Python script from Colab to accept command-line arguments using a library like `argparse` for the commands above to work.)*

## Roadmap

This project is a strong starting point. Here are some potential future enhancements:

* [ ] **Vehicle Counting:** Implement a feature to count vehicles as they cross a designated line in the video.
* [ ] **Fine-Tuning:** Fine-tune the YOLOv8 model on a custom dataset of traffic from Brahmapur, Odisha, to improve accuracy and detect region-specific vehicles (e.g., auto-rickshaws).
* [ ] **Web Interface:** Develop a web application using Flask or FastAPI where users can upload videos for processing.
* [ ] **Edge Deployment:** Deploy the model on an edge device like an NVIDIA Jetson for on-site, 24/7 live camera analysis.
* [ ] **Speed Estimation:** Add functionality to estimate the speed
