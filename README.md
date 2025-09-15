## 📌 Aim
Design and implementation of an "Automated Toll Collection System" using RFID technology and LPC2148 ARM7 microcontroller.

## 🛠️ Hardware Requirements
- LPC2148 Microcontroller
- RFID Reader + RFID Cards
- 20x4 LCD Display
- 4x4 Matrix Keypad
- AT24C256 EEPROM
- DC Motor (for gate control)
- GP2D12 Distance Sensor
- Switches (for recharge/manual mode)
- USB to UART Converter

## 💻 Software Requirements
- Embedded C
- Keil µVision (ARM Compiler)
- Flash Magic (for flashing code)

## 🔄 Implementation Steps
1. Test each peripheral separately:
   - LCD → display constants & strings
   - Keypad → input characters/numbers
   - UART → transmit/receive using interrupts
   - RFID → read card number via UART0
2. Integrate modules:
   - Sensor detects vehicle (10–15 cm range)
   - Display welcome message on LCD
   - RFID card number checked with stored database (EEPROM)
   - Deduct balance → open gate (DC motor forward)
   - Vehicle passes → close gate (DC motor reverse)
   - Switch1 → recharge account manually
   - Switch2 → manual toll deduction if RFID fails

## 📡 RFID Reader Output Format
For example, card number `12345678` →  
