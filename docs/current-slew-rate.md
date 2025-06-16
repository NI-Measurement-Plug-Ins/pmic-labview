# Current Slew Rate
Cureesnt slew rate utility vi helps users to control current slew rate of power-supply PXIe-4151.


## Hardware Setup
 
![alt text](images/current-slew-rate-hw-setup.png)

## Utility VI
### Usage

1.Download the https://github.com/NI-Measurement-Plug-Ins/pmic-labview repo

2. Open source/utility/Current slew rate.vi
   
3. Select the appropriate source resouce name, current levels, update rate and other parameters. There is option of enabling or disabling of scope.
   ![alt text](images/current-slew-rate-source-config.png)

    ![alt text](images/current-slew-rate-scope-config.png)
   
5. Run the vi. Source current graphs should be visible without any error, with help of two cursor validate if the time period of achevieing slew rate is similar to result indicator of EXPECTED TIME FOR SLEW RATE.

   Slew rate with Source capture:
  ![alt text](images/current-slew-rate-source-results.png)
   Slew rate with Scope capture:
  ![alt text](images/current-slew-rate-scope-results.png)

### Notes:
## Defination:
1. Voltage Limit Range:
  Specifies the voltage limit of the source instrument for determining compliance. 
  
2. Current Level Range:
  Specifies the current level of the source instrument. Please refer to the device current ranges.
3. Sample Rate: 
4. Update Rate:
5. Slew rate: 
6. Expected Time for Slew Rate:
7. Transient Response: 

8. Current Gain Bandwidth:
   Specifies the SourceAdapt gain-bandwidth parameter for the current control loop. 
   Higher GBW values allow for faster transients but less stability, while lower GBW values result in slower transients but more stability.

9. Current Compensation Frequency:
   Specifies the SourceAdapt compensation frequency parameter for the current control loop. It is the frequency at which a pole-zero pair is added to the system.

10. Current Pole-Zero Ratio:
    Specifies the SourceAdapt pole-zero ratio parameter for the current control loop. It is the ratio of pole and zero frequencies.


