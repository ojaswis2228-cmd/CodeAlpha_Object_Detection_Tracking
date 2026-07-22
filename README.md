# 🎥 Object Detection and Tracking using YOLO

This project was developed as part of the CodeAlpha Artificial Intelligence Internship.

## 📌 Project Overview

This project detects and tracks multiple objects in a video using a pre-trained YOLO model and ByteTrack. It assigns unique tracking IDs to detected objects and generates a processed video containing bounding boxes, class labels, confidence scores, and tracking IDs.

## ✨ Features

- Object detection using YOLO
- Multi-object tracking using ByteTrack
- Unique tracking IDs for detected objects
- Bounding boxes and class labels
- Confidence-based object detection
- Video upload and processing in Google Colab
- Processed output video generation
- Support for MOV and MP4 input videos

## 🧠 Technologies Used

- Python
- Ultralytics YOLO
- ByteTrack
- OpenCV
- FFmpeg
- Google Colab

## ⚙️ How It Works

1. A video is uploaded in Google Colab.
2. The pre-trained YOLO model detects objects in each frame.
3. ByteTrack assigns a unique tracking ID to every detected object.
4. Bounding boxes, labels, confidence scores, and tracking IDs are displayed.
5. The processed video is saved in AVI format.
6. FFmpeg converts the output into MP4 format for easier viewing and sharing.

## 📂 Project Files

- `CodeAlpha_Object_Detection_Tracking.ipynb` — Complete project implementation
- `tracked_output_small.mp4` — Sample processed video showing object detection and tracking
- `README.md` — Project documentation

## ▶️ How to Run

1. Open the notebook in Google Colab.
2. Install the Ultralytics library.
3. Import the required libraries.
4. Load the pre-trained YOLO model.
5. Upload a short video file.
6. Run the object detection and tracking code.
7. Locate the processed output video.
8. Convert the AVI video to MP4 using FFmpeg.
9. Display or download the final output.

## 🧪 Model Configuration

The project uses:

- Model: `yolo11n.pt`
- Tracker: `bytetrack.yaml`
- Confidence threshold: `0.35`
- IoU threshold: `0.5`

## 📌 Sample Tracking Code

```python
results = model.track(
    source=video_path,
    tracker="bytetrack.yaml",
    conf=0.35,
    iou=0.5,
    save=True,
    persist=True
)
