# Changelog plugin MyTado - beta

# 12/2024 - Version 3.0

- TadoX devices are now supported
- Weather is converted into a home, and the connection configuration has been shifted to this "home" device
- It is possible to configure multiple homes in case of owning both Tado and TadoX devices (what requires 2 separate homes)
- 2 new commands added to Tado(X) devices: the date of the last data update, and its battery level

# 04/11/2024 - Version 2.0

- Tado communication is now managed via a daemon to avoid latencies

# 30/10/2024 - Version 1.6

- Errors in retrieving the capabilities of an AC-type object no longer block the retrieval of other devices

# 17/10/2024 - Version 1.5

- Heating power is now collected and displayed
- It is now possible to change the default naming of your devices
- Spanish translation now available

# 13/10/2024 - Version 1.4

- Bug fix: Default name of weather commands ensured
- Different versions of the same type of known object model are now configured the same way

# 05/25/2024 - Version 1.3

- Air-conditionning and boiling devices are now managed
- Translation in german added

# 05/08/2024 - Version 1.2

- Commands enable/disable replaced by mode info and set_mode action
- Device widget updated accordingly

# 05/05/2024 - Version 1.1

- New commands to enable/disable devices as well as one to set manually targeted temperature
- First widgets' version
-
# 04/25/2024 - version 1.0

- First stable version