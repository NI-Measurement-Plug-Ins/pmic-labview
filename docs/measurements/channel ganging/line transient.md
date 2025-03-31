# Load Transient Channel Ganging
This service performs Load Transient measurement with Ganging/Stacking.

## Hardware Setup
  ![alt text](../meas-images/line-transient-ch-ganging-hw-config.PNG)

## InstrumentStudio Panel

### Usage

1. Select the appropriate source resource names of all the instruments which are stacked or ganged. One of the instruments will be master and others will be slave devices. Update the other parameters as per the system configuration.
   ![alt text](../meas-images/line-transient-ch-ganging-source-config.png)

2. Similarly, update the parameters in the load configuration.
   ![alt text](../meas-images/line-transient-ch-ganging-load-config.PNG)

3. Similarly, update the parameters in the scope configuration.
   ![alt text](../meas-images/line-transient-ch-ganging-scope-config.PNG)

4. Similarly, update the parameters in the meas configuration.
   ![alt text](../meas-images/line-transient-ch-ganging-meas-config.PNG)


5. Run the measurement. The efficiency values are plotted in the graph.
   
   Load Transient:
   ![alt text](../meas-images/line-tran-ch-meas-results.png)

## Tested with
- 2xPXIe-4151
- 2xPXIe-4051

(Note: Tested with 2 power supplies and 2 E-load's connected in parallel configuration as per the hardware setup diagram.)
