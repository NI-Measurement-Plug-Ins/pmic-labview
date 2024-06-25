# Sweep Channel Ganging
This service performs Sweep Ganging/Stacking.

## Hardware Setup
  ![alt text](../meas-images/ganging-hw-setup.png)

## InstrumentStudio Panel

### Usage

1. Select the appropriate source resource names of all the instruments which are stacked or ganged. One of the instruments will be master device and others will be slave devices. Update other parameters as per the system configuration.
   ![alt text](../meas-images/sweep-source-config.png)

2. Similarly, update the parameters in the load configuration. For both the PPS and E-Load devices to be in sync, provide source trigger and measure trigger of master PPS to master E-Load.
   ![alt text](../meas-images/sweep-load-config.png)

3. Run the measurement. The source and load I-V sweeps are plotted in the graphs.
   
   I-V Sweep:
   ![alt text](../meas-images/sweep-meas-results.png)

4. We can run the source and load independently as well. To run only sweep of source devices, make sure that the Enable button is 'ON' in the source configuration and is in 'OFF' position in the load configuration.
   ![alt text](../meas-images/sweep-source-enable.png)

   ![alt text](../meas-images/sweep-load-disable.png)

5. Run the measurement. The I-V Sweep can be seen in the graph. 
   
   Source I-V Sweep:
   ![alt text](../meas-images/sweep-source-results.png)

6. Similarly load devices sweep can be run independently without a DUT, Enable button should be 'ON' in load config and it should be 'OFF' in source config. The trigger controls can be left empty.
   ![alt text](../meas-images/sweep-source-disable.png)

   ![alt text](../meas-images/sweep-load-enable.png)

## Tested with
- 2xPXIe-4151
- 2xPXIe-4051

(Note: Tested with 2 power supplies and 2 E-load's connected in parallel configuration as per the hardware setup diagram.)




