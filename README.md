# 🤖 Automated Production Line Scale

## 📜 About the Project

This project is an automation system developed with **Arduino** to ensure weight accuracy for products on a production line. The **automated scale** monitors the weight in real-time, and once a predefined value is reached, it activates a timer. After the countdown, a motorized hatch releases the product for the next cycle, guaranteeing uniformity and quality.

It's a simple and effective solution to prevent dosage irregularities, ideal for prototyping and small-scale use.

## ✨ Features

* **High-Precision Weighing:** Uses a Load Cell and the HX711 module for accurate measurements.
* **Integrated Timer:** Automatically activated when the target weight is achieved.
* **Hatch Control:** A servo motor opens and closes the hatch, automating the discharge process.
* **Visual Feedback:** An LCD display shows the current weight and system status in real-time.

## ⚙️ Required Components

To build this project, you'll need the following hardware:

* **Arduino Uno**
* **Load Cell** (with a capacity suitable for your product)
* **HX711 Amplifier Module**
* **Servo Motor**
* **16x2 I2C LCD Display**
* **Breadboard and Jumper Wires**
* **5V Power Supply**

## 🔌 Assembly and Connections

Follow this basic wiring diagram. For a more detailed guide, refer to the `diagram.png` (or similar) file in the repository.

1.  **Load Cell -> HX711:**
    * Red (VCC) -> E+
    * Black (GND) -> E-
    * White (Signal) -> A-
    * Green (Signal) -> A+

2.  **HX711 -> Arduino:**
    * VCC -> 5V
    * GND -> GND
    * DT -> Digital Pin 4
    * SCK -> Digital Pin 5

3.  **Servo Motor -> Arduino:**
    * VCC -> 5V
    * GND -> GND
    * Signal -> Digital Pin 9

4.  **I2C LCD Display -> Arduino:**
    * VCC -> 5V
    * GND -> GND
    * SDA -> Analog Pin A4
    * SCL -> Analog Pin A5

## 💻 Installation and Code

1.  **Download the Code:** Clone this repository or download the `.ino` file.
2.  **Install the Libraries:**
    * Open the Arduino IDE, go to **Sketch > Include Library > Manage Libraries...**.
    * Search for and install: `HX711`, `Servo`, and `LiquidCrystal_I2C`.
3.  **Calibrate the Scale:**
    * Calibration is crucial for accuracy. Follow the instructions in the code to find your calibration factor, which varies depending on the load cell.
    * Initially, set `scale.set_scale(1.f);` and use a known reference weight to calculate the correct value.
4.  **Upload:** Connect the Arduino and upload the code.

---

## 🚀 How It Works

Upon startup, the system initializes and tares the scale. The LCD display shows the real-time weight. When the target weight is reached, the timer starts counting down (indicated on the display). Once complete, the servo opens the hatch to release the product, waits a few seconds, and then closes to begin a new cycle.

## 🤝 Contributions

This is my first technology project, so any suggestions and improvements are welcome! Feel free to open an issue or a pull request.
