# Single Point Channel Ganging
This service performs Single Point Ganging/Stacking.

## Hardware Setup
  ![alt text](../meas-images/ganging-hw-setup.png)

## InstrumentStudio Panel

### Usage

1. Select appropriate source resource names of all the instruments which are stacked or ganged. One of the instruments will be master device and others will be slave devices. Update other parameters as per the system configuration.
   ![alt text](../meas-images/single-point-source-config.png)

2. Similarly, update the parameters in the load configuration. For both the PPS and E-Load devices to be in sync, provide source trigger of master PPS as a trigger to master E-Load.
   ![alt text](../meas-images/single-point-load-config.png)

3. Run the measurement. The system level and individual voltages and currents are plotted in the graphs.
   
   ![alt text](../meas-images/single-point-meas-results.png)

4. To view the individual voltages and currents, click on the eye button and check the plots checkbox.
   ![alt text](../meas-images/single-point-meas-results-plot-visible.png) 

5. We can run the source and load independently as well. To run configuration of only source devices, make sure that the Enable button is 'ON' in the source configuration and is in 'OFF' position in the load configuration.
   ![alt text](../meas-images/single-point-source-enable.png)

   ![alt text](../meas-images/single-point-load-disable.png)

6. Similarly load devices can be run independently without a DUT, Enable button should be 'ON' in load config and it should be 'OFF' in source config. The trigger controls can be left empty.
   ![alt text](../meas-images/single-point-source-disable.png)

   ![alt text](../meas-images/single-point-load-enable.png)

## Tested with
- 2xPXIe-4151
- 2xPXIe-4051

(Note: Tested with 2 power supplies and 2 E-load's connected in parallel configuration as per the hardware setup diagram.)
