# Virtual-Mouse-Control
An experimental Human-Computer Interaction (HCI) application built with Python, OpenCV, and MediaPipe. Unlike standard gesture controllers, this app features a dual-display interface: a live webcam diagnostic feed and a dedicated, high-performance "Virtual Mouse" window that renders an animated multi-cursor visual.
.

🌟 Key Features
Dual-Window Architecture: * Webcam Monitor: A low-latency window showing real-time hand landmark detection and tracking status.

Virtual Workspace: A stylized window that renders a custom, animated multi-cursor (e.g., a "trail" or "halo" effect) driven by your finger movements.

Pinch-to-Action Gestures: * Navigation: Movement is controlled via the tip of the Index Finger (Landmark 8).

Action Trigger: Performs a "Left Click" when the distance between the Thumb (Landmark 4) and Index Finger falls below a dynamic threshold.

Animated Visual Feedback: The multi-cursor isn't just a dot; it uses a "velocity-aware" animation that grows, shrinks, or leaves a trail based on your hand's speed and gesture state.

Precision Smoothing: Implements a Moving Average Filter to eliminate jitter, ensuring the on-screen cursor feels fluid and intentional.

🛠️ Technical Stack
Core Logic: Python 3.x

Vision Engine: MediaPipe Hands (High-fidelity tracking of 21 3D landmarks).

Graphics & Rendering: OpenCV (for drawing the diagnostic feed and the separate animated cursor window).

System Integration: PyAutoGUI or pynput for bridging gestures to OS-level mouse events.
