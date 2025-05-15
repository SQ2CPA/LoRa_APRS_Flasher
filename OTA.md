# How to make manual OTA update?

1. Download `ota_upgrade.bin` file for specific device type (`Digi/IGate` or `Tracker`) and specific variant (T-beam, etc.) from [firmware.sq2cpa.pl](https://firmware.sq2cpa.pl)
2. Go to web configuration
3. Go to `Update` page (available at top navbar)
4. Select your `ota_upgrade.bin` file
5. Click `Local Update` button and wait

If you have any problems then please try again. Updates are quite safe and you can't brick your device easily :)

# Remote OTA (without any update bin file)

1. Connect your device to WiFi with internet connection
2. Go to `Update` page (available at top navbar)
3. Click `Remote Update`

Remember that for Remote OTA your need quite stable internet connection. If OTA failed then device will reboot.
