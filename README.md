# Blink-Based Liveness Detection System

This project implements a simple **liveness detection system** using **blink detection** and **head orientation prompts** (left/right turns) with OpenCV, dlib, and Haar cascade classifiers.

The system ensures a real user is present by instructing them to **turn their head left and right and blink**, using Eye Aspect Ratio (EAR) to detect blinks. It's useful in basic anti-spoofing systems for facial recognition.

---

## 🧠 How It Works

- Detects faces using **Haar cascades** (frontal and profile).
- Uses **dlib's 68-point face landmark predictor** to locate the eyes.
- Calculates **EAR (Eye Aspect Ratio)** to detect blinks.
- Instructs the user to:
  1. Turn left and blink.
  2. Turn right and blink.
- Confirms liveness if at least one blink is detected in each instruction.

---

## 📦 Requirements

Install the following dependencies:

```bash
pip install opencv-python dlib imutils scipy numpy
