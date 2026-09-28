# Evaporative Swamp Cooler

A microcontroller-powered swamp cooler built for CPE 301 (Embedded Systems Design) at the University of Nevada, Reno. The system monitors temperature, humidity, and water level, then automatically controls a fan and lets users adjust an air vent.

![Circuit](wholecircuit1.JPEG)

## Features
- **Four-state system:** Disabled, Idle, Running, and Error, each shown with its own LED (yellow, green, blue, red)
- **Automatic fan control:** turns the fan on when the temperature rises above 25°C
- **Water level safety:** switches to an Error state if the water level drops too low
- **Adjustable vent:** a stepper motor moves the vent left or right with button presses
- **LCD display:** shows temperature, humidity, and water level, updated every 60 seconds
- **Event logging:** records each state change with a timestamp from a real-time clock (RTC)
- **Start and stop buttons** handled with hardware interrupts

## How It Was Built
The firmware is written at the **register level** instead of relying on built-in Arduino functions. It directly configures the microcontroller's hardware for:
- Digital inputs and outputs (LEDs and buttons)
- Analog-to-digital conversion (water level sensor)
- PWM timers (fan speed)
- UART serial communication (event logging)
- External interrupts (start and stop buttons)

## Hardware
- Arduino Mega 2560 (ATmega 2560)
- DHT temperature and humidity sensor
- Water level sensor
- Fan motor
- Stepper motor
- 16x2 LCD
- DS1307 real-time clock
- LEDs and push buttons

## Files
| File | Contents |
|---|---|
| `swamp_cooler.ino` | Arduino firmware |
| `detailed_schematic.jpg` | Circuit schematic |
| `wholecircuit1.JPEG`, `wholecircuit2.JPEG` | Photos of the assembled circuit |
| `IMG_2009.MOV`, `IMG_2010.MOV` | Demo videos |
| `Cirkit Designer/` | Circuit design files |

## Tools
C/C++, Arduino IDE, Cirkit Designer

## Team 
Pinky Nguyen, Bella Picasso-Kennedy, Louis Pierce, Alexus Rowe
