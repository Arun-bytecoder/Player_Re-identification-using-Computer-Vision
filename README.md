# 🏃‍♂️ Football Player Detection and Re-Identification

This repository contains the implementation for detecting football players using a custom YOLOv8 model and tracking them with DeepSORT to ensure consistent Player IDs — even when players temporarily leave and re-enter the video frame.

---

## 🎯 Project Objective

- Detect each football player in a video using a trained YOLOv8 model
- Assign a unique Player ID
- Maintain consistent IDs across occlusion or re-entry
- Output an annotated video with bounding boxes and labels

---

## 📁 Files in the Repository

| File                           | Description                                 |
|--------------------------------|---------------------------------------------|
| `player_detection_updated.ipynb` | Jupyter Notebook with the full pipeline     |
| `best.pt`                      | Custom-trained YOLOv8 model for players     |
| `15sec_input_720p.mp4`         | Input football video                        |
| `output_player_tracking.mp4`   | Output video with tracked player IDs        |
| `report.md`                    | Project report with methodology & results   |
| `README.md`                    | This file                                   |

---

## 🛠️ Setup Instructions

1. **Install dependencies**

   
        pip install ultralytics deep_sort_realtime opencv-python-headless


2. Place Files in Working Directory

   best.pt – your trained YOLOv8 model for football players

   15sec_input_720p.mp4 – input video

3. Run the Notebook

   Open player_detection_updated.ipynb

   Execute all cells

4. Output
The annotated video will be saved as:

        output_player_tracking.mp4


## 📦 File Structure

         📁 project/
        │
        ├── player_detection_updated.ipynb   # Final working notebook
        ├── best.pt                          # Trained YOLOv8 model (for player detection)
        ├── 15sec_input_720p.mp4             # Input football video
        ├── output_player_tracking.mp4       # Output video with player IDs
        └── README.md                        # Project overview

## 🔍 Sample Output Preview

Each player is detected with a bounding box

IDs remain the same across occlusions and re-entries

## 📈 Possible Extensions

Generate player movement heatmaps

Export player statistics CSV (duration, distance)

Add event detection (goal, pass, entry to penalty box)

Multi-camera tracking and 3D pose estimation

## 🤝 Acknowledgments
          
          Ultralytics YOLO

          DeepSORT

## 📬 Contact

Arunachalam

B.Tech in AI & Data Science

phoenixadrk318@gmail.com



