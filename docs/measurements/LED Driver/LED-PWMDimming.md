# PWM Dimming Measurement
This service performs PWM dimming measurement for LED Driver.

## Hardware Setup

   Hardware Setup for PWM Dimming measurement is made as mentioned below with TPS92200D1EVM and TPS92621Q1EVM.
   ![alt text](https://github.com/NI-Measurement-Plug-Ins/pmic-labview/blob/main/docs/measurements/meas-images/LED_Driver/LED-PWM-HW-Setup.png)

   For parameter defination of PWM Measurement refer to [Parameters def](https://github.com/NI-Measurement-Plug-Ins/pmic-labview/blob/main/docs/measurements/common/parameters-def.md)

## Instrument Studio Panel 

### Usage

1. Select the appropriate source and load resource names and update other parameters as needed in Measurement, PWM source and PWM capture configuration.

   Measurement Configuration:
     There are two modes for duty cycle, select a mode through boolean control "DUTY CYCLE SINGLE PULSE/SWEEP PULSE" :
   
     i. Single - Constant duty cycle, ran multiple times (Configuration 1)
   
     ii. Sweep duty cycle (Configuration 2)

Note: Source and load configuration for TPS92200D1EVM and TPS92621Q1EVM are different other settings are same.
   
   Measurement Configuration 1:
   ![alt text](https://github.com/NI-Measurement-Plug-Ins/pmic-labview/blob/main/docs/measurements/meas-images/LED_Driver/LED-PWM-meas-config-single.png)

   Measurement Configuration 2:
   ![alt text](https://github.com/NI-Measurement-Plug-Ins/pmic-labview/blob/main/docs/measurements/meas-images/LED_Driver/LED-PWM-meas-config-sweep.png)

   Source Configuration for TPS92200D1EVM:   
   ![alt text](https://github.com/NI-Measurement-Plug-Ins/pmic-labview/blob/main/docs/measurements/meas-images/LED_Driver/LED-PWM-source-config-92200D1.PNG)

   Source Configuration for TPS92621Q1EVM:   
   ![alt text](https://github.com/NI-Measurement-Plug-Ins/pmic-labview/blob/main/docs/measurements/meas-images/LED_Driver/LED-PWM-source-config-92621.png)

   Load Configuration for TPS92200D1EVM:   
   ![alt text](https://github.com/NI-Measurement-Plug-Ins/pmic-labview/blob/main/docs/measurements/meas-images/LED_Driver/LED-PWM-load-config-92200D1.png)
 
   Load Configuration for TPS92621Q1EVM:   
   ![alt text](https://github.com/NI-Measurement-Plug-Ins/pmic-labview/blob/main/docs/measurements/meas-images/LED_Driver/LED-PWM-load-config-92621.png)
 
   PWM Source Configuration: 
   ![alt text](https://github.com/NI-Measurement-Plug-Ins/pmic-labview/blob/main/docs/measurements/meas-images/LED_Driver/LED-PWM-AWG-config.png)
 
   PWM Capture Configuration: 
   ![alt text](https://github.com/NI-Measurement-Plug-Ins/pmic-labview/blob/main/docs/measurements/meas-images/LED_Driver/LED-PWM-scope-config.png)

  
3. Run the measurement. The graphs should be visible without any error.

 i. Results for TPS92200D1EVM DUT
 
   PWM Dimming Measurement Configuration 1:
   ![alt text](https://github.com/NI-Measurement-Plug-Ins/pmic-labview/blob/main/docs/measurements/meas-images/LED_Driver/LED-PWM-meas-results-single-92200D1.PNG)
   PWM Dimming Measurement Configuration 2:
   ![alt text](https://github.com/NI-Measurement-Plug-Ins/pmic-labview/blob/main/docs/measurements/meas-images/LED_Driver/LED-PWM-meas-results-sweep-waveform-92200D1.png)
   ![alt text](https://github.com/NI-Measurement-Plug-Ins/pmic-labview/blob/main/docs/measurements/meas-images/LED_Driver/LED-PWM-meas-results-sweep-OP-VS-IP-92200D1.png)

  ii.  Results for TPS92621Q1EVM DUT
  
   PWM Dimming Measurement Configuration 1:
   ![alt text](https://github.com/NI-Measurement-Plug-Ins/pmic-labview/blob/main/docs/measurements/meas-images/LED_Driver/LED-PWM-meas-results-single-92621.png)
   PWM Dimming Measurement Configuration 2:
   ![alt text](https://github.com/NI-Measurement-Plug-Ins/pmic-labview/blob/main/docs/measurements/meas-images/LED_Driver/LED-PWM-meas-results-sweep-waveform-92621.png)
   ![alt text](https://github.com/NI-Measurement-Plug-Ins/pmic-labview/blob/main/docs/measurements/meas-images/LED_Driver/LED-PWM-meas-results-sweep-OP-VS-IP-92621.png)
