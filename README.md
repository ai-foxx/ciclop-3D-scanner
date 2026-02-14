## ciclop-3D-scanner

A homebrew 3D scanner.

![ciclop](/images/ciclop.jpg)

## Background

The BQ Ciclop scanner is fully open source meaning that all of the source files for the hardware and software are made available online. That means you are free to make adjustments and upgrades to the Ciclop and then to share those changes with the community. This is the first open source scanner with open source software on the market.

How does Ciclop work? Ciclop is a 3D rotational laser triangulation scanner. That means that is makes use of two separate lasers and projects those lasers over the object you are scanning. Your object will rotate on the turntable and the lasers will catalogue both the geometry and texture of your object. Once you unbox the Ciclop, you can fully assemble the scanner in under an hour.

Start scanning large objects today and enjoy a scannable area of 250mm in diameter by 205mm tall. That means you can scan objects that are slightly smaller than a volleyball. The scanner captures textures and details with a precision of 500 microns. 

## Specifications

_3D scanning_

* Scanning precision: 0.5 mm
* Steps per rotation: 1600 max (1/8th microstepping)
* Maximum supported weight: 3 KG
* Typical scanning time (configurable): 2-8 minutes
* 3D scanning volume:
  - Diameter: 250 mm
  - Height: 205 mm

_Electronics_

* Control Board: ZUM BT-328
* Power board: ZUM SCAN
* Logitech C270 HD Camera
* 2 Class 1 line lasers
* Connection through USB-A cable
* 12V 1.5A power connector
* 1 NEMA stepper motor (1.7A 1.8 deg/step)

## Overview of the 20180205 v1.2 Board

The **20180205 v1.2 board**, also known as the **Ciclop 3D Scanner board**, has its own unique features and specifications. Here’s an overview of its characteristics compared to typical RepRap boards:

| **Feature**              | **20180205 v1.2 Board**                   | **Typical RepRap Boards**          |
|--------------------------|-------------------------------------------|------------------------------------|
| **Processor**            | ATmega1284P                               | ATmega2560, LPC1768, STM32, etc.  |
| **Motor Drivers**        | 2 integrated stepper motor drivers        | Variable; usually up to 5+ drivers |
| **Supported Firmware**   | Specific Ciclop firmware                  | Various (e.g., [Marlin](https://github.com/MarlinFirmware/Marlin), [Smoothie](https://github.com/Smoothieware/))  |
| **Features**             | Designed for 3D scanning, includes laser control | General-purpose 3D printing features |
| **Input Voltage**        | 12V                                       | Typically 12V or 24V depending on the board |
| **Connectivity**         | USB interface for direct communication     | USB, SD card, UART, etc., depending on the board |

### Key Characteristics of the 20180205 v1.2 Board

- **Processor**: The board uses an **ATmega1284P**, which is less powerful than many 32-bit boards but sufficient for its specific operations.
  
- **Motor Drivers**: It has **two integrated stepper motor drivers**, suitable for the limited operational requirements of a 3D scanner (usually controlling two motors for rotation and movement).

- **Firmware Support**: It is tailored to run specific firmware suitable for the Ciclop scanner, which might limit versatility compared to boards supporting multiple firmware options.

- **3D Scanning Focus**: Unlike general-purpose RepRap boards, the 20180205 v1.2 is designed specifically for 3D scanning, with features optimized for laser control and scanning accuracy.

- **Connectivity**: Primarily connects via USB, which allows for direct communication with a connected computer running the associated scanning software.

### Conclusion

The **20180205 v1.2 board** is specialized for the **Ciclop 3D Scanner**, offering unique features beneficial for 3D scanning applications. While it may lack the versatility of typical RepRap boards in terms of 3D printing, it excels in its intended function and is tailored for users focused on 3D scanning projects.

## Comparison: 20180205 v1.2 Board vs. Original CowTech Board

The **20180205 v1.2 board** aligns closely with the original **CowTech** board from Kickstarter, as both are designed for the **Ciclop 3D Scanner** project. Here are some key points of comparison:

| **Aspect**                     | **20180205 v1.2 Board**                   | **CowTech Board**                   |
|--------------------------------|-------------------------------------------|-------------------------------------|
| **Designer**                   | Specific to Ciclop (promoted by BQ)      | Original design by CowTech          |
| **Processor**                  | ATmega1284P                               | ATmega1284P                         |
| **Motor Drivers**              | 2 integrated motor drivers                | 2 integrated motor drivers          |
| **Firmware**                   | Ciclop-specific firmware                   | Ciclop-specific firmware             |
| **Functionality**              | Designed for 3D scanning                  | Designed for 3D scanning            |
| **Connectivity**               | USB interface                             | USB interface                       |

### Similarities
1. **Processor**: Both boards use the **ATmega1284P**, which is adequate for the tasks required in 3D scanning applications.

2. **Motor Drivers**: Both boards include **two integrated stepper motor drivers**, suitable for operating the scanner's rotation and movement.

3. **Firmware**: They both run firmware specifically developed for the **Ciclop 3D Scanner**, facilitating the necessary operations for scanning.

4. **Functionality**: Both boards are fundamentally designed to function as a control unit for 3D scanning applications, maintaining a focus on similar objectives.

### Differences
- While the **20180205 v1.2 board** has become a standardized version with some potential enhancements, the original **CowTech board** may have featured variations depending on early prototypes or stages of development.

- Any updates or enhancements in the **20180205 v1.2 board** may include improved circuitry or design elements based on feedback from users of the original CowTech board.

### Conclusion
Overall, the **20180205 v1.2 board** maintains a close alignment with the original **CowTech board**, sharing essential components and functionality tailored for the **Ciclop 3D Scanner**.

## Ciclop 3D Scanner Power-On Sequence

The following steps outline the power-on sequence for the Ciclop 3D Scanner. It is crucial to follow this sequence carefully to prevent any potential damage to the components:

1. **Connect Power Supply**: Ensure the 12V power supply is connected to the scanner.
2. **Plug in USB Cable**: Connect the USB cable from the scanner to the computer **after** connecting the power supply.
3. **Turn On Power**: Switch on the main power source for the scanner.
4. **Initialize Components**: Allow the motors and lasers to initialize, which may include calibration sounds.
5. **Start Software**: Launch the Horus software on your computer to control the scanner.
6. **Set Up Camera**: Verify that the camera (e.g., Logitech C270) is connected and active.
7. **Calibration**: Perform calibration steps as prompted by the Horus software, ensuring correct alignment of lasers and camera detection.

For detailed guidance, refer to user manuals or community resources such as [Instructables](https://www.instructables.com/Ciclop-3d-Scanner-My-Way-Step-by-Step/) and [Mischianti's guide](https://mischianti.org/ciclop-3d-scanner-components-testing-and-calibration-4/).

## Directory structure

 * `step`: The original Ciclop step files. This folder is frozen. Find the latest version in the `freecad` folder
 * `stl`: Ciclop STL files. It also contains parts with support for 3D printing
 * `dxf`: Ciclop DXF files. It contains all methacrylate pieces cutted with laser
 * `svg`: Ciclop SVG files. This folder contains all drawings for 2D printing
 * `freecad`: Ciclop source files in Freecad
 * `bom`: Ciclop Bill of Materials.

## Calibration

In order to successfully use the instrument, calibration needs to be done via this pattern.

![pattern](/images/calibration-pattern_sm.jpg)

## Overview of ATmega1284P

The **ATmega1284P** is a popular 8-bit microcontroller from Microchip Technology (formerly Atmel) designed for a wide range of applications in embedded systems. Below are key specifications and features of the ATmega1284P.

### Key Specifications

| **Specification**          | **Details**                        |
|----------------------------|------------------------------------|
| **Architecture**           | AVR 8-bit                          |
| **Operating Voltage**      | 1.8V to 5.5V                      |
| **Flash Memory**           | 128 KB                             |
| **SRAM**                   | 16 KB                              |
| **EEPROM**                 | 4 KB                               |
| **Clock Speed**            | Up to 20 MHz                      |
| **GPIO Pins**              | 32 (I/O pins)                     |
| **ADC Channels**           | 8 (10-bit resolution)             |
| **PWM Channels**           | 6                                 |
| **USART**                  | 1 (Universal Synchronous and Asynchronous serial receiver and transmitter) |
| **SPI**                    | 1                                 |
| **I2C (TWI)**              | Yes                               |
| **Timers**                 | 3 (16-bit timers)                |
| **Interrupts**             | 24 external interrupt lines       |

### Key Features

- **Versatility**: Suitable for various applications such as robotics, automation, and sensor interfacing.
- **Low Power Consumption**: Can operate in different power-saving modes, making it ideal for battery-powered applications.
- **Wide Range of Peripherals**: Supports digital input/output, analog-to-digital conversion, and communication protocols (SPI, I2C, USART).
- **User-Friendly Development**: Compatible with popular development platforms such as the Arduino ecosystem, enhancing accessibility for hobbyists and professionals.

### Applications

- **DIY Electronics Projects**: Commonly used in homemade electronics and microcontroller-based projects.
- **3D Printers**: Frequently found in control boards for 3D printers.
- **Robotics**: Ideal for controlling motors and processing sensor data in robotic systems.
- **Data Acquisition Systems**: Suitable for collecting and processing data from various sensors.

### Conclusion

The **ATmega1284P** is a versatile and powerful microcontroller that combines a rich set of features with a user-friendly design, making it a popular choice for both hobbyists and professionals. Whether used in 3D printers, robotics, or other embedded systems, it provides an excellent balance of performance and ease of use.
