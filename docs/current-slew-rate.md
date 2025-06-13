# Current Slew Rate
Cureesnt slew rate utility vi helps users to control current slew rate of power-supply PXIe-4151.

## Hardware Setup
   ![alt text](meas-images/hw-setup.png)

## Utility VI

### Usage

1.Download the https://github.com/NI-Measurement-Plug-Ins/pmic-labview repo
2. Open source/utility/Current slew rate.vi
3. Select the appropriate source resouce name, current levels, update rate and other parameters. There is option of enabling or disabling of scope.
   ![alt text](meas-images/line-reg-config.png)

4. Run the vi. Source current graphs should be visible without any error, with help of two cursor validate if the time period of achevieing slew rate is similar to result indicator of EXPECTED TIME FOR SLEW RATE.

   Slew rate with Source capture:
   ![alt text](meas-images/line-reg-load-volt.png)

   Slew rate with Scope capture:
   ![alt text](meas-images/line-reg-load-volt-dev.png)
