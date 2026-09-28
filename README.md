# Fingerspell: Real-Time On-Device ASL Recognition

*Fingerspell* is a lightweight, privacy-first web application for real-time American Sign Language (ASL) static fingerspelling recognition. Powered by MediaPipe Hands and client-side geometric classification, all computer vision processing runs locally in the browser—no video data ever leaves the user's device.

---

## Key Features

- **Privacy-First Architecture:** Complete client-side frame processing ensures zero webcam data transmitted to external servers.
- **Rotation-Invariant Geometric Classification:** Calculates joint bend angles and Euclidean distances relative to a palm-local 3D coordinate frame.
- **Hybrid Classifier:** Combines a deterministic rule-based engine for static letters ($A$–$Y$, excluding $J$ and $Z$) with a local k-Nearest Neighbor (k-NN) calibration layer.
- **Jitter Reduction:** Applies Exponential Moving Average (EMA) landmark smoothing and temporal prediction buffering to prevent flickering.

---

## Getting Started

Because the application is built completely serverless with HTML5, CSS, and JavaScript, no complex installation or backend setup is required.

### Running Locally

1. Clone or download this repository.
2. Open `index.html` directly in any modern web browser (Google Chrome or Mozilla Firefox recommended).
3. Grant local webcam permissions when prompted.

---

## Tech Stack

- **Frontend:** HTML5, CSS3, JavaScript (ES6)
- **Computer Vision Framework:** Google MediaPipe Hands
- **Classification:** Geometric rule engine + On-device k-NN (Custom JavaScript)
