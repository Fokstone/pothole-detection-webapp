
# 🚧 RoadGuardian: Pothole Detection System using YOLOv4 Tiny  
[![MIT license](https://img.shields.io/badge/License-MIT-blue.svg)](https://lbesson.mit-license.org/)

🔗 **Live Dashboard**: [Click here to view the Dashboard](https://farhan123mohd.github.io/pothole-detection-webapp/)

---

An intelligent, AI-powered system for **real-time pothole detection** using **YOLOv4-Tiny**, capable of identifying and categorizing road damages based on severity. The system processes live video feeds, detects potholes, classifies them (Low, Medium, High), and maps their locations with timestamped data.

This tool empowers smart city initiatives by providing a reliable way to monitor road conditions and prioritize maintenance.

---

## 🧠 Key Features

- 🔍 Real-time pothole detection using YOLOv4 Tiny.
- 🎥 Works with both video files and live camera streams.
- 📦 Saves pothole images and logs data with GPS coordinates.
- 📊 Classifies pothole severity (Low / Medium / High) based on area.
- 🗺️ Visualizes potholes on an interactive web dashboard.
- ⚡ Displays FPS for performance monitoring.

---

## 📦 Requirements

Make sure the following tools and libraries are installed:

- Python (3.x)
- OpenCV (`opencv-python`)
- Geocoder (`geocoder`)
- YOLOv4 Tiny model weights (`yolov4_tiny.weights`)
- Object label file (`obj.names`)

---

## 🚀 Getting Started

1. 🔧 Install the required libraries:
   ```bash
   pip install opencv-python geocoder
   ```

2. 📁 Clone the repository:
   ```bash
   git clone https://github.com/farhan123mohd/pothole-detection.git
   cd pothole-detection
   ```

3. 🎯 Configure the following in your Python script:
   - YOLOv4 Tiny weights path
   - Config file path
   - `obj.names` path
   - Video input (camera or file)

4. ▶️ Run the detection:
   ```bash
   python main_ras.py           # For Raspberry Pi
   python Main_using_laptop_gps.py   # For Windows
   ```

5. Press **`q`** to stop the detection stream.

---

## 🌐 Web Interface & Dashboard

### 🔥 Live Features

- 🗺️ **Interactive Map**: Shows pothole locations in real time using Leaflet.js.
- 📍 **City Search**: Pan and zoom to different cities.
- 📊 **Analysis Reports**: Displays number of potholes, distances, and severity levels.
- 🆕 **Real-Time Updates**: Data updates dynamically as detection progresses.

---

## 📁 File Structure

```
📂 pothole-detection
├── camera_video.py
├── yolov4_tiny.cfg
├── yolov4_tiny.weights
├── obj.names
├── pothole_data.json
├── dashboard/
│   ├── index.html
│   ├── dashboard.html
│   ├── citySearch.js
│   ├── potholeData.js
│   ├── cities.json
│   └── styles.css
```

---

## 🗃️ Sample JSON Format

### `pothole_data.json`

```json
[
  {
    "image_path": "pothole_coordinates/pot94.jpg",
    "latitude": 19.076,
    "longitude": 72.8777,
    "severity": "Low",
    "datetime_utc": "2024-05-29 11:18:38.968232"
  },
  {
    "image_path": "pothole_coordinates/pot95.jpg",
    "latitude": 19.076,
    "longitude": 72.8777,
    "severity": "Low",
    "datetime_utc": "2024-05-29 11:18:38.987330"
  }
]
```

---

## ⚙️ Parameters and Customization

- `Conf_threshold`: Confidence level for detection (e.g., 0.5).
- `NMS_threshold`: Non-Max Suppression threshold (e.g., 0.4).
- `result_path`: Directory where pothole images and metadata are saved.

---

## ⚠️ Notes

- For better performance, use GPU-accelerated OpenCV with CUDA support.
- Adjust detection thresholds and model settings for different road environments and lighting conditions.

---

## 👨‍💻 License

This project is licensed under the MIT License.  
Feel free to use, modify, and contribute! 💙

---


