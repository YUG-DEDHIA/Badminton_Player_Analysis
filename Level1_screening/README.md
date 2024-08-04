

# Badminton Player Detection and Comparison

This project uses the YOLOv8 model to detect badminton players in an image, removes the background, and compares the players based on their feature vectors using cosine similarity.

## Project Overview

The main steps of the project include:

1. **Importing Libraries**:
   - Essential libraries for image processing and machine learning are imported, including `cv2`, `numpy`, `torch`, and `PIL`.

2. **Player Detection using YOLOv8**:
   - The YOLOv8 model is loaded for detecting players in the images.
   - The input image is split into bottom and top halves for separate analysis.

3. **Object Detection and Annotation by YOLO**:
   - Detection is performed, and the detected players are annotated.
   - The number of detected players is counted and displayed.

4. **Masking the Background**:
   - A mask is created to separate players from the background.

5. **Object Masking and Extraction**:
   - Masks for detected players and the background are generated.
   - Individual player images are extracted and saved.

6. **Background Extraction**:
   - The dominant background color is computed using k-means clustering.

7. **Background Removal**:
   - The dominant background color is removed from player images.
   - Processed images are saved in separate directories for further comparison.

8. **Player Comparison**:
   - Players are compared based on the cosine similarity of their feature vectors.
   - Players are categorized into different folders based on the similarity comparison.

## Installation

To run this project, you need to have the following dependencies installed:

- OpenCV (`cv2`)
- NumPy
- PyTorch
- PIL (Python Imaging Library)
- torchvision

You can install these dependencies using the following command:

```bash
pip install opencv-python numpy torch pillow torchvision
```

## Usage

1. **Load the YOLOv8 Model**:
   - Replace `'yolov8n.pt'` with the path to your trained YOLOv8 model.

2. **Load and Preprocess Images**:
   - Load the image and split it into bottom and top halves.

3. **Detection and Masking**:
   - Run the YOLO model on the images to detect players.
   - Create masks for the players and the background.

4. **Background Color Removal**:
   - Compute the dominant background color and remove it from the player images.

5. **Comparison of Players**:
   - Compare players based on the cosine similarity of their feature vectors.

## Acknowledgements

- [YOLOv8 Model](https://github.com/ultralytics/yolov5) for object detection.
- [OpenCV](https://opencv.org/) for image processing.
- [PyTorch](https://pytorch.org/) for machine learning capabilities.

---
