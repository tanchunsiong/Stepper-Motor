# Face-Tracking Camera with Stepper Motor

Automated face-tracking camera system using Windows IoT Core, facial recognition, and stepper motor control. The camera automatically follows detected faces by rotating the camera mount using a ULN2003 stepper motor driver.

Built for DX Hackfest in April 2016.

## Features

- Real-time face detection using Windows.Media.FaceAnalysis
- Automatic camera panning to track detected faces
- ULN2003 stepper motor driver with multiple drive modes (wave, full-step, half-step)
- GPIO-based motor control for Raspberry Pi
- Live video preview with face bounding boxes
- Adjustable tracking sensitivity and speed

## Tech Stack

- **Platform**: Windows 10 IoT Core, Universal Windows Platform (UWP)
- **Language**: C#
- **Hardware**: Raspberry Pi, ULN2003 stepper motor driver, 28BYJ-48 stepper motor
- **APIs**: Windows.Media.Capture, Windows.Media.FaceAnalysis, Windows.Devices.Gpio
- **UI**: XAML

## Hardware Requirements

- Raspberry Pi (2 or 3)
- USB webcam or Raspberry Pi camera module
- 28BYJ-48 stepper motor
- ULN2003 stepper motor driver board
- 5V power supply for motor
- Jumper wires

## GPIO Pin Configuration

Default GPIO pins (configurable in code):
- Blue wire: GPIO 26
- Pink wire: GPIO 13
- Yellow wire: GPIO 6
- Orange wire: GPIO 5

## Installation

1. Flash Windows 10 IoT Core on your Raspberry Pi
2. Connect stepper motor to ULN2003 driver board
3. Wire ULN2003 to Raspberry Pi GPIO pins as configured
4. Connect camera to USB port
5. Deploy the UWP application to your Raspberry Pi using Visual Studio
6. Enable camera permissions in device settings

## Usage

1. Launch the application on Raspberry Pi
2. Camera feed starts automatically with face detection
3. System detects faces and draws yellow bounding boxes
4. Stepper motor rotates camera to center detected face
5. Tracking continues as face moves within frame

## Drive Modes

- **Wave Drive**: Lower torque, smoother rotation (0.176° per step)
- **Full Step**: Standard mode, balanced torque and smoothness (0.176° per step)
- **Half Step**: Higher precision, doubled resolution (0.088° per step)

## License

MIT License

## Links

- Blog post: [Face-Tracking Camera with Stepper Motor Control](https://www.tanchunsiong.com/2016/04/face-tracking-camera-with-stepper-motor-control/)
- GitHub: [github.com/tanchunsiong](https://github.com/tanchunsiong)
- LinkedIn: [linkedin.com/in/tanchunsiong](https://linkedin.com/in/tanchunsiong)
- X: [x.com/tanchunsiong](https://x.com/tanchunsiong)

**Project Created:** April 2016
