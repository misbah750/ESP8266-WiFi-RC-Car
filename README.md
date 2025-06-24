
#  ESP8266 WiFi RC Car

A DIY Wi-Fi controlled RC car built using the *ESP8266 NodeMCU, **L298N motor driver, and powered by **4x 4V batteries*. This project is a personal tribute to my childhood love for racing cars and combines my passion for electronics, embedded systems, and robotics.

---

##  Inspiration

Since childhood, I’ve always been fascinated by cars — especially fast, racing ones. That curiosity eventually transformed into a desire to build something of my own. This project is a realization of that dream — a simple yet powerful Wi-Fi-enabled RC car that I can proudly say I built myself.

---

## ⚙ Components Used

| Component         | Description                             |
|------------------|-----------------------------------------|
| ESP8266 NodeMCU   | Wi-Fi-enabled microcontroller           |
| L298N Motor Driver| Dual H-Bridge motor driver              |
| DC Gear Motors    | 4 motors (2 pairs for front and back)   |
| Battery Holder    | Holds 4x 4V batteries                   |
| 4x 4V Batteries   | Power source                            |
| Wi-Fi Control App | Android app to control via Wi-Fi        |
| Wires + Chassis   | Custom wiring and acrylic car body      |



##  Control System

- Controlled using a *Wi-Fi control app* (connected via ESP8266 in station mode).
- Commands are sent over a local Wi-Fi network.
- The ESP8266 interprets commands and sends signals to the L298N motor driver.
- Supports forward, reverse, left, right, and stop functions.


### Quick Pin Reference:
| ESP8266 Pin | L298N Input |
|-------------|-------------|
| D1 (GPIO5)  | IN1         |
| D2 (GPIO4)  | IN2         |
| D3 (GPIO0)  | IN3         |
| D4 (GPIO2)  | IN4         |
| GND         | GND         |
| VIN         | VCC (L298N) |



##  How It Works

1. ESP8266 connects to the same Wi-Fi network as your phone.
2. A mobile app sends directional commands over HTTP or UDP.
3. The ESP8266 decodes those commands and drives the motors through the L298N.
4. You control the car wirelessly with real-time response!



##  Challenges Faced

- *ESP8266 Connectivity Issues:*  
  It took some trial and error to get the Wi-Fi setup working reliably. I had to experiment with different apps and modes before finding a good fit.

- *Power Management:*  
  Ensuring stable voltage to both motors and ESP8266 was tricky, especially under load. A separate battery line and voltage regulation were key.

### Getting Started

###  Prerequisites

- Arduino IDE
- ESP8266 board package
- USB cable for flashing
- Wi-Fi control app (like “ESP8266 RC Car” or custom HTTP app)

### 📥 Upload the Code

1. Open Arduino IDE.
2. Select NodeMCU 1.0 (ESP-12E Module) as the board.
3. Install required libraries (e.g. ESP8266WiFi.h).
4. Upload the code (included in this repo under /src).
5. Connect to the same Wi-Fi network from your phone.

---

## 📦 Folder Structure
