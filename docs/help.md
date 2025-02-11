# Getting Started

## Workflow
This workflow is applicable for all the PMIC.

### Adding a measurement panel to InstrumentStudio Pro

1. Open InstrumentStudio Pro
   ![alt text](images/instr-studio-open-is.png)

2. Click Manual Layout, and select required measurement under the collection (for e.g., Efficiency and Load Regulation under PMIC) and 'Create Large Panel' from dropdown. Click OK.
   ![alt text](images/instr-studio-manual-layout.png)

3. Efficiency and Load Regulation measurement UI will get displayed on a large panel as shown in below screenshot.
   ![alt text](images/instr-studio-eff-and-lr-panel.png)

### Powering ON

1. Select "Power on the DUT" option from the 'Mode Of Operation' dropdown. Give appropriate resource name the DUT is connected to and run the measurement service with the default values.
   ![alt text](images/power-on-config.png)

2. The status message will be shown if there is no error. 
   
   ![alt text](images/power-on-status.png)

### Communication with the DUT (if needed)

1. Now that the DUT is powered ON, configure the DUT settings either by using SDC panel or from the native GUI of the DUT.

   ![alt text](images/sdc-panel.png)

### Perform Measurement

1. As the communication is established with the DUT, now select "Perform Measurement" option from the 'Mode of Operation' dropdown. Give appropriate resource names the DUT is connected to and run the measurement service with the default values.
   
   ![alt text](images/perform-meas-efficiency.png)

### Powering OFF

1. After performing the measurements, make sure to Power off the DUT by selecting the option from 'Mode Of Operation' dropdown. 
   
   ![alt text](images/power-off-config.png)

2. The status message will be shown if there is no error. 
   
   ![alt text](images/power-off-status.png)

## Parameters in the UI

Please refer to [this](measurements/common/parameters-def.md) document for more detailed information on the controls/indicators used.

## Adding a  measurement step to TestStand 

Follow the workflow below to automate the measurements using TestStand and monitor it from Instrument Studio.

After adding measurement service into the Instrument Studio as explained above,

1. Open TestStand 2022 Q4 or higher version. Open a new sequence file and save the file. 

   ![alt text](images/teststand-open-seq.png)

2. Insert a 'Measurement' step under MeasurementLink in Insertion palette or by selecting Insert Step > InstrumentStudio > Measurement in right click menu.
   Rename the step as required and choose the required measurement in Step settings.

   ![alt text](images/teststand-insert-measlink-step.png)

3. To transfer the measurement configuration from the Instrument Studio to the TestStand, click on "COPY button" highlighted in the screenshot.

   ![alt text](images/instr-studio-copy-meas-config.png)

4. The below indication confirms the Measurement configuration is copied

   ![alt text](images/instr-studio-meas-config-copied.png)

5. Select the measurement step and click on the paste button as highlighted in the screenshot. There will be a message indicating that the measurement configuration is applied.

   ![alt text](images/teststand-paste-config.png)

6. Set 'Enable Monitoring' variable to True as shown in below screenshot. It will help us to monitor the results in Instr Studio.

   ![alt text](images/teststand-enable-monitoring.png)

8. Save the Sequence file and RUN the sequence. While running the sequence file in TestStand you can see measurement results and graphs updated in the InstrumentStudio as well.

   ![alt text](images/teststand-run-seq.png)

9. The measurement results are updated in the Instrument Studio as below.

   ![alt text](images/instr-studio-results-from-ts.png)

10. In TestStand, the measurment test status will be 'Done' if there is no error.

    ![alt text](images/teststand-pass-seq.png)

11. The same workflow of Power on the DUT, Perform Measurement, and Power off the DUT can be followed in TestStand, by adding three Measurement Steps along with the SDC steps. Make sure to Power off the DUT. 

    ![alt text](images/teststand-measlink-steps.png)

Please refer [this](measurements/meas-index.md) for more details on each measurement.
