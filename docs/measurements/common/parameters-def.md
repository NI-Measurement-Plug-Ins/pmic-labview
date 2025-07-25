# Parameters used in the measurements

## Measurement settings

1. DUT Setup Time:
   Specifies the setup time of a DUT, the time required to load the DUT parameters and for the DUT startup.

2. Source Delay:
   Specifies the time required for the source and load instruments to reach steady state after a setpoint change. This parameter can be minimized to reduce test time, but if it is too small the DUT will not have enough time to reach the steady state.

3. Aperture Time:
   Specifies the amount of time the source and load instruments collect samples and average the samples together to form a single measurement. Longer aperture time increases the test time but improves the noise rejection.

4. Nominal Output Voltage:
   Enter the expected nominal output voltage of the DUT. This value is used only for the calculation of load voltage deviation.

5. Level Dwell Time:
   Specifies the amount of time each setpoint value holds.

6. Measurement Time-out:
   Specifies the duration of time in which a measurement must be completed. A measurement will be aborted if the measurement time-out duration has been reached before the measurement is complete. In the case of a timeout error, it is recommended to increase this parameter. For a sweep with more than 250 steps, the recommended Measurement Time-out is 100 seconds.
   
## Source configuration

1. Current Limit:
   Specifies the current limit of the source instrument for determining compliance. Please refer to the device [specs](https://www.ni.com/docs/en-US/bundle/pxie-4151-specs/page/specs.html) for the current and voltage ranges.
   
2. Maximum Power:
   Specifies the maximum power that the supply can provide. It is used to calculate the current limit for each voltage level.
   
3. Start Voltage:
   Specifies the starting setpoint of the source voltage sweep.

4. Stop Voltage:
   Specifies the final setpoint of the source voltage sweep.
   
5. No. of Points:
   Specifies the total number of points in the sweep. (Equally spaced setpoints from start voltage to stop voltage.)

6. Voltage Gain Bandwidth:
   Specifies the SourceAdapt gain-bandwidth parameter for the voltage control loop. 
   Higher GBW values allow for faster transients but less stability, while lower GBW values result in slower transients but more stability.

7. Voltage Compensation Frequency:
   Specifies the SourceAdapt compensation frequency parameter for the voltage control loop. It is the frequency at which a pole-zero pair is added to the system.

8. Voltage Pole-Zero Ratio:
   Specifies the SourceAdapt pole-zero ratio parameter for the voltage control loop. It is the ratio of pole and zero frequencies.

## Load configuration

1. Voltage Limit Range:
  Specifies the voltage limit of the load instrument for determining compliance. 
  
2. Current Level:
  Specifies the current level of the load instrument. Please refer to the device [specs](https://www.ni.com/docs/en-US/bundle/pxie-4051-specs/page/specs.html) for the voltage and current ranges.
  
3. Sweep Type: 
  Specifies whether the configured sweep is linear or logarithmic.
  
4. Start Current:
   Specifies the starting setpoint of the load current sweep.
   
5. Stop Current:
   Specifies the final setpoint of the load current sweep.
   
6. Pts/Pts per Decade: 
   If the sweep type is Linear, specifies the total number of points in the sweep. For Logarithmic sweep type, specifies the number of points per decade.

7. Current Gain Bandwidth:
   Specifies the SourceAdapt gain-bandwidth parameter for the current control loop. 
   Higher GBW values allow for faster transients but less stability, while lower GBW values result in slower transients but more stability.

8. Current Compensation Frequency:
   Specifies the SourceAdapt compensation frequency parameter for the current control loop. It is the frequency at which a pole-zero pair is added to the system.

9. Current Pole-Zero Ratio:
    Specifies the SourceAdapt pole-zero ratio parameter for the current control loop. It is the ratio of pole and zero frequencies.

## Scope configuration

1. Sample rate:
   Specifies the sample rate of the scope instrument. Please refer to the device [specs](https://www.ni.com/docs/en-US/bundle/pxi-5122-specs/page/specs.html).

2. Acquisition time:
   Specifies the time duration for which scope acquires samples.

3. Probe attenuation:
   Specifies probe attenuation value of scope instrument.

## Known Issues

1.	The index of Array controls in “Measurement Configuration.ctl” should be less than 16. The data won’t be passed properly if the index is >=16.  [grpc-labview issue](https://github.com/ni/grpc-labview/issues/351)
2.	When Copying the configuration from InstrumentStudio to TestStand, ‘Inf’ value is not passed properly, it is copied as 8 to TestStand.


## Tips

1. To perform the measurements with larger sweep points, increase the 'Timeout' value of 'Wait For Event With Channels' VI.
   ![Timeout value](../meas-images/increase-timeout.png)
   
2. To see the results faster, remove the 'Wait(ms)' function or decrease the 'Wait' function value in the 'Perform Measurements' subVI.
   ![Wait function value](../meas-images/decrease-wait-value.png)





