# Protokeeb Assembly Instructions

<details open>
<summary>PCB Rev 1.0</summary>

# Table of Contents

## 1. [Required Tools and Components](#required-tools-and-components)

- [1.1 Tools](#tools)
- [1.2 Optional Tools/Equipment](#optional-toolsequipment)
- [1.3 Components](#components)

## 2. [Assembly Steps](#assembly-steps)

- [2.1 Step 1: Prepare the PCB for Soldering](#step-1-prepare-the-pcb-for-soldering)
  - [Apply the Solder Paste Using the SMT Stencil](#apply-the-solder-paste-using-the-smt-stencil)
  - [Apply the Solder Paste Manually](#apply-the-solder-paste-manually)
- [2.2 Step 2: Prepare the SMD Soldering Equipment](#step-2-prepare-the-smd-soldering-equipment)
  - [Hot Air Rework Station](#hot-air-rework-station)
  - [SMD Reflow Hot Plate](#smd-reflow-hot-plate)
- [2.3 Step 3: Capacitor Placement](#step-3-capacitor-placement)
- [2.4 Step 4: Diode Placement (Top Layer)](#step-4-diode-placement-top-layer)
- [2.5 Step 5: Resistor Placement (Top Layer)](#step-5-resistor-placement-top-layer)
- [2.6 Step 6: Voltage Level Translator IC Placement](#step-6-voltage-level-translator-ic-placement)
- [2.7 Step 7: ESD Protection IC Placement](#step-7-esd-protection-ic-placement)
- [2.8 Step 8: RGB LED Placement](#step-8-rgb-led-placement)
- [2.9 Step 9: Push Button Placement](#step-9-push-button-placement)
- [2.10 Step 10: Testing RGB LEDs](#step-10-testing-rgb-leds)
- [2.11 Step 11: Resistor Placement (Bottom Layer)](#step-11-resistor-placement-bottom-layer)
- [2.12 Step 12: USB Connector Placement](#step-12-usb-connector-placement)
- [2.13 Step 13: Diode Placement (Bottom Layer)](#step-13-diode-placement-bottom-layer)
- [2.14 Step 14: RP2040 Development Board Placement](#step-14-rp2040-development-board-placement)
- [2.15 Step 15: Rotary Encoder Placement](#step-15-rotary-encoder-placement)
- [2.16 Step 16: Flash the Firmware](#step-16-flash-the-firmware)
- [2.17 Step 17: Initial Testing (Optional)](#step-17-initial-testing-optional)
- [2.18 Step 18: Assemble the Case](#step-18-assemble-the-case)
  - [Sandwich/Layered Case](#sandwich-case)
  - [3D Printed Case](#3d-printed-case)

## Required Tools and Components

### Tools

- Soldering iron with a fine tip
- Solder wire with rosin flux core
- Low melting point solder paste
- Flux (optional but recommended)
- Tweezers
- Allen key/hex screwdriver bits (for case assembly)
- Multimeter (for testing connections)
- Hot air rework station (for soldering SMD components)
- Reflow hot plate (for soldering SMD components, optional)

### Optional Tools/Equipment

- Laser cutter (if you choose to cut your sandwich case layers yourself)
- 3D printer (if you choose to print your case yourself)

### Components

- Protokeeb PCB rev 1.0
- Raspberry Pi Pico / Raspberry Pi Pico W / Waveshare RP2040-Plus
- Mechanical switches (16)
- Keycaps (16)
- WS2812B-2020 LEDs (16)
- Diodes (17, as specified in the BOM)
- Rotary encoder with push button
- USB Type-C connector
- Various resistors and capacitors (as specified in the BOM)
- Various screws/bolts and nuts for mounting the Case and PCB
- Super glue
- Case (sandwich style/layered or 3D printed)

## Assembly Steps

### Step 1: Prepare the PCB for soldering

**Note:** I have not ordered the SMT stencil from the PCB fabrication house, so there are no images for the SMT stencil solder paste application process.

Choose one of the following approaches:

<details open>
<summary><a name="Apply the Solder Paste Using the SMT Stencil"></a></summary>

1. Align the Protokeeb SMT stencil properly with the Protokeeb PCB.

2. Secure the SMT stencil using masking or polyamide/Kapton tape.

3. Using a spatula or similar tool, spread the solder paste evenly over the surface of the SMT stencil, ensuring every pad of the PCB is covered with solder paste.

</details>

<details>
<summary>Apply the Solder Paste Manually</summary>

1. Use solder paste that comes in a syringe if possible, rather than in a small cylindrical container.

2. Select a small diameter blunt syringe needle (normally included with syringe-type solder paste).

   **Note:** Ensure the needle's diameter is not too small, or it will hinder the proper flow of solder paste.

3. Unlike the SMT stencil method, apply the solder paste only to the pads you are working on, such as capacitors, resistors, etc.

4. Spread the solder paste evenly, making sure not to accidentally bridge two separate pads by applying too much solder paste.

</details>

### Step 2: Prepare the SMD Soldering Equipment

<details open>
<summary>Hot Air Rework Station</summary>

1. Set the temperature of your SMD rework station according to the melting point of the solder paste.

   **Note:** Normally, a temperature of 250°C with 15 air works fine for most low melting solder pastes.

2. Secure the PCB on a PCB holder or using a third hand tool for easier soldering.

</details>

<details>
<summary>SMD Reflow Hot Plate</summary>

1. If you have a consumer or DIY SMD reflow hot plate, adjust the reflow curve settings according to the melting point and reflow properties of your solder paste. Otherwise, set the desired melting temperature.

![A-Tech Officials SMD Reflow Plate](Images/PCB_Assembly/Protokeeb_AS_3.jpg)

2. Place the Protokeeb PCB on the hot plate. If the hot plate surface area is smaller than the PCB dimensions, add support beneath the PCB areas that are not in contact with the hot plate surface to keep the PCB flat during reflow.

![A-Tech Officials Protokeeb PCB Reflow](Images/PCB_Assembly/Protokeeb_AS_2.jpg)

</details>

### Step 3: Capacitor Placement

**Note:** Open the included interactive BOM file on your laptop/desktop/tablet during soldering to easily track components and placement.

1. Using tweezers, place the required capacitors on the correct pads according to the interactive BOM file. We are using 0603 package SMD capacitors, which can be easily misplaced if not handled correctly.

![Protokeeb PCB Capacitor Placement](Images/PCB_Assembly/Protokeeb_AS_4.jpg)

2. Start the reflow process if using a hot plate, or solder each capacitor one at a time using a hot air SMD rework station.

![Protokeeb PCB Capacitor Reflow Process](Images/PCB_Assembly/Protokeeb_AS_5.jpg)

### Step 4: Diode Placement (Top Layer)

**Note:** Open the included interactive BOM file on your laptop/desktop/tablet during soldering to easily track components and placement.

1. Using tweezers, place the required 16 diodes on the correct pads according to the interactive BOM file. Ensure the diodes' direction is correct.

   **Note:** Refer to the interactive BOM for proper orientation.

![Protokeeb PCB Diode Placement](Images/PCB_Assembly/Protokeeb_AS_8.jpg)

2. Begin the reflow process if using a hot plate, or solder each diode individually using a hot air SMD rework station.

### Step 5: Resistor Placement (Top Layer)

1. Using tweezers, place the required resistors on the correct pads according to the interactive BOM file. We are using 0603 package SMD resistors, which can be easily misplaced if not handled correctly.

![Protokeeb PCB Resistor Placement](Images/PCB_Assembly/Protokeeb_AS_12.jpg)

2. Begin the reflow process if using a hot plate, or solder each resistor individually using a hot air SMD rework station.

### Step 6: Voltage Level Translator IC Placement

1. Using tweezers, place the TXB0102DCU Voltage Level Translator IC on the correct pads according to the interactive BOM file. Ensure the IC's first pin is aligned with the PCB footprint's first pin.

   **Note:** Proper alignment is crucial for functionality.

![Protokeeb Voltage Level Translator IC Placement](Images/PCB_Assembly/Protokeeb_AS_13.jpg)

2. Begin the reflow process if using a hot plate, or solder the IC using a hot air SMD rework station.

![Protokeeb Voltage Level Translator IC Reflow Process](Images/PCB_Assembly/Protokeeb_AS_16.jpg)

> There was a mistake in interpreting the datasheet of the TXB0102DCU Voltage Level Translator IC, which required circuit modifications for the Protokeeb RGB LEDs to work. This error has been rectified in the Protokeeb Rev 1.0 PCB files.

**Problem:** While designing the PCB, the TXB0102DCU IC's OE pin was pulled to ground with a 51K resistor, as suggested in the datasheet's "8.2 Typical Application" section. However, this caused the LEDs not to light up with data signals from the MCU. To fix this, I had to bypass the IC and connect the RGB data track directly to the RGB LEDs. Although not ideal since the MCU operates at 3.3V logic and the RGB LED is powered by 5V, this was a necessary modification.

![Protokeeb PCB circuit modification](Images/PCB_Assembly/Protokeeb_AS_18.jpg)

**PCB Improvements:** The updated PCB includes an option to pull the TXB0102DCU IC's OE pin high or low using a 51K resistor and solder jumper bridges JP2 and JP3 to bypass the TXB0102DCU IC, allowing a direct connection from the RGB LED data pin to the MCU.

![Protokeeb PCB Solder Bridge Jumpers](Images/PCB_Renders/AT-ProtoKeeb_rev1_5.png)

### Step 7: ESD Protection IC Placement

1. Using tweezers, place the USBLC6-2SC6 ESD Protection IC on the correct pads according to the interactive BOM file. Ensure the IC's first pin is aligned with the footprint's first pin on the PCB.

   **Note:** Proper alignment is crucial.

![Protokeeb PCB ESD Protection IC Placement](Images/PCB_Assembly/Protokeeb_AS_19.jpg)

2. Begin the reflow process if using a hot plate, or solder the IC using a hot air SMD rework station.

![Protokeeb PCB ESD Protection IC Reflow Process](Images/PCB_Assembly/Protokeeb_AS_20.jpg)

### Step 8: RGB LED Placement

1. Using tweezers, place the 16 WS2812B-2020 RGB LEDs on the correct pads according to the interactive BOM file. Ensure each LED's first pin is aligned with the footprint's first pin on the PCB. The small SMD package size makes careful handling essential.

   **Note:** Proper alignment is crucial.

![Protokeeb PCB RGB LED Size comparison](Images/PCB_Assembly/Protokeeb_AS_23.jpg)

![Protokeeb PCB RGB LED Placement](Images/PCB_Assembly/Protokeeb_AS_24.jpg)

2. Begin the reflow process if using a hot plate, or solder each LED individually using a hot air SMD rework station.

   **Note:** Avoid high temperatures that can damage the LED lens.

![Protokeeb PCB RGB LED Reflow Process](Images/PCB_Assembly/Protokeeb_AS_26.jpg)

> The Protokeeb Rev 1.0 PCB allows for two separate RGB data signals from the MCU: Rows 1 and 2 share "DATA-IN-1," and Rows 3 and 4 share "DATA-IN-2." This enables different RGB animations/colors for each group. To use a single data signal for all rows, bridge solder jumper "JP1."

![Protokeeb PCB Solder Bridge Jumpers](Images/PCB_Renders/AT-ProtoKeeb_rev1_5.png)

### Step 9: Push Button Placement

1. Using tweezers, place the two SMD push buttons on their respective pads according to the interactive BOM file. Ensure proper alignment.

![Protokeeb PCB Push Button Placement](Images/PCB_Assembly/Protokeeb_AS_27.jpg)

2. Begin the reflow process if using a hot plate, or solder each push button using a hot air SMD rework station.

![Protokeeb PCB Push Button Reflow Process](Images/PCB_Assembly/Protokeeb_AS_28.jpg)

### Step 10: Testing RGB LEDs

Before soldering the Raspberry Pi Pico development board onto the Protokeeb PCB, let's test the RGB LEDs.

1. Solder jumper wires to the following test pads:

   | Silkscreen Reference | Function  |
   | :------------------: | :-------: |
   |         TP1          |    5V     |
   |         TP2          |    GND    |
   |         TP3          | Data-in-1 |

![Protokeeb PCB Jumper Wire Soldering Process](Images/PCB_Assembly/Protokeeb_AS_29.jpg)

2. Prepare a second Raspberry Pi Pico or any other RP2040 development board and upload the CircuitPython firmware onto it. You can get the CircuitPython firmware .uf2 file [here](https://circuitpython.org/board/raspberry_pi_pico/)

3. Download the required CircuitPython libraries from [here](https://circuitpython.org/libraries) For our testing purposes, we only need the "neopixel" and the "adafruit_led_animation" libraries.

4. Connect the Jumper wires to the RP2040 development board according to the table below:

   | Jumper Wire | RP2040 Dev board |
   | :---------: | :--------------: |
   |   TP1/5V    |        5V        |
   |   TP2/GND   |       GND        |
   |  TP3/Data   |      GPIO10      |

   **Note:** (Optional) Connect a 100-ohm resistor between the data pin of the RGB LED and the RP2040 pin (GPIO10).

5. Plug the Raspberry Pi Pico or RP2040 dev board into your computer. It should appear as "CIRCUITPY". Extract the CircuitPython bundle you downloaded and copy the "adafruit_led_animation" folder from the lib directory to the lib directory on your CircuitPython device.

6. Open the "code.py" file (located on your CircuitPython device) with your preferred editor and replace its content with the code below:

```python
import board
import neopixel
from adafruit_led_animation.animation.rainbow import Rainbow
import time

# Configuration for the NeoPixel LEDs
pixel_pin = board.GP10 # Change if required, according to your setup
num_pixels = 16 # Number of pixels, in our case 16-Keys so 16-pixels
# Specify the color order, e.g., neopixel.RGB in our case since using WS2812B-2020 LEDs
pixels = neopixel.NeoPixel(pixel_pin, num_pixels, brightness=0.5, auto_write=False, pixel_order=neopixel.RGB)

# Create a rainbow animation object
# Feel free to adjust the speed and period parameters of the
# Rainbow class to customize the appearance of the swirl effect.
# The speed parameter controls how fast the colors move,
# and the period parameter defines the length of the rainbow cycle.
rainbow = Rainbow(pixels, speed=0.1, period=2)

# Main loop to run the animation
while True:
    rainbow.animate()
    time.sleep(0.01)  # Short delay to make the animation smoother
```

7. Run the CircuitPython code and check if all the RGB LEDs are working properly.

![Protokeeb PCB RGB LED Testing](Images/PCB_Assembly/Protokeeb_AS_30.jpg)

### Step 11: Resistor Placement (Bottom Layer)

1. Grab the required resistors and place them on the correct pads according to the Interactive BOM file. Use tweezers to handle the 0603 package SMD resistors, as they can be easily misplaced.

2. Use a hot air rework station or a fine-tip soldering iron to solder the resistors one at a time.

   **Note:** You cannot use the SMD Reflow Hot Plate because the top layer of the PCB is populated with electronic components.

![Protokeeb PCB Resistor Placement](Images/PCB_Assembly/Protokeeb_AS_33.jpg)

### Step 12: USB Connector Placement

1. Grab the USB 2.0/3.1 Type-C connector and place it securely on its respective pad according to the Interactive BOM file.

2. Use a hot air rework station or a fine-tip soldering iron to solder the USB connector securely.

![Protokeeb PCB USB Connector Placement](Images/PCB_Assembly/Protokeeb_AS_31.jpg)

### Step 13: Diode Placement (Bottom Layer)

1. Grab a Schottky barrier diode (according to the BOM) and, using tweezers, place it on its respective pad according to the Interactive BOM file.

   **Note:** Ensure the diode direction is correct as per the Interactive BOM file.

2. Use a hot air rework station or a fine-tip soldering iron to solder the diode securely.

![Protokeeb PCB USB Connector Placement](Images/PCB_Assembly/Protokeeb_AS_32.jpg)

### Step 14: RP2040 Development Board Placement

1. (Optional) If using a Raspberry Pi Pico or Pico W, it is recommended to de-solder its micro USB connector as it will not be used in this project.

2. Apply some solder paste on the Raspberry Pi Pico footprint/pads located on the Protokeeb PCB.

3. Align the RP2040 development board on its respective pad/footprint using tweezers.

![Protokeeb PCB Raspberry Pi Pico Soldering Process](Images/PCB_Assembly/Protokeeb_AS_34.jpg)

4. Use a hot air rework station to solder it in place.

   **Note:** It is recommended to hover the hot air station handle on the entire RP2040 development board area in a circular motion to ensure the pads underneath solder properly with the PCB pads.

![Protokeeb PCB Raspberry Pi Pico Placement](Images/PCB_Assembly/Protokeeb_AS_35.jpg)

### Step 15: Rotary Encoder Placement

1. Take a rotary encoder with a built-in push button (as specified in the BOM) and place it in its respective location.

![Rotary Encoder](Images/PCB_Assembly/Protokeeb_AS_36.jpg)

2. Apply some flux, and use a soldering iron to solder the rotary encoder in place.

![Protokeeb PCB Rotary Encoder Placement](Images/PCB_Assembly/Protokeeb_AS_37.jpg)

Congratulations! You have just completed the soldering part of the assembly process. We are almost done.

![Fully Assembled Protokeeb PCB](Images/PCB_Assembly/Protokeeb_AS_48.jpg)

### Step 16: Flash the Firmware

1. Connect the Protokeeb to your computer via USB.

2. Follow the QMK/KMK firmware flashing instructions to upload the firmware.

**QMK:** The QMK firmware file is included in this GitHub repo at "Firmware > QMK > protokeeb_rev1_default.uf2". Put the Protokeeb into bootloader mode and simply copy and paste the file into the Protokeeb's flash memory. This firmware file consists of the default keymap; if you need anything specific, please refer [here](https://docs.qmk.fm/#/newbs_building_firmware) for further development.

### Step 17: Initial Testing (Optional)

1. Before powering on the Protokeeb PCB, use a multimeter in continuity mode to test each pad and ensure the ground and power lines are not shorted.

2. After uploading the firmware, the RGB LEDs will turn on by default. Check if all the LEDs function properly.

3. Verify that the Protokeeb does not frequently disconnect from your PC.

4. Check these essential test pads for the correct voltages:

   | Silkscreen Reference | Function |
   | :------------------: | :------: |
   |         TP1          |    5V    |
   |         TP2          |   GND    |
   |       TP7/TP11       |   3.3V   |

### Step 18: Assemble the Case

<details>
<summary><a name="Sandwich Case"></a></summary>

A sandwich/layered case is created in layers, with each layer adding thickness/dimension to the case. Common materials include acrylic (affordable and easy to laser cut), ABS, and polycarbonate. Metals like aluminum or stainless steel can be used but are more expensive.

**Note:** If you decided to use metal for your sandwich/layered case it is recommended to use a slightly flexible material for the switch plate layer and keep the switch plate layer thickness to not more than 2mm.

You can order the laser cutting parts for this case according to the table below:

Layer Specifications:

|       Layer        | Thickness |
| :----------------: | :-------: |
|     Top Layer      |    2mm    |
| Switch Plate Layer |    3mm    |
|   Close Layer-1    |    3mm    |
|    Open Layer-1    |    3mm    |
|    Open Layer-2    |    3mm    |
|   Close Layer-2    |    3mm    |
|    Bottom Layer    |    3mm    |

Total case thickness: 20mm.

You can customize colors for a unique look.

> You may find Protokeeb sandwich case images shown in this guide to be slightly different from the released CAD files because at the time of designing the sandwich case for the Protokeeb PCB I had done some mistakes. These mistakes has been rectified in the Protokeeb rev1.0 sandwich case CAD files.

![Protokeeb Sandwich/Layered Case with protective covering](Images/Sandwich_Case/Protokeeb_SC_1.jpg)

1. Prepare the case:

   - Remove protective material/paper from acrylic parts.

![Protokeeb Sandwich/Layered Case](Images/Sandwich_Case/Assembly/Sandwich_Case_AS_3.jpg)

2. Gather hardware:

   |       Hardware       |                     Description                     | Quantity |
   | :------------------: | :-------------------------------------------------: | :------: |
   | M3 Socket Head Bolts |      Length - 20mm (Socket Style - Allen/Hex)       |    6     |
   |       M3 Nuts        |                                                     |    6     |
   |     Encoder Knob     | Outer Diameter - 16mm or 19mm, Shaft Diameter - 6mm |    1     |
   | Silicon/Rubber Feet  |             Diameter - 7.5mm (Optional)             |    4     |
   |       Keycaps        |       Preferred profile and colour (Optional)       |    16    |

![M3 Nuts and Bolts](Images/Sandwich_Case/Assembly/Sandwich_Case_AS_10.jpg)

![Allen Socket Head M3 Bolt](Images/Sandwich_Case/Assembly/Sandwich_Case_AS_11.jpg)

![Rubber Feet Sheet](Images/Sandwich_Case/Assembly/Sandwich_Case_AS_12.jpg)

3. Install switches:

   - Place 16 Cherry MX style/profile mechanical switches on the switch plate layer.

![Protokeeb Switch Plate Mechanical Switch Installation](Images/Sandwich_Case/Assembly/Sandwich_Case_AS_13.jpg)

4. Solder PCB:

   - Solder the Protokeeb PCB onto the installed switches, securing it without additional screws.

5. Glue layers:

   - Apply super glue to the bottom layer and attach close layer-2.
   - Align correctly and press firmly.

6. Secure nuts:

   - Apply super glue to the M3 Nuts cutout on the merged layer (close layer-2 + bottom layer) and place all x6 M3 Nuts.

7. Stack layers:

   - Arrange layers in order: Open Layer, Switch Plate Layer, Close Layer-1, Open Layer-1, Open Layer-2, Merged Layer.

8. Assemble case:

   - Insert x6 M3 Bolts and tighten with an Allen key or hex screwdriver.

![Protokeeb with Sandwich Case](Images/Sandwich_Case/Assembly/Sandwich_Case_AS_7.jpg)

9. Rubber Feet Placement (Optional):

   - Place rubber feet on the bottom side of the case to prevent the Protokeeb from slipping on the table surface.

10. Attaching Keycaps: (Optional)

    - Attach keycap on each key of the Protokeeb Keyboard by gently pressing it on the mechanical key's stem.

11. Final Testing (Optional):

    1. Press all mechanical switches to ensure they work without obstruction.

    2. Check for any gaps between the layers of the sandwich case (unlikely to happen because we have designed the case according to the PCB dimensions and proper measurements).

    3. Verify the USB Type-C port is properly aligned and accessible. Test by connecting a Type-C cable.

    4. Connect the Protokeeb to your PC and ensure everything functions correctly, including RGB LEDs, switches, and the rotary encoder.

> Congratulations! Your Protokeeb is now fully assembled and ready to use. Enjoy your custom keyboard!

![Protokeeb Keyboard with Sandwich Case](Images/KB_Images/Protokeeb_2.jpg)

> For any questions or issues during assembly, please open an issue on GitHub.

</details>

<details open>
<summary>3D Printed Case</summary>
The Protokeeb 3D printed case consists of two parts:

- Switch Plate
  ![Protokeeb 3D Printed Switch Plate](Images/3D_Printed_Case/3D_Case_2.jpg)

- Bottom Enclosure
  ![Protokeeb 3D Printed Bottom Enclosure](Images/3D_Printed_Case/3D_Case_3.jpg)

Recommended 3D printing settings and materials:

- Switch Plate Part:

  - Material: PETG or ABS
  - Layer Height: 0.2mm
  - Infill: 20%

- Bottom Enclosure
  - Material: PLA
  - Layer Height: 0.2mm
  - Infill: 40%

> You may adjust these print settings based on your printer and environment. Suggestions for improved material choices or printing parameters are welcome to help create a flawless Protokeeb case.

1. Prepare the Case:

   - Use a small nipper or cutter to carefully remove any support structures from both the switch plate and bottom enclosure.

2. Gather Required Hardware:

   |        Hardware        |                     Description                     | Quantity |
   | :--------------------: | :-------------------------------------------------: | :------: |
   | Threaded Brass Inserts |                     M2.5 x 4mm                      |    5     |
   |   CSK Philips Screws   |                     M2.5 x 10mm                     |    5     |
   |      Encoder Knob      | Outer Diameter - 16mm or 19mm, Shaft Diameter - 6mm |    1     |
   |  Silicon/Rubber Feet   |             Diameter - 7.5mm (Optional)             |    4     |
   |        Keycaps         |       Preferred profile and colour (Optional)       |    16    |

![Hardware for Protokeeb 3D Printed Case](Images/3D_Printed_Case/Assembly/3D_Case_AS-19.jpg)

![Rubber Feet Sheet](Images/Sandwich_Case/Assembly/Sandwich_Case_AS_12.jpg)

> [!NOTE]
> In the images provided, you’ll see I used socket head (Allen/hex) M2.5×10mm screws instead of the recommended CSK Phillips screws. That’s because I didn’t have the correct ones at the time of assembly. The switch plate is designed specifically for M2.5×10mm CSK Phillips screws, so I recommend sourcing them for the best fit.

3. Install Threaded Brass Inserts:

   Option-1 (recommended):

   - Use a specialized soldering iron attachment/soldering tip that is designed for threaded brass inserts placement. With that attachment insert the threaded brass insert into its respective hole on the bottom enclosure.

   Option-2

   - With the help of a tweezer align a threaded brass insert into its respective hole on the bottom enclosure.

   ![Aligning threaded brass insert inside the bottom enclosure](Images/3D_Printed_Case/Assembly/3D_Case_AS-23.jpg)

   - Use a fine conical soldering iron tip to insert the threaded brass insert into its respective hole on the bottom enclosure.

   ![Fine Conical Soldering Iron Tip](Images/3D_Printed_Case/Assembly/3D_Case_AS-21.jpg)

   > It’s best to use a temperature-controlled soldering iron to prevent overheating, which can deform the PLA walls around the insert holes.

   - Insert the brass insert vertically (90°). If inserted at an angle, it will misalign the screws later.

   - Once the insert is fully inside, gently pull out the iron while simultaneously pressing down on the insert with the help of tweezers, to avoid pulling it out with the iron.
     > Ensure the insert is completely flush and that melted PLA fills its knurled grooves to hold it securely.

![Bottom enclosure with threaded brass inserts](Images/3D_Printed_Case/Assembly/3D_Case_AS-29.jpg)

> [!NOTE]
> As shown in the images above, the cylindrical holes designed for the threaded brass inserts in the bottom enclosure had very thin walls. This caused the PLA to deform, preventing the inserts from sitting fully flush within the case.
> These issues have been corrected in the final release of the 3D Printed Case STL files.
> Additionally, using a fine conical soldering tip for inserting the brass inserts is not an ideal method—it’s difficult to maintain proper alignment and vertical insertion. As a result, some inserts may end up tilted rather than perfectly perpendicular (90°), which can cause alignment issues when fastening screws.

4. Test Fit the Case:

   - Align the Protokeeb PCB’s USB Type-C port with its cutout and place it into the bottom enclosure.

   ![Protokeeb PCB mounted in the Bottom Enclosure of the case](Images/3D_Printed_Case/Assembly/3D_Case_AS-38.jpg)

   - Next, take the switch plate and carefully align it with the bottom enclosure, ensuring that the push button section on the switch plate is properly aligned with the push buttons on the top side of the Protokeeb PCB.

   ![View of the Switch Plate push button area and the Protokeeb PCB push button alignment](Images/3D_Printed_Case/Assembly/3D_Case_AS-67.jpg)

   - Insert five M2.5x10mm CSK Philips screws/bolts into their designated holes on the switch plate and fasten them using a Philips screwdriver.
   - Check for any visible gaps between the bottom enclosure and the switch plate. Minor gaps may appear if the threaded brass inserts were not properly installed in their respective holes.
   - After completing the test fit, disassemble the case by removing the screws and taking out the Protokeeb PCB.

![3D Printed Case Test Fitting](Images/3D_Printed_Case/Assembly/3D_Case_AS-35.jpg)

5. Install Switches:

   - Insert 16 Cherry MX-compatible switches into the switch plate.
     > Ensure correct orientation — the switch's LED cutout/window should face downward, as the Protokeeb PCB uses south-facing LEDs.

![Switch placement in Protokeeb Switch Plate-1](Images/3D_Printed_Case/Assembly/3D_Case_AS-43.jpg)

![Switch placement in Protokeeb Switch Plate-2](Images/3D_Printed_Case/Assembly/3D_Case_AS-44.jpg)

![Top View of Switch Plate with all the switches mounted](Images/3D_Printed_Case/Assembly/3D_Case_AS-47.jpg)

6. Solder the PCB:

   - Align the Protokeeb PCB onto the mounted switches and solder each pin.
     > No screws are required to mount the PCB—it is secured via the soldered switches.

![Bottom View of Switch Plate with all the switches mounted](Images/3D_Printed_Case/Assembly/3D_Case_AS-48.jpg)

![Protokeeb PCB switches Soldering Stage](Images/3D_Printed_Case/Assembly/3D_Case_AS-50.jpg)

![Protokeeb PCB with Soldered switches](Images/3D_Printed_Case/Assembly/3D_Case_AS-52.jpg)

![Protokeeb PCB switches solder joints closeup](Images/3D_Printed_Case/Assembly/3D_Case_AS-63.jpg)

7. Test Mechanical Keys (Optional but Recommended)

   - Flash QMK firmware on the Protokeeb MCU, to test the soldered switches.

     1. Download the [protokeeb_rev1_via.uf2](https://github.com/atechofficials/protokeeb/tree/master/Firmware/QMK) file from the Firmware/QMK folder.

     2. Enter bootloader mode by holding the BOOT button (on the bottom of the Protokeeb Rev1 PCB) and plugging the device into your computer via USB-C.

     3. A new drive called RPI-RP2 will appear.

     4. Copy the .uf2 file to the RPI-RP2 drive.

     5. Open https://usevia.app/ in your browser.

     6. Click **Authorize device** and select **Protokeeb**.

     ![Protokeeb Keyboard with Sandwich Case](Images/Software_Images/Via_App_1.png)

     7. Go to the Test section (Stethoscope icon).

     ![Protokeeb Keyboard with Sandwich Case](Images/Software_Images/Via_App_2.png)

     8. Press each key to verify it’s registered.

   - If all keys function properly, unplug the device and continue with the assembly.

![Protokeeb Key Testing](Images/3D_Printed_Case/Assembly/3D_Case_AS-60.jpg)

8. Final case assembly:

   - Align the fully assembled stack (switch plate + keys + soldered PCB) and insert it into the bottom enclosure.
   - Insert five M2.5x10mm CSK Philips screws/bolts into their designated holes on the switch plate and fasten them using a Philips screwdriver.
   - Mount the encoder knob on the encoder shaft and tighten it using its set screw and a flat-head screwdriver.

![Fully Assembled Protokeeb with 3D Printed Case](Images/3D_Printed_Case/Assembly/3D_Case_AS-81.jpg)

9. Add Rubber Feet (Optional):

   - Remove four 7.5mm diameter rubber/silicone feet from the adhesive sheet.
   - Stick them into the circular recesses on the bottom of the case.

![Protokeeb Case Rubber Feet Placement](Images/3D_Printed_Case/Assembly/3D_Case_AS-75.jpg)

![Protokeeb Case with Rubber Feet Installed](Images/3D_Printed_Case/Assembly/3D_Case_AS-79.jpg)

10. Attach Keycaps (Optional):

    - Press a keycap onto each switch stem, aligning them according to your preferred layout.

> Congratulations! Your Protokeeb is now fully assembled and ready to use. Enjoy your custom keyboard!

![Protokeeb Keyboard with 3D Printed Case](Images/KB_Images/Protokeeb_3D-12.jpg)

> For any questions or issues during assembly, please open an issue on GitHub.

</details>

</details>

<details>
<summary>PCB Rev 1.1</summary>

Work-in-progress...

</details>
