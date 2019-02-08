# WatchCuts
WatchCuts and Cronios lets you trigger the running of shortcuts on iPhone **and** iPad straight from your connected iCloud devices, including your Apple Watch and your Mac!

***

## System Requirements
WatchCuts has the following minimum system requirements:

- iOS 12
- Shortcuts 2.1.2
- Cronios 1.2

***

## Installation 
When you first install and WatchCuts, you will be prompted to do the following things:

1. Create a Reminders list called `WatchCuts ({{Device Name}})`. WatchCuts will refer to this list for your shortcuts. 
2. Create a Calendar called `WatchCuts`. WatchCuts will use this calendar to store (optional) responses from shortcuts that run via WatchCuts. 
3. Add the WatchCuts cron job to Cronios. If you want your shortcuts to run automatically, WatchCuts needs to be running periodically via Cronios, the shortcuts scheduler for iOS. 

>Run WatchCuts from the Shortcuts Home screen instead of the Edit screen. While it’s not as long as shortcuts like Cronios, LaunchCuts, or GeoCuts, it’s long enough to make things slow. 

Once setup is complete, let’s add your first shortcut to WatchCuts!

***

## Your First WatchCut Shortcut
From the WatchCuts Home screen, do the following to create and test your first WatchCut shortcut:

1. Tap **Add Shortcuts**. 
2. Choose which shortcuts you want to be able to trigger from other iOS devices. If you want to search for a shortcut, tap the Search icon, followed by Done. If you choose Search and some shortcuts, the Search screen will appear. 
3. Tap Done when you have selected your shortcuts. 
4. Switch to the Reminders app on your Mac, Apple Watch, iPhone, or iPad.
5. Go to the `WatchCuts ({{Device Name}})` list. You should see the shortcuts that you added in Step 2-3. 
6. Complete one or more the reminders. The last reminder you complete will be the first  shortcut that runs.
7. Return to WatchCuts in the Shortcuts app. 
8. Tap Run Once. 

Your shortcuts will now run on your iOS device. If there were no errors, you will see the reminders you completed reappear in the `WatchCuts ({{Device Name}})` Reminders list. 

***

## Running WatchCuts Automatically via Cronios
Pretty cool, eh? You can now trigger shortcuts to run on a specific iOS device from any iCloud-connected device — Mac, iPhone, iPad, or Apple Watch. 

>The server time on iCloud.com appears to be running a few seconds or minutes behind the time on your iOS devices. As a result, completing tasks in the Reminders web app on iCloud.com may not be triggered by WatchCuts. 

What makes WatchCuts even more powerful is when you pair it with Cronios, the shortcuts scheduler for iOS. This allows you to run shortcuts **automatically** on specific iOS devices from any iCloud-connected device. 

To get this up and running, perform the following tasks:

1. Install [Cronios](http://cronios.com) if you haven’t done so already. 
2. Open WatchCuts. 
3. Tap **Add WatchCuts to Cronios**. 
4. Choose the frequency that you want WatchCuts to monitor your shortcut-reminders in the`WatchCuts ({{Device Name}})` Reminders list. Every minute will give you the quickest performance. 
5. Cronios will open to the import dialog. Tap Done to complete the import.
6. Make sure the imported WatchCuts cron job is enabled. 
6. Tap Run Continuously in either Cronios or WatchCuts. 
7. Go to the Reminders app on any of your iCloud-connected devices. 
8. Complete some shortcut-Reminders. 
9. Wait for the next minute. 

If Cronios is running and the WatchCuts cron job is running, your shortcuts should run automatically. 

If you return to the Reminders app, you will see the tasks you completed re-added. You can then complete them again and the shortcut-reminders will be run automatically again. 

***

## The WatchCuts Interface
The WatchCuts Home is where you'll add new shortcuts, remove existing shortcuts, delete completed reminders and WatchCuts response events, evaluate any shortcut reminders, and start Cronios.

![WatchCuts Home](https://adamtow.github.io/watchcuts/images/watchcuts-home.png)

- **Enable Monitoring**: Master ON/OFF switch for WatchCuts. If disabled, WatchCuts will not run in either Run Once mode or when called by Cronios.
- **Add WatchCuts to Cronios**: Until you install the WatchCuts cron job into Cronios, this menu item will appear. Tap it to start the cron job import process.
- **Run Continuously in Cronios**: Starts up Cronios in "Run Continuously" mode. Provided you have added the WatchCuts cron job to Cronios, WatchCuts will now be monitoring completed shortcut-reminders in the `WatchCuts ({{Device Name}})` list.
- **Run Once**: Instructs WatchCuts to find any shortcut-reminders that have been completed since the last run date. Shortcuts for newly completed reminders will then run.
- **Add Shortcuts**: Adds shortcuts from WatchCuts and shortcuts-reminders to the `WatchCuts ({{Device Name}})` list.
- **Remove Shortcuts**: Removes shortcuts from WatchCuts and shortcuts-reminders to the `WatchCuts ({{Device Name}})` list.
- **Clean Up**: Deletes completed shortcut-reminders in the `WatchCuts ({{Device Name}})` list and WatchCuts Response calendar entries in the `WatchCuts` calendar. Only events that were created on this device will be deleted.
- **Shortcuts**: A list of shortcuts that are available for running via WatchCuts on this iOS device.
- **Open Reminders**: Opens the Reminders app. Note: there is currently no way to open Reminders to a specific list, so you will have to navigate to them `WatchCuts ({{Device Name}})` list manually.
- **About**: Displays the about dialog, along with the current version and build number for WatchCuts.
- **Tip Jar**: If you find WatchCuts useful, I'd appreciate a tip!
- **Help**: Displays simple instructions with a link to the documentation you are reading now.
- **Settings**: Opens the [WatchCuts Settings page](#settings).

### Shortcuts Menu
If you tap on any of the shortcuts in the Shortcuts list, you'll be presented with the following actions:

![WatchCuts Settings](https://adamtow.github.io/watchcuts/images/watchcuts-settings.png)

- **Run Shortcut**: Runs the shortcut, suppplying it with a WatchCuts Cronios dictionary item.
- **Edit**: Opens the shortcut for editing. iOS will temporarily switch to mobile Safari for this to work.
- **Remove**: Removes the shortcut from the list.
- **Back**: Rrturn to the WatchCuts Home screen.

![Editing a Shortcut](https://adamtow.github.io/watchcuts/images/shorcuts.edit.png)


***

<span id="settings"></span>
## Settings
WatchCuts can be configured in the following ways from the Settings page:

![WatchCuts Settings](https://adamtow.github.io/watchcuts/images/watchcuts-settings.locked.png)

- **Run at Launch**: Look for and run any shortcut-reminders since the last time WatchCuts ran an evaluation.
- **Allow WatchCut Responses**: Shortcuts can be developed to return a response to WatchCuts. Disabling this feature prevents WatchCuts Responses from being added to this iOS device. [Learn more about WatchCuts Responses here](#watchcut-responses).
- **Show Notifications**: Enable to display the result of WatchCuts evaluating your shortcut-reminders.
- **Check for Update Automatically**: As startup, WatchCuts will check Routinehub.co for any updates to WatchCuts.
- **Enable Debug Mode**: Displays banners during operation for debugging purposes.
- **Tools**
	- **Add WatchCuts to Cronios**: Adds the WatchCuts cron job to Cronios.
	- **Change Language**: WatchCuts comes default with English, but it's fully prepared to be localized.
	- **Check for Updates**: Manually check for updates of WatchCuts on Routinehub.co.
	- **Reset**: Resets WatchCuts' settings or erase all content and settings.
	- **Back**: Returns to the WatchCuts Home screen.

***

<span id="watchcut-responses"></span>
## Retrieving Responses From Shortcuts Run Via WatchCuts
Shortcuts that are run via WatchCuts can return data by supplying a `WatchCuts Response` dictionary when they exit. WatchCuts reads this dictionary and creates a new event in the `WatchCuts {{Device Name}}` calendar. iCloud will sync this calendar data to all of your connected devices, including your Apple Watch. 

>If you have not created a calendar named `WatchCuts {{Device Name}}`, the WatchCuts Resppnse Dictionary will be ignored. 

You can then look at the results of your shortcuts straight from your iOS Device. This is a convenient way deliver more information than Siri could display or speak to you via voice. You can also use this method to review past shortcut responses, similar to Notification Center. 

Here are the fields that you can fill out in the WatchCuts Response Dictionary:

- **Title**: The title of the WatchCut Response corresponds to the title of the event. 
- **Location**: Maps to the location field of the event. Force-pressing on the calendar event on the Apple Watch will display an option to get directions. 
- **Start Date**: The starting date of the event. If left blank, it will start at the current time. 
- **End Date**: The ending date of the event. If left blank it will be one minute after the starting date. 
- **All Day**: A Boolean value. Specify true to create an All Day event. Specify false or leave blank to create a timed calendar event. 
- **Notes**: Free-form text field for your WatchCuts Response. 

## Handling Errors
If a shortcut has an error while being run by WatchCuts, it will not run again until you “unlock” or resolve the shortcut in WatchCuts. 

1. Open **WatchCuts**.
2. Tap **Locked Shortcuts**.
3. Select the shortcuts that should be unlocked. 
4. Tap **Done**. 

![Dealing with locked shortcuts.](https://adamtow.github.io/watchcuts/images/shortcuts-locked.png)

## Security
It goes without saying that you should keep **absolute** control over who has access to your Reminders on all of your devices connected to your iCloud account. 

If WatchCuts is running via Cronios, it will look at the `WatchCuts {{Device Name}}` Reminders List every few minutes for new completed tasks. Any reminder that was completed after the last check will run the shortcut with the same name. 

### Disabling WatchCuts In Cronios
To disable automatic monitoring of your WatchCuts Reminders list, do one of the following:

- Turn off Cronios. 
- Turn off monitoring in WatchCuts.
- Deactivate the WatchCuts cron job in Cronios. 
- Delete the WatchCuts cron job in Cronios. 
- Remove shortcuts in WatchCuts.

## Uninstalling WatchCuts
To uninstall WatchCuts, do the following:

- Delete the WatchCuts shortcut from Shortcuts
- Delete the WatchCuts folder in `iCloud Drive/Shortcuts`.
- Delete the Reminders list `WatchCuts {{Device Name}}`. 
- Delete the Calendar named `WatchCuts {{Device Name}}` if présent. 