# DIY Arduino Radar System

In this tutorial, we'll be building a radar that scans its surroundings and displays detected objects on your computer screen.

To start, get these parts:
* **Arduino Uno**
* **Ultrasonic Sensor (HC-SR04)**
* **Servo Motor**
* **Breadboard & Jumper Wires**
* **Computer** (with Arduino IDE and Processing installed)

---

## Step 1: Wire the Hardware
Connect your components to the Arduino exactly as follows:

### Servo Motor
* **Red Wire:** 5V
* **Brown/Black Wire:** GND
* **Yellow/Orange Wire:** Pin 12

### Ultrasonic Sensor
* **VCC:** 5V
* **GND:** GND
* **Trig:** Pin 10
* **Echo:** Pin 11

*Note: Mount the sensor on top of the servo motor using tape or a bracket so it can rotate.*

---

## Step 2: Upload the Arduino Code
1. Open the **Arduino IDE**.
2. Copy the code from `arduino_code.txt` and paste it into a new sketch.
3. Plug in your Arduino via USB.
4. Select your board and port, then hit **Upload**.
5. The servo should start rotating back and forth automatically.

---

## Step 3: Run the Radar Display
1. Open the **Processing** software.
2. Copy the code from `processing_code.txt` into the window.
3. **Important:** Look for the line: `myPort = new Serial(this, "COM5", 9600);`.
4. Change `"COM5"` to match the port number your Arduino is actually using (check this in the Arduino IDE under Tools > Port).
5. Hit the **Run** (Play) button.

---

## Step 4: Use the Radar
Once the green screen pops up:
* **Green Sweep:** Represents the sensor's clear path.
* **Red Areas:** Show objects detected in real-time.
* **Status Bar:** The bottom of the screen shows the current angle and distance of the object in centimeters.

---

## Troubleshooting
* **Screen stays blank?** Make sure the Serial Monitor in the Arduino IDE is CLOSED before running Processing.
* **Motor not moving?** Double-check that the signal wire is in Pin 12.
* **No red dots?** Ensure the sensor pins (Trig/Echo) aren't swapped.
