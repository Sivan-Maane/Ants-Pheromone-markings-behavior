# Ant Tracking Using YOLO + ByteTrack

This project implements an automatic tracking pipeline for ants using **YOLO** for detection and **ByteTrack** for multi-object tracking. The goal is to accurately detect and track individual ants in video sequences for behavioral analysis.

---

## Features

- **Object Detection**: Uses YOLO (You Only Look Once) for detecting ants in each video frame.
- **Multi-Object Tracking**: Integrates ByteTrack for assigning consistent IDs to ants across frames.
- **Robust to Fast Movement**: Handles fast and erratic ant movements.
- **Handles Occlusions and Pauses**: Maintains tracking IDs even when ants stop or overlap.
- **Outputs**: Generates tracking data including ant trajectories and speed profiles.

---

## Installation

1. Clone this repository:
   ```bash
   git clone https://github.com/Sivan-Maane/Ants-Pheromone-markings-behavior/tree/master
   cd your-repo
   
2. Install dependencies (example for Python environment):
   pip install -r requirements.txt

3. Download pretrained YOLO weights if not included (specify link or instructions).

## Usage

Place your input videos in the videos/ folder (or specify your path).

Run the tracking pipeline:

python track_ants.py --input videos/your_video.mp4 --output results/your_video_output.json
The output includes:

Detected bounding boxes per frame.

Tracking IDs are assigned to each ant.

Speed and trajectory data (optional).

## Configuration
YOLO model weights and configuration files can be modified in config.yaml or directly in the script.

ByteTrack parameters such as IOU threshold, track memory, and detection confidence are configurable.

## Results
Example visualizations and tracking outputs are available in the results/ folder.

## References
YOLO: https://pjreddie.com/darknet/yolo/
ByteTrack: https://github.com/ifzhang/ByteTrack







   
