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
