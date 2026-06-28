# Arduino Core Hardware & Sensor Firmware Collection

This repository contains standalone Arduino C++ (`.ino`) scripts designed to manage basic electronics, read environmental sensors, control mechanical actuators, and execute automation logic.

### 🔗 Companion Hardware Repository
> 💡 **Looking for the circuit diagrams?** The virtual breadboards, component schematics, and simulation layouts for these exact code scripts are hosted in the companion repository:  
> 👉 **[Arduino-Proteus-Hardware-Simulations](https://github.com/arunk133/Arduino-Proteus-Hardware-Simulations)** 

---

## 📂 Project Explanations

* **Simple LED Blinking (`LED_BLINKING.ino`)** Acts as the basic operational heartbeat for the microcontroller. It continuously switches a single built-in light on and off at a steady pace, pausing for exactly one second during each transition. Matches the hardware setup in `single led.pdsprj`.
    
* **Staggered Three-LED Sequence (`THREE_LED_BLINKING.ino`)** Controls three independent lights in a rhythmic cascade similar to a simplified traffic signal. It turns the first light on for a second, shuts it off, waits three seconds, and then repeats the sequence for the next two lights. Matches the hardware setup in `7 led.pdsprj`.

* **Push Button Light Control (`PUSH_BUTTON_LED.ino`)** Creates an interactive digital switch. The microcontroller constantly monitors a physical push button; holding the button down powers on an indicator light, and releasing it shuts the light off. Matches the hardware setup in `switch.pdsprj`.

* **Servo Motor Sweeper (`SERVO_MOTOR.ino`)** Drives a mechanical arm capable of precise angular movements. Instead of spinning continuously, it smoothly rotates the motor arm back and forth in a full arc from 0° to 180° and back again to its starting position.

* **Automatic Soil Moisture Irrigation (`SOIL_MOISTURE.ino`)** Implements an automated watering loop by monitoring a soil sensor. When the sensor detects that the surrounding soil is adequately wet, the water pump motor remains off. The moment the soil dries out past a specific threshold, the pump immediately engages to begin watering. Matches the hardware setup in `NEW CIRCUIT FILE.pdsprj`.

* **Temperature & Humidity Serial Logger (`TEMP_HUMIDITY.ino`)** Transforms the hardware setup into a live digital weather station. It polls an environmental sensor for current air temperature and relative humidity metrics, then instantly streams those values to a connected computer screen for real-time tracking.

---

## 🛠️ Software & Library Requirements

1.  **Arduino IDE:** Required to verify, compile, and upload these code files to your target microcontroller hardware.
2.  **Peripherals Library:** To run the weather logging script, ensure the `DHT sensor library` by Adafruit is installed via the Arduino IDE Library Manager before compilation.
