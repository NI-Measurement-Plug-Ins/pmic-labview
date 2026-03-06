# Efficiency and Load Regulation Measurement
Efficiency and Load Regulation measurement evaluate how well a power device delivers output power and maintains a stable output voltage as the load varies. By applying an input source and adjusting the load current, the measurement calculates overall efficiency and observes voltage changes, helping verify power supply performance across different operating conditions. 

## Hardware Setup
Make the setup and verify that the PXIe Chassis and Modules are powered and connected.  
1) Single Source-Single Load
  ![alt text](../meas-images/Efficiency_Meas_Images/single-single-dut-hw-setup.png)

2) Single Source-Ganged Load
  ![alt text](../meas-images/Efficiency_Meas_Images/single-ganged-dut-hw-setup.png)

3) Ganged Source-Single Load
   ![alt text](../meas-images/Efficiency_Meas_Images/ganged-single-dut-hw-setup.png)

4) Ganged Source-Ganged Load
   ![alt text](../meas-images/Efficiency_Meas_Images/ganged-ganged-dut-hw-setup.png)  

## InstrumentStudio Panel

Launch InstrumentStudio (2024 Q3 or higher) and open "Efficiency and Load Regulation Measurement".



![alt text](../meas-images/Efficiency_Meas_Images/is-panel-efficiency-meas.png)

### Usage

1) The measurement has different modes of operation - Power ON/Power OFF and Perform Measurement. 

2) #### Power ON:
   In this mode of operation, a Voltage within the allowable operating range of the DUT is set in Voltage level, to Initialize. The DUT can be powered using either a single source or multiple ganged sources, depending on the selected configuration, as defined below:
   
   a) Configuration 1: Single Source
   ![alt text](../meas-images/Efficiency_Meas_Images/single-source-power-on.png)
   

   b) Configuration 2: Ganged Source
   ![alt text](../meas-images/Efficiency_Meas_Images/ganged-source-power-on.png)

4) #### Perform Measurement:
  This mode evaluates system behaviour across different configurations.
  
  3.1) Select the appropriate Source and Load resource names and update other parameters as needed.
  
  3.2) Run the measurement for following configurations.

   a) Configuration 1: Single Source, Single Load

   i) Efficiency
   ![alt text](../meas-images/Efficiency_Meas_Images/eff-single-single.png)

   ii) Load Regulation (V/A)
   ![alt text](../meas-images/Efficiency_Meas_Images/lr-va-single-single.png)

   iii) Load Regulation (%)
   ![alt text](../meas-images/Efficiency_Meas_Images/lr-percent-single-single.png)

   b) Configuration 2: Single Source, Ganged Load

   i) Efficiency
   ![alt text](../meas-images/Efficiency_Meas_Images/eff-single-ganged.png)

   ii) Load Regulation (V/A)
   ![alt text](../meas-images/Efficiency_Meas_Images/lr-va-single-ganged.png)

   iii) Load Regulation (%)
   ![alt text](../meas-images/Efficiency_Meas_Images/lr-percent-single-ganged.png)

   c) Configuration 3: Ganged Source, Single Load

   i) Efficiency
   ![alt text](../meas-images/Efficiency_Meas_Images/eff-ganged-single.png)

   ii) Load Regulation (V/A)
   ![alt text](../meas-images/Efficiency_Meas_Images/lr-va-ganged-single.png)

   iii) Load Regulation (%)
   ![alt text](../meas-images/Efficiency_Meas_Images/lr-percent-ganged-single.png)

   d) Configuration 4: Ganged Source, Ganged Load

   i) Efficiency
   ![alt text](../meas-images/Efficiency_Meas_Images/eff-ganged-ganged.png)

   ii) Load Regulation (V/A)
   ![alt text](../meas-images/Efficiency_Meas_Images/lr-va-ganged-ganged.png)

   iii) Load Regulation (%)
   ![alt text](../meas-images/Efficiency_Meas_Images/lr-percent-ganged-ganged.png)

4) #### Power OFF:
   This mode disables the voltage supplied to the DUT for each supporting specific configurations -

   a) Configuration 1: Single Source, Single Load
   ![alt text](../meas-images/Efficiency_Meas_Images/single-single-power-off.png)

   b) Configuration 2: Single Source, Ganged Load
   ![alt text](../meas-images/Efficiency_Meas_Images/single-ganged-power-off.png)

   c) Configuration 3: Ganged Source, Single Load
   ![alt text](../meas-images/Efficiency_Meas_Images/ganged-single-power-off.png)

   d) Configuration 4: Ganged Source, Ganged Load
   ![alt text](../meas-images/Efficiency_Meas_Images/ganged-ganged-power-off.png)

     
## Tested with
- 2xPXIe-4151
- 2xPXIe-4051






