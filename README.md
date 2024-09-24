# v41.0.7
- Video ads
- Custom theme (Footer texts, and Kiosk background)
- Bluetooth thermal printer integration for receipt printing  (Any bluetooth thermal printer models with minimum 58mm paper width are supported).
       1. Pair your bluetooth printer from android bluetooth settings.
       2. Tap "Bluetooth Printer" in the DafoxTech Kiosk app menu.
       3. Enable or check "Print Receipt" from your online portal machine setting.
       
- Auto-sync settings when online portal settings changed (Machine need to be connected to internet).
- Bulk apply settings to all when fees changed.
- Added 21 new ecash providers like Palawanpay and more ...
- Remote machine commands now easily accessible sa online portal
- Wallet checking before transaction.
- Fixes for the frozen back button on some android versions
- Instant cash-in via Palawan

** New version of our app: POS mode for manual payment**

# v41.0.0
**Warning: Before update, make sure that you have a PC ready with adb driver. Android device owner command is now required for security reason. Some machines that has not been setup correctly will be required to set device owner using a PC with adb driver. All of the steps here http://bit.ly/43LZqvu should be followed accordingly.**

- New Kiosk UI
- New feature: Bills Payment
   - You need to activate the **Bills Payment** service on your **Online Portal** -> **License & E-loaders** -> **E-loaders**
   - Set your fee per biller in the **Bill Fees** page
- 2 available themes: Modern or Classic
- New Shortcode (**Smart Shortcode**): Free sms shortcode for SMART/TNT/SUN machine sim cards.
- Kiosk mode new menu options
    - To show menus, double press the **power button** (1 second interval, make sure that the screen turns off and ON), and then double press the **volume +** button
    - Sync Settings (_needs internet to show_). This will sync your E-load and bills payment settings from your online portal to your machine.
- Removed app menus: Set trusted number, Eload Products
    - To transfer or change trusted number, you can do it from your online portal **License & E-loaders** -> action button **Transfer**
    - To change or set pricings, you can do it from your online portal **E-Load Pricing** and **Bill Fees**. Then sync it to your machine using the kiosk menu (_double press power and then double press volume +_) **Sync Settings**. 
    - Other way to popup the **Sync setting menu**, is to send command “Update Machine” using the send command action from the online portal. 


# v40.4.0
* Remove exit kiosk button from the Inquire credits page
* Disable manual loading
* Fixed loading screen issue on some lower android versions
  
# v40.3.4
* Add handler for ghost credits caused by loose connection or other hardware issues

# v40.3.3
* Added Coins.ph cash-in
* Amount input for ecash cash-ins
* Re-arranged services option

# v40.3.1
* Added Maya cash-in
* Enhancements & security fixes
* Enhanced products syncing
   - you can now set pricing per provider denominations in your online portal and they will reflect on your machines pricing after a successful products syncing
* New machine command: sync eload-products
   - You can send the command on your online portal: Licenses & E-loaders -> Eloaders, actions column "Send Command"
   - Will only take effect on internet connection type setup.
   - Trigger the machine to fetch updated eload products and denomination pricings
   - Advisable to send this command during standby-mode state when no interactions on the machine's screen.
* Full support for internet only connection type, transaction confirmation will now work via internet.
   - Sim card is still advisable for sms machine commands to take effect.
   - For machines with sim card, please activate via Online Portal.
   - For cheaper internet, sim with no expiry data promo is advisable like SMART magic data
* New machine command: inquire-credits[space]CUSTOMER#
   - You can send this command via messenger or viber. The system will respond to your trusted number.
* New machine command: update-credits[space]Customer#[space]AMOUNT
   - You can send this command via messenger or viber. This will be usable if you want to update the customer's credits, set the AMOUNT to 0 to clear credits.



# v40.2.1
* Fixes transaction sending error marked as incomplete

# v40.2.0
* added auto-shutdown (no-prompt) on selected android models (Android API version 21)
   - This will be usable in case of power outage to prevent draining of android battery.
   
# v40.1.9
- Exit kiosk button click trigger changes
   * From double press volume+ changed to double press power and then volume+
   
   
# v40.1.7
* Disable pending transaction checking if **Internet Connection** is used
* Bugfixes and optimizations

After installing this version, please update the eload products using the following steps:

1.  Make sure that the tablet is connected to the internet via Wifi or Data connection
2. Go to Fox Eloading app **Top-right** menu (3 dots).
3. Select **Eload Products**
4. Tap or click the circle button with rotating arrow icon. Tap YES on the prompt.
5. Wait for the success message

# v40.1.6
* implement handler for gateway downtime - disable kiosk purchase when there's 2 or more pending transactions.


# v40.1.5
* Add confirmation/prompt when selecting eload promo


# v40.1.4
* FIXES unconfirmed transactions caused by an update from telco that affects some of our machines


# v40.1.3
* Updated GSM gateway numbers


# v40.1.2
* Added new Globe Short code gateway

_Go to Top-right menu and then click **Connection Setting** and select **SMS (GLOBE Short code 2)**_ 


# v40.1.0
* New Gcash amounts AVAILABLE
   - GCASH500, GCASH800, GCASH1000
   - System Transaction fee would be 1.5% + 5
     _(1.5% is the rebates that was added to your account when you replenish your wallet)_
      Fox example, you will set the price in your machine to:
      GCASH500 = 500 + 7.5[1.5%] + 5[system fee] + 10 [your profit]
      GCASH800 = 500 + 12[1.5%] + 5[system fee] + 10 [your profit]

----
      
# v40.0.9
* FIX serious security vulnerability

----

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
