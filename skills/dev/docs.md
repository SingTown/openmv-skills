# OpenMV API Documentation Reference

The complete OpenMV documentation (tutorials + API reference) is bundled as a single plain-text RST file: **`llms-full.txt`** (~4.5 MB, in this skill's directory).

Source: https://docs.openmv.io/v5.0.0/llms-full.txt — re-download to refresh when a new docs version is released.

## How to Search

```
Grep: pattern="<function_name>" path="llms-full.txt" -n   (find where an API is documented)
Read: offset=<line> limit=100                              (read the surrounding documentation)
```

The file is organized into module sections marked with `.. module:: <name>`. To jump to a module's API reference:

```
Grep: pattern="^\.\. module:: image" path="llms-full.txt" -n
```

## Key Modules

### Vision & Image Processing
- **`image`** — The most important module. Image class with all processing methods: `find_blobs`, `find_edges`, `find_circles`, `find_lines`, `find_rects`, `find_qrcodes`, `find_barcodes`, `find_apriltags`, `find_features`, `draw_rectangle`, `draw_string`, etc.
- **`csi`** — New CSI camera module: `csi.CSI()`, `.reset()`, `.pixformat()`, `.framesize()`, `.snapshot()`
- **`sensor`** — Legacy camera sensor control (deprecated, replaced by `csi`)

### Machine Learning
- **`ml`** — Machine learning: `ml.Model()`, TensorFlow Lite inference
- **`ml.preprocessing`** — ML input preprocessing
- **`ml.postprocessing.ultralytics`** — YOLO (Ultralytics) postprocessing
- **`ml.postprocessing.darknet`** — YOLO (Darknet) postprocessing
- **`ml.postprocessing.mediapipe`** — MediaPipe postprocessing
- **`ml.postprocessing.edgeimpulse`** — EdgeImpulse postprocessing
- **`ml.apps`** — High-level ML applications
- **`ml.utils`** — ML utilities

### Display & Output
- **`display`** — Display output (LCD, SPI, RGB, DSI displays)
- **`gif`** — GIF recording
- **`mjpeg`** — MJPEG recording

### Sensors
- **`fir`** — Thermal/FIR sensor reading
- **`tof`** — Time-of-Flight sensor
- **`imu`** — IMU sensor
- **`audio`** — Audio capture

### Math (NumPy-like)
- **`ulab`** / **`numpy`** — `from ulab import numpy as np`; arrays, linalg, fft, scipy subset

### Hardware Peripherals
- **`machine`** — `Pin`, `I2C`, `SPI`, `UART`, `PWM`, `ADC`, `LED`, `CAN`, `I2S`, `RTC`, etc.

### Standard MicroPython Modules
- `asyncio`, `bluetooth`, `json`, `socket`, `os`, `time`, `struct`, `io`, `network`, etc.

## Tutorials

Tutorial content (quickstart, Python basics, vision guides) is at the beginning of `llms-full.txt`, before the module reference sections. Search by topic keyword, e.g. `Grep: pattern="color tracking" -i`.
