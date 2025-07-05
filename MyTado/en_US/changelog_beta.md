# Changelog plugin MyTado - beta

# 28/06/2025 - Version 7.0

- Added open window detection command. **Warning: You must update dependencies and resynchronize.**  
- The **Set desired temperature** command is now of subtype *slider*. **Warning: This impacts scenarios, so make sure to review and adjust them after the update.**  
- Added distinction between relative distance and calculated distance for user equipment (new command).
- Simplified command handling to allow for greater flexibility in the future.  
- The plugin moved to the "wellness" category.

# 04/05/2025 - Version 6.2

- Fixed a synchronization bug (introduced in version 6.0)  

# 04/01/2025 - Version 6.1

- Fixed a bug when creating commands for a new home (introduced in version 6.0)  

# 03/23/2025 - Version 6.0

- Adaptation of the connection to Tado following the API change on 03/21/2025  

# 03/19/2025 - Version 5.1

- Reorganization of the equipment page display  
- Fixed an issue with synchronization during a new plugin installation  
- Image display corrected for devices of the RU02B model (RU02 managing thermostat and hot water)  

# 03/09/2025 - Version 5.0

- Redesign of equipment configuration management for greater flexibility in the future, regardless of plugin versions.
- Added **user**-type equipment to obtain detailed information on Tado user locations for your scenarios.
- It is now possible to customize user images, which are displayed on the **home** widget when present.
- Ability to choose the data refresh frequency.

# 02/20/2025 - Version 4.1

- For **TadoX** devices, the displayed temperature is now the **one measured by the device** (instead of the zone temperature).
- The **Tado Home widget** now shows **the number of people present**.

# 02/16/2025 - Version 4.0

- The daemon now relies on the JeedomDaemon module by Mips, which eliminates any memory leaks.
- The home equipment has a new action to determine how many users are at home.
- Objects with multiple roles (e.g., boiler and water heater control) are now represented by one piece of equipment per function.
- Action parameters are now available for command testing and in scenarios.  

# 01/19/2025 - Version 3.1


- The possible values for the various parameters of air conditioning modules are now retrieved dynamically.  
- Fixed an issue with retrieving the state of a TadoX device when it is in manual mode for a defined duration.  
- Updated the documentation to describe how to manage scenarios with MyTado.

# 12/2024 - Version 3.0

- TadoX devices are now supported
- Weather is converted into a home, and the connection configuration has been shifted to this "home" device
- It is possible to configure multiple homes in case of owning both Tado and TadoX devices (what requires 2 separate homes)
- 4 new commands added for Tado(X) devices: enable, disable, time of the last data update, and battery level

# 11/2024 - Version 2.0

- Tado communication is now managed via a daemon to avoid latencies

# 10/30/2024 - Version 1.6

- Errors in retrieving the capabilities of an AC-type object no longer block the retrieval of other devices

# 10/17/2024 - Version 1.5

- Heating power is now collected and displayed
- It is now possible to change the default naming of your devices
- Spanish translation now available

# 10/13/2024 - Version 1.4

- Bug fix: Default name of weather commands ensured
- Different versions of the same type of known object model are now configured the same way

# 25/05/2024 - Version 1.3

- Air-conditionning and boiling devices are now managed
- Translation in german added

# 08/05/2024 - Version 1.2

- Commands enable/disable replaced by mode info and set_mode action
- Device widget updated accordingly

# 05/05/2024 - Version 1.1

- New commands to enable/disable devices as well as one to set manually targeted temperature
- First widgets' version

# 25/04/2024 - version 1.0

- First stable version