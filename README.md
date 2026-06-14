# [SAC] Shield Anti-Cheat
![Supported Platform](https://img.shields.io/badge/Supported%20Platform-Windows%2010%2F11-darkred?logo=windows&logoColor=white)
![Security](https://img.shields.io/badge/Security-Anti--Cheat-darkred)
![Version](https://img.shields.io/badge/Version-Beta-darkred)

## Core Features

- Advanced Kernel Detections

- Advanced External Detections

- Advanced Internal Detections

- Advanced Input Detections

- Blacklisted Programs Detections

- Advanced HWID & IP Ban System

- Sending User Logs To Your Console

- Fully Personalized Settings

- Lifetime Fully Free Plan

- Wonderfully Optimized

## Project Structure

```
[SAC] Shield Anti-Cheat/
├── Configuration/
│   ├── Configuration.hpp               # Main anti-cheat settings and limits
│   ├── Logs.hpp                        # Local file logs and Discord Webhook output
│   └── Whitelist.hpp                   # List of safe and trusted system processes
├── Detections/
│   ├── AntiIPBanBypass.hpp             # Stops players from bypassing IP bans
│   ├── Bans.hpp                        # Logic for banning cheaters
│   ├── BlacklistDetections.hpp         # Blocks known cheat tools
│   ├── ExternalDetections.hpp          # Finds external cheats running in Windows
│   ├── HandleHijackingDetections.hpp   # Blocks cheats from stealing program handles
│   ├── Heartbeat.hpp                   # Keeps the anti-cheat alive and checks if it is running
│   ├── InputDetections.hpp             # Detects fake mouse inputs
│   ├── InternalDetections.hpp          # Scans game memory for hidden hacks and injected DLLs
│   ├── InternetConnection.hpp          # Checks connection to the anti-cheat server
│   ├── MicrosoftVulnerableDriverBlocklist.hpp # Blocks dangerous drivers used by cheats
│   ├── WindowsMemoryIntegrity.hpp      # Checks if Windows Memory Integrity (HVCI) is active
│   └── WindowsSecureBoot.hpp           # Checks if Windows Secure Boot is turned on
└── Menu/
    ├── Main.cpp                        # Main entry point that starts all detection loops
    └── Menu.hpp                        # Simple UI code for the anti-cheat status screen
