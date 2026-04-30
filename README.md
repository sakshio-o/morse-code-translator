# Whispers in Morse

> Encrypting and Decrypting Messages using Arduino

![Arduino](https://img.shields.io/badge/Arduino-UNO-blue?style=flat-square\&logo=arduino)
![Embedded](https://img.shields.io/badge/System-Morse%20Translator-green?style=flat-square)
![License](https://img.shields.io/badge/License-MIT-yellow?style=flat-square)

---

## Overview

This project implements a **Morse Code Translator System** using an Arduino microcontroller that enables communication using **dot (.) and dash (-) signals**.

The system:

* Accepts Morse input via **push buttons**
* Converts it into **text**
* Displays output on an **I2C LCD**
* Provides **audio feedback using a speaker**

It is specifically designed as an **assistive communication tool for speech-impaired individuals** and for **emergency communication scenarios**.

---

## Key Idea

> Minimal input → Intelligent decoding → Multi-modal output (Text + Audio)

---

## Project Preview

###  System Architecture

![System Architecture](images/system_architecture.png)

###  Circuit Diagram

![Circuit Diagram](images/circuit.png)

###  Prototype

![Prototype](images/prototype.png)

###  Output Example

![Output](images/output.png)

---

## Features

*  Real-time Morse code decoding
*  Dual input system (Dot / Dash buttons)
*  LCD text output
*  Audio feedback for each input
*  Custom Morse code system (unique patterns + shortcut words)
*  Assistive communication support

---

## Methodology

### 1. Input System

* Two push buttons:

  * Dot (.)
  * Dash (-)
* Debouncing applied for accurate input detection

---

### 2. Signal Processing

* Inputs stored as sequences of dots and dashes
* Timing used to detect:

  * Character end → 1.5 sec pause
  * Word end → 3 sec pause

---

### 3. Decoding Logic

* Morse sequence matched using **predefined lookup table**
* Supports:

  * Alphabets (A–Z)
  * Numbers (0–9)
  * Custom shortcut words (YES, NO, HELP)

---

### 4. Output Handling

* LCD displays decoded text
* Speaker provides audio cues
* Optional speech using Talkie library

---

### 5. Error Handling

* Invalid sequences → replaced with `?`
* Errors logged via Serial Monitor

---

## System Workflow

```id="flow123"
Button Input
   ↓
Signal Detection
   ↓
Morse Sequence Formation
   ↓
Lookup Table Matching
   ↓
Decoded Character
   ↓
LCD Display + Audio Output
```

---

## Hardware Requirements

* Arduino UNO
* I2C LCD (16x2)
* Push Buttons (x2)
* Speaker / Buzzer
* Breadboard
* Resistors
* Jumper Wires

---

## Software Requirements

* Arduino IDE
* Libraries:

  * LiquidCrystal_I2C
  * Wire
  * Talkie

---

## Pin Configuration

| Component   | Pin |
| ----------- | --- |
| Dot Button  | D2  |
| Dash Button | D3  |
| Speaker     | D4  |
| LCD SDA     | A4  |
| LCD SCL     | A5  |

---

## Setup Instructions

### 1. Clone Repository

```bash id="clone123"
git clone https://github.com/YOUR_USERNAME/morse-code-translator.git
cd morse-code-translator
```

---

### 2. Install Dependencies

* Install Arduino IDE
* Add required libraries

---

### 3. Upload Code

* Open `main.ino`
* Select Arduino UNO
* Upload

---

## Usage

| Action            | Result           |
| ----------------- | ---------------- |
| Press Dot Button  | Adds "."         |
| Press Dash Button | Adds "-"         |
| Pause 1.5 sec     | Decode character |
| Pause 3 sec       | Add space        |

---

## Example

Input:

```id="ex123"
... --- ...
```

Output:

```id="ex456"
SOS
```

---

## Applications

* Assistive communication for speech-impaired individuals
* Emergency communication in remote areas
* Silent communication environments
* Secure encoded messaging

---

## Advantages

* Simple and easy to use
* Cost-effective system
* Works without internet
* Reliable in emergency conditions

---

## Limitations

* Requires learning Morse code
* Slower input speed
* No intelligent error correction

---

## Future Scope

* Wearable Morse input device
* Multilingual output system
* AI-based prediction and correction
* Mobile app integration

---

## Description

> *Developed an Arduino-based Morse code translator that converts dot-dash inputs into real-time text and audio output, enabling assistive and emergency communication.*

---

## Authors

* Kishor Jawale
* Sakshi Jadhav
* Chaitrali Deshpande
* Siddhi Gadekar
  
---

## License

MIT License

---

## Copyright

© 2025 Whispers in Morse Project Team. All rights reserved.  
The project titled *"Whispers in Morse: Encrypting and Decrypting Messages"* has been successfully copyrighted.
