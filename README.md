Seam Carving – Content Aware Image Resizing

A C++ implementation using OpenCV

📌 Overview

This project implements seam carving, a content-aware image resizing algorithm. Unlike naive scaling, seam carving removes low-energy seams (paths of least importance) from an image, preserving the most significant content while reducing dimensions.

The program supports:

Vertical seam removal (reduce width)

Horizontal seam removal (reduce height)

Visualization of seams being removed in real time

Saving the resized image as resizedImage.jpg

⚙️ Features

Energy Calculation – Computes energy of each pixel using gradient magnitude.

Dynamic Programming – Finds the minimum-energy seam efficiently.

Seam Removal – Removes seams iteratively to reach target width/height.

Visualization – Displays intermediate steps with seams highlighted.

Custom Memory Management – 3D/2D arrays manually managed (no STL vectors).

🛠️ Tech Stack

Language: C++

Library: OpenCV (for image I/O and visualization)

📂 Project Structure
SeamCarving/
│── main.cpp          # Source code
│── sample.jpg        # Input image (example)
│── resizedImage.jpg  # Output image (generated after execution)
│── README.md         # Documentation
│── Makefile          # For compilation (optional)

🚀 How to Run
1. Install OpenCV

On Ubuntu:

sudo apt-get update
sudo apt-get install libopencv-dev


On Windows:

Install OpenCV from opencv.org

Configure paths in your IDE/MinGW setup

2. Compile the Code
g++ main.cpp -o seamCarving `pkg-config --cflags --libs opencv4`

3. Run the Program
./seamCarving


Enter the image path and desired new dimensions when prompted:

Enter path of image
sample.jpg
Given Image has Height:800 and Width:1200
Enter the new height and width (This value should be strictly lesser than original height and width)
600 900

📊 Example

Input Image (1200×800)
→ Output Image (900×600)

The algorithm gradually removes seams until the desired size is reached.

Seams being removed are shown in black (vertical) or red (horizontal).

🧮 Algorithm Steps

Read Image – Load pixels into a 3D RGB matrix.

Energy Matrix – Compute gradient energy for each pixel.

DP Matrix – Use dynamic programming to find minimum-energy seam.

Seam Detection – Trace back seam path.

Seam Removal – Delete seam and shift pixels.

Repeat until target width/height is achieved.

📌 Sample Output
Resized image saved as resizedImage.jpg
