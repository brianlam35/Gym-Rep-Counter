README.md — Gym Rep Counter

Gym Rep Counter — Real-Time Angle-Based Rep Tracking

The Gym Rep Counter is a lightweight, single-file Python tool that uses OpenCV and pose-estimation landmarks to automatically count repetitions for common exercises. By tracking key body joints and computing real-time joint angles, the script detects full movement cycles (e.g., squat down → squat up) and increments reps without any manual input.

⸻

Features
	•	Automatic rep counting based on joint-angle thresholds
	•	Real-time pose estimation for exercises like squats, curls, shoulder press, etc.
	•	Skeleton and angle overlay drawn directly on the video feed
	•	No external UI needed — simple, single-file execution
	•	Supports webcams or video files

⸻

How It Works
	1.	Pose landmarks are extracted every frame.
	2.	Relevant joint angles (knee, elbow, shoulder, etc.) are computed using vector geometry.
	3.	When an angle reaches a “bottom” threshold and then returns to a “top” threshold, one rep is counted.
	4.	The result, skeleton, and angle are displayed live on screen.

```py
python gym_rep_counter.py
```

Press q to quit the window.
	•	Modify the script variables to switch exercises or angle thresholds.

⸻

🛠 Requirements
	•	Python 3
	•	OpenCV
	•	Mediapipe (or your pose-estimation model)
	•	NumPy

Install dependencies:
```py
pip install opencv-python mediapipe numpy
```

Project Goal

Provide a minimal, real-time, angle-based workout analyzer for tracking reps without wearables, buttons, or sensors.
