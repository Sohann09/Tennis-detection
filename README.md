# 🎾 Tennis Court Object Detection with YOLOv5 🚀

Welcome to the **Tennis Court Object Detection** project! This mini-project leverages the power of YOLOv5 (You Only Look Once) to detect key elements in a tennis court, such as **players**, **nets**, and **pitch lines**. Whether you're a tennis enthusiast, a computer vision hobbyist, or just someone who loves cool tech, this project is for you!

---

## 🧐 What's Inside?

This project uses **YOLOv5**, a state-of-the-art object detection model, to identify and localize objects in tennis court images. Here's what you'll find in this repository:

- **YOLOv5 Implementation**: We've cloned the YOLOv5 repository and set it up for tennis court object detection.
- **Dataset**: A custom dataset (`tennis.v1i.yolov5pytorch.zip`) containing images of tennis courts, annotated with bounding boxes for players, nets, and pitch lines.
- **Training & Inference**: The code is ready for training the model on the dataset and running inference to detect objects in new images.

---

## 🛠️ How It Works

1. **Clone YOLOv5**: We start by cloning the YOLOv5 repository, which provides the backbone for our object detection model.
2. **Install Dependencies**: All necessary dependencies are installed to ensure smooth execution.
3. **Dataset Preparation**: The dataset is unzipped and organized into `train` and `test` folders, each containing images and corresponding labels.
4. **Training**: The model is trained on the dataset to learn how to detect players, nets, and pitch lines.
5. **Inference**: Once trained, the model can be used to detect objects in new images or videos.

---

## 🚀 Getting Started

### Prerequisites

- **Google Colab**: We can make use of the free tier provided by google for this project.

### Steps to Run the Project

1. **Clone the Repository**:
   ```bash
   !git clone https://github.com/ultralytics/yolov5.git
   ```

2. **Navigate to the YOLOv5 Directory**:
   ```bash
   %cd yolov5
   ```

3. **Install Dependencies**:
   ```bash
   !pip install -qr requirements.txt
   ```

4. **Unzip the Dataset**:
   ```bash
   !unzip tennis.v1i.yolov5pytorch.zip
   ```

5. **Train the Model**:
   ```bash
   !python train.py --img 640 --batch 16 --epochs 50 --data data.yaml --weights yolov5s.pt
   ```

6. **Run Inference**:
   ```bash
   !python detect.py --source test/images --weights runs/train/exp/weights/best.pt --conf 0.4
   ```

---

## 📊 Results

After training, the model will be able to detect:
- **Players**: Identify players on the court.
- **Nets**: Locate the tennis net.
- **Pitch Lines**: Detect the boundaries and lines of the tennis court.

![image1](https://github.com/user-attachments/assets/a261e7f4-ce11-4197-a09f-09181767c528)


## 🧠 Why YOLOv5?

- **Speed**: YOLOv5 is incredibly fast, making it suitable for real-time applications.
- **Accuracy**: Despite its speed, YOLOv5 maintains high accuracy in object detection tasks.
- **Ease of Use**: The YOLOv5 repository is well-documented and easy to set up, even for beginners.

---

## 🤔 Challenges & Solutions

- **Challenge**: The dataset may have imbalanced classes (e.g., more players than nets).
  - **Solution**: Use data augmentation techniques to balance the dataset and improve model performance.
  
- **Challenge**: Overfitting on the training data.
  - **Solution**: Implement early stopping and regularization techniques during training.

---

## 🎯 Future Enhancements

- **Real-Time Detection**: Integrate the model with a live video feed for real-time tennis court analysis.
- **Multi-Court Detection**: Extend the model to detect multiple courts in a single frame.
- **Player Tracking**: Add player tracking to analyze movement patterns during a match.

---

## 🙌 Credits

- **YOLOv5**: Thanks to the Ultralytics team for their amazing work on YOLOv5.
- **Dataset**: The dataset used in this project was sourced from [Roboflow](https://roboflow.com/).

---


## 🎉 Happy Coding!

Whether you're a tennis fan or a tech enthusiast, we hope you enjoy this project. Feel free to contribute, raise issues, or suggest improvements. Let's ace this game of object detection together! 🎾

---

**Made with ❤️ by Sohan**  
*"In tennis, love means zero . I know this is a small project but small steps to reach the top right"* 😄
