# Driver Drowsiness Detection System (DDD-KU)

## 📋 Project Overview

A real-time driver drowsiness detection system using deep learning and computer vision. The system monitors driver's eye state (open/closed) to detect signs of drowsiness and provide alerts.

### Key Features
- **Real-time Eye State Detection**: Uses MobileNetV2-based CNN model
- **Face Landmark Detection**: MediaPipe for facial feature tracking
- **Drowsiness Alert System**: Audio and visual alerts when drowsiness detected
- **Multiple Input Sources**: Supports webcam and video file input
- **High Accuracy**: Fine-tuned transfer learning model

### System Architecture

```
Input (Webcam/Video) 
    ↓
Face Detection (MediaPipe)
    ↓
Eye Region Extraction
    ↓
Eye State Classification (MobileNetV2)
    ↓
Drowsiness Detection Logic
    ↓
Alert System (Audio/Visual)
```

---

## 🚀 How to Install

### Step 1: Clone the Repository
```bash
git clone https://github.com/yourusername/DDD-KU.git
cd DDD-KU
```

### Step 2: Create Virtual Environment

**Windows:**
```bash
python -m venv venv
venv\Scripts\activate
```

**Linux/Mac:**
```bash
python3 -m venv venv
source venv/bin/activate
```

### Step 3: Install Dependencies
```bash
pip install -r requirements.txt
```

---

## 🎯 How to Run

### Open the Demo Notebook
```bash
jupyter notebook demos/demo_script.ipynb
```

### Configure Input Source

In the notebook, locate the configuration cell and set the input source:

```python
# ============= INPUT SOURCE CONFIGURATION =============

# Option 1: Use Webcam (Camera)
VIDEO_PATH = None
INPUT_SOURCE = 0 if VIDEO_PATH is None else VIDEO_PATH

# Option 2: Use Video File
# VIDEO_PATH = r'C:\path\to\your\video.mp4'
# INPUT_SOURCE = 0 if VIDEO_PATH is None else VIDEO_PATH
```

### Understanding the Configuration

**When `VIDEO_PATH = None`:**
- The system will use your **computer's camera** (webcam)
- `INPUT_SOURCE = 0` means use the default camera
- Change to `1`, `2`, etc. if you have multiple cameras

**When `VIDEO_PATH` is set to a file path:**
- The system will use the **video file** instead of camera
- Example: `VIDEO_PATH = r'C:\videos\test_video.mp4'`
- `INPUT_SOURCE` will be set to the video file path

### Run the Demo

1. Set `VIDEO_PATH = None` to use webcam
2. Run all cells in the notebook
3. Press `q` or `ESC` to quit

---

### Demo video
Both the demo video and the video used in the demo can be found at this link:
- https://drive.google.com/drive/folders/1puIjROW2Rsw23dBPtFqzkRba2mCDp7M3