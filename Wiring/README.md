# Wiring / Electronics
The wiring is based around the VFD, the proximity sensors, and the solenoid valve. The VFD gets the analog signal from the Shapeoko controller. That is what turns the spindle on and sets the speed. For safety I wired the tool release solenoid valve through the VFDs relay output with the parameter defined to be closed any time the spindle is spinning. That prevents the tool from being released at speed, which would be a disaster. I'm going to put together an enclosure layout and wiring diagram for all this.

The tool release button enclosure is in the STLs folder. The wording for tool release is slightly debossed into that file. If you have a multi color 3D printer you can paint that surface in your slicing software.
