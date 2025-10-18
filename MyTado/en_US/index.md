# <img src="../images/MyTado_icon.png" width="60"/> MyTado Plugin

The **MyTado** plugin allows you to retrieve data from your connected Tado and Tado X devices, as well as weather information managed by Tado.

These data are refreshed regularly according to your active cron selection (between 5 and 30 minutes).

> **Supported devices**
>
> Only the BU0X, BP0, BR0X, CK04, RU0X, SU0X, VA0X, and WR0X models are fully supported as of now (regardless of their version).
> For any unsupported device or if you have issues with any of the listed devices, follow the instructions in the [In case of problems](#in-case-of-problems) section.

---

# Configuration

## Plugin Configuration

1. Go to the plugin configuration.
2. Install dependencies.
3. Launch the daemon.

If the daemon doesn't start, it is possible that the default port (59969) is already in use. In this case, choose an available port (e.g., 59970), save, and then restart the daemon. If the problem persists, consult the [In case of problems](#in-case-of-problems) section.

### Plugin Configuration

First, you can configure:
- The temperature measurement unit (Celsius by default).
- The naming convention for your devices.


**IMPORTANT**: Tado introduced new API limitations in September 2025. Configuration is now **mandatory**:
- **With Auto-Assist** (paid Tado subscription): 20,000 API calls/day allowed
- **Without Auto-Assist** (free): 100 API calls/day maximum

Therefore, here is the required plugin configuration:
1. **Select your Auto-Assist mode**: This will select ideal options for the following settings, which you can still adjust (but be sure of what you're doing)
2. **Adjust synchronization frequency** according to your needs:
   - With Auto-Assist: 15-minute synchronization recommended
   - Without Auto-Assist: hourly synchronization recommended (or less frequent)
3. **Enable/disable optional synchronizations**:
   - Weather synchronization (consumes API calls)
   - Geolocation synchronization (consumes API calls)

> **DECISION HELP**: The API Call Counter
>- View your real-time API call consumption in the configuration
>- The counter automatically resets to zero each day
>- Visual alerts appear if you approach the limit

> **Required Action**: If you haven't configured these settings yet, a notification will appear in your configuration. Configure these options to ensure proper plugin operation.

### Configuring your home

After saving the correct plugin configuration (see above):

1. Close the configuration page.
2. Click on "Add a home".
3. Name your home (the name can be different from the one on Tado).
4. Enter the exact name (case-sensitive) of your home on the Tado app.
5. Save your home.
6. Click on **Connect to Tado** and follow the authentication procedure.

Once the correct information is entered, the devices will be automatically synchronized. Close the home to check if your devices appear. If not, refresh the page or check the logs.

> **INFO**
>
> If you have both Tado *and* TadoX devices, you must create a home for each of your accounts. All devices will be listed, regardless of their origin.

## Device Configuration

> **REMINDER**
>
> Use the **Sync** command to retrieve any new device you've added or newly supported by a plugin update.

### Tado Connected Devices
<img src="../images/WR0X.png" width="60"/><img src="../images/BU0X.png" width="60"/><img src="../images/RU0X.png" width="60"/><img src="../images/VA0X.png" width="60"/><img src="../images/VA04.png" width="60"/><img src="../images/RU04.png" width="60"/><img src="../images/CK04.png" width="60"/>

Clicking on a Tado device gives you access to:

- **Device name**: Based on its serial number and zone (by default, you can change the naming convention in the plugin configuration).
- **Parent device**: To be defined according to your organization.
- **Category**: Choose the device category.

**Commands** tab:
- List of available commands.
- Option to log numerical values.
- Manual refresh possible with the **Refresh** command.

On the dashboard, the widget shows the device's image, its information, and current configuration.

Available modes:
- **Autonomous**: Following Tado's schedule.
- **Manual**: Direct control of settings.
- **Off**: The device is turned off.

> **Important:**
> Any manual temperature change will affect *all* devices in the same zone (Tado behavior).

### Tado Home <img src="../images/HomeEq.svg" width="60"/>

Available information:
- Device name
- Parent device
- Category
- Latitude / Longitude (used for weather)

Available commands:
- Data logging (weather and others)
- Manual update possible (this will update all devices in the home at the same time)

The widget displays: weather, temperature, brightness, presence.

### Tado User <img src="../images/MyTado_user.png" width="60"/>

Configurable settings:
- User name
- Parent device
- Category
- User image (customizable)

**Commands** tab: list of commands, possibility to log data.

> **Home distance**:
> - Tado returns only a relative distance (between 0 and 1)
> - MyTado provides a representation in km, but this is experimental since there is no information on how the relative value is calculated
> - Returns **-1** if the user's location is not enabled on the phone.

---

# Managing Scenarios

No special constraints, except **for AC modules**:
Before configuring a temperature or setting, **change the AC mode** (different from "auto"). Otherwise, an error will appear in the logs.

---

# In case of problems

1. Set **MyTado** logs to **debug** mode.
2. Restart the daemon.
3. Check the logs to identify the issue.

Otherwise, check the [FAQs](#faqs), and lastly the [Request help](#request-help) section.

## FAQs

### Fatal Error: [Errno 98] address already in use

The communication port between your Jeedom and the daemon (default is 59969) is in use. Change it to another one (e.g., 59970) in the configuration, and then restart the daemon.

### Missing Token

Tado invalidated the current token. Go to your home device > **Connect to Tado** to reauthenticate.

### Empty dependencies and daemon panels

Check your Debian version. You need at least Debian 11 (which provides PHP 7.4+ and Python 3.9+ required for the plugin to work properly). You must update your Jeedom installation.

## Request help

1. Check if your problem is already listed in the [Jeedom community](https://community.jeedom.com/tag/plugin-mytado)

2. If not, create a new topic and provide:
   - Your Jeedom configuration
   - The Tado/TadoX models you use
   - The full **MyTado** and **MyTado_daemon** logs (attached files), ensuring they contain the steps leading to the issue (in debug mode!)

> **Mask your personal data in the logs before posting!**

# Other recommendations

1. Please leave a review on the market if you like this plugin.
2. Share your improvement ideas with the developer!

---

**Thank you for using the MyTado plugin!**

Your feedback is valuable to continue improving it 😊
