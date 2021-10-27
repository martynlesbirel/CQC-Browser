# CQC-Browser

A simple 3 screen Power App with two flows that demonstrates usage of the [CQC Browser Independent Connector](https://docs.microsoft.com/en-us/connectors/cqcdata/).

The first allows the entry of a complete or partial post code.

This is then passed to the _Get Locations_ flow which pulls back the current list of locations filters them against the required post code and returns the resulting list to the Power App.

The second screen then displayed the resulting list in a gallery allowing the user to select a facility.

When a facility is selected it's id is passed to the _Get Location Details_ flow which then fetches the location details and trims them down to a subset for the Power App before returning them.

The final screen will display a locations details. The web site address, if available provides a link to that address which will open up in a seperate browser tab. The ratings table if clicked on will pull down the related report in PDF format and display that in a seperate browser tab as well. 

___Installation___

Create a connect first calling it _CQC Connector_.

Then import the canvas app package directly remember during the import to specify your newly created CQC Connector as the one the Power App should use.

Once the Power App is imported check the flows you should have two new ones called _Get Locations_ and _Get Location Details_ ensure these are turned on. Although they will have been imported they are turned off and the Power App needs them to function.

Once the flows are enabled you should be able to use the Power App as you wish.
