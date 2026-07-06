# OpenMV Example Scripts Reference

All examples at `examples/`. MicroPython `.py` files organized by category.

## Example Categories

| Directory | Content |
|-----------|---------|
| `00-HelloWorld` | LED blink, hello world |
| `01-Camera/00-Snapshot` | Basic camera capture |
| `01-Camera/01-Video-Recording` | Video recording |
| `01-Camera/02-Optical-Flow` | Optical flow |
| `01-Camera/03-Event-Cameras` | Event camera usage |
| `01-Camera/04-Global-Shutter` | Global shutter cameras |
| `01-Camera/05-Thermal-Cameras` | Thermal/FIR cameras |
| `01-Camera/06-Time-of-Flight` | ToF sensors |
| `01-Camera/07-Sensor-Control` | Sensor settings (exposure, gain, white balance) |
| `01-Camera/08-Readout-Control` | Sensor readout control |
| `02-Image-Processing/00-Drawing` | Drawing shapes, text on images |
| `02-Image-Processing/01-Image-Filters` | Edge detection, filters, histograms |
| `02-Image-Processing/02-Color-Tracking` | Color blob tracking (find_blobs) |
| `02-Image-Processing/03-Frame-Differencing` | Motion detection |
| `03-Machine-Learning/00-TensorFlow` | ML model inference (classification, YOLO v2/v5/v8, BlazeFace, face/hand landmarks, MoveNet pose, micro speech) |
| `03-Machine-Learning/01-ST-CubeAI` | ST CubeAI inference |
| `03-Machine-Learning/02-Haar-Cascade` | Face detection (Haar Cascade) |
| `04-Barcodes` | QR code, barcode, DataMatrix scanning |
| `05-Feature-Detection` | Edges, circles, lines, rectangles, template matching, keypoints |
| `06-April-Tags` | AprilTag detection and 3D positioning |
| `07-Interface-Library/00-Arduino` | Arduino communication |
| `07-Interface-Library/01-Pixy-Emulation` | Pixy camera emulation |
| `07-Interface-Library/02-MAVLink` | MAVLink protocol (drones) |
| `07-Interface-Library/03-Modbus` | Modbus protocol (industrial) |
| `08-RPC-Library/34-Remote-Control` | Remote procedure calls |
| `08-RPC-Library/36-Web-Servers` | HTTP web servers |
| `09-WiFi` | WiFi networking (scan, HTTP, MQTT, NTP, MJPEG streaming) |
| `09-WiFi/WINC1500` | WINC1500 firmware update/version tools |
| `10-Bluetooth` | BLE examples |
| `11-Open-AMP` | Multi-core (dual core) examples |
| `12-Protocol` | OpenMV protocol library (custom data channels over USB/UART/network) |
| `50-Arduino-Boards/Giga-H7` | Arduino Giga H7 specific |
| `50-Arduino-Boards/Nano-33-BLE-Sense` | Arduino Nano 33 BLE Sense specific |
| `50-Arduino-Boards/Nano-RP2040` | Arduino Nano RP2040 specific |
| `50-Arduino-Boards/Nicla-Vision` | Arduino Nicla Vision specific |
| `50-Arduino-Boards/Portenta-H7` | Arduino Portenta H7 specific |
| `50-OpenMV-Boards/50-IMXRT-Boards` | OpenMV IMXRT boards |
| `50-OpenMV-Boards/50-STM32-Boards` | OpenMV STM32 boards |
| `50-OpenMV-Boards/51-Pure-Thermal` | Pure Thermal boards |
| `50-OpenMV-Boards/52-Alif-Boards` | Alif Ensemble boards |
| `50-OpenMV-Boards/53-N6-Boards` | STM32N6 boards |
| `50-OpenMV-Boards/60-Shields` | Shield accessories |

## Common Task Mapping

| Task | Best Example Directory |
|------|----------------------|
| Face detection | `03-Machine-Learning/02-Haar-Cascade` |
| Color tracking | `02-Image-Processing/02-Color-Tracking` |
| QR code scanning | `04-Barcodes` |
| Object detection (YOLO) | `03-Machine-Learning/00-TensorFlow` |
| Pose / face / hand landmarks | `03-Machine-Learning/00-TensorFlow` |
| Line following | `05-Feature-Detection` |
| AprilTag tracking | `06-April-Tags` |
| Motion detection | `02-Image-Processing/03-Frame-Differencing` |
| Arduino communication | `07-Interface-Library/00-Arduino` |
| Drone integration | `07-Interface-Library/02-MAVLink` |
| Web streaming | `08-RPC-Library/36-Web-Servers` |
| Bluetooth | `10-Bluetooth` |
| Custom host communication channels | `12-Protocol` |

## How to Search

```
Grep: pattern="<keyword>" path="examples/" (search file contents)
Glob: pattern="examples/**/*<keyword>*.py" (search filenames)
```
