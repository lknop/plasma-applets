## v49 - September 15 2017

* Fix inability to logout of google calendar which got broken during earlier refactoring.
* Show notification when an event is added or deleted.
* Lots of refactoring needed for supporting different calendar backends.

## v48 - July 7 2017

* Add Spanish translation by Zipristin
* Fix plasmashell crash when closing eventcalendar's config window.
* Support extra timezones in the tooltip based on digitalclock.
* The meteogram colors are now configurable.
* The in progress color in the agenda is now configurable.

## v47 - June 9 2017

* Add German translation by frispete
* Add button in the config to simply installing translations (hopefully it works).
* Ability to set colors in the agenda/meteogram. Only available in the debugging/advanced view for now. A simpler editor will come soonish.
* Scale meteogram/agenda icons based on the DPI.
* Show clickable date in agenda for each day in selected month.
* Wait 100ms after receiving events before updating the interface. Should minimize stuttering when events are loading.

## v46 - April 27 2017

* Add ability to set the radius of the selected date.
* Fix different sized labels (for 1-9 vs 10-31) in the calendar when the cell height is greater than the width.
* French translations by Amathadius.

## v45 - April 22 2017

* Get rid of padding between event summary and the timestamp.
* Polish the Google calendar list in the config. Adding a refresh list button, mark which calendars are read only, and sort the list alphabetically.
* [upstream] Shrink and elide week names like is done with day delegate

## v44 - April 8 2017

* Fix "ConfigSerializedString.qml is missing" error when installed via a package manager that downloaded from GitHub by commiting the file.
* Support event specific colors. When a specific event is assigned a color, a colorId is used rather than a hex color (#ffffff). So we package a hardcoded set of colours for now until we download the user selected colors from the API.

## v43 - April 6 2017

* A notification is now displayed when an event is starting.
* Can now delete non-reoccuring events from the context menu.
* Prepare widget for translations (thanks Victor).
* Use same popup size as digital clock when only the calendar widget is enabled.
* A new event badge has been added which shows all the colors for that day in a line.
* Add toggle for hiding the background when used as a desktop widget.
* Close new event form with Esc
* Support kelvin/fahrenheit freezing points (below freezing the meteogram line turns blue).
* Refactor the config code. Add an advanced debugging view.
* Show calendar colours in the config.
* When the meteogram is disabled, move the timer to the top right, and have the agenda consume the entire left half of the popup.
* Fix timer overlaying the calendar when using a non-default font size.

## v42 - February 14 2017

* Possible fix for emojis in the event summary crashing plasmashell.

## v41 - February 13 2017

* Hide the daily weather column if there's no data.
* Add new clock preset.
* Add debugging mode.

## v40 - February 6 2017

* Can now edit the event summary (except for repeating events) from the right click menu.
* A few HiDPI fixes from @vcucek. Begin testing with 2x DPI.
* [upstream fix] Fix "title" button's height in the calendar.
* Refactor the event fetching code so it's not cluttering UI files.
* Cleanup some debug logging + warnings.
* Change whitespace between weather/date/events in the agenda to padding inside the button.

## v39 - November 30 2016

* Fixed clock height is no longer limited to a max of 99px.
* Fix current date not advancing when used as a desktop widget.
* Fix weather/events being spam fetched XX times when first loaded (using the deferred pattern). This caused the tooltip to jitter for a bit as all the responses came in and caused updates.
* Panel tooltip now shows the seconds + timezone (still follows the locale instead of your 12h/24h setting though).
* Added "Big Number" style for the current date.
* Added a full height single column layout where the agenda is placed above the calendar.
* Refactor cached weather/event models so it's stored at the widget scope rather than the popup scope.
* Refactor most configurable code to not pass config values but look at a global object.

## v38 - October 21 2016

* Fix inability to set the weather affecting new users.
* Fix bug when viewing the weather config page in Kubuntu 16.04.

## v37 - October 15 2016

* Default to using a qdbus command to change the volume (with the GUI).
* Don't force user to hit apply after opening the "Google Calendar" tab in the config.
* Option to toggle outlines of icons when the bg color set by the theme is ugly as sin.
* Added a GUI for chosing your city.
* Lots of work for using Weather Canada as as a data source (still unfinished).
* Show a message to either hide or configure the weather when city is not set.
* Ability to set a fixed clock height.
* Jump by 1% instead of 5% when setting the clock's 2nd line height.
* Added a new event badge with just the decimal number of events that day.

## v36 - August 5 2016

* Show the 3h weather forecast icons in the meteogram.
* Show calendar colour in the calendar tooltip.
* Number of hours shown in the meteogram is now configurable (default: 30 hours).
* Use chronometer icons in the Timer. Also use toggle buttons instead of checkboxes.

## v35 - July 3 2016

* Tooltips for 3h periods for the Meteogram.
* Toggles for hiding the calendar/agenda.
* Periodically refresh the calendar events and update the forecast.
* Fix defaulting to the "bottom bar" event badge when the "theme" event badge isn't supported.
* Change version of QtMultimedia dependency from 5.6 to 5.4.

## v34 - June 14 2016

* Fix clock scaling on vertical panels.
* Use the locale's timeformat by default.
* Can now also choose your theme's calendar event indicator. By default it uses the theme, or the old solid rectangle if on an older version of KDE.
* Included a dots event indicator showing if there's 0-3+ events on that day.
* Performance increase when drawing the agenda (specifically the invisible new event form).
* 24h labels in the meteogram and the calendar tooltips.

## v33 - June 13 2016

* Round percipitation if >1mm.
* Show past events in the current month.
* Fix last selected calendar not saving.
* Properly scale the widget when resized (eg: desktop widget).
* Add a pin button.
* The meteogram now takes up the entire top row when the timer is disabled.

## v32 - May 9 2016

* Fix in-progress multiday events positioning the current day in agenda in the wrong place.

## v31 - May 9 2016

* Highlight current weather, date, and events in progress.
* Add non persistent (bug) sound toggle in the timer.
* Scroll over the timer to add/remove a minute from the duration.
* Show mm percipitation label in each 3h period.
* Fix scrolling to selection. Reenable showing previous events earlier in the current month since it now scrolls to the current date properly.

## v30 - Apr 29 2016

* Fix events from next month not showing in the agenda when on the current month (when in the next 14 days).
* Add optional sound effect when timer completes. Now depends on QtMultimedia.
* Add clock preset with custom color.
* Show current version in the config.

## v29 - Apr 22 2016

* Fix full day events showing an extra day in the calendar.
* Only show events from the current month in the agenda (but always show the next 2 weeks).
* Add a few presets to the clock config.
* Add tooltip to events without events so its stays open when hovering over them.
* Optionally remember the selected calendar in the new event form.

## v28 - Apr 17 2016

* Fix full day events showing an extra day in agenda.
* Add digitalclock's week numbers.
* Add Fahrenheit + Kelvin options.
* Redesign mousewheel config section.

## v27 - Apr 15 2016

* Fix duplication of events longer than a month in the agenda.
* Performance tweak with events with really long durations (like years).

## v26 - Apr 14 2016

* Update meteogram on hour change.
* Event badges each day in the calendar for multiday events.
* Better event date formatting for multiday events.
* Terrible support for use as a desktop widget. A desktop widget is a fixed size, and only shows the popup calendar view. The background border doesn't scale to fit either, but you can resize it to fit the widget by clicking and holding the background, then resizing it.
* Don't serialize the google calendar login code to the config if not logged in.

## v25 - Apr 9 2016

* Calendar borders are optional.
* Multiday events are optionally shown each day in the agenda (not yet shown in the calendar).
* Tooltips when hovering agenda weather and in the calendar.
* Can change clock font and bold each line.

## v24 - Apr 7 2016

* Add current date to month view title when on the current month.
* Add very simple meteogram with 24 hour temp and percipitation. Needs to be rewritten.
* Support vertical panels.

## v23 - Apr 5 2016

* Fix plasmashell crashing in Plasma/Qt 5.6.
* Add ability to customize height of second line in the clock.

## v21 - Mar 29 2016

* Make the weather icons into a button that opens the current city's weather in the browser.
* Hide the weather description text, made the weather icon bigger. Both are customizable.
* Add optional second line in the clock.
* Fix the popup cutting off the bottom sometimes.

## v20 - Mar 26 2016

* Fix transparency of new agenda buttons.

## v19 - Mar 26 2016

* Use the zero padded hh:ss for the default 24h clock format.
* Fix the timeout on the timer completion notification.
* Added a slim coloured line next to events in the event's calendar's colour.
* Clicking a the day in the agenda will open up a quick new event form.
* Clicking the event in the agenda will open the event in the browser.


## v18 - Mar 24 2016

* Can now customize the date/time format in the clock.
* Fix hiding widgets getting permanently hidden, and the popup not getting resized.
* Use start/pause icons in the timer.
* Reduce the spacing + widen the timer buttons.

## v17 - Mar 24 2016

* Show minutes/date in the agenda events if relevant.
* Add ability to toggle the placeholder & timer widgets.
* A single click in the month view scrolls to the agenda item.

## v16 - Mar 23 2016

* Toggle 24 hour clock.
* Update the agenda when the access_token changes (like after the first sync) or when the weather city id is changed, or when calendars are hidden/revealed.
* Properly hide calendars (events aleady fetched were left in the agenda).

## v15 - Mar 23 2016

* Scrolling over the clock controls the volume.
* Support Multiple Calendars.

## v10 - Mar 23 2016

* First release version.
* Syncs with Google Calendar using Device Code OAuth (access token stored in applet configuration) instead of KAccounts.
* Double click a day in the MonthView to open the new event template in the browser.
