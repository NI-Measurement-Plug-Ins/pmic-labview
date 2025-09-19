# Startup
This service performs LED Driver Startup measurement.

## Hardware Setup

   Hardware Setup for LED Startup measurement is made as mentioned below. 
   
   ![alt text](https://github.com/NI-Measurement-Plug-Ins/pmic-labview/blob/users/bkumarng-NI/LED_Startup_Documentation/docs/measurements/meas-images/LED_Driver/LED_Startup_HWSetup.png)
   
   The Startup Measurement is implemented with PXIe-4139,acting as Emulated LED Load. The LED Load mimic, requires combination of CV and CR Mode, with LED Parameters defined 'Vo','Vd' & 'Io' for LED operation. The CR Mode implementation using PXIe-4139 is based on specification provided in PXIe-4139 manual(page 10), where different Resistance Range supported against the 'Current Limit Range' is provided.

   Note: For Parameter definition , advised to refer 'parameters-def.md'   

## InstrumentStudio Panel

### Usage

1. Select the appropriate source and load resource names and update other parameters as needed in Measurement Config,Source Config and Load configuration.

   Measurement Configuration:
   ![alt text](https://github.com/NI-Measurement-Plug-Ins/pmic-labview/blob/users/bkumarng-NI/LED_Startup_Documentation/docs/measurements/meas-images/LED_Driver/LED_Startup_MeasConfig.png)

   Source Configuration:   
   ![alt text](https://github.com/NI-Measurement-Plug-Ins/pmic-labview/blob/users/bkumarng-NI/LED_Startup_Documentation/docs/measurements/meas-images/LED_Driver/LED_Startup_SourceConfig.png)

   Load Configuration:   
   ![alt text](https://github.com/NI-Measurement-Plug-Ins/pmic-labview/blob/users/bkumarng-NI/LED_Startup_Documentation/docs/measurements/meas-images/LED_Driver/LED_Startup_LoadConfig.png)
    

2. Run the measurement. The graphs should be visible without any error.

   Case 1: Expected Output Current(Io) is more than the minimum current, that can be sinked in CR Mode, with provided Output Voltage(Vo). 
   ![alt text](https://github.com/NI-Measurement-Plug-Ins/pmic-labview/blob/users/bkumarng-NI/LED_Startup_Documentation/docs/measurements/meas-images/LED_Driver/LED_Startup_Io_gt_Imin.png)

   Case 2: Expected Output Current(Io) is less than the minimum current, that can be sinked in CR Mode, with provided Output Voltage(Vo). 
   ![alt text](https://github.com/NI-Measurement-Plug-Ins/pmic-labview/blob/users/bkumarng-NI/LED_Startup_Documentation/docs/measurements/meas-images/LED_Driver/LED_Startup_Io_lt_Imin.png)
   
   Case 3: DUT Current limit is below the Load 'Current Limit Range'. 
   ![alt text](https://github.com/NI-Measurement-Plug-Ins/pmic-labview/blob/users/bkumarng-NI/LED_Startup_Documentation/docs/measurements/meas-images/LED_Driver/LED_Startup_Io_upto_%20I_DUT.png)
      
   ![alt text](https://github.com/NI-Measurement-Plug-Ins/pmic-labview/blob/users/bkumarng-NI/LED_Startup_Documentation/docs/measurements/meas-images/LED_Driver/LED_Startup_Io_upto_%20I_DUT2.png)
   
