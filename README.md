# A-YOLO-and-DeepSORT-Based-Vehicle-Surveillance-System
project
```python
from ultralytics import YOLO

model = YOLO("runs/yolov8l_vehicles/weights/best.pt")
results = model("video.mp4", save=True, conf=0.5)
# Load both models
vehicle_model = YOLO("runs/yolov8l_vehicles/weights/best.pt")
plate_model = YOLO("runs/yolov8l_plates/weights/best.pt")

# Run both models on the same video
# This is just a simplified example – actual implementation combines results in one output video
vehicle_results = vehicle_model("video.mp4", conf=0.5)
plate_results = plate_model("video.mp4", conf=0.5)

```

To run with DeepSORT tracking, use the code inside `03_inference_and_tracking.ipynb`.
@@ -113,5 +120,5 @@ pip install ultralytics opencv-python torch deep_sort_realtime albumentations py
