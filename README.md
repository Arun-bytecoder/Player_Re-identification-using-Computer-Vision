# Player_Re-identification-using-Computer-Vision

# 🏃‍♂️ Football Player Detection and Re-Identification

This project detects football players in a video using a custom-trained YOLO model and tracks them with consistent Player IDs using DeepSORT. It ensures that players who temporarily leave the frame are re-identified correctly when they reappear.

---

## 🎯 Project Objective

- 🎥 Input: A 15-second football video (`15sec_input_720p.mp4`)
- 🧠 Detect each player using a custom YOLOv8 model
- 🏷️ Assign a unique Player ID
- 🔁 Maintain the same ID even after occlusion or re-entry
- 💾 Output: An annotated video (`output_player_tracking.mp4`) with bounding boxes and player labels

---

## 🛠️ Tech Stack

| Component         | Technology              |
|------------------|--------------------------|
| Object Detection | YOLOv8 (`best.pt`)       |
| Tracking         | DeepSORT                 |
| Video Handling   | OpenCV                   |
| Programming      | Python                   |
| Output Format    | MP4 video with overlays  |

---

## 🧪 Setup Instructions

1. **Install Requirements**
   ```bash
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
   
# 📦 File Structure

bash
Copy
Edit
📁 project/
│
├── player_detection_updated.ipynb   # Final working notebook
├── best.pt                          # Trained YOLOv8 model (for player detection)
├── 15sec_input_720p.mp4             # Input football video
├── output_player_tracking.mp4       # Output video with player IDs
└── README.md                        # Project overview

🔍 Sample Output Preview

Each player is detected with a bounding box

IDs remain the same across occlusions and re-entries

# 🤝 Acknowledgments
Ultralytics YOLO

DeepSORT


