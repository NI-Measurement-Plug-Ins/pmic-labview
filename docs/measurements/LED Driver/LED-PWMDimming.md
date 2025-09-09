# PWM Dimming Measurement
This service performs LED Driver PWM dimming measurement.

## Hardware Setup

   Hardware Setup for PWM Dimming measurement is made as mentioned below with TPS92200D1.
   ![alt text](https://github.com/NI-Measurement-Plug-Ins/pmic-labview/blob/main/docs/measurements/meas-images/LED_Driver/LED-PWM-HW-Setup.png)
   

## Instrument Studio Panel 

### Usage

1. Select the appropriate source and load resource names and update other parameters as needed in Measurement, PWM source and PWM capture configuration.

   Measurement Configuration:
     There are two mode for duty cycle one is constant duty cycle ran multiple time and other is sweeping duty cycle through boolean control "DUTY CYCLE SINGLE PULSE/SWEEP PULSE".
Note: Except load configuration all the configurations are same for TPS92200D1 and TPS92621Q1 EVM.
   
   Measurement Configuration 1:
   ![alt text](https://github.com/NI-Measurement-Plug-Ins/pmic-labview/blob/main/docs/measurements/meas-images/LED_Driver/LED-PWM-meas-config-single.png)

   Measurement Configuration 2:
   ![alt text](https://github.com/NI-Measurement-Plug-Ins/pmic-labview/blob/main/docs/measurements/meas-images/LED_Driver/LED-PWM-meas-config-sweep.png)

   Source Configuration:   
   ![alt text](https://github.com/NI-Measurement-Plug-Ins/pmic-labview/blob/main/docs/measurements/meas-images/LED_Driver/LED-PWM-source-config-92621.png)

   Load Configuration for TPS92200D1 EVM:   
   ![alt text](https://github.com/NI-Measurement-Plug-Ins/pmic-labview/blob/main/docs/measurements/meas-images/LED_Driver/LED-PWM-load-config-92200D1.png)
 
   Load Configuration for TPS92621 EVM:   
   ![alt text](https://github.com/NI-Measurement-Plug-Ins/pmic-labview/blob/main/docs/measurements/meas-images/LED_Driver/LED-PWM-load-config-92621.png)
 
   PWM Source Configuration: 
   ![alt text](https://github.com/NI-Measurement-Plug-Ins/pmic-labview/blob/main/docs/measurements/meas-images/LED_Driver/LED-PWM-AWG-config.png)
 
   PWM Capture Configuration: 
   ![alt text](https://github.com/NI-Measurement-Plug-Ins/pmic-labview/blob/main/docs/measurements/meas-images/LED_Driver/LED-PWM-scope-config.png)

  
3. Run the measurement. The graphs should be visible without any error.
   
   PWM Dimming Measurement Configuration 1 for TPS92200D1 EVM:
   ![alt text](https://github.com/NI-Measurement-Plug-Ins/pmic-labview/blob/main/docs/measurements/meas-images/LED_Driver/LED-PWM-meas-results-single-92200D1.PNG)
   PWM Dimming Measurement Configuration 2 for TPS92200D1 EVM:
   ![alt text](https://github.com/NI-Measurement-Plug-Ins/pmic-labview/blob/main/docs/measurements/meas-images/LED_Driver/LED-PWM-meas-results-sweep-waveform-92200D1.png)
   ![alt text](https://github.com/NI-Measurement-Plug-Ins/pmic-labview/blob/main/docs/measurements/meas-images/LED_Driver/LED-PWM-meas-results-sweep-OP-VS-IP-92200D1.png)
 
   PWM Dimming Measurement Configuration 1 for TPS92621Q1 EVM:
   ![alt text](https://github.com/NI-Measurement-Plug-Ins/pmic-labview/blob/main/docs/measurements/meas-images/LED_Driver/LED-PWM-meas-results-single-92621.png)
   PWM Dimming Measurement Configuration 2 for TPS92621Q1 EVM:
   ![alt text](https://github.com/NI-Measurement-Plug-Ins/pmic-labview/blob/main/docs/measurements/meas-images/LED_Driver/LED-PWM-meas-results-sweep-waveform-92621.png)
   ![alt text](https://github.com/NI-Measurement-Plug-Ins/pmic-labview/blob/main/docs/measurements/meas-images/LED_Driver/LED-PWM-meas-results-sweep-OP-VS-IP-92621.png)
