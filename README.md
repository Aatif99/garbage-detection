# 🗑️ Garbage Detection using YOLOv5

Welcome to the Garbage Detection project! This repository contains a custom-trained YOLOv5 model designed to detect various types of garbage in images and videos. The goal is to aid in environmental cleanliness by automating the detection of waste materials.

---

## 📂 Project Structure

- `best.pt`: The trained YOLOv5 model weights.
- `detect.py`: Script to run inference using the trained model.
- `requirements.txt`: Python dependencies required to run the project.
- `README.md`: Project documentation.

---

## 🚀 Getting Started

### Prerequisites

- Python 3.7 or higher
- pip package manager

### Installation

```bash
git clone https://github.com/Aatif99/garbage-detection.git
cd garbage-detection
pip install -r requirements.txt
```

---

## 🖼️ Running Inference

To perform garbage detection on an image or video, use the `detect.py` script:

```bash
python detect.py --weights best.pt --img 640 --conf 0.25 --source path/to/your/image_or_video
```

**Parameters:**
- `--weights`: Path to the trained model weights.
- `--img`: Inference image size.
- `--conf`: Confidence threshold for detections.
- `--source`: Path to the input image, video file, directory, URL, or webcam index.

**Examples:**

- Detect garbage in an image:

  ```bash
  python detect.py --weights best.pt --img 640 --conf 0.25 --source data/images/trash.jpg
  ```

- Detect garbage using the webcam:

  ```bash
  python detect.py --weights best.pt --img 640 --conf 0.25 --source 0
  ```

---

## 🧠 Model Training

If you wish to train the model on your own dataset:

1. **Prepare your dataset** in YOLO format with corresponding `.yaml` configuration.

2. **Run the training script:**

   ```bash
   python train.py --img 640 --batch 16 --epochs 50 --data data/garbage.yaml --weights yolov5s.pt --cache
   ```

**Training Parameters:**
- `--img`: Training image size.
- `--batch`: Batch size.
- `--epochs`: Number of training epochs.
- `--data`: Path to the dataset configuration file.
- `--weights`: Pretrained weights to start training from.
- `--cache`: Cache images for faster training.

---

## 📊 Results

After running inference, results will be saved in the `runs/detect/exp` directory by default. This includes:

- Annotated images with bounding boxes.
- Inference statistics and logs.

---

## 🧮 Contributing

Contributions are welcome! If you have suggestions or improvements, feel free to fork the repository and submit a pull request.

---

## 📄 License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

---

# 🚀 Let's Make the World Cleaner!
