# Audio Streaming Project with STM32F407 and ESP32

## Project Overview
Welcome to my audio streaming project! This project involves capturing audio through a microphone, processing the data on the STM32F407 Discovery board, and transmitting it to a PC using the ESP32 integrated Bluetooth chip for playback.

## Table of Contents
1. [Project Goals](#project-goals)
2. [Components Used](#components-used)
3. [System Architecture](#system-architecture)
4. [Setup and Configuration](#setup-and-configuration)
5. [Implementation Details](#implementation-details)
6. [Audio Processing](#audio-processing)
7. [PC Audio Playback](#pc-audio-playback)
8. [Testing and Debugging](#testing-and-debugging)
9. [Conclusion](#conclusion)

## Project Goals
- Capture audio data from a microphone.
- Process the audio data using STM32F407.
- Transmit the processed audio to a PC via Bluetooth (ESP32).
- Enable playback of audio on the PC.

## Components Used
- **Microcontroller**: STM32F407 Discovery Board
- **Bluetooth Module**: ESP32 (integrated)
- **Microphone**: Compatible with both analog and digital formats
- **Software**:
  - FreeRTOS (for task management)
  - STM32CubeMX (for peripheral configuration)
  - Development Environment: [Your IDE of Choice]

## Setup and Configuration
1. **STM32F407 Discovery Board**:
   - Use STM32CubeMX to configure peripherals.
   - Enable ADC for analog microphone or I2S for digital microphone.

2. **ESP32 Configuration**:
   - Set up the ESP32 for Bluetooth communication.
   - Use the Arduino IDE or ESP-IDF for programming.

3. **FreeRTOS Setup**:
   - Download and integrate FreeRTOS into your STM32 project.
   - Create tasks for audio capture, processing, and transmission.

## Implementation Details
- **Microphone Connection**:
  - Connect the microphone to the STM32F407 board (analog or digital).
  - Use appropriate circuitry for analog microphones (e.g., op-amps, filters).

- **Audio Capture**:
  - Implement a task to continuously sample audio data.
  - Store captured audio in a buffer for processing.

- **Bluetooth Communication**:
  - Establish a Bluetooth Serial connection between the STM32 and PC.
  - Use UART to send processed audio data over Bluetooth.

## Audio Processing
- Implement basic audio processing algorithms (e.g., filtering, gain control) in a dedicated task.
- Process the audio data before sending it to the PC.

## PC Audio Playback
- Create a simple application on your PC (using Python) to receive audio data via Bluetooth.
- Use libraries such as PyAudio to play the received audio.

## Testing and Debugging
- Test each component separately:
  - Verify microphone functionality and audio capture.
  - Test Bluetooth communication with the PC.
  - Check audio playback on the PC.

## Conclusion
This project demonstrates the integration of audio capture, processing, and Bluetooth transmission using STM32F407 and ESP32. Future enhancements could include adding advanced audio processing features or improving the user interface on the PC side.

## Contact
For questions or suggestions, feel free to reach out!

## References
- [STM32 ADC Documentation](https://www.st.com/en/embedded-software/stm32-audio-application.html)
- [ESP32 Bluetooth Setup Guide](https://docs.espressif.com/projects/esp-idf/en/latest/esp32/api-reference/bluetooth/bluedroid/index.html)
- [FreeRTOS Documentation](https://www.freertos.org/)
