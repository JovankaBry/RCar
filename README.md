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
| Motor Driver (DRV8833)  | 1        | Controls the brushless motor                |
| Servo Motor (SG90 ) | 1 | Steering system                             |
| LiPo Battery (2S/3S)   | 1        | Power source for motor + ESP32              |
| Step Up Volate  MT3608 SOT23-6| 1        | Boost 3,7V to 15V         |
| Motor Mount + Wheels   | 1 set    | For chassis assembly                        |
| PS5 Controller | 1     | For Bluetooth control                       |
| Ultrasonic Sensor (Optional) | 1  | For distance measurement                    |
| MPU6050 (Optional)     | 1        | IMU for orientation feedback                |
| Power Switch           | 1        | On/off toggle                               |
| Chassis + Wires + Screws | -      | General mechanical components               |

---

## 📷 Project Preview
1.ESP32-C3 Supermini

![image](https://github.com/user-attachments/assets/0e7a89e8-c1dd-4ad8-8778-f63d90622e44)

2.Brushless Motor

![image](https://github.com/user-attachments/assets/6b6495b1-1b1f-4654-8bce-e9b251031d1c)

3.Motor Driver (DRV8833) 

![image](https://github.com/user-attachments/assets/12fbf853-9f7b-4820-9b21-c58f826696f6)
https://de.aliexpress.com/item/32857376192.html?spm=a2g0o.cart.0.0.5cad4ae47fSjmx&mp=1&pdp_npi=5%40dis%21EUR%21EUR%202.50%21EUR%202.05%21%21EUR%202.05%21%21%21%40211b80e117482671612856494e812f%2165342873775%21ct%21DE%211737591246%21%211%210&gatewayAdapt=glo2deu

![image](https://github.com/user-attachments/assets/4f4d44cc-d612-4f95-b58c-2d848c51ea31)

4.Servo Motor(SG90)

![image](https://github.com/user-attachments/assets/b3b8fc74-a058-4250-8e32-cd7d91c5e63d)

5.LipoBattery 3,7 3000mAH

![image](https://github.com/user-attachments/assets/055ecd44-349f-4089-8217-eb8469a8ca31)

6.Booster(MT3608 SOT23-6)

![image](https://github.com/user-attachments/assets/b6ee8eec-df11-4d4b-91dd-3f0ed1c8dfd3)

7.optional











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
