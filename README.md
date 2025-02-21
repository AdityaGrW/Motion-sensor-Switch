# Motion-sensor-Switch
This project shows how to make a low cost motion sensor light switch using the CD4017 IC and IR proximity sensor. You can use this motion activated light circuit as an automatic room light switch. Here, each time the IR proximity sensor sense detects any motion, it send the clock pulse to CD4017 IC. Then the 4017 changes its previous state.

## Table of Contents
- [Introduction](#introduction)
- [Required Components](#required-components)
- [Setup Instructions](#setup-instructions)
- [Usage Instructions](#usage-instructions)
- [APPLICATIONS](#APPLICATIONS)

## Introduction
Here, each time the IR proximity sensor sense detects any motion, it send the clock pulse to CD4017 IC. Then the 4017 changes its previous state.When anyone enters the room the IR proximity sensor senses the motion and turns on the light.
After that when he or she exits the room, the IR sensor again sense the motion and turn off the light.

## Required Components
1) CD4017 IC
2) LM358 IC
3) BC547 Transistor
4) 100uF 25V Capacitor
5) 1000uF 25V Capacitor
6) 220-ohm 0.25watt Resistors – 4 no
7) 10k 0.25watt Resistor
8) 10k Trimmer
9) LED 5mm – 3no
10) IR LED pair (Detector & Emitter)
11) 1N4007 Diode
12) 5V SPDT Relay

## Setup Instructions
The IR emitter LED continuously emits infrared. When any object comes within the range, some amount of infrared reflects from the object surface and that reflected infrared can be detected by the IR receiver LED.
The LM358 compares the voltage across the IR receiver LED with the predefined value. When any motion detected the voltage across the IR receiver crosses the predefined value, so the output pin (pin 1) of LM358 becomes high.
The clock pin (Pin-14) of CD4017 IC is connected with the output pin of LM358. So when any motion detected, the 4017 IC receives a clock pulse and changes the current state of Pin-2.
The Pin-2 of CD4017 is connected with the base of the BC547 NPN transistor, So when the Pin-2 becomes high the transistor turns on.
 When the transistor turns on, the current can flow through the relay coil. So the load connected with the relay also turns on.
If the Pin-2 becomes low, the transistor turns off and accordingly the load connected with the relay also turns off.


## Usage Instructions
1. **Power On**: Ensure all components are connected as per the setup instructions. Connect the power supply to the circuit.
2. **Motion Detection**: The IR proximity sensor will continuously emit infrared radiation. When it detects motion within its range, the infrared reflected from the object will be sensed by the IR receiver.
3. **Light Activation**: Upon detecting motion, the LM358 IC will compare the received signal and, if it crosses the predefined threshold, will send a clock pulse to the CD4017 IC.
4. **Relay Activation**: The CD4017 IC will change its state, turning the transistor on, which in turn activates the relay. This will switch on the connected light or load.
5. **Automatic Turn Off**: When no motion is detected, the IR sensor will not send a signal, causing the relay to turn off the light or load after a predefined interval.
6. **Adjustments**: Use the 10k trimmer to adjust the sensitivity of the IR proximity sensor as required.
7. **Troubleshooting**: If the light does not turn on or off as expected, check all connections, ensure the power supply is stable, and verify the components are functioning correctly.
By following these steps, you can use the motion sensor switch to automatically control lighting in a room.


## APPLICATIONS 
A motion sensor light triggers a response when motion is detected. They can be installed indoors, on walls, ceilings, and in doorways, or outside, on the exterior of buildings and homes. Motion sensors are used primarily in home and business security systems, but they can also be found in phones, paper towel dispensers, game consoles, and virtual reality systems.


## Contributing
Contributions are welcome! Please read the [contributing guidelines](CONTRIBUTING.md) for more information.

## License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
