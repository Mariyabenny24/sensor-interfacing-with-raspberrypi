# sensor-interfacing-with-raspberrypi

### Introduction
In this lab, students explore embedded sensor interfacing by working with the Raspberry Pi 5 and Sense HAT. The lab aims to demonstrate how to read data from sensors—including temperature, humidity, and pressure—and how to display messages on the
LED matrix. Through this exercise, students gain practical experience in Python-based
embedded programming, with a focus on applications in IoT and smart technologies.

### Methodology
The Raspberry Pi was set up in headless mode, enabling remote access via SSH. Following
the setup, the Sense HAT library was installed to facilitate sensor interaction. Two
separate Python scripts were created: the first script handled displaying custom messages
on the LED matrix, while the second script focused on retrieving and printing data from
onboard sensors, including temperature, humidity, and pressure readings.

### Software and Hardware Used
- Programming language: Using Python 3
- Libraries: primary libraries being sense-hat and time
- Hardware:Raspberry Pi 5 with a Sense HAT connected through the GPIO interface.

  ### Algorithm Setup
  #### Initial Configuration for Raspberry Pi 5 and Sense HAT
1.Download and flash Raspberry Pi OS onto the SD card using the Raspberry Pi
Imager.
2. In the Imager settings, enable SSH and configure the hostname, username, and
Wi-Fi credentials.
3. Insert the SD card into the Raspberry Pi and power it on.
4. Connect to the Raspberry Pi via terminal using SSH (e.g., ssh pi@192.168.0.10).
5. Update the system and install the Sense HAT library using terminal commands:

```sudo apt update```<br>
```sudo apt install sense - hat```

### Part 1: LED Matrix Message Display
1. Import the necessary libraries: sense_hat and time.
2. Create a SenseHat object to interface with the Sense HAT hardware.
3. Use the ```show_message()``` function to scroll text on the LED matrix.
4. Adjust the appearance of the message using optional parameters such as ```text_colour```
and ```scroll_speed```.

### Part 2: Environmental Sensor Data Reading
1. Import the necessary Python libraries: sense_hat and time.
2. Initialize the SenseHat object to access sensor data.
3. Start an infinite loop using while True.
4. Read sensor values using the following methods:<br>
- ```get_temperature()``` for ambient temperature.
- ```get_humidity()``` for relative humidity.
- ```get_pressure()``` for barometric pressure.
5. Format the sensor data using Python string formatting techniques.
6. Display the formatted data in the terminal using the ```print()``` function.
7. Add a delay between readings using ```time.sleep(2)``` to prevent output flooding.


### 3 Results
Real-time environmental data was measured printed in the terminal at 2-second intervals.
The LED matrix displayed the message as expected.

