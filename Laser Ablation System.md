# Laser Ablation System

## Overview

![PXL_20210116_122811618](https://github.com/user-attachments/assets/a9a11b88-22a8-4542-b2ad-aaf597c6c314)

![PXL_20210116_101825729 NIGHT](https://github.com/user-attachments/assets/9f4128fd-db88-46f0-90fd-548bb6b7900a)

## Protocol

### I. Preparation

1. Open the Ti microscope, select the eyepiece port. Choose a proper objective (NA>0.9 is recommended) and put the a sample on.
   - a. Move the sample to a blank region for avoiding photodamage on regions of interest.
   - b. $$\textrm{\color{red}Alarm: make sure the laser power is turned off when switching to a camera port!}$$
2. Insert the CFP filterset ($$\textrm{\color{red}with the excitation filter removed}$$) into the lower filter turret on the microscope.
   - a. $$\textrm{\color{red}Alarm: make sure the emission filter is in position!}$$

![Picture2](https://github.com/user-attachments/assets/2a06cfac-42ba-4ed0-ba48-14d3c8f89dc9)

3. Plug in the USB of the arduino chip.
4. Plug in the socket of the power supply.

![Picture1](https://github.com/user-attachments/assets/34157b23-700f-4e10-b452-0e6b37260c7e)

5. Open NIS Elements software.
6. Open 'Command' dialogue, choose and open the correspoding serial port.
   - a. $$\textrm{\color{red}Upon opening the port, there will be a transient blink from the laser.}$$
   - b. Make sure the 'Terminater by CR' is ticked.

![Untitled3](https://github.com/user-attachments/assets/1ea46ebc-1389-4367-a34b-7b1f5a8c034d)

7. Write 'o1' (open 2% power) to the serial port, the laser power is then turned on to a low level.
8. Use eyepiece port to adjust the focus.
   * a. $$\textrm{\color{red}Alarm: make sure the emission filter is in position before this step!}$$
   * b. The laser spot should be located at the left field of view.
   * c. A perfect focus is reached when a rectangle spot is observed.
   * d. When a distorted laser spot, e.g., a tilted cone is observed, the obtical path is shifted. Call Wang Yuhao for re-adjusting the obtical path.

![PXL_20210116_093911491](https://github.com/user-attachments/assets/9eb7ad67-dc27-4471-a4fa-c21349ffaf8e)

9. Write 'c0' (close to 0% power) to the serial port, the laser power is then turned off.

### II. Test and ablate

$$\textrm{\color{red}It is highly recommended to Wear a laser protective glass in the following steps.}$$

![PXL_20210116_102354482](https://github.com/user-attachments/assets/ac2e5df5-7985-49fb-bc2a-621be176701e)

1. Move the sample to a testing region.
2. Set ablation parameters and test:
   * a. Open the 'laser ablation point' macro
   * b. Set the \textrm{\color{red}power}$$ in 'WritePort(9,"o\textrm{\color{red}50}$$",13,0);', 50% power by default;
   * c. Set the ablation \textrm{\color{red}time (s)}$$ in 'Wait(\textrm{\color{red}2}$$);', 1 s ablation by default;
   * d. Execute and examine the ablation effect. Change parameters if necessary.3

![Untitled](https://github.com/user-attachments/assets/59785dd8-f2ff-42b9-a869-5ca80454be7b)

3. Set ablation points and ablate:
   * a. Set the coordinates of ablation points in 'ND Acquisition';
   * b. Tick the 'Execute Command' and choose the macro 'laser ablation point';
   * c. Execute by 'Run Now'.

![Untitled2](https://github.com/user-attachments/assets/8335de8d-4601-4f0e-b91a-91a6da668801)

4. Examine the ablation results, close the serial port, and close NIS elements.
5. Unplug the socket of the power supply and the USB of the arduino chip.

## Specs

Laser maximum power: 2000 mW

Laser power control: PMW

Laser wavelength: 444±5 nm

Laser spectrum:

![image](https://github.com/user-attachments/assets/d86ed525-45ed-4732-a809-a3385f373018)
