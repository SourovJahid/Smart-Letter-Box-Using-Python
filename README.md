# Smart Letter Box

This project implements a Smart Letter Box using an M5Stack Core and several modules to detect and indicate the presence of letters or papers in the box. The project uses the M5Stack development kit, an ultrasonic sensor, RGB lights, and a speaker to provide feedback on the status of the letter box. Data is saved both locally and to the EZData cloud service.

## Table of Contents
- [Features](#features)
- [Hardware Requirements](#hardware-requirements)
- [Software Requirements](#software-requirements)
- [Installation](#installation)
- [Usage](#usage)
- [Code Description](#code-description)
- [Contributing](#contributing)
- [License](#license)

## Features
- Detects the presence of papers using an ultrasonic sensor.
- Provides visual feedback using RGB LEDs.
- Emits sound notifications via the speaker.
- Saves the status locally and to the EZData cloud service.
- Displays status messages on the M5Stack LCD screen.

## Hardware Requirements
- M5Stack Core
- M5Stack RGB Unit (PORTC)
- M5Stack Ultrasonic Sensor Unit (SONIC_IO, PORTB)
- MicroSD card (for local data storage)

## Software Requirements
- M5Flow UI
- uiflow library
- ezdata library

## Installation
1. Clone this repository to your local machine:
   ```sh
   git clone https://github.com/yourusername/smart-letter-box.git
Open the project in the M5Flow UI.

Ensure you have the required libraries installed:

uiflow
ezdata
Upload the code to your M5Stack device.

Usage
Set up your M5Stack Core with the RGB Unit and Ultrasonic Sensor Unit as per the port configurations mentioned.

Insert a MicroSD card into the M5Stack Core.

Power on the device and connect it to a Wi-Fi network.

The device will automatically start monitoring the letter box. When a paper is detected, the RGB LED will turn green, and a message will be displayed on the LCD screen indicating "Paper Pushed". If the box is empty, the RGB LED will turn red, and the message "Paper Popuped" will be displayed.

Data regarding the status of the letter box will be saved both locally on the MicroSD card and to the EZData cloud service.

Code Description
buttonA_wasPressed(): Handles the event when Button A is pressed, indicating that a paper has been pushed into the box.
buttonB_wasPressed(): Handles the event when Button B is pressed, indicating that a paper has been popped out of the box.
saveDataToEZData(): Saves the current status data to the EZData cloud service.
savedToSSD(): Saves the current status data to the MicroSD card.
Main loop: Continuously checks the distance using the ultrasonic sensor to determine the presence of papers in the box and updates the status accordingly.
Contributing
Contributions are welcome! Please open an issue or submit a pull request for any changes.

License
This project is licensed under the MIT License - see the LICENSE file for details.

css
Copy code


This README file provides a comprehensive guide for your project, including installation instructions, usage, and a brief description of the code. Be sure to replace `yourusername` with your actual GitHub username in the repository URL.
