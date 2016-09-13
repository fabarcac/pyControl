.. _nacelle_hydraulics_digital_inputs:

Digital inputs handling
=======================

The wind turbine controller monitors permanently the digital signals produced by the
hydraulics system components, and reacts following this logic:

* The error *HydLevAl* is triggered when the digital input signal *InHydLevAl* is
  **False**
* The error *HydLevSt* is triggered when the digital input signal *InHydLevSt* is
  **False**

Note that there is no logic implemented to reset these alarms, although they might be
automatically reset by the controller based on the configured error properties. See the
errors definition table to get a full description of their properties.

.. attention::

    The above rules are not applied if any of the following conditions are met:

    * The safety line is open
    * DeviceNet 125kbps bus communication issues, namely:

        * General communication fault
        * Duplicated MAC detected
        * Communication timeout with control cabinet slave

I/O signals
-----------

List of DeviceNet signals read and/or written by this routine.

Parameters
----------

List of parameters used by this routine.

Errors
------

List of errors triggered, reset or checked by this routine.

