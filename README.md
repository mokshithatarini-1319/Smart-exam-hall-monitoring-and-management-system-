# Smart Exam Hall Monitoring and Management System

## Project Overview

The Smart Exam Hall Monitoring and Management System is an embedded systems project developed using the LPC2148 microcontroller. The main aim of this project is to automate examination timing, monitor room temperature, and provide real-time examination status indications.

The system integrates an RTC (Real-Time Clock), 16x2 LCD, 4x4 matrix keypad, LM35 temperature sensor, two multiplexed 7-segment displays, LEDs, switches, and a buzzer.

It helps invigilators manage examination schedules, monitor the remaining examination time, and maintain environmental awareness while reducing manual intervention and timing errors.

## Objectives

- Display the current date, time, and room temperature on an LCD.
- Configure examination duration using a keypad.
- Implement an automatic examination countdown timer.
- Display the remaining examination time using two 7-segment displays.
- Provide visual alerts through Green, Yellow, and Red LEDs.
- Enable password-protected configuration.
- Implement Pause and Resume functionality.
- Automatically record examination start and end times using the RTC.

## Key Features

- **Real-Time Clock:** Displays the current date and time.
- **Password Protection:** Secures examination configuration settings.
- **Examination Countdown:** Automatically tracks the remaining examination time.
- **7-Segment Display:** Displays the remaining time in minutes.
- **LED Alert System:** Indicates examination status using three different LEDs.
- **Temperature Monitoring:** Measures room temperature using the LM35 sensor.
- **Pause/Resume:** Controls the countdown using external interrupts.
- **Buzzer Alert:** Indicates when the examination time reaches zero.
- **Automatic Time Logging:** Records examination start and end times.

## Hardware Requirements

| Component | Purpose |
|---|---|
| LPC2148 Microcontroller | Main controller |
| 16x2 LCD | Displays time and temperature |
| 4x4 Matrix Keypad | User input and configuration |
| RTC | Real-time clock and event timing |
| LM35 Sensor | Room temperature monitoring |
| Seven-Segment Displays | Remaining examination time |
| LEDs | Examination status indication |
| Switches | External interrupt control |
| Buzzer | Examination completion alert |
| USB-UART Converter / DB-9 Cable | Programming and communication |

## Software Requirements

- Embedded C Programming
- Flash Magic

## Working Principle

### 1. Normal Monitoring Mode
The LCD continuously displays the current date, time, and room temperature obtained from the RTC and LM35 sensor.

### 2. Secure Configuration Mode
The invigilator uses Switch 1 (External Interrupt 0) to enter configuration mode. The system requests an administrator password through the keypad. After successful authentication, the invigilator can configure the RTC date and time, examination start time, and examination duration.

### 3. Examination Countdown
When the examination starts, the RTC records the start time and the countdown timer begins. The LCD displays the current time, temperature, and remaining examination time. Two multiplexed 7-segment displays show the remaining time in minutes.

### 4. LED Alert Indication

| LED | Condition |
|---|---|
| Green LED | More than 10 minutes remaining |
| Yellow LED | Final 10 minutes |
| Red LED | Last 1 minute |

When the countdown reaches zero, the buzzer activates to indicate the end of the examination.

### 5. Temperature Monitoring
The LM35 sensor continuously monitors room temperature, and the measured temperature is displayed on the LCD.

### 6. Pause and Resume
Switch 2 (External Interrupt 1) provides Pause/Resume functionality. Pressing it once pauses the countdown, and pressing it again resumes the timer from where it stopped.

### 7. Automatic Time Recording
The RTC is used to record the examination start and end times for administrative verification and documentation.

## System Architecture

The LPC2148 microcontroller acts as the central controller and interfaces with the RTC, LCD, keypad, LM35 temperature sensor, 7-segment displays, LEDs, switches, and buzzer.

## Project Outcome

The project provides an automated and user-friendly solution for examination hall monitoring. It combines examination scheduling, countdown management, temperature monitoring, visual alerts, interrupt-based controls, and automatic time recording in a single embedded system.

## Skills Demonstrated

- Embedded C Programming
- LPC2148 Microcontroller
- Microcontroller Interfacing
- RTC Interfacing
- LCD and Keypad Interfacing
- Sensor Interfacing
- External Interrupts
- Timer and Countdown Implementation
- Seven-Segment Display Interfacing

## Author

Developed as an academic embedded systems project.
