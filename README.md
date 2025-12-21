# ESP32-CAM License Plate Recognition (LPR) System

An embedded computer-vision system using the ESP32-CAM to capture vehicle images and perform license plate recognition. The system integrates a push-button trigger, OLED display feedback, and cloud-based image processing to extract and display license plate text.

---

## Demo
▶️ **Full system demonstration:** ESP32-CAM License Plate Recognition (LPR) System: https://youtu.be/9p-DTRr-KFo?si=irp0Q5tMMEhJN-Yl   

The video shows the system in its baseline idle state, followed by a user-triggered image capture via a push-button input. The ESP32-CAM captures an image and transmits it for remote processing. After that, a processed JPEG image is returned with the recognized license plate text overlaid on the original image and the identified text is displayed on the OLED screen.

---

## Inputs, System Components and Outputs

### Inputs
- Push-button trigger (GPIO13)
- Power input (5 V via FTDI USB-to-UART adapter)

### System Components
- ESP32-CAM onboard camera module used to capture images upon button press

### Outputs
- OLED display (SSD1306, I²C) showing system status and recognized license plate text
- Processed JPEG image returned from remote processing with detected license plate text overlaid
- Serial monitor output used for debugging, calibration, and system verification

---

## Design Notes
- The ESP32-CAM handles image capture and data transmission, while license plate recognition is performed remotely.
- GPIO14 and GPIO15 are used as custom I²C pins for the OLED display.
- A physical push-button provides controlled image capture instead of continuous streaming.
- System behavior was verified using serial output, OLED feedback, and returned image results.

---

## Images & Documentation

This repository includes schematic documentation, physical wiring verification, and development artifacts demonstrating correct system design and functionality.

### Circuit Design & Hardware
- **LPR_Schematic (Fritzing).pdf**  
  Breadboard schematic created using Fritzing, showing electrical connections between the ESP32-CAM, FTDI adapter, OLED display, and trigger button.

- **LPR_Development_progression.png**  
  Image documenting staged hardware development and wiring verification.

- **LPR_Demo.png**  
  Representative system demonstration image.

---

## Code
- **LPR_code**  
  Firmware implementing image capture, button handling, OLED communication, serial debugging, and data transmission for license plate recognition processing.

---

## External Reference Acknowledgment
This project was developed independently with limited reference to CircuitDigest resources for initial ESP32-CAM setup guidance and code structure. The final system design, hardware integration, control logic, and documentation were independently implemented.

CircuitDigest resources enabled cloud-based image processing, allowing captured images to be processed remotely and returned as JPEG files containing AI-generated license plate recognition results overlaid on the original image.

---

## Power Source
- Primary Power Source: 5 V via FTDI USB-to-UART adapter
- ESP32-CAM onboard regulation supplies required 3.3 V logic levels
