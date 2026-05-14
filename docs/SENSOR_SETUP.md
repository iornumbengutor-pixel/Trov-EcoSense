# Sensor Setup Guide for Trov EcoSense

This guide will help you set up the IoT sensors for Trov EcoSense. Ensure you have all the required components before beginning.

---

### **Required Components**

#### Environmental Gas Monitoring:
- MQ-series sensors (MQ-2, MQ-135, etc.)
- ESP32/NodeMCU or Raspberry Pi
- Resistors and connecting wires
- Breadboard

#### Waste Level Monitoring:
- Ultrasonic Sensor (HC-SR04)
- Microcontroller (e.g., Arduino, ESP32, Raspberry Pi)
- Power supply (battery or USB-powered)

#### Other Tools:
- Soldering kit (optional)
- Multimeter (for testing connections)

---

### **Connections**

#### MQ-Series Sensors:
1. Connect the analog output pin of the MQ sensor to an ADC pin on the ESP32 or Raspberry Pi.
2. Connect VCC and GND to the power supply.
3. Adjust the potentiometer if needed for sensitivity calibration.

#### Ultrasonic Sensor:
1. Connect VCC to a 5V pin.
2. Connect GND to the ground pin.
3. Connect the TRIG pin to a GPIO pin on the microcontroller.
4. Connect the ECHO pin to another GPIO pin (or directly to the ADC if available).

---

### **Configuration**

1. Install Drivers (if using ESP32):
   - Install the CP210x or CH340 drivers for USB communication.

2. Flash the Firmware:
   - Open Arduino IDE or ESP-IDF.
   - Use the provided firmware code to upload the script to your microcontroller.

3. Connect to Wi-Fi:
   - Update the SSID and password in the firmware script.

4. Test Sensors:
   - Run the test script provided in the `/tests` folder to ensure connectivity and accurate readings.

---

### **Troubleshooting**

- **No Data from Sensors**:
  - Check the wiring connections.
  - Ensure the microcontroller is powered.
  - Use a multimeter to measure voltage levels.

- **Wi-Fi Connectivity Issues**:
  - Verify the SSID and password.
  - Reduce the distance between the router and the microcontroller.

---

### **Next Steps**
- Move to the backend setup guide to integrate your hardware data with the cloud.

For further support, feel free to reach out.