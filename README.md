# [SAC] 🛡️ Shield Anti-Cheat (x64)
![Supported Systems](https://img.shields.io/badge/Supported%20Systems-Windows%2010%2F11-0067b5?logo=windows&logoColor=white)
![Security](https://img.shields.io/badge/Modern-Anti--Cheat-darkred)
![Version](https://img.shields.io/badge/Version-Pre--Beta-009400)

## ℹ️ Overview

Shield Anti-Cheat is a separate program running on client side. But you can still connect it to your servers. You can easily send logs to your VPS, website, or even to a Discord webhook. We tested it on many free and paid cheats. It works for every game engines.

## 🌟 Core Features

- Kernel Detections

- Advanced External Detections

- Advanced Internal Detections

- Advanced Input Detections

- Blacklisted Programs Detections

- Advanced HWID & IP Ban System

- Sending Logs To Your Server

- Configurable

- Well Optimized

## 📂 Project Structure

```
[SAC] Shield Anti-Cheat/
├── Configuration/
│   ├── Configuration.hpp                       # Main anti-cheat settings and limits
│   ├── Logs.hpp                                # Local file logs
│   └── Whitelist.hpp                           # List of safe and trusted system processes
├── Detections/
│   ├── AntiIPBanBypass.hpp                     # Stops players from bypassing IP bans
│   ├── Bans.hpp                                # Logic for banning cheaters
│   ├── BlacklistDetections.hpp                 # Blocks known cheat tools
│   ├── ExternalDetections.hpp                  # Finds external cheats running in Windows
│   ├── HandleHijackingDetections.hpp           # Blocks cheats from handle hijacking
│   ├── Heartbeat.hpp                           # Keeps the anti-cheat alive and checks if it is running
│   ├── InputDetections.hpp                     # Detects fake mouse inputs
│   ├── InternalDetections.hpp                  # Scans game memory for hidden hacks and injected DLLs
│   ├── InternetConnection.hpp                  # Checks connection to the server
│   ├── MicrosoftVulnerableDriverBlocklist.hpp  # Blocks vulnerable drivers used by cheats
│   ├── WindowsMemoryIntegrity.hpp              # Checks if Windows Memory Integrity (HVCI) is active
│   └── WindowsSecureBoot.hpp                   # Checks if Windows Secure Boot is turned on
└── Menu/
    ├── Main.cpp                                # Main entry point that starts all detection loops
    └── Menu.hpp                                # Simple UI code
```
## 📄 Documentation For Developers
**Architecture and mode of operation**
- The system operates entirely on the client-side at the User Mode level. It does not require injecting DLL files into the game process or installing Kernel-mode drivers on the player's computer.

**Implementation Guide**
- 1. Select the version of Anti-Cheat you want to use and install it (We always prefer the latest one)
- 2. Run the installed version of the anti-cheat and configure it according to your needs.

**Supported operating systems and game engines**
- Windows 10 and Windows 11. It operates independently of the game engine used.

**Detection methods and protection modules**
- BlacklistDetections - Identification and immediate blocking of commonly known programs and tools used to manipulate application behavior.
- ExternalDetections - Detection of unauthorized programs running in the system background that attempt to interact with the running game.
- InternalDetections - Real-time protection of the game's internal structure. The module ensures that the game code is not illegally modified or expanded with unapproved elements.
- HandleHijackingDetections - Blocks advanced attempts of illegal takeover of privileges and control over the game by other applications.
- InputDetections - Heuristic analysis of mouse and keyboard input data. Detects artificial movement patterns.
- MicrosoftVulnerableDriverBlocklist - Preventive protection against the exploitation of known system vulnerabilities in drivers.
- WindowsMemoryIntegrity - Verification of the integrity of the operating system kernel memory areas.
- WindowsSecureBoot - Checking the secure boot status of the computer. This guarantees that the player's operating system booted in a trusted manner and was not modified before launching the game itself.
- Heartbeat - A system of mutual verification of activity between the game, anti-cheat, and the server. It prevents attempts to intentionally freeze, slow down, or completely block the protective process.
- InternetConnection - Constant monitoring of the stability and authenticity of the network connection. Protects against artificial manipulation of data packets and intentional induction of network delays for the purpose of cheating.
- Bans - Logic responsible for reading the player's hardware identifiers. Upon detection of an incident, it is responsible for immediately imposing a permanent ban on the given computer.
- AntiIPBanBypass - An additional layer of network protection. It prevents attempts to mask identity and immediately cuts off attempts by banned users to return to the game using advanced methods of changing network parameters.
  
**Data And Logs Export**
- Although SAC operates on the client-side, it offers extensive log export capabilities. Detections, warnings, and errors can be sent directly to VPS Servers, Dedicated web panels Or Discord Channels via Webhook.
