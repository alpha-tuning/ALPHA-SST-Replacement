# ALPHA Legacy Flash Replacement Hardware

## Overview

Before low-cost real-time emulation became widely available, these boards were developed as an alternative to traditional 27SF512-based Honda ECU chip tuning solutions.

This project adapts larger PLCC32 flash memory devices into the factory-style 28-pin DIP footprint commonly used in OBD1 Honda ECUs. The custom breakout boards allow larger flash devices to be installed directly into standard ECU sockets while maintaining compatibility with existing tuning workflows.

Supported devices include:

- SST39SF040
- SST39SF010
- ST M29F040B
- AMD AM29F010

## Design Features

- PLCC32 to 28-pin DIP adapter design
- Compatible with standard Honda OBD1 ECU chip sockets
- Support for larger flash memory devices than the original 27SF512
- A15/A16 bank selection through onboard header configuration
- Live map switching capability
- Programming mode support without requiring a dedicated 32-pin adapter

Address lines above A14 use 10K pull-up and pull-down resistors to prevent floating inputs, unintended sector selection, and accidental bank switching.

## ALPHAburner Compatibility

These boards were designed specifically for use with **ALPHAburner**.

The original ALPHAburner platform was based on an STM32 microcontroller and is now deprecated. Later revisions moved to an RP2350B-based design before development shifted toward real-time emulation solutions.

## Legacy Status

This project is considered **legacy hardware**.

At the time of development, flash-based tuning was still one of the most common ways to modify Honda OBD1 ECUs. Since then, open-source real-time emulation platforms such as **oneROM** have heavily reduced the need for traditional chip swapping, external burners, and repeated flash programming.

With oneROM making real-time emulation possible at roughly a $10 hardware cost, traditional chip tuning has largely been put to bed for development, testing, calibration, and live map switching workflows.

These designs remain available for:

- Historical reference
- Educational purposes
- Existing hardware maintenance
- Documentation of the ALPHA hardware development timeline

## Disclaimer

This repository is maintained for archival and reference purposes. Active development has ceased, and future ALPHA work is focused on modern real-time emulation platforms.

## Educational Use & Required Attribution

This repository is provided for **educational, historical, and reference purposes only**.

The hardware designs, documentation, notes, and related files are shared so others can study legacy Honda OBD1 ECU flash replacement hardware, PLCC32-to-DIP adaptation, address line handling, bank switching, and chip programming workflows.

If you use, modify, copy, redistribute, reference, document, build from, or create derivative work based on anything in this repository, attribution is required.

Required attribution:

**Original ALPHA hardware/design by ALPHA Tuning**  
**https://github.com/alpha-tuning**

Attribution must remain visible in any public repository, documentation, board files, video content, product listing, derivative hardware, or related project.

You may not remove ALPHA attribution, claim this work as your own original design, or present derivative versions in a way that hides the original source.

All materials are provided as-is with no warranty. You are responsible for verifying safety, compatibility, and proper use before applying these designs to any ECU, vehicle, programmer, or hardware setup.
