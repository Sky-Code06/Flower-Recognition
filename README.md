# Flower Recognition

Dataset link: https://www.kaggle.com/datasets/alxmamaev/flowers-recognition

Project Summary: Flower Classification System 🌸
Project Overview This project builds an Artificial Intelligence system capable of visually recognizing and classifying 5 different types of flowers: Daisy, Dandelion, Rose, Sunflower, and Tulip. The core objective is to compare two different Deep Learning strategies—building a brain from scratch versus "borrowing" a genius brain—to see which is more effective.

Methodology
Data Processing (The Assembly Line):
Used the "Flowers Recognition" dataset.

Implemented Data Augmentation: We artificially rotated, flipped, and zoomed images. This forced the AI to learn the concept of a flower rather than just memorizing specific photos (e.g., recognizing a sunflower even if it's upside down).

Approach A: Custom CNN (The "Student"):
Built from Scratch: We constructed a Convolutional Neural Network layer-by-layer using Conv2D (to find edges) and MaxPooling (to compress data).
Performance: Like a beginner student, it started with low accuracy (~55%) and slowly learned over time, reaching about 65-70% accuracy. It struggled to distinguish tricky flowers.

Approach B: Transfer Learning (The "Expert"):
Used MobileNetV2: We utilized a pre-trained model created by Google that had already studied 1.4 million images (ImageNet).
Technique: We "froze" its feature detection layers (so it wouldn't forget its prior knowledge) and only trained the final "decision" layer.
Performance: It achieved ~85-90% accuracy almost immediately, proving to be much faster and smarter than the custom model.

Key Results
Visual Proof: The accuracy graph clearly showed the Transfer Learning model (Orange Line) consistently outperforming the Custom CNN (Blue Line).
Real-World Test: When tested on random images from the internet, the Transfer Learning model correctly identified flowers with high confidence (e.g., 99%), whereas the Custom model was often less confident or incorrect.

Technologies Used
TensorFlow/Keras: To build and train the Neural Networks.
Python: The programming language.
Matplotlib: To visualize the accuracy comparison graphs.
NumPy: For image data manipulation.
