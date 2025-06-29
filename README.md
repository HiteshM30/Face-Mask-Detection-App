# Face Mask Detection App

This project is a real-time face mask detection web application designed to enhance safety by identifying whether individuals are wearing masks. Built with a combination of advanced technologies, it provides an efficient and user-friendly solution for monitoring compliance.

## Technologies Used
- YOLOv8: For real-time object detection, specifically to detect faces.
- MediaPipe: For landmark validation to ensure detections are valid human faces and reduce false positives.
- TensorFlow/Keras (optional): For additional mask classification capabilities.
- Flask: Serves as the backend web server to handle requests and responses.
- SQLite: Used for logging mask violation data with timestamps.
- HTML/CSS/JavaScript: Powers the frontend interface for an interactive user experience.

## Features
- Real-time Camera Access: Utilizes the user's webcam for live detection.
- Multiple Face Detection: Capable of identifying and analyzing multiple faces simultaneously.
- Mask Classification: Classifies each detected face as "Mask" or "No Mask".
- Bounding Boxes: Highlights detected faces with colored bounding boxes for visual feedback.
- Violation Logging: Stores timestamped violation data (e.g., no mask detected) in a SQLite database.
- Dashboard: Provides a live feed view and access to logged violation data.

## Project Structure
```
├── face_mask_dataset_dashboard
├── runs
├── templates
├── yolo_dataset_ready
├── gitignore
├── analyze_violations.py
├── app.py
├── face_mask_detector_keras
├── log_to_db.py
├── mask_violations.db
├── prepare_dataset.py
├── README.md
├── requirements.txt
├── split_train_val_yolo.py
├── tempCodeRunnerFile.py
├── violations.log
└── yolo8n.pt
```

## How to Run
1. Clone the Repository:  
   `git clone https://github.com/HiteshM30/Face-Mask-Detection-App.git`
2. Install Dependencies:  
   `pip install -r requirements.txt`
3. Run the Application:  
   `python app.py`
4. Access the App: Open your web browser and navigate to the provided local host address (e.g., `http://127.0.0.1:5000`).

## Model Info
- YOLOv8 Model: Trained on a custom dataset located in the `yolo_dataset_ready/` folder. The model uses YOLO annotation (.txt files) for labeling.
- MediaPipe Integration: Enhances accuracy by validating face landmarks, ensuring detections are of human faces.

## Database
- File: `mask_violations.db`
- Stored Data:
  - Timestamp of detection
  - Detection type (mask or no_mask)
  - Image (optional, stored as base64 or file path)

## Dataset
- Location: `yolo_dataset_ready/` folder
- Format: YOLO annotation (.txt files) for training data.

## Contributing
We welcome contributions to improve this project! Please follow these steps:
- Fork the repository and create your branch.
- Submit pull requests for review. For major changes, please open an issue first to discuss the proposed changes.
- Ensure your code adheres to the project's coding standards and includes appropriate documentation.