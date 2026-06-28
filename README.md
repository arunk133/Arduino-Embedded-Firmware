# Arduino Core Hardware & Sensor Firmware Collection

This repository contains standalone Arduino C++ (`.ino`) scripts designed to manage basic electronics, read environmental sensors, control mechanical actuators, and execute automation logic. 

---

## 📂 Project Explanations

* **Simple LED Blinking (`LED_BLINKING.ino`)**
    Acts as the basic operational heartbeat for the microcontroller. It continuously switches a single built-in light on and off at a steady pace, pausing for exactly one second during each transition.
    
* **Staggered Three-LED Sequence (`THREE_LED_BLINKING.ino`)**
    Controls three independent lights in a rhythmic cascade similar to a simplified traffic signal. It turns the first light on for a second, shuts it off, waits three seconds, and then seamlessly repeats the exact same sequence for the next two lights before looping back to the start.

* **Push Button Light Control (`PUSH_BUTTON_LED.ino`)**
    Creates an interactive digital switch. The microcontroller constantly monitors a physical push button; holding the button down immediately powers on an indicator light, and releasing it instantly shuts the light off.

* **Servo Motor Sweeper (`SERVO_MOTOR.ino`)**
    Drives a mechanical arm capable of precise angular movements. Instead of spinning continuously, it smoothly rotates the motor arm back and forth in a full arc from 0° to 180° and back again to its starting position.

* **Automatic Soil Moisture Irrigation (`SOIL_MOISTURE.ino`)**
    Implements an automated watering loop by monitoring a soil sensor. When the sensor detects that the surrounding soil is adequately wet, the water pump motor remains off. The moment the soil dries out past a specific threshold, the pump immediately engages to begin watering.

* **Temperature & Humidity Serial Logger (`TEMP_HUMIDITY.ino`)**
    Transforms the hardware setup into a live digital weather station. It polls an environmental sensor for current air temperature and relative humidity metrics, then instantly streams those values to a connected computer screen for real-time tracking.

---

## 🛠️ Software & Library Requirements

1. **Arduino IDE:** Required to upload these code files to your target microcontroller hardware.
2. **Peripherals Library:** To run the weather logging script, ensure the `DHT sensor library` by Adafruit is installed via the Arduino IDE Library Manager before compilation.
