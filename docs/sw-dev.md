# Setup a Development Environment
If you want to commit changes to the repo, we recommend you use the current versions of application software unless a newer version enables new features. Software should work with newer versions of these dependencies.

## Software dependencies:
Install the below softwares and packages from NIPM

- LabVIEW 64-bit (2021 SP1 or higher)
- NI-DCPower (2024 Q1 or higher)
- NI-SCOPE (2023 Q4 or higher)
- NI-FGEN (2023 Q4 or higher)
- InstrumentStudio Pro (2024 Q3 or higher)
- TestStand 2022 Q4
- Semiconductor Device Control Add-On 2023 Q4

## VIPM packages

Download and install the below packages in this [link](https://github.com/ni/measurement-plugin-labview/releases/tag/v3.0.0.3).
- ni_lib_labview_grpc_library-1.0.1.1
- ni_lib_labview_grpc_servicer-1.0.1.1
- ni_protobuf_types-1.0.0.1
- ni_measurement_plugin_sdk_service-3.0.0.3
- ni_measurement_plugin_sdk_generator-3.0.0.3

## Tested with:
- InstrumentStudio Pro 2024 Q3
- TestStand 2022 Q4
- Semiconductor Device Control Add-On 2023 Q4

## Building NIPM packages
To build NIPM packages for the measurement plugin, refer to the [this](build-plugin.md) document.
