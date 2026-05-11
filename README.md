# Tuyyo-Smart-Speaker

**TUYO is a compact, AI-powered voice assistant speaker that was designed and built completely from scratch. It combines custom embedded hardware with modern AI to create a portable assistant that can listen, process speech, and respond in real time.**

<img width="1754" height="2480" alt="imresizer-trical p (1)" src="https://github.com/user-attachments/assets/4b3a1ad5-baac-4630-a411-e30323f6602a" />

## Build Instructions

1. Download or clone this repository.
2. Open the KiCad project from the `PCB/` folder.
3. Review the schematic and PCB layout.
4. Generate or use the included Gerber files for PCB manufacturing.
5. Order the components listed in `BOM.csv`.
6. Assemble the PCB by soldering the ESP32-S3, microphone, amplifier, USB-C, charger, regulator, resistors, capacitors, LED, buttons, and connectors.
7. Place the assembled PCB inside the 3D printed enclosure.
8. Upload the firmware from `Firmware/tuyo_firmware.ino`.
9. Connect the external AI processing system for speech-to-text, AI response generation, and text-to-speech.
10. Power the device using USB-C or a LiPo battery.

## PCB and Schematic

The PCB was designed in KiCad. The `PCB/` folder includes the schematic, PCB layout, and manufacturing files.

## Firmware and AI Integration

The ESP32-S3 firmware initializes Wi-Fi, the I2S microphone, I2S amplifier, buttons, and status output. The ESP32 does not run the full AI model locally. It captures audio and is intended to send it to an external AI system, which handles speech-to-text, response generation, and text-to-speech playback.



# How to use it
-Power the device using a LiPo battery or USB-C connection.

-Ensure the system handling AI processing is connected.

-Speak clearly into the microphone.

-The device captures and processes your voice.

-The AI generates a response.

-The response is played through the speaker.

The interaction is designed to feel natural, similar to existing voice assistants.
# Components used
1. ESP32-WROOM-32 (Main Cintroller)
   -This is the brain of Tuyyo
   - Processes the input from the microphone
   - Sends data to the AI system
   - Receives responsee
   - Controls audio output with amplifier.
   - Handles system Logic and connects all other components.

  2. ICS-43434 I2S Microphone
  - This is a digital microphone used to capture voice output.
  - Convertes sound to digital signals.
  - Sends audio data to ESP32 using I2S protocol
  - Provides clear and noise-resistant audio input.

 3. MAX98357A I2S Audio Amplifier.
    - Recives data from ESP32.
    - Coverts to analog signal.
    - Enables clear audio output.
4. Speaker
   - Converts electrical signals into sound
   - Plays AI-generated responses
  
5. TP4056
   - Charges the battery from Usb-c port.

6. LiPO battery
   - Provides portable power
   - Replaceble
7. AMS1117-3.3 Voltage regulator
   - Converts 5V to 3.3V
   - Supplies power to ESP32 and other components that require 3.3V.
8. CH340C USB to UART.
   - Converts USB signal.
   - Helps in programming the ESP32.
9. USB-C RECEPTABLE
   - Provides 5v power to the system.
   - Allows connection to computer and charger.
10. APA-106-F5
11. FerriteBead
12. Resistors and Capacitors.

    <img width="1284" height="889" alt="Screenshot 2026-04-17 084305" src="https://github.com/user-attachments/assets/e42c2f91-c4f4-4cf0-ae90-35623895073a" />


   # This project was created to explore the connection between hardware engineering and artificial intelligence.
   Rather than relying on existing smart speaker platforms, the goal was to understand and rebuild the entire system from the ground up. That meant designing the PCB, choosing the right components, managing power delivery, and integrating AI-based voice interaction into a working physical product.

   # What makes TUYO unique
-Fully custom-designed PCB

-Integration of AI with embedded systems

-Compact and portable design

-Clear separation of input, processing, and output

-Built from scratch as a complete system

<img width="850" height="805" alt="Screenshot 2026-04-17 125200" src="https://github.com/user-attachments/assets/15edc0f2-3657-40fd-bbad-34810dbc6f88" />

<img width="802" height="598" alt="image" src="https://github.com/user-attachments/assets/a0d0e7c2-f468-4106-bc9b-6969c333d9e0" />

Visit this BOM file for component list- "https://github.com/andaniayan-jpg/Tuyyo-Hackclub/blob/12cad96ed76dfa4e5342a210ed5bca2d6a44b040/pcb/Tuyyo%20all%20the%20gerbers.zip"


