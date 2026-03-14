# 🔊 Gesture Based Volume Control – Milestone 3

## 📌 Project Overview
The **Gesture Based Volume Control Interface** is a real-time computer vision application that allows users to control the system volume using hand gestures. The system uses **MediaPipe hand tracking** to detect hand landmarks and calculates the distance between the **thumb and index finger** to determine the desired volume level.

The application is built using **Streamlit, OpenCV, and MediaPipe**, providing a live interface where users can see hand detection, volume percentage, and graphical visualization of the distance-to-volume mapping.

This milestone extends the previous gesture recognition system by integrating **actual system volume control** and adding **data visualization components** such as real-time graphs and volume history tracking.

---

# 🎯 Objectives
- Detect hand landmarks using **MediaPipe**
- Measure the distance between **thumb and index finger**
- Map finger distance to **system volume levels**
- Adjust the **device volume in real time**
- Display **live webcam preview**
- Show **distance-to-volume mapping graph**
- Track **volume history over time**

---

# 🛠️ Technologies Used

| Technology | Purpose |
|------------|--------|
| Python | Core programming language |
| Streamlit | Interactive web interface |
| OpenCV | Webcam capture and image processing |
| MediaPipe | Hand tracking and landmark detection |
| NumPy | Mathematical calculations |
| Matplotlib | Data visualization |
| Pycaw | Windows system volume control |
| OS commands | macOS/Linux volume control |

---

# 📂 Project Structure

```
HAND_GESTURE_MILESTONE3
│
├── milestone3.py
├── README.md


---

# ⚙️ Installation

## 1️⃣ Clone the Repository

```bash
git clone https://github.com/akhilakummari-26/HAND_GESTURE_MILESTONE_3/.git


---

## 2️⃣ Install Dependencies

 Install the below libraries

```bash
pip install streamlit opencv-python mediapipe numpy matplotlib pycaw comtypes
```

---

# ▶️ Running the Application

Run the Streamlit application:

```bash
streamlit run milestone3.py
```

The application will open in your browser:

```
http://localhost:8501
```

---

# 🖥️ Application Interface

The interface consists of two main sections.

---

## Left Panel – Distance to Volume Mapping

Displays a **graph showing how finger distance maps to system volume percentage**.

- Shows the relationship between gesture distance and volume
- Highlights the current distance and volume point

---

## Right Panel

### 🔊 Current Volume
Displays the **current system volume percentage**.

### 📷 Live Preview
Shows the **live webcam feed** with detected hand landmarks.

### 📈 Volume History
Displays a **graph tracking volume changes over time**.

---

# 🧠 How the System Works

1. The webcam captures live video frames using **OpenCV**.
2. Frames are processed using **MediaPipe Hands** to detect hand landmarks.
3. The system identifies:
   - **Thumb tip (Landmark 4)**
   - **Index finger tip (Landmark 8)**
4. The **distance between these two points** is calculated.
5. The distance is mapped to a **volume range (0–100%)**.
6. The system volume is updated accordingly.

---

# 📐 Distance to Volume Mapping

The system uses interpolation:

```
Volume = interpolate(distance, [20,120] → [0,100])
```

Where:

- **20 pixels → 0% volume**
- **120 pixels → 100% volume**

This allows smooth gesture-based control.

---

# ✋ Gesture Control

| Finger Distance | Volume Level |
|----------------|--------------|
| Small distance | Low volume |
| Medium distance | Medium volume |
| Large distance | High volume |

---

# 📊 Features

- Real-time **gesture-based volume control**
- Live **hand landmark detection**
- **Distance-to-volume visualization**
- **Volume history graph**
- **Cross-platform support** (Windows / macOS / Linux)
- Smooth **volume interpolation**

---

# 💻 Supported Operating Systems

| OS | Volume Control Method |
|----|-----------------------|
| Windows | Pycaw API |
| macOS | AppleScript |
| Linux | amixer command |

---

# 🚀 Future Improvements

Possible future enhancements include:

- Gesture-based **media playback control**
- **Machine learning gesture classification**
- Multi-hand gesture support
- Voice + gesture hybrid control
- Smart home integration

---

# 📚 Applications

Gesture-based volume control can be used in:

- Touchless computer interfaces
- Smart home systems
- Assistive technologies
- Virtual reality systems
- Gaming environments
- Public interactive displays

---

# 👩‍💻 Author

**Akhila Kummari**

---

# 📜 License

This project is licensed under the MIT License.

