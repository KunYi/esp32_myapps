# ESP32S3 WS2812 LED Test Project

This project demonstrates the control of onboard WS2812 LED on ESP32S3 development boards. Built with ESP-IDF v5.3.1 framework, it showcases basic LED control functionality using GPIO48.

## Hardware Requirements

- ESP32S3 development board with onboard WS2812 LED

## Pin Configuration

- LED Data Pin: GPIO48 (Default pin for onboard WS2812 LED)

## Software Dependencies

- ESP-IDF v5.3.1
- LED Strip Component: espressif/led_strip (v3.0.0)

## Getting Started

1. Install ESP-IDF v5.3.1
2. Clone this repository
3. Connect your development board
4. Build and flash the project:
   ```bash
   get_idf
   idf.py build
   idf.py -p (PORT) flash
   ```

## Important Notes

- The project is specifically designed for development boards with pre-installed WS2812 LED
- Default configuration uses GPIO48 for the onboard LED control

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
