
# 📑 Project Report: Football Player Detection and Re-Identification

## 🎯 Objective
To detect football players in a video and re-identify them consistently using a YOLOv8 model and DeepSORT tracking. Players should maintain the same ID even after leaving and re-entering the frame.

---

## 🧠 Approach & Methodology

### 1. **Model Setup**
- Used a **custom-trained YOLOv8 model (`best.pt`)** trained to detect football players.
- Integrated with **DeepSORT** for multi-object tracking and consistent identity assignment.

### 2. **Player Detection**
- The YOLO model detects players frame-by-frame.
- Only detections with high confidence (e.g., > 0.5) and class ID matching "player" are accepted.

### 3. **Player Re-identification**
- DeepSORT tracks players using spatial and appearance features.
- IDs are preserved across frames, even when players are temporarily occluded or exit the scene.

---

## 🧪 Techniques Tried

| Technique        | Outcome |
|------------------|---------|
| YOLOv8           | High accuracy player detection |
| DeepSORT         | Reliable tracking and re-identification |
| Confidence Filtering | Reduced false detections |
| Bounding Box Debugging | Validated class indexes from model output |

---

## 🚧 Challenges Encountered

- Initially, the model detected footballs instead of players. Root cause: class filtering.
- DeepSORT sometimes reassigned IDs during long occlusions. Solution: increased `max_age` and tuned `nn_budget`.

---

## ⏱️ Efficiency

- Real-time capable on GPU (15 FPS+)
- Optimized inference using batch processing in YOLO (where applicable)

---

## 🧩  Future Work
If given more time:
- Add player heatmaps and movement trails
- Export CSV with player statistics (e.g., time on field)
- Implement team classification via jersey color clustering
- Add goal or possession event detection

---

## ✅ Final Deliverables

- 📁 `player_detection_updated.ipynb`: Complete source code
- 🧠 `best.pt`: Custom YOLO model for player detection
- 🎥 `15sec_input_720p.mp4`: Input video
- 📦 `output_player_tracking.mp4`: Tracked video with consistent player IDs
- 📄 `README.md`: Instructions and overview
- 📑 `report.md`: This document

---

## 📬 Author
Arunachalam  
_B.Tech in AI & Data Science_  
📧 phoenixdark318@gmail.com
