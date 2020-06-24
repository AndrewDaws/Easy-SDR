# Assembly guide for Antenna Mini-Whip (SMD) module

## PCB requirements
In the manufacture of the device, use the material of the FR-4 printed circuit board with a thickness of 1.6 mm (this is not the best material for RF equipment, but it is the most popular and affordable). This is necessary to comply with the wave impedance of the RF line equal to 50 Ohms. If this requirement is not observed, the wave impedance of the RF line will be different from 50 Ohms, which may lead to incorrect operation of the device. Wave resistance calculations were performed for a material with Er = 4.6 (FR-4) using [Saturn PCB Design V7.08](http://www.saturnpcb.com/pcb_toolkit/).

## Components installing 
Due to the use of SMD components and relatively tight mounting, this module has some recommendations on the soldering order of components, this is necessary to facilitate soldering (no hard-to-reach areas for the soldering iron will be formed).
Also, it is strongly recommended that you **use an antistatic wrist strap and do not use soldering irons that are powered directly from the 220V / 110V network**, which can damage the MOSFET BF998 when soldering.

Soldering order of components:

- **Main module:** R2 -> R1 -> R4 -> R6 -> C2 -> R7 -> R3 -> L1 -> R5 -> C1 -> R8 -> C5 -> R9 -> C4 -> С3 -> R10 -> R11 -> L2 -> Q2 -> Q1 -> SMA con.  
- **Power feed unit:** C7 -> C6 -> C8 -> L3 -> D1 -> DC1 -> SMA con.
- **Power feed unit (with RF-isolation transformer):** C10 -> D2 -> C9 -> C11 -> P2 -> T1 -> DC2 -> SMA con.

## Additional instructions
A useful step can also be to check the output voltage level with a multimeter. To prevent damage to your receiver, connect PFU to the power supply, and perform voltage measurement on the SMA connector (PFU-to-receiver connector). The value of the output voltage must be zero. After that, you can make further connections and work with the antenna.

## Installation recommendations
Immediately before installation, you can place the antenna in a plastic housing, this will additionally protect your antenna from precipitation. The installation of the antenna in the plastic housing does not interfere with the normal reception.

To install the Mini-Whip antenna, you can choose a grounded metal or dielectric mast.

**In the case of selecting a metal mast, it is necessary to place the antenna above the top of the mast, and the mast itself must have a good grounding (the cable shield is also grounded)**. Qualitative grounding is necessary for the correct operation of the antenna since its principle is based on the principle of measuring the potential between the metal plate of the antenna itself and the ground (earthed mast), after which the transmitted signal is transmitted to the receiver.  
![Metal mast installation](../../Resources/Antenna%20Mini-Whip/Metal-mast-installation.png)  

**In case of using a mast made of dielectric material, you also need to perform high-quality grounding of the shield of the coaxial cable used.** Since in this case the potential difference is measured between the antenna plate and the shield of the coaxial cable.  
![Dielectric mast installation](../../Resources/Antenna%20Mini-Whip/Dielectric-mast-installation.png)  

An additional advantage will also be the location of the antenna at the highest available point of installation.

## Power supply recommendations
When powering the antenna, **do not use power banks or other power supplies with impulse converters**. These devices create a sufficiently large amount of interference, which can adversely affect reception quality. It is recommended to use a battery with a nominal voltage of 5 - 13 V. In addition, a good solution will be the use of ferrite filters on power cables.
