# Line Regulation Channel Ganging
This service performs Line Regulation measurement with Ganging/Stacking.

## Hardware Setup
  ![alt text](../meas-images/ganging-hw-setup.png)

## InstrumentStudio Panel

### Usage

1. Select the appropriate source resource names of all the instruments which are stacked or ganged. One of the instruments will be master and others will be slave devices. Update the other parameters as per the system configuration.
   ![alt text](../meas-images/line-reg-ch-source-config.png)

2. Similarly, update the parameters in the load configuration.
   ![alt text](../meas-images/line-reg-ch-load-config.png)

3. Run the measurement. The efficiency values are plotted in the graph.
   
   Line Regulation(V/V):
   ![alt text](../meas-images/line-reg-ch-load-volt.png)

   Line Regulation(%):
   ![alt text](../meas-images/line-reg-ch-load-volt-dev.png)

## Tested with
- 2xPXIe-4151
- 2xPXIe-4051

(Note: Tested with 2 power supplies and 2 E-load's connected in parallel configuration as per the hardware setup diagram.)
