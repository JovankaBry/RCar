# 🚗 Small RC-Car

A small, ESP32-based remote-controlled car project using brushless motors, designed for hobby and educational use. The car is controllable via Bluetooth or Wi-Fi, and supports brushless motor drive, steering, and optional real-time sensor feedback.

---

## 📦 Features
- Compact RC car platform using ESP32
- Brushless motor drive with ESC
- Steering via servo motor
- Control via:
  - PS5 Controller (Bluetooth)
  - Smartphone (Wi-Fi web interface)
- Optional sensor integration (IMU, ultrasonic, etc.)
- Open-source and customizable firmware

---

## 🔧 Components Used

| Component               | Quantity | Description                                 |
|------------------------|----------|---------------------------------------------|
| ESP32-C3 Supermini     | 1        | Main controller (Wi-Fi + Bluetooth capable) |
| Brushless Motor (e.g., 3650) | 1    | Drive motor for high torque/speed           |
| ESC (e.g., 30A car ESC) | 1        | Controls the brushless motor                |
| Servo Motor (e.g., SG90 / MG996R) | 1 | Steering system                             |
| LiPo Battery (2S/3S)   | 1        | Power source for motor + ESP32              |
| Motor Mount + Wheels   | 1 set    | For chassis assembly                        |
| PS5 Controller (Optional) | 1     | For Bluetooth control                       |
| Ultrasonic Sensor (Optional) | 1  | For distance measurement                    |
| MPU6050 (Optional)     | 1        | IMU for orientation feedback                |
| Buck Converter (5V)    | 1        | Step-down voltage to power ESP32            |
| Power Switch           | 1        | On/off toggle                               |
| Chassis + Wires + Screws | -      | General mechanical components               |

---

## 📷 Project Preview

![image](https://github.com/user-attachments/assets/0e7a89e8-c1dd-4ad8-8778-f63d90622e44)


---

## 🛠️ Setup & Installation

### 1. Flash ESP32
- Use Arduino IDE or PlatformIO
- Select correct board: `ESP32 Dev Module`
- Install required libraries:
  - `ESP32Servo`
  - `BluetoothSerial`
  - `WiFi`
  - (optional) `Adafruit_MPU6050`, `NewPing`, etc.

### 2. Wiring Overview
- ESC signal → ESP32 PWM pin (e.g., GPIO18)
- Servo PWM → ESP32 (e.g., GPIO19)
- Sensors → I2C or Digital pins (if used)
- Power:
  - ESC powered by battery
  - ESP32 powered via buck converter (5V)

### 3. Control Methods
- **Bluetooth**: Connect PS5 controller and map analog triggers to throttle/steering
- **Wi-Fi**: Host a web UI with ON/OFF buttons or sliders

---

## 📁 File Structure

```plaintext
RCar/
├── src/
│   └── main.ino          # Main firmware code
├── README.md
└── images/               # Car photos or wiring diagrams

---

Let me know if you want:
- Wiring diagram (`Fritzing` or `KiCad` style)
- Example code for the Bluetooth control or motor control
- Web interface for controlling the car via ESP32

Happy building!
