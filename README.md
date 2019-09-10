# Domoticz-MoonPhases script
A dzVents script to show moonphase information in Domoticz.
## Installation instructions:

### Create a HERE Dev Account 
First step is to create a freemium developer account via https://developer.here.com/ to get an appid and appcode.
Note your App_id and App_code.

### Upload Custom Images
Upload the zip files in the icon folder in order from 1 to 8 to Domoticz via Setup/More Options/Custom Icons.<br>
If you have no custom icons than the value of the moonphaseicon variable in the script is 100 (default).<br>
If you already have custom icons, count the number and add 100 to it. So if you already have 10 custom icons, then the value of the moonPhaseIcon variable becomes 110.

### Dummy sensors
Create 5 Dummy sensors in Domoticz:
- Moonrise, Text
- Moonset, Text
- MoonPhaseDesc, Text
- MoonPercentage, Percentage
- MoonPhase, Custom (X-axis use a space)

### Edit script variables
Download the script and add it to Domoticz via Setup/More Options/Events. Click on the + and add a dzVent, Global data script.<br>
Paste the contents of the moonphase_script.txt file into the window, overwriting what is already there.<br>
Edit the variables:<br>
- App_id
- App_code
- town = the town where you live
- language = DUT or ENG for Dutch or English
- domo_ip= your domoticz ip-address
- domo_port = your domoticz port number
- 24hour = 24 hours notation for moonset or moonrise time, yes or no.
- moonPhaseIDX = idx number of the dummy sensor named <b>MoonPhase</b>
- moonPhaseIcon = as mentionend above the startnumber of the custom moonphase icons.

Save the script and check the log for any errors. By default the script runs every hour, for testing you can change it to every minute.
