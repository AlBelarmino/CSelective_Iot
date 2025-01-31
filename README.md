# Arduino & FastAPI Projects 🚀

Welcome to my collection of Arduino projects! This repository contains various activities that explore LED control, sensor integration, and web-based interaction using Python and Arduino.

Each project is organized into its own folder, with a dedicated `README.md` inside for detailed explanations, code, and setup instructions.

## 📂 **Project List**  

### 🔹 **[Led sequence](./Led sequence/)**
**Description:** A simple LED running light effect using five LEDs connected to Arduino digital pins. The LEDs turn on and off sequentially with a 1-second delay.

### 🔹 **[act-2-led-fade](./act-2-led-fade/)**
**Description:** A smooth LED brightness transition using PWM (Pulse Width Modulation). LEDs gradually increase in brightness before turning off, creating a fading effect.

### 🔹 **[act-3-fire-detection](./act-3-fire-detection/)**
**Description:** A basic fire detection system using a temperature sensor (NTC thermistor) and a photoresistor. If both temperature and brightness exceed set thresholds, an LED alert is triggered.

### 🔹 **[act-4-light-sensor-alert](./act-4-light-sensor-alert/)**
**Description:** An ambient light monitoring system using a photoresistor. When brightness surpasses a set limit, an LED alert is activated. The system also allows stopping the blinking effect via serial commands.

### 🔹 **[act-5-led-web-control](./act-5-led-web-control/)**
**Description:** Control an Arduino-connected LED via a FastAPI-based web API. A Python script communicates with the Arduino over serial to toggle the LED using HTTP requests.

### 🔹 **[act-6-button-to-api](./act-6-button-to-api/)**
**Description:** Reads a button press on an Arduino and sends its status (`1` for pressed, `0` for not pressed) to a FastAPI server, which then triggers an API call to control an LED.

---
