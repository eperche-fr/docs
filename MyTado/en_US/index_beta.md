# <img src="../images/MyTado_icon.png" width="60"/> Plugin MyTado

The **MyTado** plugin allows you to retrieve data from your connected Tado and Tado X devices, as well as weather information managed by Tado.

Data refreshes every 30 minutes.

>**Supported Devices**
>
>Currently, only models BU0X, BP0, BR0X, CK04, RU0X, SU0X, VA0X, and WR0X are fully supported (regardless of their version).
>If you encounter issues with unsupported devices or any problems with the listed ones, please refer to the [Troubleshooting section](#Troubleshooting).

# Configuration

## Plugin Configuration

First, go to the plugin configuration.
Make sure to install dependencies and then start the daemon.
If you can't start the daemon, the default port (59969) might already be in use.
In this case, set a known available port in the configuration section, save, and try to restart the daemon.
If the problem persists, follow the instructions in the [Troubleshooting section](#Troubleshooting).

Optionally, you can also change the following two parameters:
1. The temperature unit to display. **Celsius is the default unit**.
2. The naming convention for your devices.
3. Set the refresh frequency of your objects by choosing the cron 5, 10, 15, or 30 minutes (keep only one of these crons). Keep the daily cron, which is necessary for object configuration.

Once the daemon is running, close the configuration page to return to the main plugin page, and follow these steps:  
1. Click on "Add a home".  
2. Give your home a name (the name does not need to be the same as in Tado), then click "Ok".  
3. Enter the exact name (case-sensitive) of your home in the Tado application.  
4. Save your home.  
5. Finally, authenticate yourself using the **Connect to Tado** button and follow the described procedure.  

If the information is correct, additional details about your home will be added, and Tado or TadoX devices (depending on your home) will be synchronized within a few seconds.
Close the home to check if your devices appear.
If nothing happens after a few seconds, refresh the page manually.
If your devices do not appear, check the logs to see if you can resolve any issues.
Otherwise, follow the instructions in the [Troubleshooting section](#Troubleshooting).

Finally, if you add devices to your Tado/TadoX home, the **Synchronization** button is there to fetch them.

>**INFORMATION**
>
>If you own both Tado and TadoX devices, you will have two homes. You must create a home for each of your Tado accounts.
>All devices will be listed regardless of which home they come from.

## Device Configuration

>**REMINDER**
>
>Simply use the **Synchronization** command to fetch any new connected devices added to your Tado home or after a plugin update that supports a new type of device you own.

### Your connected Tado devices
<img src="../images/WR0X.png" width="60"/><img src="../images/BU0X.png" width="60"/><img src="../images/RU0X.png" width="60"/><img src="../images/VA0X.png" width="60"/><img src="../images/VA04.png" width="60"/><img src="../images/RU04.png" width="60"/><img src="../images/CK04.png" width="60"/>

Clicking on a connected Tado device takes you directly to its configuration page:

- **Device Name**: Name of the device based on its serial number.
- **Parent Object**: Indicates the parent object to which the device belongs. You define this.
- **Category**: Allows you to choose the category of the device.

Clicking on the **Commands** tab shows a list of all available commands and the option to log numerical values.
Data updates every 30 minutes, but you can force an update on demand with the **Refresh** command.

In the dashboard, the widget displays the image corresponding to your device and the current information and configurations.
You can also set the operating mode of your device:
- 'Autonomous': The schedule set on the Tado app is applied;
- 'Manual': Allows you to exit automatic mode and set the parameter(s) of your choice;
- 'Off': The device is completely turned off.

>**Important Information**
>
>In the case of a manual temperature change, it will be applied to all devices in the same zone as your device (this is how Tado works).

### Tado Home <img src="../images/HomeEq.svg" width="60"/>

Clicking on your Tado home takes you directly to its configuration page:

- **Device Name**: Name you gave to your home in Jeedom.
- **Parent Object**: Indicates the parent object to which the device belongs. You define this.
- **Category**: Allows you to choose the category of the device.
- **Latitude**: Latitude referenced on Tado for your home and used to retrieve the corresponding weather.
- **Longitude**: Longitude referenced on Tado for your home and used to retrieve the corresponding weather.

As well as your Tado connection information for this home (don't forget to change your password here if you change it on the Tado website!).

Clicking on the **Commands** tab shows a list of all available commands and the option to log numerical values and weather status.
Data updates every 30 minutes, but you can force an update on demand with the **Refresh** command (note that this forces the update of weather data as well as all your devices belonging to this home).

The widget displays the current weather as an image, along with the temperature, current brightness, and the people present at home.

### The Tado User <img src="../images/MyTado_user.png" width="60"/>  

Clicking on a Tado user takes you directly to their configuration page:  
- **Equipment name**: The name you assigned to the person in Jeedom (by default, the name set in Tado will appear).  
- **Parent object**: Indicates the parent object to which the user is associated. You need to define it.  
- **Category**: Allows you to choose the equipment category.  
- **Change Image**: Allows you to choose a picture to personalize the user's identification in the list of objects and the presence on the *home* widget.

Clicking on the **Commands** tab displays a list of all available commands, along with the option to store the obtained values.  

> **Important Information for the 'Distance from Home' Command**  
> The distance from home is calculated based on your Tado configuration of the radius you consider as home (400 meters by default). Tado determines your distance as long as you are within a radius of up to 10 times the home radius (4 kilometers by default). Beyond that, the displayed distance is incorrect since Tado will return this maximum radius (4 kilometers by default, even if you are further away).
> The command shows -1 if the user's location is not enabled on their phone.

### Managing Scenarios

There are no particular constraints when using actions in your scenarios.  
Except for configuration actions for AC modules.  
In this case, you must always first switch to an AC mode other than "auto" before setting a desired temperature (and probably other parameters).  
Otherwise, you will receive an error in the logs informing you of this constraint.

### Troubleshooting

Contact the developer specifying the models of Tado/TadoX devices you own, missing features, or malfunctions, as well as any information you deem useful.  
Do not forget to provide the logs of the plugin and its daemon (be sure to mask personal data).
