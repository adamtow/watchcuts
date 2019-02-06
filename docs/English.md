# WatchCuts
WatchCuts and Cronios lets you trigger the running of shortcuts on iPhone **and** iPad straight from your connected iCloud devices, including your Apple Watch and your Mac!


## System Requirements
WatchCuts has the following minimum system requirements:

- iOS 12
- Shortcuts 2.1.2
- Cronios 1.2.1

## Retrieving Responses From Shortcuts Run Via WatchCuts
Shortcuts that are run via WatchCuts can return data by supplying a `WatchCuts Response` dictionary when they exit. WatchCuts reads this dictionary and creates a new event in the `WatchCuts {{Device Name}}` calendar. 

>If you have not created a calendar named `WatchCuts {{Device Name}}`, the WatchCuts Resppnse Dictionary will be ignored. 

You can then look at the results of your shortcuts straight from your iOS Device. This is a convenient way deliver more information than Siri could display or speak to you via voice. You can also use this method to review past shortcut responses, similar to Notification Center. 

Here are the fields that you can fill out in the WatchCuts Response Dictionary:

- **Title**: The title of the WatchCut Result corresponds to the title of the event. 
- **Location**: Maps to the location field of the event. Force-pressing on the calendar event on the Apple Watch will Display an option to get directions. 
- **Start Date**: The starting date of the event. If left blank, it will start at the current time. 
- **End Date**: The ending date of the event. If left blank it will be one minute after the starting date. 
- **All Day**: A Boolean value. Specify true to create an All Day event. Specify false or leave blank to create a timed calendar event. 
- **Notes**: Free-form text field for your WatchCuts Response. 


## Security
It goes without saying that you should keep **absolute** control over who has access to your Reminders on all of your devices connected to your iCloud account. 

If WatchCuts is running via Cronios, it will look at the `WatchCuts {{Device Name}}` Reminders List every few minutes for new completed tasks. Any reminder that was completed after the last check will run the shortcut with the same name. 

### Disabling WatchCuts In Cronios
To disable automatic monitoring of your WatchCuts Reminders list, do one of the following:

- Turn off Cronios. 
- Deactivate the WatchCuts cron job in Cronios. 
- Delete the WatchCuts cron job in Cronios. 
- Remove shortcuts in WatchCuts.

## Uninstalling WatchCuts
To uninstall WatchCuts, do the following:

- Delete the WatchCuts shortcut from Shortcuts
- Delete the WatchCuts folder in `iCloud Drive/Shortcuts`.
- Delete the Reminders list `WatchCuts {{Device Name}}`. 
- Delete the Calendar named `WatchCuts {{Device Name}}` if présent. 