# PMIC - LabVIEW

 These MeasurementLink LabVIEW plugins makes measurements for Power Management IC's.
 
 The tests supply power to a DUT and sinks power from the DUT and validates the DUT's specifications by performing measurements that are common for PMIC's.

## Key Features

 - Single channel measurements
   - Efficiency and Load Regulation
   - Line Regulation
   - Load Transient Response
   - Ripple
   - Multi-Channel Output Voltage Accuracy

 - Channel Ganging measurements
   - Single point channel ganging
   - Sweep channel ganging
   - Efficiency channel ganging measurement

Click here for a detailed list of measurements and their functionality: [Measurement List](docs/measurements/meas-index.md)

## Hardware Dependencies

- NI Programmable Power Supply (PXIe-4151)
- NI Electronic Load (PXIe-4051)
- NI Oscilloscope (PXI-5122) (note: required for Ripple measurement)
- [optional] NI Digital Pattern Instrument (PXIe-6570/1) (note: the software does not include DPI or its dependencies, but it may be required to communicate with the DUT)

Validated hardware for these plugins:
- PXIe-4151
- PXIe-4051
- PXIe-6570/1
- PXI-5122

## Software Dependencies
(*This section is applicable if you only want to use the pre-compiled plug-ins. If you want to open the source code, go to [software development](docs/sw-dev.md).*)  
Install from NI Package Manager:

- InstrumentStudio Pro (2024 Q3 or higher)
- NI-DCPower (2023 Q4 or higher)
- NI SDC Add-On (2023 Q4 or higher) (note: only if using DPI for DUT communication)
- NI-SCOPE (2023 Q4 or higher) (note: if using Ripple measurement)

Download the latest NI package from the releases section of this repo or add the feed to NI Package Manager to get updates from this repo and other in this community. To use the NI Package Manager feeds, refer to this: [Subscribing to package feeds](https://github.com/NI-MeasurementLink-Plug-Ins/package-manager-feeds)

## Getting Started
When you are ready to start using the software, reference the [getting started documentation](docs/help.md).

## Contributing
Use the instructions in [software development](docs/sw-dev.md) for setting up a development environment and overview of the code.
