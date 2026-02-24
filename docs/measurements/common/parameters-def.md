# Parameters used in the measurements

## Measurement settings

1. There are three modes of operation -
   
   i) Power ON: In this mode of operation, a Voltage within the allowable operating range of the DUT is set in Voltage level, to Initialize.
   
   ii) Perform Measurement: This mode assesses DUT performance across three operating states—source and load enabled, source only, and load only—while validating each state under multiple source-load configuration combinations.
  
   iii) Power OFF: This mode removes the applied voltage from the DUT and evaluates its shutdown behaviour across three operating states, covering all supported source-load configurations.

2. DUT Setup Time: Specifies the setup time of a DUT, the time required to load the DUT parameters and for the DUT startup.

3. Source Delay: Specifies the time required for the source and load instruments to reach steady state after a setpoint change. This parameter can be minimized to reduce test time, but if it is too small the DUT will not have enough time to reach the steady state.

4. Aperture Time: Specifies the amount of time the source and load instruments collect samples and average the samples together to form a single measurement. Longer aperture time increases the test time but improves the noise rejection.

5. Nominal Output Voltage: Enter the expected nominal output voltage of the DUT. This value is used only for the calculation of load voltage deviation.

6. Level Dwell Time: Specifies the amount of time each setpoint value holds.

7. Measurement Time-out:
   Specifies the duration of time in which a measurement must be completed. A measurement will be aborted if the measurement time-out duration has been reached before the measurement is complete. In the case of a timeout error, it is recommended to increase this parameter. For a sweep with more than 250 steps, the recommended Measurement Time-out is 100 seconds.

8. System Configuration: Defines how multiple instrument channels are interconnected to function as a combined system, typically by arranging them in either series (stacking) or parallel (ganging) to increase voltage or current capacity.
   
   i) In a series configuration, channels are connected end to end to increase total output voltage while current stays the same.
   
   ii) In a parallel configuration, channels are connected side by side to increase total current or capacity while maintaining the same voltage.

9. Output Function: Configures the function that the specified channels attempt to generate.
    
   i) When DC Voltage is selected, a channel generates the desired voltage level on the output as long as the output current is below the current limit. (Note: For Powering ON the DUT, DC Voltage must be selected).
   
   ii) When DC Current is selected, a channel generates the desired current level on the output as long as the output voltage is below the voltage limit.

   iii) When Pulse Voltage is selected, a channel generates pulses at the desired pulse voltage levels on the output as long as the output current is below the pulse current limit.

   iv) When Pulse Current is selected, a channel generates pulses at the desired pulse current levels on the output as long as the output voltage is below the pulse voltage limit.

10. Voltage Level: Specifies the output voltage, in volts, that the instrument channel(s) are configured to generate.

11. Voltage Level Range: Specifies the allowable minimum to maximum voltage, in volts, that the instrument channel(s) can be configured to generate.

12. Sense: Measures the voltage the instrument uses for regulation according to its internal feedback path.

    i) Remote sense uses HI S and LO S wires to measure voltage directly at the load and compensate for cable loss errors.

    ii) Local sense measures voltage at the instrument’s own HI/LO terminals and therefore does not compensate for cable losses.
   
## Source configuration

1. Maximum Power: Specifies the maximum power that the supply can provide. It is used to calculate the current limit for each voltage level.
   
2. Scale: Describes how values are distributed between a start and end value—whether the values change in equal increments (linear scale) or by equal ratios/multipliers (logarithmic scale).
   
3. Start Voltage: Specifies the starting setpoint of the source voltage sweep.

4. Stop Voltage: Specifies the final setpoint of the source voltage sweep.
   
5. No. of Points: Specifies the total number of points in the sweep. (Equally spaced setpoints from start voltage to stop voltage.)

6. Limit Symmetry: Specifies whether compliance limits for current generation and voltage generation for the device are applied symmetrically about 0 V and 0 A or asymmetrically with respect to 0 V and 0 A.

   i) When set to Symmetric , voltage limits and current limits are set using a single property with a positive value. The resulting range is bounded by this positive value and its opposite.

   ii) When set to Asymmetric , we must separately set a limit high and a limit low using distinct properties. (Note: For asymmetric limits, the range bounded by the limit high and limit low must include zero.)

7. Current Limit : Specifies the current limit of the source instrument for determining compliance. Please refer to the device [specs](https://www.ni.com/docs/en-US/bundle/pxie-4151-specs/page/specs.html) for the current and voltage ranges.

8. Current Limit Range: Specifies the current limit range, in amps, for the specified channel(s). The range defines the valid values to which the current limit can be set (Note: The Current Limit Range property is applicable only if the Output Function property is set to DC Voltage).

9. Current Limit Low: Specifies the minimum current, in amps, that the output can produce when generating the desired voltage on the specified channel(s).

10. Current Limit High: Specifies the maximum current, in amps, that the output can produce when generating the desired voltage on the specified channel(s).

11. Transient Response: Defined as supply’s ability to return its output voltage to the correct level, within a specified time, after a sudden change in load or output setting, with minimal overshoot or undershoot.

12. Voltage Gain Bandwidth: Specifies the SourceAdapt gain-bandwidth parameter for the voltage control loop. Higher GBW values allow for faster transients but less stability, while lower GBW values result in slower transients but more stability.

13. Voltage Compensation Frequency: Specifies the SourceAdapt compensation frequency parameter for the voltage control loop. It is the frequency at which a pole-zero pair is added to the system.

14. Voltage Pole-Zero Ratio: Specifies the SourceAdapt pole-zero ratio parameter for the voltage control loop. It is the ratio of pole and zero frequencies.

## Load configuration

1. Device Current Rating: Refers to maximum continuous current that device can safely handle without overheating and degrading. 
  
2. Current Level: Specifies the current level of the load instrument. Please refer to the device [specs](https://www.ni.com/docs/en-US/bundle/pxie-4051-specs/page/specs.html) for the voltage and current ranges.
  
3. Sweep Type: Describes how values are distributed between a start and end value—whether the values change in equal increments (linear scale) or by equal ratios/multipliers (logarithmic scale).
  
4. Current Start Level: Specifies the starting setpoint of the load current sweep.
   
5. Current Stop Level: Specifies the final setpoint of the load current sweep.
   
6. Pts/Pts per Decade: If the sweep type is Linear, specifies the total number of points in the sweep. For Logarithmic sweep type, specifies the number of points per decade.

7. Current Level Range: Specifies the current level range, in amps, for the specified channel(s). The range defines the valid values to which the current level can be set. (Note: The Current Level Range property is applicable only if the Output Function property is set to DC Current) .

8. Voltage Limit Range: Specifies the voltage limit of the load instrument for determining compliance.

9. Voltage Limit Low: Specifies the minimum voltage, in volts, that the output can produce when generating the desired current on the specified channel(s).

10. Voltage Limit High: Specifies the maximum voltage, in volts, that the output can produce when generating the desired current on the specified channel(s).

11. Source Trigger: Receiving a Source trigger causes a channel to modify the source configuration. This trigger is available only when sourcing DC voltage or DC current.

12. Measure Trigger : Receiving a Measure trigger, if “Measure When” is set to “On Measure Trigger”, causes a channel to take a measurement. A channel ignores this trigger if a measurement is already in progress or if “Measure When” is set to a different value.

13. Current Gain Bandwidth: Specifies the SourceAdapt gain-bandwidth parameter for the current control loop. Higher GBW values allow for faster transients but less stability, while lower GBW values result in slower transients but more stability.

14. Current Compensation Frequency: Specifies the SourceAdapt compensation frequency parameter for the current control loop. It is the frequency at which a pole-zero pair is added to the system.

15. Current Pole-Zero Ratio: Specifies the SourceAdapt pole-zero ratio parameter for the current control loop. It is the ratio of pole and zero frequencies.

## Scope configuration

1. Sample rate:
   Specifies the sample rate of the scope instrument. Please refer to the device [specs](https://www.ni.com/docs/en-US/bundle/pxi-5122-specs/page/specs.html).

2. Acquisition time:
   Specifies the time duration for which scope acquires samples.

3. Probe attenuation:
   Specifies probe attenuation value of scope instrument.

## Duty Cycle configuration

1. Duty Cycle Single Pulse/ Sweep Pulse:
   Specifies if single duty cycle is repeated or Sweep the duty cycle from start and stop point.

2. Frequency:
   Specifies the frequency at which AWG will source PWM signal and Load SMU will sink.

3. Duty Cycle:
   Specifies the pulse ON of cycle in percentage.

4. Number of Pulse Cycle:
   Specifies the number of cycle pulse will be repeated.

5. Start Duty Cycle:
   Specifies the starting set-point of the duty cycle sweep.

6. Stop Duty Cycle:
   Specifies the final setpoint of the duty cycle sweep.

7. Number of Sweep Points:
   If the sweep type is Linear, specifies the total number of points in the sweep. For Logarithmic sweep type, specifies the number of points per decade.

8. Sweep Type:
   Specifies whether the configured sweep is linear or logarithmic for duty cycle
   
## PWM Source configuration

1. Resource name:
   Specifies the AWG Resource name for PWM generation

2. Amplitude:
   Specifies Amplitude at which AWG will generate signal

3. DC Offset:
   Specifies the offset of the PWM signal

4. Load Impedence:
   Specifies the Load Impedence in three values Match Output, High Z and Custom

5. Load Impedence Custom:
   Specifies the Load Impedence value for AWG, enabled if load impedence is custom 

6. Source Trigger:
   Configures the start trigger of AWG for edge triggering.

7. Measure Trigger:
   Configure the measure trigger for exporting the selected signal for starting edge triggering for AWG from Load.

## Known Issues

1.	The index of Array controls in “Measurement Configuration.ctl” should be less than 16. The data won’t be passed properly if the index is >=16.  [grpc-labview issue](https://github.com/ni/grpc-labview/issues/351)
2.	When Copying the configuration from InstrumentStudio to TestStand, ‘Inf’ value is not passed properly, it is copied as 8 to TestStand.


## Tips

1. To perform the measurements with larger sweep points, increase the 'Timeout' value of 'Wait For Event With Channels' VI.
   ![Timeout value](../meas-images/increase-timeout.png)
   
2. To see the results faster, remove the 'Wait(ms)' function or decrease the 'Wait' function value in the 'Perform Measurements' subVI.
   ![Wait function value](../meas-images/decrease-wait-value.png)





