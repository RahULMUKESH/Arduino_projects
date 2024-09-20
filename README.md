RFID Access Control with Servo Lock
This Arduino project implements an RFID-based access control system that operates a servo motor to unlock a mechanism when a valid RFID card is presented. The system reads the UID of the RFID card and allows access only if the card matches predefined UIDs.

Components Required
Arduino board (e.g., Uno, Nano)
RFID reader (MFRC522)
Servo motor (SG90)
RFID tags/cards
Jumper wires
Breadboard (optional)
Features
Reads RFID card UIDs and checks for authorized access.
Controls a servo motor to simulate locking and unlocking.
Provides feedback via the Serial Monitor to indicate access status.
Code Explanation
Libraries Used:

SPI.h: Enables communication with the RFID reader.
MFRC522.h: Controls the MFRC522 RFID reader.
Servo.h: Controls the servo motor.
Pin Configuration:

SS_PIN: Slave select pin for the RFID reader.
RST_PIN: Reset pin for the RFID reader.
Setup Function:

Initializes the servo and positions it to the locked position.
Initializes serial communication and the SPI bus.
Initializes the RFID reader and prompts the user to present an RFID card.
Loop Function:

Continuously checks for new RFID cards.
Reads the UID of the presented card.
Displays the UID in the Serial Monitor.
Compares the UID with authorized UIDs (modifiable in the code).
If a match is found, the servo unlocks (moves to 0 degrees) for 5 seconds, then locks again (moves to 180 degrees).
If no match is found, the servo remains locked, and an "Access denied" message is displayed.
Setup Instructions
Wiring:

Connect the RFID reader to the Arduino (refer to your RFID module documentation for specific pin connections).
Connect the servo motor to pin 3.
Upload the Code:

Copy and paste the provided Arduino code into the Arduino IDE.
Upload the sketch to your Arduino board.
Run the Project:

Open the Serial Monitor to view access status and UID readings.
Present an RFID card to test access.
