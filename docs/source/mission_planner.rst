Introduction to Mission Planner
################################

First Steps
************
  **The default refresh rates of MP are fairly slow and undesirable for live updates during flight operations.**

  To adjust this navigate to the **CONFIG** tab
  - In the lefthand navigation pane select **Planner**
  - You will be modifying the *Telemetry Rates* parameters as follows
    - Altitude: **100**
    - Position:  **100**
    - Mode/Status:  **100**
    - RC:  **100**
    - Sensor:  **100**

  **While you are in this page I recommend the following changes: **
    - Dist Units: **Personal preference**
    - Alt Units: **Feet** - Since operating restrictions are given in feet this is best to leave in feet to ensure you are operating within legal limits
    - Speed Units: **Personal preference** - meters_per_second or mph are recommended

    - Map Follow: **Not enabled**

    - Theme: **HighContrast.mpsystheme** - Easiest to see on a screen in direct sunlight

    - Layout: **Advanced**

    - Running on a slow computer: **Unchecked initially** - You may opt to enable this if you are having performance issues with MP during operations


Avionics Setup
***************

Compass
==========================
Available hardware:

 - CUAV v5 Nano: **Compass**
 - External GPS: **GPS + Compass**



.. _servo-outputs:
Servo Outputs
==========================
To configure servo outputs, first navigate to the **SETUP** tab. In the lefthand pane expand the **>>Mandatory Hardware** section, then select **Servo Output**

The interface is split into a few key sections:
 - #
 - Function
 - Min, Trim, Max

**#** directly corresponds to the physical port number on the flight controller for PWM outputs. For this example, we'll be configuring the **right aileron**, plugged into **port #1**.

At rest, we should see the **position** readout to the right of the port number display 1500. This represents 1500 PWM. For control surfaces with bi-directional control (all control surfaces), a neutral input translates to the middle of the range of motion. Note that for throttle controls, a neutral input would be 0. 

To assign this output to ailerons, we will set the **function** to **Aileron**. 

We will then set our min, trim, and max as follows:
  Min: **1000**
  Trim: **1500**
  Max: **2000**

These values are a good starting point. To test our changes, ensure you are in manual mode, your radio controller is connected, and the plane is pre-armed. When aileron input is given, we should now see the right aileron we just configured move accordingly. Try deflecting the control surface to its extents in both directions. We will then adjust the min, trim, and max such that the control surface is allowed to move just short of its physical limits in either direction, and at neutral (no stick input) the trim is set such that the control surface is even with the rest of the wing. 





ESC Calibration
==========================

Flight Modes
==========================

Failsafe
==========================

Optional
**********

Sik Radio
==========================

Battery Monitor
==========================

Compass/Motor Calibration
==========================

Airspeed
==========================

Battery Monitor
==========================

Flaperon Configuration
==========================
