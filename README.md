# Planar Augmented Reality using Classical and Deep Feature Matching

This project implements a complete **planar augmented reality (AR) pipeline** for images and videos using both **classical computer vision** and **deep learning–based feature matching** techniques.  
The system overlays images or videos onto a planar surface (a monitor) while maintaining geometric consistency and temporal stability.

---

## 📌 Project Overview

The notebook demonstrates:
- Perspective warping using **homography estimation**
- Feature-based planar tracking in videos
- Seamless image/video compositing with feathered blending
- A comparison between **SIFT-based** and **SuperGlue-based** matching pipelines

The final result is a realistic AR effect where static or dynamic content appears naturally attached to a moving surface.

---

## 🧠 Implemented Pipelines

### 1. Image-to-Image Planar Overlay
- Manual corner annotation of a planar surface
- Homography estimation using point correspondences
- Perspective warping and feathered blending

---

### 2. Image-on-Video Augmentation (Classical CV)
- SIFT feature detection and description
- Brute-force matching with Lowe’s ratio test
- RANSAC-based homography estimation
- Temporal homography smoothing for jitter reduction
- Robust fallback using last valid transformation

---

### 3. Video-on-Video Augmentation (Classical CV)
- Continuous planar tracking across frames
- Dynamic warping of video frames onto a target surface
- Automatic looping of source video
- Seamless blending for realistic display

---

### 4. Deep Learning–Based Augmentation with SuperGlue
- **SuperPoint** for learned keypoint detection
- **SuperGlue** for context-aware feature matching
- Improved robustness under motion blur, illumination changes, and viewpoint shifts
- Identical AR pipeline with a learned matcher replacing SIFT

---

## 🔧 Core Techniques Used

- Projective Geometry (Homographies)
- RANSAC Outlier Rejection
- Temporal Filtering via Exponential Smoothing
- Feature-Based Planar Tracking
- Feathered Alpha Blending
- Classical vs Deep Feature Matching

---

## 🧪 Outputs

The notebook generates:
- Image overlays on planar surfaces
- Image-on-video AR results
- Video-on-video AR results
- Versions using both **SIFT** and **SuperGlue** for comparison

All processed outputs are saved as images or MP4 videos.

---

## 📊 Classical vs Deep Matching

| Aspect | SIFT | SuperGlue |
|------|------|-----------|
| Feature Type | Hand-crafted | Learned |
| Robustness | Moderate | High |
| Matching Consistency | Frame-dependent | Context-aware |
| AR Stability | Good | Excellent |

---

## 📁 Dataset

The project uses provided images and videos featuring a planar monitor surface.  
Monitor corner coordinates are manually annotated in the reference frame.

---
