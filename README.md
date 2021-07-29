# v40.0.8
* Disallow load purchase on network/telco downtime
* Auto-enable load purchase on network/telco uptime

----

# v40.0.7
* Implement Auto-boot and auto shutdown
   - for Android api v21 and later, unlock OEM and enable auto start using "fastboot oem-off-mode charge 0". Then in the app menu, select "Set Accessibility" and turn on Accessibility for Fox Eloader.
   - for old Android KITKAT, proceed directly to the menu "Set Accessibility" and turn on Accessibility for Fox Eloader.

----

# v40.0.6
* Added backup Short code gateway
* Smart charging updated turn off charging when battery reached 99% and turn on charging when battery goes down to 50%.

----

# v40.0.5
* Kiosk support for smaller screen (non-tablet)
* Set default Connection setting value to "Sms (Globe Shortcode)
* Update default DITO denominations
* Disable back button on pending/processing payment
* Security updates

----

# v40.0.4
* Disable sms notification from the Machine, to prevent consumption of machine regular load
* Delegate sms notification to DafoxTech Gateway
   #### The following commands that will be sent to Machine will be responded by DafoxTech. Gateway
   - bal
   - sales today
   - sales yesterday
   - sales this week
   - sales last week
   - sales this month
   - sales last month
   - Sales YYYY-MM-DD to YYYY-MM-DD

---- 

# v40.0.3
* Support for Gcash Cash-in
### Available Amounts
- 10, 20, 30, 40, 50, 60, 70, 80, 90, 100, 150, 200, 250

* Exit Kiosk Mode on double press of the volume up button

---- 

# v40.0.2

* supports connection over globe shortcode (free sms)
    -  *Machine should use GLOBE SIM card*
    -  *no need monthly maintenance load*

* add support for DITO load

---- 
# v40.0.1

* supports connection over internet instead of sms

* can sync load promos from server

* can manually add network phone prefix
