# OpenMV API Documentation Reference

RST format docs at `html/_sources/library/`. Cleaner than HTML, preferred for searching.

## Key API Docs

### Vision & Image Processing
- **`omv.image.rst.txt`** — The most important doc. Image class with all processing methods: `find_blobs`, `find_edges`, `find_circles`, `find_lines`, `find_rects`, `find_qrcodes`, `find_barcodes`, `find_apriltags`, `find_features`, `draw_rectangle`, `draw_string`, etc.
- **`omv.sensor.rst.txt`** — Camera sensor control: `sensor.reset()`, `sensor.set_pixformat()`, `sensor.set_framesize()`, `sensor.snapshot()`, etc.
- **`omv.csi.rst.txt`** — New CSI camera module (replacing sensor module)

### Machine Learning
- **`omv.ml.rst.txt`** — Machine learning: `ml.Model()`, TensorFlow Lite inference
- **`omv.ml.preprocessing.rst.txt`** — ML input preprocessing
- **`omv.ml.postprocessing.ultralytics.rst.txt`** — YOLO (Ultralytics) postprocessing
- **`omv.ml.postprocessing.darknet.rst.txt`** — YOLO (Darknet) postprocessing
- **`omv.ml.postprocessing.mediapipe.rst.txt`** — MediaPipe postprocessing
- **`omv.ml.postprocessing.edgeimpulse.rst.txt`** — EdgeImpulse postprocessing
- **`omv.ml.apps.rst.txt`** — High-level ML applications
- **`omv.ml.utils.rst.txt`** — ML utilities

### Display & Output
- **`omv.display.rst.txt`** — Display output (LCD, SPI display, DSI display)
- **`omv.display.spidisplay.rst.txt`** — SPI display
- **`omv.display.rgbdisplay.rst.txt`** — RGB display
- **`omv.display.dsidisplay.rst.txt`** — DSI display
- **`omv.tv.rst.txt`** — TV output
- **`omv.gif.rst.txt`** — GIF recording
- **`omv.mjpeg.rst.txt`** — MJPEG recording

### Sensors
- **`omv.fir.rst.txt`** — Thermal/FIR sensor reading
- **`omv.tof.rst.txt`** — Time-of-Flight sensor
- **`omv.imu.rst.txt`** — IMU sensor
- **`omv.audio.rst.txt`** — Audio capture

### Communication & Networking
- **`omv.rpc.rst.txt`** — Remote procedure call library
- **`omv.rtsp.rst.txt`** — RTSP video streaming
- **`omv.gt911.rst.txt`** — GT911 touch controller
- **`omv.ft5x06.rst.txt`** — FT5x06 touch controller

### Hardware Peripherals (`machine.*`)
- **`machine.rst.txt`** — Machine module overview
- **`machine.Pin.rst.txt`** — GPIO pins
- **`machine.I2C.rst.txt`** — I2C bus
- **`machine.SPI.rst.txt`** — SPI bus
- **`machine.UART.rst.txt`** — UART serial
- **`machine.PWM.rst.txt`** — PWM output
- **`machine.ADC.rst.txt`** — Analog-to-digital converter
- **`machine.LED.rst.txt`** — LED control
- **`machine.CAN.rst.txt`** — CAN bus
- **`machine.I2S.rst.txt`** — I2S audio
- **`machine.RTC.rst.txt`** — Real-time clock

### Standard MicroPython Modules
- `asyncio.rst.txt`, `bluetooth.rst.txt`, `json.rst.txt`, `socket.rst.txt`, `os.rst.txt`, `time.rst.txt`, `struct.rst.txt`, `io.rst.txt`, etc.

### Tutorials
- `html/_sources/openmvcam/` — RST format tutorials and quickstart guides

## How to Search

```
Grep: pattern="<function_name>" path="html/_sources/library/" (find relevant API docs)
```
