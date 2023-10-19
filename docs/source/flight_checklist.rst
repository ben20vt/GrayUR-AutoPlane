Pre-Flight Checklist
====================

.. warning::

   Never power on air or ground radios without an antenna connected. This will kill the   
   transmitters.

.. warning::

   This sequence will cause the prop to spin. Keep the area around the prop clear at all times 
   - assume that if power is connected the prop is able to spin 
   without warning.

Procedure
------------
1. Open Mission Planner (MP)
2. Connect the telemetry radio ground module to the laptop
  - You will see a flashing green light - this means the radio is on standby
3. Connect the batteries to both inputs of the parallel power harness. Then connect the harness to the ESC power input
  - You should hear a trill from the GPS - it will flash multiple colors as it starts up, then begin flashing yellow. This indicates that the plane is now on standby
  - You should hear two low-pitched beeps
  - The motor will buzz 5 times, with the last buzz being higher pitched than the previous 
  four. This indicates that the ESC has started up correctly and identified the battery 
  correctly (5 tones for the 5 battery cells) 
  - The telemetry radio ground module should now have a flashing red light. This light 
  indicates that data packets are being transmitted between the ground and air modules (I.E., 
  the radios are connected and talking to each other) 
4. Search for and open **Device Manager** on the ground station laptop (GCS). Expand the category **Ports (COM & LPT)** and search for the air radio.
5. From the dropdown in the top left of MP, select COM(X) (where X is the number you identified in Device Manager)
  .. image:: Picture1.png
  - Mission Planner will say "Mavlink Connecting" and take a few seconds to load all the 
  parameters from the flight controller. This can take significantly longer if there are 
  communication issues between the air and ground radios (I.E. loose antenna connections or 
  significant distance between radios)
6. To check that the flight controller is communicating with MP in realtime, move the plane or 
flight controller around and confirm that the artificial horizon in the GCS interface moves as well.
7. Turn on the handheld radio controller
  - The radio controller will beep once when it is powered on
  - This will be followed by a low and high pitch beep, which indicates that the radio 
  controller is communicating with the receiver.

.. note::

   The radio control system will fail to initialize until the throttle is moved to its minimum 
   position

8. **[Optional]** Calibrate the radio
  - Recommended if you are having servo trim or range of motion issues

   a. In MP go to **Setup > Mandatory Hardware > Radio Calibration**
   b. Click "Calibrate Radio" and follow the instructions in MP

   .. note::

   Once you start the calibration process **you must finish it**. Move all sticks and switches     through all positions. Failure to do so may result in servo jitter which can damage servos      and control surfaces

9. Check the current flight mode of the plane
  - **Setup > Mandatory Hardware > Flight Modes**

  - For tuning and control surface checks, the flight mode should be set to manual
  - To change flight modes, toggle the three-position switch [SWNUM] on the radio controller

.. warning::

   **When working with the plane on the bench, make sure that the prop is not mounted on the     
   motor, or that the motor is physically disconnected from the power supply, or both**

10. Pre-arm the plane by pressing and holding the safety button on the GPS antenna. The button will change from blinking to solid blue. You will see the servos and control surfaces jump to position
  - You will now have control over all aspects of the plane *except* throttle. Before doing 
  work on the plane, try giving some throttle input to make sure the motor does not engage.
11. Check servo trim, direction of motion and range of motion
  #. This is most easily done in the **Servo Output** tab under **Optional Hardware**

  #. For our servos, trim (center) is defined at 1500 PWM
    - During normal operation, set min = 1000 PWM and max = 2000 PWM
    - If additional range of motion is needed, the absolute min and max PWM should be 800 and 2200, respectively
    - To avoid unnecessary strain on the servos, make sure min and max values are set to be equal or less than the control surfaces' physical limits
  #. If direction of motion is incorrect, select the reverse button next to the incorrect servo
12. Calibrate accelerometers (**Setup > Mandatory Hardware > Accel Calibration**)

  .. note::

   *This is not necessary for bench testing but should be done at the beginning of each 
   flight day (or power-up) and repeated if the plane is behaving improperly*

  #. Select the top option and follow the instructions in MP for physically orienting the 
  aircraft. This will require two people at a minimum.
  #. Select the middle option and hold the plane level (as it would be at cruising)
13. Calibrate compass (**Setup > Mandatory Hardware > Accel Calibration**)

  .. note::

     *This is not necessary for bench testing but should be done at the beginning of each 
     flight day (or power-up) and repeated if the plane is behaving improperly*

  - Click start, under “onboard mag calibration” and rotate the plane about all axes until all 
  three green bars are full (this is a finicky process and requires two people)
14. Check plane response in other flight modes than manual
We currently use *FBWA**, **AutoTune**, and/or **Stabilize**
  - Rotate the plane and check that control surfaces deflect such that the plane would return 
  to level if in flight

Final Checks
------------
1. Is MP reading the proper battery voltage and current?
2. Is the plane at the correct location and heading when sitting on the runway?
3. Do all other quick-reference values look normal?
   For example:
     - Ground speed
     - Airspeed
     - Altitude
     - Current when a small throttle blip is applied
     - # of GPS antennas connected (min 5 recommended)
     - AOA reasonable for current position at rest
4. Are all failsafes configured correctly
  See :doc:`configuration` for more information]

Arm Plane
------------
-	In the field, this should be done by pressing and holding the safety button on the GPS. The GPS will beep when armed, and you will now be able to throttle up the motor.
- In Surge or any other GPS-denied location, the plane must be force-armed. This can be done by clicking on the arm/disarm button found under the actions tab in the lower left corner of the MP home screen (where the map and artificial horizon are located)

Important Contacts
------------------
Brooks Saville, Agricultural Program Coordinator: bsaville@vt.edu
Roanoke Approach: 540-563-5985
Flight Service Station, to establish/cancel NOTAM: 1-877-4-US-NTMS (1-877-487-6867)
  Note: KEAS is located 9.2 NM from PSK VOR on radial 050 (or 5.9 NM northeast of KPSK)
Seymour Johnson AFB, to notify of NOTAM concerning VR43: 4oss.osos2@us.af.mil 
