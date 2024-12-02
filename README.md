# Face-Recognition-using-MtCNN

# Introduction
A face recognition system combines detection and recognition techniques to capture facial images and convert them into unique face prints for applications like security and verification. MTCNN efficiently detects and isolates faces, while recognition algorithms classify them based on distinctive features. The process involves image acquisition, detection using MTCNN, and recognition using CNNs with TensorFlow and TFlearn. This robust system enhances security by identifying individuals through automated facial recognition.

# Project Goals
The main goal of the project is to develop a robust face recognition system that accurately detects and recognizes individuals based on unique facial features. Applications include enhancing security in public spaces, enabling person verification, and preventing criminal activities. It can be used in surveillance systems, attendance management, and secure access control. This system is crucial for improving safety and operational efficiency across various domains.

# Methodology
Convolutional Neural Networks (CNNs) are deep learning models designed to process structured grid-like data such as images, extracting meaningful features through convolutional layers. They are highly effective for image classification, object detection, and face recognition due to their ability to learn spatial hierarchies of features.
MTCNN (Multi-task Cascaded Convolutional Networks) is specifically used for face detection because it efficiently locates faces in images and identifies key facial landmarks like eyes and mouth. Its multi-tasking nature, combining face detection and landmark localization, makes it fast, accurate, and robust against variations in pose, lighting, and facial expressions.

The Multi-task Cascaded Convolutional Network (MTCNN) operates through a three-stage cascaded framework for efficient and accurate face detection and facial landmark localization:
Proposal Network (P-Net):
Scans the image at different scales to generate candidate face regions.
Uses a sliding window approach to identify potential bounding boxes for faces.
Outputs bounding boxes with a confidence score and applies non-maximum suppression (NMS) to reduce overlapping boxes.
Refine Network (R-Net):
Refines the candidate face regions generated by the P-Net.
Filters out false positives and adjusts the bounding box coordinates for better accuracy.
Again, applies NMS to maintain high-quality bounding boxes
Output Network (O-Net):
Processes the refined bounding boxes and provides precise face detection results.
Outputs five facial landmarks (eyes, nose, and mouth corners) to assist in alignment or further processing.
Optimizes both the bounding box and the landmark locations for accurate face detection.
Key Features:
The cascading design progressively narrows down to the most accurate detections.
Simultaneously performs face detection and facial landmark localization, ensuring speed and accuracy.
Handles variations in pose, scale, and lighting effectively.
This multi-stage approach makes MTCNN highly reliable for face detection tasks.

# Analysis
 MTCNN algorithm for face detection and InceptionResnetV1 for face recognition. It first processes a dataset of images to extract facial embeddings and save them to a file (data.pt). Then, it continuously captures frames from the webcam, detects faces, and compares the extracted face embeddings with the saved ones to recognize individuals. If a match is found with a sufficiently low distance, the person's name is displayed and the frame is saved. The program also installs necessary libraries like facenet-pytorch and opencv-python.

# Conclusion
In conclusion, MTCNN proves to be a highly accurate and robust face detection algorithm, capable of handling varying conditions such as different face sizes, lighting, and rotations. Its efficiency in real-time processing, achieving up to 45 FPS on rescaled videos and 6-8 FPS on full HD videos on a CPU, makes it well-suited for practical applications requiring face detection at high speeds. This performance ensures that MTCNN is a reliable choice for real-time face recognition systems, enhancing their usability in security, surveillance, and other related fields
