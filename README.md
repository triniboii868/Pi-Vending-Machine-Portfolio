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

## What is a Vending Machine?

A vending machine is an automated device that dispenses items such as snacks, drinks, or other goods when a user inserts money or uses a digital payment method. It consists of mechanical and electronic components to process payments, select products, and deliver them to the user. This is the what we have tried implementing with the use of the Raspberry Pi with the addition of Python code and Vend Breadboard setup from previous assignments to carry out the transaction. 

### Image Of Vending Machine

![vending machine](https://github.com/user-attachments/assets/34873970-7416-4039-9f37-59729eb4b005)


# Setting up the Raspberry Pi Vend Machine

Throughout this part of the project, we have taken a couple of steps to complete this raspberry Pi vending machine setup and have it fully functional. First, we prepared the breadboard with the initial setup connecting the board to the GPIO pins in the Raspberry Pi device to receive inputs by using its GPIO (General Purpose Input/Output) pins connected by F-M Wires as seen below. 

![initial setup](https://github.com/user-attachments/assets/9f9924cf-387f-4195-a1b7-0a9946dd062b)

## Javascript Code which accepts input from Breadboard and Outputs into Console.

Secondly, A program called Real VNC Viewer was installed where we can connect to the host and have a GUI to operate the Raspberry Pi device. The neat thing about this device is that it has the same functions a computer has as well as applications which we can use to write code. In this instance, we used Thonny to write code in Javascript to allow the functionality of the device correctly, to receive outputs/inputs and have it displayed in a program. 

![first part of code](https://github.com/user-attachments/assets/964aaff5-05d5-41a7-b4fa-be028824dee8)

## Javascript code and Breadboard showing the outputs on Console for each scenario.

### Case 1: Coin is inserted (Pressed)

![coin pressed UPDATED](https://github.com/user-attachments/assets/26584f15-6c74-438d-8018-d3b2a7e678f6)

### Case 2: Vend is Initiated (Pressed)

![vend pressed UPDATED](https://github.com/user-attachments/assets/51622508-cd70-40f7-916e-748a95ff39a2)

## HTML Server setup to Display output from a remote location. 

![html part](https://github.com/user-attachments/assets/6df01a99-e543-4160-8318-da33d87fbcc7)

## Webpage with Vending Info

![Screenshot 2025-03-27 101800](https://github.com/user-attachments/assets/7b693389-811e-4881-9fbb-9ff0e3f123e1)


# Special mention to the Contributor for the completion of this Portfolio

### Tomas Nadale who soughted the completion of the Github page. 


### Ronald Kiprono who contributed to the javascript code. 

![IMG_3405](https://github.com/user-attachments/assets/f7f9ba21-3287-4dcd-adfa-7dfa02fb8062)

### Noah Newton who aided in the physical setup of the vending machine. 

![IMG_3371](https://github.com/user-attachments/assets/a1eb2964-8069-4300-a01c-8741e648865f)


## Works Cited

Ltd, R. P. (n.d.). Raspberry Pi for home – Raspberry Pi. Raspberry Pi. https://www.raspberrypi.com/for-home/ 

GeeksforGeeks. (2023, November 2). Architecture of Raspberry Pi. GeeksforGeeks. https://www.geeksforgeeks.org/architecture-of-raspberry-pi/

Timmons-Brown, D. (2019). Learn robotics with Raspberry Pi: Build and code your own moving, sensing, thinking robots. No Starch Press. 
