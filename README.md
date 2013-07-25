PAC Stats
=========

**Description**: Usage statistics for PAC developer (a la Cyanogenmod Stats)

CyanogenMod has a feature to report anonymous Statistics to the Cyanogenmod Team: on first boot the user is given the choice to send anonymous statistics to CyanogenMod website (http://stats.cyanogenmod.com).


The submitted data contains:
* **Device hash**: which is a salted MD5 hash of the IMEI (or wifi MAC, if imei is unavailable for some reason)
* **Device name**: the property "ro.product.model" of build.prop
* **Device version**: the property "ro.build.display.id" of build.prop
* **Country**: from the Android API, getNetworkCountryIso
* **Carrier**: from the Android API, getNetworkOperatorName
* **Carier ID**: from the Android API, getNetworkOperator
* **ROM Name**: from the newly added property "ro.pacstats.name"
* **ROM version**: from the newly added property "ro.pacstats.version"

in addition to this data, the database has an extra 2 columns:
* **First registration date**: the first time the device registered on the server
* **Last check-in date**: the last time the device (with same device hash) checked in, to remove inactive devices after 90 days
