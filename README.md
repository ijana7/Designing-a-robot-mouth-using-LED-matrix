# Designing a Robot Mouth using LED Matrix

## Introduction
This project demonstrates how to design a robot mouth using an LED matrix. The LED matrix is controlled by an Arduino board and the MAX7219 chip, which allows for easy control of the individual LEDs. The project includes a simple animation of a smiling face on the LED matrix.

## the link
https://wokwi.com/projects/318864638990090834 (with explanation)


<img width="1710" alt="‏لقطة الشاشة ١٤٤٦-٠١-٠٩ في ٢ ٤٨ ٥٠ ص" src="https://github.com/user-attachments/assets/8a63f355-b982-44ea-b13d-4c5de099b2e8">


## Hardware Requirements
- Arduino board (e.g., Arduino Uno, Arduino Nano)
- MAX7219 LED matrix driver chip
- 4x4 LED matrix
- Jumper wires
- Breadboard (optional)

## Circuit Diagram
The circuit diagram for this project is as follows:

```
Arduino   MAX7219
  CLK  ->   CLK
  DIN  ->   DIN
  CS   ->   CS
```
## Code Explanation
The code provided in the introduction includes the following functions:

1. `shiftAll(byte send_to_address, byte send_this_data)`: This function sends data to all the segments of the LED matrix.
2. `setup()`: This function initializes the Arduino pins and sets up the LED matrix.
3. `loop()`: This function clears the LED matrix and then calls the `drawLargeSmiley()` function to display a large smiley face on the LED matrix.
4. `drawLargeSmiley()`: This function draws the eyes and mouth of the smiley face on the LED matrix.
5. `set_pixel(uint8_t x, uint8_t y, uint8_t mode)`: This function sets the state of a single pixel on the LED matrix.
6. `safe_pixel(uint8_t x, uint8_t y, uint8_t mode)`: This function checks the validity of the pixel coordinates before setting the pixel state.
7. `clear()`: This function clears the LED matrix by turning off all the pixels.
8. `show()`: This function updates the LED matrix with the contents of the `fb` array.

## Usage
1. Connect the Arduino board and the MAX7219 chip according to the circuit diagram.
2. Upload the provided code to the Arduino board.
3. The LED matrix will display a large smiley face, which will be updated every 500 milliseconds.

## Customization
You can customize the design of the robot mouth by modifying the `drawLargeSmiley()` function. You can change the position and shape of the eyes and mouth, or even add additional features like eyebrows or a nose.

## References
- [MAX7219 Datasheet](https://datasheets.maximintegrated.com/en/ds/MAX7219-MAX7221.pdf)
- [Arduino SPI Library Documentation](https://www.arduino.cc/en/Reference/SPI)
