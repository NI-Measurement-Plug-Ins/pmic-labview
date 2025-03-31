# Q-current Channel Ganging
This service performs Q-current Ganging/Stacking.

## Hardware Setup
  ![alt text](../meas-images/q-current-ch-ganging-hw-setup.png)

## InstrumentStudio Panel

### Usage

1. Select appropriate source resource names of all the instruments which are stacked or ganged. One of the instruments will be master device and others will be slave devices. Update other parameters as per the system configuration.
   ![alt text](../meas-images/q-current-ch-ganging-meas-config.png) and ![alt text](../meas-images/q-current-ch-ganging-source-config.png)

2. Run the measurement. The system level and individual voltages and currents are plotted in the graphs.
   
   ![alt text](../meas-images/q-current-ch-ganging-meas-result.png)


## Tested with
- 2xPXIe-4151


(Note: Tested with 2 power supplies connected in parallel configuration as per the hardware setup diagram.)
