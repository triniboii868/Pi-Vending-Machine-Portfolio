# Pi-Vending-Machine-Portfolio

## What is a Raspberry Pi device?
A Raspberry Pi device is a small, powerful, and inexpensive single-baord computer (SBC). It enables wireless internet & bluetooth connectivity, HDMI/USB/Audio ports, and other devices found on a typical computer. It is commonly used to teach programming and building hardware projects to home automation, robotics, and can also act as a streamer or web server. 

## Labelled Diagram of Raspberry Pi Board.

![RASPBERRY PI BOARD LABELLED](https://github.com/user-attachments/assets/19ebbb48-85b1-46ed-a9ef-0a747b50d28f)

### Component List and their functions:

**CPU** - ARM processor with integrated graphics. It is the heart of the device which controls the I/O devices and computations. 

**HDMI Ports** - High Definition Multimedia Interface used for transmitting video and digital audtio data from a computer to monitor or digital TV. 

**GPIO Ports** - General Purpose Input Output Ports which allows the user to interface various I/P devices. 

**Stereo Audio** - Audio connector used for connecting audio output devices such as speakers and headphones.

**USB Ports** - A common port available for various peripheral devices, such as a mouse, keyboard, HDD etc. This model has both 2.0 and 3.0 USB ports.  

**Micro SD Card Slot** - SD card slot which is required for booting the device with an installed and functional operating system. 

**Ethernet Port** - This connector allows the user access to a wirred network, however only available on the model B of Raspberry Pi.

**CSI Camera Port** - Camera Serial Interface connects the Broadcom processor to the Pi camera. 

**15-Pin Ribbon Connector** - Display Serial Interface (DSI) is used for connecting LCD to Raspberry Pi using 15 15-pin ribbon cables. DSI provides a high-resolution display interface that is specifically used for sending video data.

**PoE HAT Header** - The PoE HAT allows you to power your Raspberry Pi using Power over Ethernet–enabled networks. 

**USB-C Power Port** - This USB-C port serves primarily as the power input, allowing the device to be powered via a USB-C power adapter.


## Additional Apparatus

![Screenshot 2025-03-19 013251](https://github.com/user-attachments/assets/0f2589fd-9996-4263-b52e-972114c1d1ab)

### Component List and their functions:

**Ultrasonic Sensor**: This sensor measures the distance between itself and an object using ultrasonic waves. It's commonly used in obstacle detection for robots or distance measurement applications.

**5050 RGB LED Stick**: A small stick of individually addressable RGB LEDs. It allows you to control the color and brightness of each LED independently, useful for creating colorful light effects.

**Lego Wheel**: A basic wheel part compatible with Lego Technic sets. Often used to create robot bases or moving vehicles.

**Wii Remote**: A game controller from the Nintendo Wii console, often repurposed in DIY projects to provide motion input or button controls via Bluetooth.

**5MP Camera Module**: A small camera, likely compatible with Raspberry Pi, used to capture images or video, and can be implemented for computer vision projects.

**Infared Reflective Sensor**: This component measures temperature. It might output analog or digital signals to microcontrollers for applications like weather stations or environment monitoring.

**Vending Machine Breadboard**: A reusable board for prototyping electronic circuits without soldering. It allows you to connect various components and test circuit designs.

**Raspberry Pi Build HAT**: A small, affordable computer used for a variety of electronics projects. It serves as the control unit that can run programs, control sensors, and process data.

**Speaker**: A small audio output device used to produce sounds or play audio signals in projects.

**2 x 20 Pin Connector**: A connector likely used to interface other components or GPIO pins with the Raspberry Pi, making it easier to connect various peripherals.

**Lego Color Sensor**: A sensor that detects the color of an object, often used in robotics for tasks like line following or object sorting.


## Recall the Truth Table for the SR Latch Operation

![Screenshot 2025-02-27 170519](https://github.com/user-attachments/assets/2a66e5f6-53b8-48e2-965a-cc7c4722212d)


## Diagram Showing Vending Machine Circuit

![Screenshot 2025-02-27 165710](https://github.com/user-attachments/assets/44c1ac37-5cf1-4551-866c-4e9e99b33a91)

In this diagram, you can see where the previously built SR latch was modified, adding on a few new devices onto the breadboard. The only differences are
that the S button represents the COIN button and the out Q LED represents the COIN indicator LED. In addition, a capacitor is added to acquire the desired
delayed reset in the circuit along with two resistors to control the current flow the LEDs and capcitors. 

## Circuit Showing Both COIN and VEND Set to Off "0"

![off](https://github.com/user-attachments/assets/14dcaa3d-d644-4973-9b0d-cb9cfc56eda6)

The circuit shows two inputs: a COIN and a VEND buttoN. Pressing COIN represents inserting a coin & pressing vend represents the machine doing the vending
action of an item. In this case both of the buttons are set to OFF "0" therefore neither the COIN or VEND LEDs are lit up. 

## Circuit Showing COIN set to On "1" and VEND Set to Off "0"

![coin](https://github.com/user-attachments/assets/7c2b2605-c4ce-41c6-8ef7-cd737a3c097a)

In this scenario, the COIN button is pressed and the input crosses the gates which causes an output of "1" or ON state in the COIN LED, which is why it is
lit, however the VEND button isn't pressed, hence still in the OFF state "0".

## Circuit Showing COIN set to On "1" and VEND Set to On "1"

![vend](https://github.com/user-attachments/assets/04b37ea9-f49b-49d2-aeff-53176f36e124)

Finally, the VEND button is click after the coin is inserted (COIN button pressed) and the both LEDS are lit up for a short period. This portrays that an
item is being vended. The delayed reset is important for the action to be completed. After the action is completed, the circuit repeats itself by returning
to the "no coin" state which causes both the COIN and VEND LEDs to come off after the delayed reset.

## Setting up the Raspberry Pi Vend Machine




## Works Cited

Ltd, R. P. (n.d.). Raspberry Pi for home – Raspberry Pi. Raspberry Pi. https://www.raspberrypi.com/for-home/ 

GeeksforGeeks. (2023, November 2). Architecture of Raspberry Pi. GeeksforGeeks. https://www.geeksforgeeks.org/architecture-of-raspberry-pi/

Timmons-Brown, D. (2019). Learn robotics with Raspberry Pi: Build and code your own moving, sensing, thinking robots. No Starch Press. 
