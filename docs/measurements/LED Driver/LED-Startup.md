# Start-up
This service performs LED Driver Start-up measurement.

## Hardware Setup

   Hardware Setup for LED Start-up measurement is made as mentioned below, with Buck Regulator type LED Driver DUT. 
   
   ![alt text](https://github.com/NI-Measurement-Plug-Ins/pmic-labview/blob/users/bkumarng-NI/LED_Startup_Documentation/docs/measurements/meas-images/LED_Driver/LED_Startup_HWSetup.png)
   
   The Start-up Measurement is implemented with PXIe-4139, acting as an Emulated LED Load. To mimic the loading characteristics of an LED load, the E-load requires a combination of CV and CR Mode, with the LED Parameters defined as 'Vo','Vd' & 'Io' for emulated LED operation. The CR Mode implementation using the PXIe-4139 is based on specification provided in PXIe-4139 manual (page 10), where different Resistance Ranges are supported against the 'Current Limit Range' when the device is in 'Voltage Mode'.

   Note: 
         i. 'Voltage Start Level', 'Voltage Stop Level' parameters in 'Source Configuration' tab corresponds to the Input Voltage range of DUT.   
         ii. For Parameter definition used in start-up Measurement, please refer to 'parameters-def.md'   

## InstrumentStudio Panel

### Usage

1. Select the appropriate source and load resource names and update other parameters as needed in Measurement Config, Source Config, and Load configuration.

   Measurement Configuration:
   ![alt text](https://github.com/NI-Measurement-Plug-Ins/pmic-labview/blob/users/bkumarng-NI/LED_Startup_Documentation/docs/measurements/meas-images/LED_Driver/LED_Startup_MeasConfig.png)

   Source Configuration:   
   ![alt text](https://github.com/NI-Measurement-Plug-Ins/pmic-labview/blob/users/bkumarng-NI/LED_Startup_Documentation/docs/measurements/meas-images/LED_Driver/LED_Startup_SourceConfig.png)

   Load Configuration:   
   ![alt text](https://github.com/NI-Measurement-Plug-Ins/pmic-labview/blob/users/bkumarng-NI/LED_Startup_Documentation/docs/measurements/meas-images/LED_Driver/LED_Startup_LoadConfig.png)
    

2. Run the measurement. The graphs should be visible without any error.

   Case 1: Expected Output Current (Io) is more than the minimum current that can be sinked in CR Mode, with provided Output Voltage (Vo). In this case, multiple points along V-I curve are plotted, up to the 'DUT Current Limit/Load Current limit range'.
   
   ![alt text](https://github.com/NI-Measurement-Plug-Ins/pmic-labview/blob/users/bkumarng-NI/LED_Startup_Documentation/docs/measurements/meas-images/LED_Driver/LED_Startup_Io_gt_Imin.png)

   Case 2: Expected Output Current (Io) is less than the minimum current that can be sinked in CR Mode, with provided Output Voltage (Vo). In this case, only a single point is plotted in the V-I curve.
   
   ![alt text](https://github.com/NI-Measurement-Plug-Ins/pmic-labview/blob/users/bkumarng-NI/LED_Startup_Documentation/docs/measurements/meas-images/LED_Driver/LED_Startup_Io_lt_Imin.png)
   

   
