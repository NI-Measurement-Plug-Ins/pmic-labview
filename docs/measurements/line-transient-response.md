# Line Transient
This service performs Line Transient measurement. This mesurement supports 4151 and 4139 as power supply.

## Hardware Setup
   PXIe-4151 and PXIe-4051
   ![alt text](meas-images/hw-line-trans-4151-setup.png)
   PXIe-4139 and PXIe-4051
   ![alt text](meas-images/hw-line-trans-4139-setup.png)

## InstrumentStudio Panel

### Usage

1. Select the appropriate source and load resource names and update other parameters as needed.

   ![alt text](meas-images/line-transient-sourceandload-config.png)
   ![alt text](meas-images/line-transient-scope-config.png)
   Note:Disable scope if don't want to use

3. Run the measurement. Line transient graphs should be visible without any error.

   Line Transient 4151 and 4051 :
   ![alt text](meas-images/line-transient-meas-4151-result.png)
   ![alt text](meas-images/line-transient-scope-4151-result.png)
   
   Line Transient 4139 and 4051 :
   ![alt text](meas-images/line-transient-meas-4139-result.png)
   ![alt text](meas-images/line-transient-scope-4139-result.png)
