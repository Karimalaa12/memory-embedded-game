# memory-embedded-game
Memory Game System — Embedded Systems Project

Demo video: https://drive.google.com/file/d/1blTCUlHgotf3x-XPJuPv4F1-OHO2EyTj/view?usp=drive_link

Overview

Designed and developed a multi-mode embedded Memory Game system using the ATmega328P microcontroller (Arduino Uno platform) programmed in Embedded C. The system supports single-player and multiplayer gameplay modes with real-time interaction, persistent score storage, audio/visual feedback, and power-efficient operation.

The project was implemented using low-level AVR programming techniques including timers, interrupts, EEPROM management, GPIO control, I2C communication, and finite state machine architecture.

Features
Game Modes
1. Solo Sprint
System generates LED sequences
Player repeats the sequence using push buttons
Difficulty increases progressively:
Longer sequences
Faster LED timing
2. Synchronous Duel
Two players compete simultaneously
Both players replicate the displayed sequence
Winner determined by:
Accuracy
Response speed
3. Challenger Mode
One player creates a custom sequence
Second player attempts replication
Includes “proof” mechanism:
Challenger must re-enter the original sequence if opponent fails
Hardware Components
ATmega328P / Arduino Uno
8 Push Buttons
4 LEDs
16×2 LCD Display with I2C Interface
Passive Buzzer
EEPROM Internal Memory
Embedded Systems Concepts Implemented
Real-Time System Design
Non-blocking firmware architecture
Millisecond system scheduler using Timer1
Concurrent input handling for multiplayer interaction
Interrupts
Pin Change Interrupts (PCINT)
Timer Interrupts
Interrupt-safe shared variable handling
Finite State Machine (FSM)

Implemented FSM architecture for:

Main menu navigation
Gameplay logic
Sequence display
Input validation
Score handling
Sleep/wake management
Timer Applications
Timer1
1 ms system tick (millis)
Real-time scheduling
Timer2
Passive buzzer tone generation
CTC mode waveform generation
Software Features
Input Management
Software button debouncing
Circular buffer input queues
Multi-player simultaneous input processing
LCD Interface
I2C communication using AVR TWI hardware
HD44780 LCD driver implementation
Custom LCD characters
EEPROM Storage
Persistent high-score saving
EEPROM wear reduction using update operations
Magic-number validation system
Power Optimization
Sleep mode implementation
Automatic inactivity timeout
LCD backlight and LED shutdown during idle state
System Architecture

The project was developed using a modular driver-based architecture.

Main Modules
main.c → system initialization and main FSM
input.c/h → button queue and interrupt handling
lcd.c/h → I2C LCD driver
buzzer.c/h → Timer2 audio driver
game_common.c → shared utilities and timing logic
mode1.c/h → Solo Sprint mode
mode2.c/h → Duel mode
mode3.c/h → Challenger mode
eeprom.h → persistent storage management
Technical Skills Demonstrated
Embedded C Programming
AVR Register-Level Programming
Real-Time Embedded Systems
Interrupt Handling
Timer Configuration
GPIO Programming
EEPROM Management
I2C/TWI Communication
Finite State Machines
Modular Firmware Design
Non-Blocking Embedded Architecture
Software Debouncing
Concurrent Event Processing
Development Environment
Microcontroller: ATmega328P
Platform: Arduino Uno
Language: Embedded C
Toolchain: AVR-GCC
Libraries:
avr/io.h
avr/interrupt.h
avr/eeprom.h
avr/sleep.h


<img width="1009" height="661" alt="image" src="https://github.com/user-attachments/assets/09fe1820-9545-4238-8fc0-a9227f493632" />
