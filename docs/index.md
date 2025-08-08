# 🤖 UKMARSBOT Pages Demo

Welcome to the official guide for **[UKMARSBOT]**! This page walks you through everything you need to assemble, wire, and test your robot.

Hey Ho!

---

## 🧩 Bill of Materials

A complete list of components is available in the [BOM](./bom/bom.csv).  
You can source parts from your preferred vendors or use the links provided in the spreadsheet.

---

## 🛠️ Mechanical Assembly

Download the [3D CAD file](./mechanical/assembly.step) to view the full assembly.  
Refer to the [exploded view image](./images/exploded_view.png) for part placement.

### Tools Required
- Allen keys
- Screwdriver set
- 3D printer (optional)

---

## ⚡ Electronics & Wiring

All schematics are available in the [ECAD folder](./schematics/Arduino_Nano-Rev3.2-SCH.pdf).  
Follow the wiring diagram to connect motors, sensors, and the microcontroller.

### Microcontroller
- Arduino Nano / ESP32 / Raspberry Pi Pico

### Sensors
- IMU (MPU6050)
- Ultrasonic or IR distance sensors

---

## 🧠 Firmware & Software

Upload the firmware using the Arduino IDE or PlatformIO.  
Source code is located in the `firmware/` folder.

```bash
cd firmware
arduino-cli compile --fqbn arduino:avr:nano
arduino-cli upload -p /dev/ttyUSB0 --fqbn arduino:avr:nano
```

---

## 🧪 Testing & Calibration

Once assembled, run the diagnostics script to verify motor direction and sensor readings.  
Use the serial monitor to check output and calibrate the IMU.

---

## 📷 Media & Demos

![Robot in action](./images/demo_photo.jpg)

Watch a demo video [here](https://www.youtube.com/watch?v=your-demo-link).

---

## 📬 Feedback & Contributions

Found a bug or have a suggestion? Open an issue or submit a pull request.  
We welcome contributions from makers, educators, and robotics enthusiasts!

---

© [Your Name or Team] – Licensed under [MIT License](./LICENSE)
