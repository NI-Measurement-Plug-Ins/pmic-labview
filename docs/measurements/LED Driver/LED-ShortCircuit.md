# Short Circuit
This service performs LED Driver Short Circuit measurement.

## Hardware Setup

   Hardware Setup for Short Circuit measurement is made as mentioned below. To Perform Short-Circuit measurement, DUT output path connection is switched between Load and DMM, to capture both Pre-Short and Post-Short condition.  
   
   i. During Pre-Short,only the Relay connected to Load is Activated.
   
   ii.During Post-Short , Relay connected to Load is De-Activated and the Relay connected to DMM is Activated, to measure the Short-Circuit current.

   Note: By default both the Relays are maintained in De-Activated state.
   
   ![alt text](https://github.com/NI-Measurement-Plug-Ins/pmic-labview/blob/main/docs/measurements/meas-images/LED_Driver/LED_SCT_Setup.png)

## InstrumentStudio Panel

### Usage

1. Select the appropriate source and load resource names and update other parameters as needed in Switch Config,DMM Config and Short Circuit configuration.

   Measurement Configuration:
   ![alt text](meas-images/LED_Driver/LED_SCT_Measurement_Config.png)

   Source Configuration:   
   ![alt text](meas-images/LED_Driver/LED_SCT_Source_Config.png)

   Load Configuration:   
   ![alt text](meas-images/LED_Driver/LED_SCT_Load_Config.png)
 
   Switch Module Configuration: 
   ![alt text](meas-images/LED_Driver/LED_SCT_Switch_Config.png)
 
   DMM Module Configuration: 
   ![alt text](meas-images/LED_Driver/LED_SCT_DMM_Config.png)

   Short-Circuit Test Configuration:   
   ![alt text](meas-images/LED_Driver/LED_SCT_Config.png)

2. Run the measurement. The graphs should be visible without any error, shows the Pre-Short and Post-Short Circuit measurement results.

   Short-Circuit Measurement:
   ![alt text](meas-images/LED_Driver/LED_SCT_Measurement_Result.png)

