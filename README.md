# Seam Carving – Content Aware Image Resizing  
*A C++ implementation using OpenCV*  

## 📌 Overview  
This project implements **seam carving**, a content-aware image resizing algorithm. Unlike naive scaling, seam carving removes **low-energy seams** (paths of least importance) from an image, preserving the most significant content while reducing dimensions.  

The program supports:  
- **Vertical seam removal** (reduce width)  
- **Horizontal seam removal** (reduce height)  
- Visualization of seams being removed in real time  
- Saving the resized image as `resizedImage.jpg`  

---
## Demo

<table>
<tr>
<td width="50%" align="center">

https://github.com/user-attachments/assets/f48a06ce-c108-4d7e-b0bb-f2df71ed20ce

<b>seam carving </b> — width height reduction

</td>
<td width="50%" align="center">

https://github.com/user-attachments/assets/83219d38-95ea-4c10-b11f-8e50a41e28ff

<b>seam carving </b> — width height reduction

</td>
</tr>
</table>

---

## ⚙️ Features  
- **Energy Calculation** – Computes energy of each pixel using gradient magnitude.  
- **Dynamic Programming** – Finds the minimum-energy seam efficiently.  
- **Seam Removal** – Removes seams iteratively to reach target width/height.  
- **Visualization** – Displays intermediate steps with seams highlighted.  
- **Custom Memory Management** – 3D/2D arrays manually managed (no STL vectors).  

---

## 🛠️ Tech Stack  
- **Language**: C++  
- **Library**: OpenCV (for image I/O and visualization)  

---

## 📂 Project Structure  

---SeamCarving/  
│── SeamCarving.cpp # Source code  
│── README.md 
## 🚀 How to Run  

### 1. Install OpenCV  
On Ubuntu:  
```bash
sudo apt-get update
sudo apt-get install libopencv-dev
```
### 2. Compile the Code
``` bash
g++ main.cpp -o seamCarving `pkg-config --cflags --libs opencv4`
```
### 3. Run the Program
``` bash
./seamCarving
```

Enter the image path and desired new dimensions when prompted:  
```
Enter path of image  
sample.jpg  
Given Image has Height:800 and Width:1200  
Enter the new height and width (This value should be strictly lesser than original height and width)  
600 900 
```  
---

