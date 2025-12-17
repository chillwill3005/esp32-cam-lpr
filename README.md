# ESP32-CAM Automatic Number Plate Recognition (ANPR)

An ESP32-CAM–based automatic number plate recognition (ANPR) system using Wi-Fi connectivity for smart parking and vehicle access control.

## Overview
This project demonstrates a low-cost, embedded vehicle detection system built using an ESP32-CAM module.  
The system captures vehicle images, transmits them over Wi-Fi, and performs license plate recognition to support automated parking and access-control applications.

The implementation is based on a reference design and workflow from CircuitDigest, adapted and documented for educational and prototyping purposes.

## Demo
> (Optional – add later)
- Live camera capture and plate recognition workflow
- JPEG image output via ESP32-CAM
- OLED display feedback (if enabled)

## System Features
- ESP32-CAM image acquisition
- Wi-Fi-based image transmission
- Automated license plate recognition workflow
- Low-cost embedded hardware solution
- Portable and scalable system design

## Hardware Components
- ESP32-CAM module
- FTDI programmer (for flashing)
- External power supply (5V)
- Optional OLED display
- Jumper wires and breadboard (for setup)

## Software & Tools
- Arduino IDE
- ESP32 board support package
- C/C++ (Arduino framework)
- Wi-Fi communication libraries

## Design Notes
- The project follows a reference ANPR workflow provided by CircuitDigest.
- Image processing and recognition are handled externally after image transmission.
- Emphasis was placed on system integration, reliability, and response time rather than custom ML model development.

## References
- CircuitDigest ANPR Project:  
  https://circuitdigest.com/projects/license-plate-recognition-using-esp32-cam
