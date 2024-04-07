# Continuous Run in InstrumentStudio

## How to Enable
In InstrumentStudio, go to File>>Preferences. Under the **Preview features** section, enable the option called *Allow running measurements continuously*.  
![Enable RunContinuous](../meas-images/enable-continuous-run.png)

## How to Use
Next time that you launch InstrumentStudio, the **Run** button will have a drop down next to it where to can select the mode.  
![Continuous Run Button](../meas-images/continuous-run-button.png)  
In continuous run mode, InstrumentStudio will execute the measurement service and when it is complete, it will immediately run it again until the **Stop** button is pressed. If any controls tied to the measurement service are updated, the execution will be aborted and run again with the new values.

