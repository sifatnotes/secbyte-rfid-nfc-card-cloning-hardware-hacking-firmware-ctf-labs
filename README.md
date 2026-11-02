# secbyte-rfid-nfc-card-cloning-hardware-hacking-firmware-ctf-labs
A practical collection of cybersecurity CTF labs covering RFID/NFC contactless card cloning (MIFARE Classic, TapTrace, access badge forensics), hardware reverse engineering (controller teardowns, EEPROM memory analysis, logic analyzers, SPI/I2C protocol sniffing), and embedded firmware exploitation (secure boot bypass, bootloader extraction).
# RFID/NFC Card Cloning, Hardware Reverse Engineering, Bus Analysis & Firmware Exploitation CTF Labs

Welcome to the **RFID/NFC Card Cloning, Hardware Reverse Engineering, Bus Analysis & Firmware Exploitation CTF Lab Collection**. This repository serves as an organized, searchable catalog of practical cybersecurity labs hosted on Learn SecByte.

This collection focuses on physical access card security, low-level hardware communication protocol analysis, and embedded system reverse engineering—spanning **RFID/NFC Contactless Security & Badge Forensics (MIFARE Classic cloning, TapTrace tag analysis, badge access forensics, field basics)**, **Hardware Security & Controller Teardowns (Access controller lab, EEPROM analysis, lost access badges)**, **Serial Protocol & Bus Traffic Analysis (Logic analyzer basics, I2C decoding, SPI bus investigation)**, and **Embedded Firmware Exploitation & Secure Boot (Bootloader secret dumps, trust chain breakdowns)**.

---

## Lab Collection Index

### 1. RFID/NFC Card Cloning & Physical Access Forensics
* **RFID Fundamentals: The Lost Access Badge**  
  *Lab Link:* [https://learn.secbyte.org/ctf/rfid-fundamentals-the-lost-access-badge](https://learn.secbyte.org/ctf/rfid-fundamentals-the-lost-access-badge)  
  *Focus:* Fundamentals of radio frequency identification (125 kHz vs. 13.56 MHz), interrogating lost access badges, reading raw UID streams, and mapping facility codes.

* **MIFARE Classic: The Clone in the Reader**  
  *Lab Link:* [https://learn.secbyte.org/ctf/mifare-classic-the-clone-in-the-reader](https://learn.secbyte.org/ctf/mifare-classic-the-clone-in-the-reader)  
  *Focus:* Cracking MIFARE Classic Crypto-1 cipher keys using nested/hardnested attacks, cloning card sector dumps to magic UID cards (UID Gen1a/Gen2), and analyzing reader validation.

<Image src="image_agent_tag_8510669015541547940" alt="Physical access control system diagram showing proximity reader, controller, and electric strike door lock" caption="Physical Access Control System Architecture & Card Reader Topology" />

---

* **TapTrace: NFC Tag Analysis**  
  *Lab Link:* [https://learn.secbyte.org/ctf/taptrace-nfc-tag-analysis](https://learn.secbyte.org/ctf/taptrace-nfc-tag-analysis)  
  *Focus:* Inspecting NTAG/MIFARE Ultralight tags, parsing NDEF record payloads (URI, Text, MIME types), identifying unprotected OTP bytes, and analyzing tag lock flags.

* **RFID Card Cloning: Badge Access Forensics**  
  *Lab Link:* [https://learn.secbyte.org/ctf/rfid-card-cloning-badge-access-forensics](https://learn.secbyte.org/ctf/rfid-card-cloning-badge-access-forensics)  
  *Focus:* Performing post-incident forensic analysis of cloned access cards, comparing legitimate vs. cloned card timing characteristics, and auditing physical reader access logs.

* **NFC Taproom: Field Basics & Card Cloning Indicators**  
  *Lab Link:* [https://learn.secbyte.org/ctf/nfc-taproom-field-basics-card-cloning-indicators](https://learn.secbyte.org/ctf/nfc-taproom-field-basics-card-cloning-indicators)  
  *Focus:* Measuring RF field strength parameters, detecting active anti-collision anomalies, and identifying indicators of card emulation attacks using Proxmark3/ChameleonUltra.

### 2. Hardware Reverse Engineering & Memory Analysis
* **Hardware Reverse Engineering: Access Controller Lab**  
  *Lab Link:* [https://learn.secbyte.org/ctf/hardware-reverse-engineering-access-controller-lab](https://learn.secbyte.org/ctf/hardware-reverse-engineering-access-controller-lab)  
  *Focus:* Teardown and PCB reverse engineering of physical access control units (ACUs), tracing circuit board traces, identifying component ICs, and locating debug header pinouts (JTAG/UART).

* **EEPROM Memory Analysis: Corrupted Badge Reader**  
  *Lab Link:* [https://learn.secbyte.org/ctf/eeprom-memory-analysis-corrupted-badge-reader](https://learn.secbyte.org/ctf/eeprom-memory-analysis-corrupted-badge-reader)  
  *Focus:* Dumping SPI/I2C EEPROM chip memory binaries (`24Cxx`/`25Cxx`), analyzing persistent configuration data structures, recovering stored master access PINs, and patching corrupt byte blocks.

### 3. Serial Protocol & Hardware Bus Analysis
* **Logic Analyzer Essentials: Serial Signals Under the Microscope**  
  *Lab Link:* [https://learn.secbyte.org/ctf/logic-analyzer-essentials-serial-signals-under-the-microscop](https://learn.secbyte.org/ctf/logic-analyzer-essentials-serial-signals-under-the-microscop)  
  *Focus:* Capturing raw hardware voltage waveforms with Saleae/PulseView logic analyzers, measuring baud rates, decoding UART serial communications, and isolating command packets.

<Image src="image_agent_tag_8510669015541549927" alt="I2C bus protocol diagram showing master controller connected to multiple slave peripherals with SDA and SCL pullup resistors" caption="I2C Serial Communication Bus Architecture & Signal Routing" />

---

* **I2C Communication Analysis: Decoding Peripheral Bus Traffic**  
  *Lab Link:* [https://learn.secbyte.org/ctf/i2c-communication-analysis-decoding-peripheral-bus-traffic](https://learn.secbyte.org/ctf/i2c-communication-analysis-decoding-peripheral-bus-traffic)  
  *Focus:* Sniffing Inter-Integrated Circuit (I2C) serial clock (SCL) and serial data (SDA) lines, decoding 7-bit slave addresses, analyzing read/write transactions, and reconstructing sensor telemetry.

* **SPI Bus Investigation**  
  *Lab Link:* [https://learn.secbyte.org/ctf/spi-bus-investigation](https://learn.secbyte.org/ctf/spi-bus-investigation)  
  *Focus:* Inspecting Serial Peripheral Interface (SPI) four-wire buses (MISO, MOSI, SCK, CS), decoding high-speed SPI Flash memory reads, and extracting firmware images in real-time.

### 4. Embedded Firmware Exploitation & Secure Boot
* **Firmware Dump Extraction: From Bootloader to Secrets**  
  *Lab Link:* [https://learn.secbyte.org/ctf/firmware-dump-extraction-from-bootloader-to-secrets](https://learn.secbyte.org/ctf/firmware-dump-extraction-from-bootloader-to-secrets)  
  *Focus:* Extracting raw flash dumps via U-Boot command shells or programmer hardware (CH341A), carving file systems (`binwalk`), and extracting hardcoded cryptographic keys and root password hashes.

* **Secure Boot Bypass: Trust Chain Breakdown**  
  *Lab Link:* [https://learn.secbyte.org/ctf/secure-boot-bypass-trust-chain-breakdown](https://learn.secbyte.org/ctf/secure-boot-bypass-trust-chain-breakdown)  
  *Focus:* Analyzing hardware root-of-trust (RoT) verification stages, identifying cryptographic signature validation flaws in stage 1 bootloaders (SPL/FSBL), and achieving arbitrary code execution during boot.

---

## Learning Path

### Path A: RFID/NFC Card Cloning & Access Control Specialist
1. **RFID & NFC Fundamentals:** Start with [RFID Fundamentals](https://learn.secbyte.org/ctf/rfid-fundamentals-the-lost-access-badge) and [TapTrace: NFC Tag Analysis](https://learn.secbyte.org/ctf/taptrace-nfc-tag-analysis).
2. **Card Cloning & Forensics:** Master card exploitation via [MIFARE Classic: The Clone in the Reader](https://learn.secbyte.org/ctf/mifare-classic-the-clone-in-the-reader), [RFID Card Cloning Forensics](https://learn.secbyte.org/ctf/rfid-card-cloning-badge-access-forensics), and [NFC Taproom](https://learn.secbyte.org/ctf/nfc-taproom-field-basics-card-cloning-indicators).

### Path B: Hardware Reverse Engineering & Protocol Analyst
1. **PCB & Memory Analysis:** Teardown hardware in [Hardware Reverse Engineering: Access Controller Lab](https://learn.secbyte.org/ctf/hardware-reverse-engineering-access-controller-lab) and dump chips via [EEPROM Memory Analysis](https://learn.secbyte.org/ctf/eeprom-memory-analysis-corrupted-badge-reader).
2. **Bus Sniffing:** Master signal analysis in [Logic Analyzer Essentials](https://learn.secbyte.org/ctf/logic-analyzer-essentials-serial-signals-under-the-microscop), [I2C Communication Analysis](https://learn.secbyte.org/ctf/i2c-communication-analysis-decoding-peripheral-bus-traffic), and [SPI Bus Investigation](https://learn.secbyte.org/ctf/spi-bus-investigation).

### Path C: Embedded Firmware & Secure Boot Engineer
1. **Firmware Carving & Dumping:** Extract image files in [Firmware Dump Extraction](https://learn.secbyte.org/ctf/firmware-dump-extraction-from-bootloader-to-secrets).
2. **Trust Chain Exploitation:** Break hardware secure boot in [Secure Boot Bypass: Trust Chain Breakdown](https://learn.secbyte.org/ctf/secure-boot-bypass-trust-chain-breakdown).

---

## How to Use the Labs

1. Select a practice scenario from the **Lab Collection Index**.
2. Click the corresponding direct link to launch the exercise environment hosted on Learn SecByte.
3. Review scenario directives, Proxmark3 trace dumps (`.pm3`), pulse view capture files (`.sr`), or raw flash memory binaries (`.bin`).
4. Crack MIFARE sector keys, decode SPI/I2C logic analyzer waveforms, extract embedded file systems using `binwalk`, or bypass bootloader trust verification to capture flags.

---

## Target Audience

* **Hardware Pentesters & Embedded Security Researchers:** Perform PCB teardowns, analyze JTAG/UART interfaces, decode I2C/SPI bus traffic, and bypass secure boot chains.
* **Physical Security Auditors & Systems Integrators:** Evaluate card cloning risks across MIFARE/EM4100 badge readers, inspect door controller hardware, and audit access badge logs.
* **Firmware Engineers & DevSecOps Teams:** Hardened embedded Linux build pipelines, secure bootloader verification steps, and prevent memory dump secrets leakage.
* **Cybersecurity Students:** Acquire practical hands-on experience in short-range RF security, hardware bus analysis with logic analyzers, and embedded system reverse engineering.

---

## Disclaimer

All lab links provided in this repository direct to official training environments hosted on Learn SecByte. All materials and exercises are provided strictly for educational purposes, defensive skill building, and authorized security research. Unauthorized scanning, signal replay, card cloning, or physical hardware tampering against real-world systems without explicit permission is strictly prohibited.
