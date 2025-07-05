# Intel Unnati DL Streamer Project – Aashwika Khurana

![Header](images/Header.png)

## 🎯 Problem Statement
Create a pipeline (detect, decode and classification) using DL Streamer and define system scalability for Intel HW.

## 🚀 Project Summary
- Real-time object detection across multiple video streams
- Simulates a smart hospital using DL Streamer + OpenVINO
- Benchmarks on Intel Core i7 CPU and Iris Xe GPU
- Identifies scalability limits and performance bottlenecks
- Includes visual graphs for FPS, resource usage, and decoding delays

## 🏥 Real-World Scenario
A smart hospital monitoring system using DL Streamer to detect people, vehicles, and bikes in real time, with classification and multi-stream scalability.

## 🛠️ Tools & Technologies Used
- Intel® DL Streamer
- OpenVINO™ Toolkit
- GStreamer
- Intel® Core i7 CPU with Iris Xe GPU
- Ubuntu 22.04
- Diagnostic tools: `htop`, `intel_gpu_top`, `iotop`

## 🛠️ Example Inference Pipeline (DL Streamer)
This pipeline demonstrates real-time video analytics using Intel® DL Streamer and OpenVINO™, running on the GPU. It performs end-to-end object detection and vehicle classification on an input video using optimized Intel models.

```bash
gst-launch-1.0 filesrc location=sample_video.mp4 ! \
decodebin ! videoconvert ! \
gvadetect model=person-vehicle-bike-detection-2000.xml device=GPU ! \
gvaclassify model=vehicle-attributes-recognition-barrier-0039.xml device=GPU ! \
gvawatermark ! videoconvert ! fpsdisplaysink

🎯 What It Does
1. Reads a video file (sample_video.mp4)
2. Detects people, vehicles, and bikes using gvadetect
3. Classifies vehicle attributes (type, color) using gvaclassify
4. Overlays bounding boxes and attribute labels in real time
5. Displays FPS and rendering stats using fpsdisplaysink

### 📈 Sample Terminal Output

frame: 226 drop: 2 fps: 18.03 avg_fps: 17.94
frame: 227 drop: 2 fps: 17.95 avg_fps: 17.94
frame: 228 drop: 2 fps: 17.92 avg_fps: 17.94

✅ This confirms the pipeline sustains ~18 FPS throughput — well above the real-time threshold (10 FPS) defined in the project benchmarks.


## 📊 Benchmark Summary

| Mode | Max Streams | Avg FPS/Stream | Bottleneck |
|------|-------------|----------------|------------|
| CPU  | 2           | ~11 FPS        | Compute    |
| GPU  | 4           | ~17 FPS        | IO/Decode  |

## 📎 Files Included
- `Intel_Unnati_Aashwika_Khurana.pdf` – Final project report
- `images/` – Screenshots and visual outputs (optional)

## 🧠 Key Insights
- DL Streamer with OpenVINO enables real-time classification.
- CPU handles 2 streams, GPU handles 4.
- IO becomes bottleneck beyond 4 streams.
- Tools like `htop`, `intel_gpu_top`, and `iotop` help diagnose performance.

## 📊 Performance Snapshot

![Performance Comparison Chart](images/performance%20comparision%20chart.png)

## 💡 Bottleneck Analysis

![Bottleneck Source Breakdown](images/Bottleneck%20Source%20Breakdown.png)


## 👤 Author
**Aashwika Khurana**  
GITAM, Hyderabad  
Email: akhurana@gitam.in

