
---
title: Setup
permalink: /setup
classes: wide
header:
  overlay_color: "#000000"
  overlay_filter: "0.0"
  overlay_image: /assets/vendor/weatherlink/images/landing.jpg
---

Click on the Account icon (the leftmost of these in the right side navigation bar).
<br><br>
<img src="./AccountIcon.png" alt="AccountIcon">
<br><br>

From there, click on the Account Integration pulldown and select "Azure FarmBeats".
<br><br>
<img src="./AccountIntegration2.png" alt="AccountIntegration">
<br><br>

This should bring up the Azure FarmBeats window.  If you have yet to set up your connection, the window will look like this:
<br><br>
<img src="./UI_without_data.png" alt="UI_without_data">
<br><br><br>
Let's go through each of the fields and the selections.
<ul>
	<li>Documentation</li>
	That would be this document that you are currently reading.<br><br>

	<li>Display Name</li>
	This is a free-form field to describe your setup.  It could be something like "Dave's Farm".<br><br>

	<li>API Endpoint</li>
	This is a field that should be provided from your Azure FarmBeats account.
	It is a custom URL for your account.<br><br>

	<li>Tenant Id</li>
	This is a field that should be provided from your Azure FarmBeats account.
	This is basically a "group ID".<br><br>

	<li>Client Id</li>
	This is a field that should be provided from your Azure FarmBeats account.
	This is basically your "account Id".<br><br>

	<li>Client Secret</li>
	This is a field that should be provided from your Azure FarmBeats account.
	This is considered to be the confidential "account password".<br>
	It is normally shown as asterisks ("***").  The eye icon will show/hide the actual value.<br><br>

	<li>EventHub aka EventHub Connection String</li>
	This is a field that should be provided from your Azure FarmBeats account.<br>
	This is also considered to be confidential.<br>
	This is a long, string containing several snippets of "someName=someValue"-type sections.<br><br>

	<li>Telemetry Start Date</li>
	This is the date from which you want Historical Data to be sent.
	Say you are filling out this form on December 1 2019.  <br>
	However, you're equipment had been setup and collecting data since July 3rd 2019.<br>
	If you want all that data from July 3rd until now to be sent to FarmBeats, select July 3rd 2019 as the Telemetry Start Date.<br>
	Once your connection is fully established, then both LIVE telemetry data as well as 
	the "Historical" telemetry data (from July 3rd until now) will be sent to FarmBeats.<br><br>
	Note that this historical data can easily generate massive amounts of data.<br>
	The record count is grossly like: (num stations * num records/day * num days).<br>
	Under certain situations, this could be 10s of thousands of records which could take days to be generated and then sent to Azure FarmBeats.
	<br><br>
	
	<li>Available EM Stations</li>
	This alerts you to the total number of EM stations that you currently own or are shared to your accounts.<br>
	If this number is not what you expect, go back and check your configuration.<br><br>

	<li>Last Telemetry Sent</li>
	This value shows the datetime of the last telemetry record sent to FarmBeats for this account.<br>
	If nothing has yet to be sent, then "--" will be displayed.<br><br>

	<li>Connection Status</li>
	This shows the current condition of the connection to your FarmBeats installation.<br>
	There are 3 different statusses:<br>
	<ul>
		<li>None or "--"</li>
		Indicates that no connection has even be attempted yet.<br><br>

		<li><img src="./greenCheck.png" alt="greenCheck"></li>
		Indicates that the connection is currently up/good.<br><br>

		<li><img src="./redX.png" alt="redX"></li>
		Indicates that the connection is currently down/disconnected.<br><br>
	</ul>

	<li>Unlink</li>
	Clicking on this will terminate the link or connection from WeatherLink to Azure FarmBeats for your data.<br><br>
	This effectively stops data from ever being sent from WeatherLink to Azure FarmBeats again.

	<li>Exit</li>
	Exit the page.<br><br>

	<li>Save</li>
	Clicking on this does:<br>
	<ul>
		<li>Check data validity</li>
		A quick check of the required entry fields is made to see if the data could possibly be valid.<br>
		For example, the lengths of the fixed length fields are validated.<br><br>

		<li>Connection Test</li>
		Using the given data, a test connection is attempted.  This can can take up to 15 seconds.<br>
		If this fails, a detailed error message will be shown.<br>
		Please ensure that you haven't lost any characters cut-n-pasting into these fields.<br>

		<li>Save data to the database</li>
		If the test connectiono succeeds, the data will be saved to the database.<br>
		This begins an up to 20 minute long process for the "back end servers" to process the request<br>
		and being to start the data flowing.<br><br>

		<li>Success Message</li>
		<br><br>
		<img src="./AddAccepted.png" alt="AddAccepted">
		<br><br>
		Note that the 20 minutes is an approximate value.

	</ul>
</ul>

<h3 id="AddInProgress">Waiting to Add</h3>

Once you've entered data into all the fields and have successfully saved your data, you must then wait for the "backend servers" 
to process this request.  <br>
While this request is being processed, we cannot allow you to edit or change any data.  <br>
Therefore, you will see the following graphic anytime you click on the "Azure FarmBeats" pulldown:
<br><br>
<img src="./AddInProgress.png" alt="AddInProgress">
<br><br>

<h2 id="dataflow">Verifying Data is Flowing</h2>

<h3 id="wl_dataTab">Verifying Data is Flowing into WeatherLink</h3>

Before data can be sent to FarmBeats, it has to be received by WeatherLink.
Here is how to verify that your data is being received.

<br><br>
<img src="./dataTab.png" alt="dataTab">
<br><br>

Above is the data tab. Let's try to verify that data is flowing for your station called YourStationName.
<ul>
	<li>Select the Station</li>
	Make sure that YourStationName is selected in the pulldown in the upper-right station pulldown.
	<br><br>

	<li>Make sure the required telemetry fields are selected</li>
	On the right-hand navigation pane, you should find YourStationName as a name in bold (as Weather Station is shown above).<br>
	Under that, make sure the required telemetry fields (i.e., Temp, SoilMoisture, etc.) are shown as selected.
	<br><br>

	<li>Select the correct date & time</li>
	In the upper left-hand corner, select today's date and a span of time that includes NOW (for example, span: 1 day).
	<br><br>

	<li>Scroll up/down to find the most recent time</li>
	<br>

	<li>Scroll right/left to find YourStationName</li>
	Note that a barometer for some station is just about to be scrolled to the left off the page (above)<br>
	and a WeatherStation called "Weather Station" is being shown.
	<br><br>

</ul>

Once all that has been accomplished, you should be showing the current data that is being generated by YourStationName.<br>
If you see data (as is shown in the graphic), then your system is properly sending data to WeatherLink.<br>
<br>
If YourStationName is not available in the pulldown, then it is not configured properly.<br>
If the system does not show a current time for YourStationName, then WeatherLink is not receiving data for your system.<br>
If all the field values in the table display as "--", then WeatherLink is configured to receive data but is not actually receiving data from YourStationName.<br>

<h3 id="wl_dataTab">Verifying Data is Flowing into FarmBeats</h3>

<ul>
	<li>Ensure that data is flowing into WeatherLink</li>
	See the section above.
	<br><br>

	<li>Ensure that the WeatherLink side seems to be sending data</li>
	Go back to the Account page.  Select "Azure FarmBeats" from the pulldown to show the FarmBeats page.<br>
	It should look something like this:

	<br><br>
	<img src="./UI_with_data.png" alt="UI with data">
	<br><br>

	Notes:<br>
	<ul>

		<li>The Last Telemetry Sent and Connection Status fields. These should show (ideally) a green checkmark and a sent date that is pretty recent.</li>
		<li>If you only have 1 EM system and it is on a 15 minute plan (for example), then this field would only update every 15 minutes.</li>
		<li>If you have 5 EM system each on a 5 minute plan (and with unrealistically perfect timing), then this field could update every minute.</li>
		<li>If you have (or have shared to you) multiple EM systems, then it could be the minimum minutes plan for all of those systems.</li>
		<li>Note that this is *not* an automatically updating page; it shows the status for when the page was put up.  If you want updated data, close the page and bring it back up again.</li>
	</ul>
	<br>

	<li>Ensure that FarmBeats is receiving the data</li>

	<br><br>
	To know more about FarmBeats, please visit: <a href="https://aka.ms/FarmBeatsdocumentation">their documentation.</a> 
	<br><br>
</ul>
