# Upcounter with Dual 7-Segment Displays 🔄️🔄️

Welcome to the repository for a simple yet effective upcounter project utilizing two 7-segment displays for visual output. This project is designed to count up in a sequential manner, demonstrating the basics of digital counting circuits and display interfacing.

## Overview

This circuit uses two 74HC4026B ICs, which are BCD-to-7-segment decoders with a built-in counter, to drive two common cathode 7-segment displays (LSD5161-SC58). Each IC handles one digit of the count, allowing for a two-digit display from 00 to 99.

## Components

- **2x 74HC4026B** - BCD to 7-Segment Decoder/Counter
- **2x 7-Segment Displays (LSD5161-SC58)** - Common Cathode type
- **Resistors (1kΩ)** - For current limiting to each segment of the displays
- **Capacitors (1µF)** - For debouncing the clock input
- **Push Button** - For manual clock input
- **Reset Button** - To reset the counter to 00

## Circuit Diagram

![Schematic_dsd-project_2024-02-25](https://github.com/user-attachments/assets/7f2b508d-9e26-427c-aa0a-45361f340c00)


The above image shows the schematic design of the upcounter with dual 7-segment displays. Here's a brief overview of how it works:

- The clock signal is derived from a push button, which increments the count when pressed.
- The reset button resets both counters to zero.
- Each 74HC4026B IC decodes the BCD output into a 7-segment display format, with one IC driving each display.
- The resistors limit the current to each segment of the displays to prevent damage.
- Capacitors are used for debouncing the push button inputs to ensure clean clock signals.

## How to Use

1. **Assembly:** Construct the circuit as per the schematic diagram provided. Ensure all connections are secure and correct.

2. **Power Supply:** Connect VCC to a 5V power supply and GND to ground. Make sure your power supply can handle the current requirements of the LEDs in the displays.

3. **Operation:**
   - Press the clock button to increment the count. Each press will increase the count by one.
   - Press the reset button to reset the counter back to '00'.

4. **Testing:** Check each segment of the displays to ensure they light up correctly. If any segment does not light, double-check the connections and component orientation.

## Troubleshooting

- **Display not incrementing:** Verify the clock button connection and ensure it's not stuck or shorted. Check the capacitors for proper debouncing.
- **Display showing incorrect numbers:** Ensure the BCD to 7-segment decoding is correct by checking the pin connections from the ICs to the displays.
- **Dim or no light on display:** Check the current limiting resistors; they might be too high or there could be a connection issue.

## Learning Outcomes

- Understanding BCD to 7-segment conversion.
- Basic operation of counters in digital circuits.
- Interfacing digital ICs with display devices.
- Practical application of debouncing in button inputs.

## Contributions

This project is open for contributions. If you have ideas for improvements, additional features, or educational enhancements, feel free to fork this repo and submit a pull request. Examples could be adding automatic counting, integrating with a microcontroller, or improving the reset functionality.

## License

This project is open source under the [MIT License](LICENSE.md). Feel free to use, modify, and distribute as per the terms of the license.
