# Magic Circle Hand Tracker

This project creates an interactive augmented reality (AR) application that overlays "Doctor Strange" style magic circles on your hands as you gesture. When you open your palm, the program displays animated magical circles that follow your hand movements.

## Overview

The application uses computer vision and hand tracking to:
1. Detect hand landmarks in real-time using the webcam
2. Track specific hand positions and gestures
3. Display magical circles when you open your palm
4. Show magical energy lines connecting your fingertips in certain hand positions

## Requirements

- Python 3.6+
- OpenCV (`cv2`)
- MediaPipe
- Magic circle image assets (in a folder named `magic_circles`)
  - `magic_circle_1.png`
  - `magic_circle_2.png`

## Installation

```bash
pip install opencv-python
pip install mediapipe
```

## Usage

1. Place two magic circle PNG images (with transparency) in a folder called `magic_circles`:
   - `magic_circles/magic_circle_1.png`
   - `magic_circles/magic_circle_2.png`

2. Run the program:
   ```bash
   python magic_circles.py
   ```

3. Hand gestures:
   - Open your palm wide to display the rotating magic circles
   - Partially close your hand to display magical energy lines between your fingertips

4. Press 'q' to quit the application

## How It Works

The application:
- Captures video from your webcam
- Uses MediaPipe's hand detection to identify hand landmarks
- Calculates the ratio between finger distances to detect hand gestures
- When your palm is wide open, it overlays rotating magic circles centered on your hand
- When your hand is partially closed, it draws glowing lines connecting your fingertips

## Customization

You can modify various aspects of the program:
- Change the magic circle images
- Adjust the shield size variable to make the circles larger or smaller
- Modify the rotation speed by changing the `ang_vel` value
- Customize the color and thickness of the energy lines in the `draw_line` function

## Acknowledgments

This project uses:
- MediaPipe for hand tracking capabilities
- OpenCV for image processing and display
