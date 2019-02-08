# WatchCuts
WatchCuts lets you trigger the running of shortcuts on your iPhone and iPad from all of your connected iCloud devices. Pair WatchCuts with Cronios — the shortcuts scheduler for iOS — and have your shortcuts run automatically when you complete tasks on your iPhone, iPad, Mac, or Apple Watch!

![WatchCuts](https://adamtow.github.io/watchcuts/images/watchcuts-hero.png)

***

## Table of Contents

{{TOC}}

***

## System Requirements
WatchCuts has the following minimum system requirements:

- iOS 12
- Shortcuts 2.1.2
- Cronios 1.2.0

***

## Installation 
When you first install and WatchCuts, you will be prompted to do the following things:

### 1. Create an Reminders list for WatchCuts
First you will create called `WatchCuts ({{Device Name}})`. WatchCuts will refer to this list for your shortcuts.

1. Tap the **+** button. 
2. In the menu that appears, tap **List**. 
3. Paste the clipboard which contains the word `WatchCuts ({{Device Name}})` where `{{Device Name}}` is the name of you iOS device (minus any special characters). 
4. Tap **Done**. 
5. Return to Shortcuts. 

![Creating the Reminders list](https://adamtow.github.io/watchcuts/images/setup-reminders.png)

### 2. Create a WatchCuts Calendar
Second, create a new calendar in the Calendar app called `WatchCuts`.

1. Tap **Calendars** at the bottom of the screen. 
2. Tap **Add Calendar**. 
3. Paste the clipboard which contains the word `WatchCuts`. 
4. Make sure the account says iCloud. 
5. Tap **Done**. 
6. Return to Shortcuts. 

> Be sure to set the account of the calendar to `iCloud` so your WatchCut Responses can be viewed by all of your iCloud-connected devices. 

WatchCuts will use this calendar to store responses from shortcuts that run via WatchCuts.

![Creating the WatchCuts calendar](https://adamtow.github.io/watchcuts/images/setup-calendar.png)

### 3. Add the WatchCuts Cron Job to Cronios
If you want your shortcuts to run automatically, WatchCuts needs to be running periodically via [Cronios, the shortcuts scheduler for iOS](#cronios). 

>Always run WatchCuts from the Shortcuts Home screen instead of the Edit screen. While it’s not as long of a shortcut as Cronios, LaunchCuts, or GeoCuts, it’s long enough to make things slow if you tap run from the Edit screen. 

Once setup is complete, your next task is to create your first shortcut-reminder in WatchCuts. 

***

## Your First WatchCut Shortcut-Reminder
From the WatchCuts Home screen, do the following to create and test your first WatchCut shortcut-reminder:

1. Tap **Add Shortcuts**. 
2. Choose which shortcuts you want to be able to trigger from other iOS devices. If you want to search for a shortcut, tap the **Search** icon, followed by **Done**. If you choose **Search** and some shortcuts, the Search screen will appear. 
3. Tap **Done** when you have selected your shortcuts. 
4. Switch to the Reminders app on your Mac, Apple Watch, iPhone, or iPad.
5. Go to the `WatchCuts ({{Device Name}})` list in Reminders. You should see the shortcuts that you added in Step 2-3. 
6. Complete one or more the reminders. The last reminder you complete will be the first  shortcut that runs.
7. Wait a few seconds for iCloud to sync your completed tasks to your iOS device. 
8. Return to **WatchCuts** in the Shortcuts app. 
9. Tap **Run Once**. 

![WatchCuts Home](https://adamtow.github.io/watchcuts/images/watchcuts-home.png)

> If you are running WatchCuts on an iPad, place both Shortcuts and Reminders in a Split View so you can see both apps at the same time. 

Your shortcuts should now run on your iOS device. If there were no [errors](#errors), you will see the reminders you completed reappear in the `WatchCuts ({{Device Name}})` Reminders list. 

> WatchCuts only runs tasks that have been completed in the current day. If you completed a shortcut-reminder at 11:59 pm and ran WatchCuts at 12:00 am, the shortcut will not run. 

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
- **Clean Up**: Deletes completed shortcut-reminders in the `WatchCuts ({{Device Name}})` list and WatchCuts Response calendar entries in the `WatchCuts` calendar. Only events that were created on this device will be deleted. [Learn more about the Clean Up command here](#clean-up). 
- **Shortcuts**: A list of shortcuts that are available for running via WatchCuts on this iOS device. Tap on a shortcut to see the [Shortcuts Menu](#shortcuts-menu). 
- **Open Reminders**: Opens the Reminders app. Note: there is currently no way to open Reminders to a specific list, so you will have to navigate to them `WatchCuts ({{Device Name}})` list manually.
- **About**: Displays the about dialog, along with the current version and build number for WatchCuts.
- **Tip Jar**: If you find WatchCuts useful, I'd appreciate a tip!
- **Help**: Displays simple instructions with a link to the documentation you are reading now.
- **Settings**: Opens the [WatchCuts Settings page](#settings).

***

<span id="cronios"></span>
## Running WatchCuts Automatically via Cronios
Pretty cool, eh? You can now trigger shortcuts to run on a specific iOS device from any iCloud-connected device — Mac, iPhone, iPad, iCloud, or Apple Watch. 

>The server time on iCloud.com appears to be running a few seconds or minutes behind the time on your iOS devices. As a result, completing tasks in the Reminders web app on iCloud.com may not be triggered reliably by WatchCuts. 

Make WatchCuts even more powerful by pairing it with [Cronios](http://cronios.com), the shortcuts scheduler for iOS. WatchCuts + Cronios will allow you to run shortcuts **automatically** on specific iOS devices from your iCloud-connected devices. 

To get this up and running, perform the following tasks:

1. Install [Cronios](http://cronios.com) if you haven’t done so already. 
2. Open **WatchCuts**. 
3. Tap **Add WatchCuts to Cronios**. 
4. Choose the frequency that you want WatchCuts to monitor your shortcut-reminders in the `WatchCuts ({{Device Name}})` Reminders list. Every minute will give you the quickest performance. 
5. Cronios will open to the import dialog. Tap **Done** to complete the import.
6. Make sure the imported WatchCuts cron job is enabled. 
6. Tap **Run Continuously** in either Cronios or WatchCuts. 
7. Go to the Reminders app on any of your iCloud-connected devices. 
8. Complete some reminders in the `WatchCuts ({{Device Name}})` list. 
9. Wait for the next minute. 

If Cronios is running and the WatchCuts cron job is enabled, your shortcuts should run automatically.

>Since Cronios works in the background, you can go ahead and switch apps. 

If you return to the Reminders app, you will see the tasks you completed have been re-added. You can then complete them again and the shortcut-reminders will be run automatically again according to the cron job schedule you set for WatchCuts in Cronios. 

***

<span id="shortcuts"></span>
## Shortcuts
The shortcuts list displays all the shortcuts in the `WatchCuts ({{Device Name}})` Reminders list that are managed by WatchCuts.

<span id="shortcuts-menu"></span>
### Shortcuts Menu
If you tap on any of the shortcuts in the Shortcuts list, you'll be presented with the following actions:

![Shortcut Menu](https://adamtow.github.io/watchcuts/images/shortcut-menu.png)

- **Run Shortcut**: Runs the shortcut, suppplying it with a WatchCuts Cronios dictionary item.
- **Edit**: Opens the shortcut for editing. iOS will temporarily switch to mobile Safari for this to work.
- **Remove**: Removes the shortcut from the list.
- **Back**: Return to the WatchCuts Home screen.

### Editing a Shortcut
Tapping Edit from the Shortcut Menu will exit out of Shortcuts and take you to a Mobile Safari page. Safari will then raise an alert asking you to open Shortcuts. Tap **Open** to open the shortcut within the Edit screen. 

![Editing a Shortcut](https://adamtow.github.io/watchcuts/images/shortcut-edit.png)

***

<span id="clean-up"></span>
## Clean Up
As you use WatchCuts, you will accumulate a lot of completed reminders in the `WatchCuts ({{Device Name}})` Reminders list and potential [responses](#responses) in the `WatchCuts` calendar. The Clean Up command is used to delete these items. 

![Cleaning Up In WatchCuts](https://adamtow.github.io/watchcuts/images/clean-up.png)

1. From the WatchCuts Home screen, tap **Clean Up**. 
2. Read the menu prompt and tap **Clean Up Reminders ans Responses**. 
3. If you have a lot of reminders in the `WatchCuts ({{Device Name}})` list and/or responses in the `WatchCuts` calendar, iOS swill prompt you to confirm the deletion. 

WatchCuts **only** deletes reminders and calendar entries from the `WatchCuts ({{Device Name}})` Reminders list and `WatchCuts` calendar. 

### Resetting the Last Run Date
In the Clean Up menu, there is a menu item called Reset Last Run Date. Tapping this will set the Last Run Date in WatchCuts to the current date and time. 

Any reminders that you completed between your last run of WatchCuts and now will be skipped over when you run WatchCuts again. 

***

<span id="settings"></span>
## Settings
WatchCuts can be configured in the following ways from the Settings page:

![WatchCuts Settings](https://adamtow.github.io/watchcuts/images/watchcuts-settings.png)

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
## WatchCuts Responses
Shortcuts that are run via WatchCuts can return data by supplying a `WatchCuts Response` dictionary when they exit. WatchCuts reads this dictionary and creates a new event in the `WatchCuts {{Device Name}}` calendar. iCloud will sync this calendar data to all of your connected devices, including your Apple Watch. 

![A WatchCuts Response](https://adamtow.github.io/watchcuts/images/watchcuts-response.png)

>If you have not created a calendar named `WatchCuts {{Device Name}}`, the WatchCuts Resppnse Dictionary will be ignored. 

You can then look at the results of your shortcuts straight from your iOS Device. This is a convenient way deliver more information than Siri could display or speak to you via voice. You can also use this method to review past shortcut responses, similar to Notification Center. 

Here are the fields that you can fill out in the WatchCuts Response Dictionary:

- **Title**: The title of the WatchCut Response corresponds to the title of the event. 
- **Location**: Maps to the location field of the event. Force-pressing on the calendar event on the Apple Watch will display an option to get directions. 
- **Start Date**: The starting date of the event. If left blank, it will start at the current time. 
- **End Date**: The ending date of the event. If left blank it will be one minute after the starting date. 
- **All Day**: A Boolean value. Specify true to create an All Day event. Specify false or leave blank to create a timed calendar event. 
- **Notes**: Free-form text field for your WatchCuts Response. 

***

<span id="errors"></span>
## Handling Errors

<span id="locked-shortcuts"></span>
### Locked Shortcuts
If a shortcut experiences an error while being run by WatchCuts, it will not run again until you “unlock” or resolve the shortcut in WatchCuts. 

1. Open **WatchCuts**.
2. Tap **Locked Shortcuts**.
3. Select the shortcuts that should be unlocked. 
4. Tap **Done**. 

![Dealing with locked shortcuts.](https://adamtow.github.io/watchcuts/images/shortcuts-locked.png)

Errors occurs for a variety of reasons:

- A time-out occurred and Shortcuts crashed or was terminated by iOS. 
- The shortcut tried to do something in the background that it was not allowed (i.e. retrieve the current location in the background). 
- An unexplained Shortcuts error occurred (i.e. -9806 error). 

When an error happens, WatchCuts and Cronios will terminate. You will have to relaunch Cronios in “Run Continuously” mode again for monitoring to resume.

>If you are using the Cronios Watcher with Cronios, you’ll be alerted that Cronios has stopped within minutes. 

### Paused Shortcuts
WatchCuts will pause any shortcuts that ran if they ran immediately before a shortcut that caused an error. For instance, suppose you completed three reminders in the `WatchCuts ({{Device Name}})`:

1. Shortcut A
2. Shortcut B
3. Shortcut C

Shortcut A runs fine, but Shortcut B has error and WatchCuts, Cronios, and Shortcuts all stop. 

Shortcut B is placed in the Locked Shortcuts group and Shortcut A is placed in the Running/Paused group. 

If you were to run WatchCuts again, this is what will happen:

1. Shortcut A will be skipped since it ran already. 
2. Shortcut B will be skipped because it’s locked. 
3. Shortcut C will run. 

When WatchCuts runs without any errors, it clears out the list of paused shortcuts. This, you can complete Shortcut A again and it will run. Shortcut be will remain locked [until you unlock it](#errors). 

***

<span id="security"></span>
## Security
It goes without saying that you should keep **absolute** control over who has access to your Reminders on all of your devices connected to your iCloud account. 

If WatchCuts is running via Cronios, it will look at the `WatchCuts {{Device Name}}` Reminders List according to its schedule for any new completed tasks. Any reminder that was completed after the last check will run the shortcut with the same name. 

When you are the one completing the tasks, this is very powerful, but if other people are completing these tasks without your knowledge, it can be jarring and potentially dangerous!

>It is **not recommended** to share the `WatchCuts ({{Device Name}})` Reminders list with other people. While there are legitimate use-cases for this, it opens up a whole new realm of potential security problems. 

### Disabling WatchCuts In Cronios
To disable automatic monitoring of your WatchCuts Reminders list, do one of the following:

- Turn off Cronios. 
- Turn off monitoring in WatchCuts.
- Deactivate the WatchCuts cron job in Cronios. 
- Delete the WatchCuts cron job in Cronios. 
- Remove shortcuts in WatchCuts.

***

## Uninstalling WatchCuts
To uninstall WatchCuts, do the following:

- Delete the WatchCuts shortcut from Shortcuts
- Delete the WatchCuts folder in `iCloud Drive/Shortcuts`.
- Delete the Reminders list `WatchCuts {{Device Name}}`. 
- Delete the Calendar named `WatchCuts {{Device Name}}` if présent. 

***

<span id="localization"></span>
## Localization 
WatchCuts is fully localized and ready to be translated in your language.

Visit the [WatchCuts page on GitHub](https://github.com/adamtow/watchcuts) and submit a pull request!

***

## License
Copyright © 2019 Adam Tow • tow.com • @atow

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.