
---
title: App
permalink: /app
classes: wide
header:
  overlay_color: "#000000"
  overlay_filter: "0.0"
  overlay_image: /assets/vendor/weatherlink/images/landing.jpg
---


<!DOCTYPE html>
<html>

<head>
  <title>FarmBeats Trouble Shooting Guide</title>
  <meta charset="UTF-8">
  <style>
      hr { 
        display: block;
        margin-top: 0.5em;
        margin-bottom: 0.5em;
        margin-left: auto;
        margin-right: auto;
        border-style: inset;
        border-width: 1px;
      } 
      h1 {
        text-align: center;
        text-transform: uppercase;
      }
      body {
        font-family: "Lato", sans-serif;
	background-color: Gainsboro;
      }

      .sidenav {
        height: 100%;
        width: 20%;
        position: fixed;
        z-index: 1;
        top: 0;
        left: 0;
        background-color: #353535;
        overflow: auto;
        padding-top: 20px;
      }
      
      .sidenav a {
        padding: 6px 6px 6px 26px;
        text-decoration: none;
        font-size: 22px;
        color: #818181;
        display: block;
      }
      
      .sidenav a:hover {
        color: #f1f1f1;
      }
      
      .main {
        margin-left: 50px; /* Same as the width of the sidenav . Use 250 if doing sidenav */
      }

      /* numbering headings */
	body { counter-increment: H1; } 	/* Create the counter for H1 */
	h1:before {
  	/*content: counter(H1) ". "; */ 	/* Print the H1 number */
  	counter-increment: H1; 	/* Add 1 to next H1 */
	}
	h1 { counter-reset: H2; }
	h2:before {
  	content: counter(H1) "." counter(H2) " ";
  	counter-increment: H2;
	}
	h2 { counter-reset: H3; }
	h3:before {
  	content: counter(H1) "." counter(H2) "." counter(H3) " ";
  	counter-increment:H3;
	}
      
      @media screen and (max-height: 450px) {
        .sidenav {padding-top: 15px;}
        .sidenav a {font-size: 18px;}
      }
</style>
</head>
<body>

<!--
	Comment out sidenav for now

<div class="sidenav">
  <a href="#title">(top)</a>
  <a href="#bluetooth">Bluetooth</a>
  <a href="#cellconnection">Cell Connection</a>
  <a href="#howtheappcanhelp">App</a>
  <a href="#gateway">Gateway</a>
  <a href="#whatdothegatewaystatusledsindicate">Gateway Status LEDs</a>
  <a href="#node">Node</a>
</div>
-->

<div class="main">
<h1 id="title">Trouble Shooting Guide</h1>

<hr>

<h2 id="questions">What is your issue?</h2>

Select a suspected issue and you will be be shown information to hopefully help you resolve that issue.
<br><br>

<ul>
	<li>Overview</li>
	<li>Setup</li>
	<li>What Data will be sent?</li>
	<li>TroubleShooting Azure FarmBeats</li>
		<ul>
			<li>Verifying dta is flowing</li>
			<li>What to do if Connection Status shows as X?</li>
			<li>What should I look for in Azure Farmbeats?</li>
		</ul>

	<li>TroubleShooting Enviromonitor Setup</li>
		<ul>
			<li>Bluetooth</li>
			<li>Cell Connection</li>
			<li>How the App can help</li>
		</ul>
	<li>TroubleShooting Hardware Issues</li>
	<ul>
			<li>Gateway</li>
			<li>Node</li>
	</ul>
	<li>Other problems/concerns</li>
	<ul>
			<li>Tech Support</li>
	</ul>


	<li>TroubleShooting Enviromonitor Setup?</li>
	
		<li><a href="#fbsetup">Setup</a></li>
		<li><a href="#dataflow">Verifying data is flowing</a></li>
		<li><a href="#connectionX">What to do if Connection Status shows as an X?</a></li>
		<li><a href="#systemsAndSharing">What Data will be sent to Azure FarmBeats?</a></li>
	</ul>
	<br>
	<li>EnviroMonitor Setup?</li>
	<ul>
		<li><a href="#bluetooth">Bluetooth</a></li>
		<li><a href="#cellconnection">Cell Connection</a></li>
		<li><a href="#howtheappcanhelp">App</a></li>
	</ul>
	<br>
	<li>Hardware Issues?</li>
	<ul>
		<li><a href="#gateway">Gateway</a></li>
		<li><a href="#node">Node</a></li>
	</ul>
	<br>
	<li>Other/Unknown?</li>
	<ul>
		<li><a href="#howdoireachtechsupport">Davis Instruments Tech Support</a></li>
	</ul>
	<br>
</ul>

<br>
<hr>

<h2 id="fbsetup">Setting up your Azure FarmBeats Connection</h2>

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

<h2 id="connectionX">What to do if Connection Status shows as an X?</h2>

Let us assume that your connection status shows this:
<br><br>
<img src="./connectionStatus.png" alt="connectionStatus">
<br><br>

This shows that:
<ul>
	<li>Connection is currently BAD</li>
	<li>We have not sent telemetry data since Oct 24th</li>
</ul>

A bad connection typically means either:
<ul>
	<li>A temporary bad Internet connection</li>
	<li>Something has happened to your Azure Farmbeats installation</li>
	<li>You changed your Azure FarmBeats credentials</li>
</ul>

Close and reopen this page several times over a couple of minutes, checking the Connection Status field.<br>
If the problem doesn't clear up, then it may not be a temporary issue.<br>
Try clicking the Save button.  This would cause the webpage to retry the connection with the current data.<br>
If you get an error, that means that the website could not build a connection (using your credentials) to your Azure FarmBeats installation.<br>

<br>
At this time, it may make sense to investigate from the Azure FarmBeats side; to do so, please visit: <a href="https://aka.ms/FarmBeatsdocumentation">their documentation.</a> 
<br><br>

<h2 id="systemsAndSharing">What Data will be sent to Azure FarmBeats?</h2>

FarmBeats is currently an EnviroMonitor-based system.  Therefore, only data related to EnviroMonitors (EMs) will be sent to FarmBeats.
This applies to any and all EMs that:
<ul>
	<li>you own and are registered under your account</li>
	<li>that are pro-shared to your account.</li>
</ul>

The graphic below shows where you can view both the Owned as well as Shared stations.
<br><br>
<img src="./Stations.png" alt="Stations">
<br><br>


<h2 id="bluetooth">Bluetooth</h2>

<p>To setup the EnviroMonitor, the Bluetooth connections with your phone are very important.
When setup up, to start the Bluetooth Connection (BLE) , you would first need to press the 2 pads inside the main GATEWAY for a couple of seconds. 
You should then see the green and blue light appear with the Blue light flashing. 
At this point, open the phone app; then press GATEWAY or select the gateway you are trying to connect to. 
You should see the BLE light turn SOLID, and your phone should acknowledge the gateway.</p>
<p>Following are some of the Bluetooth-related issues you may run into.</p>

<h3 id="thelightsdonotlightup">The lights do not light up.</h3>

<p>Make sure the battery is connected. 
Make sure the pads are clean</p>

<h3 id="thephonereportsthegatewayisregisteredtoanotheruser">The Phone reports â€œThe Gateway is registered to another userâ€</h3>

<p>The gateway you are connecting to is already registered either to you or someone else.</p>

<h3 id="thephonewillnotconnect">The phone will not connect</h3>

<p>Make sure the phone is in range.  Some phones may need to be very close to the device; you may want to rest the phone next to the board.</p>

<h2 id="cellconnection">Cell Connection</h2>

<p>Cell connections are required for the device. Your reseller should have worked with you in getting a unit that will work in your location, but sometimes, the coverage is not what we think it should be.
If the device does not sync to the cell tower, first, make sure the device is registered on the WeatherLink Site. 
(Use the phone app to register the device and it will create the account).</p>

<h3 id="checkthelights">Check the Lights</h3>

<p>Press the touch pads inside the box and see what the lamps are doing.
The LED on the left is â€œcellConnectionâ€ LED.
The LED on the right is the â€œBluetooth/BLUEâ€ LED.
If the CellConnection LED on the LEFT is SOLID AMBER during bootup, this is normal for the first 3 seconds.
If the CellConnection LED is flashing GREEN, the device is trying to wait for the device to connect to the tower. Wait for the CellConnection LED to turn solid green.
If the CellConnection LED is solid green, you should be working and transmitting data.
If the CellConnection LED is FLASHING AMBER, then then the unit is trying to connect but the battery is low. Check the battery and the solar panel for good connections and that there is not any blockage of the solar panel.
If you have a solid AMBER CellConnection LED after booting, then the device is connected to the WeatherLink site, but the battery is low. 
If the CellConnection LED is blinking RED, then gateway cannot reach the tower.
The CellConnection LED is solid RED, the gateway is not setup in the phone, use the app to configure the device.
IF you do not have cell connection after a reasonable period of time, try to reboot and test again. If it still fails, try another location and see if that works.
IF the LEDs  look good, you should be able to add the NODES and the Weather Station.
If you have added a weather station through the APP and have it plugged in, you should start seeing data shortly though the APP or the WeatherLink Website.
If you do not see it, make sure you are using a CABLED ISS.
If you are having issues with the Gateway, you have some other tools with the PHONE APP.</p>

<h2 id="howtheappcanhelp">App</h2>

<h3 id="networkstatus">Network Status</h3>

<p>The Mesh connection will give you a colored value. You would want to see a GREEN.  This indicates the strength is over -90db.
If it is less, then the connections to the nodes are not optimum and tweaking with placement, elevation or adding nodes will help.
Yellow is -90 to -99 medium mesh network status, but you may get reliable data
Red is &lt; -100. Poor network status you probably will not get data or it will be spotty.</p>

<h3 id="cellconnection-1">Cell Connection</h3>

<p>This is an indication of the connection to the CELL TOWER.
GOOD will be a value of > 9 You should have good consistent data.
A value of 5 to 9 will be a mediocre connection and may be spotty. Try moving or raising the gateway.
Red will indicate poor cell connection. This may be caused by a temporary cell outage, wait and see if it recovers, or contact support for an update. Try moving the unit, and again, raising the device. Make there are not pieces of equipment that may be creating EFI or other interference.</p>

<h3 id="gatewaypower">Gateway Power</h3>

<p>The battery indicate should be GREEN. This means you have a good strong battery and you should be fine to run for several weeks if the sun down not come out.
If the battery indicator is YELLOW, that indicates a weak battery.  The device could be in a state where the battery has been draining due to lack of solar. Check the panel, has there been cloud cover for a few days? Check connections from the solar to the charging board and the battery connections.
If it is RED, then the battery is in a LOW voltage state. This is below 5.75. You unit will be subject to dropping of line if the battery is not recharged. Check the solar panels for any shadows, during the main part of the day. Shadows are one of the biggest causes for poor charging.</p>

<p>Next, you can start adding NODES.</p>

<p>You need to have the NODES and the GATEWAY either above or below the canopy.  For the best distance it should be ABOVE the canopy by a good SEVERAL feet. The MATURE canopy should be taken into consideration. IF you place the device 2 feet above the canopy and then the crop grows 3 feet, you would be buried in the canopy and your coverage would be non-existent.</p>

<p>If your coverage is very weak, raise the devices. For best penetration, about 8-10 feet above the canopy is best. You can also stretch the distance by adding more nodes to use as repeaters.</p>

<p>If you are having issues with the NODES, there are several issue that could occur.</p>

<p>First is no connection or an intermittent connection.</p>

<p>You have some tools on your phone app that can help you with these issues. 
There are also tools on the NODE.  When you open the door, the lights should light up. The follow will give you indications of the connection and other issues.</p>

<p>There are two lights the BLUE (BLE and the one to its right which is a TRICOLOR LED</p>

<p>The Tricolor is SOLID green means it is connected to a PARENT. </p>

<p>Solid Amber means it is connected to the parent but the batteries are low. Make sure all of the D Cell are fully seated and then the voltage on the lithium is over 5.6</p>

<p>A blinking green is that the node is not connecting to a parent. Raise the unit or move it closer to another device and see if it connects.</p>

<p>A blinking amber is that the node is not connecting to a parent. And the batteries are low.</p>

<p>Solid RED is that the device is not configured in the APP. Please use the app to configure.</p>

<p>The BLE light will flash when the BLUETOOTH can connect but is not currently connected. Us the Phone to connect to the device.</p>

<p>Solid Blue indicated the phone is ready and connected to the node and you can configure as needed.</p>

<p>The NODE also has some phone tools and they can help trouble shoot.
The NODE Network status has 3 reading we are primarily concerned with: RSSI, ETX and Rank.</p>

<h4 id="rssi">RSSI</h4>

<p>RSSI is the power of the signal. The reading should be GREEN  and in the range of >-90 This will give you good solid reading though out.
Yellow is indicating that the RSSI is compromised and is in the range of -90 to -99
Red is poor. It is for a range of &lt;-100. 
Issues that affect RSSI are distance, height and interference </p>

<h4 id="etx">ETX</h4>

<p>ETX is the  value that references how well it is connecting though a multi hop network. This should be a low value. 
Green Anything under &lt; 1000 is good .
Yellow is OK, and is 1000-1499
Red is over 1500.
If you have poor numbers, you can try adding a node as a repeater or moving the nodes around so that you may have a more optimum â€œmeshâ€ pattern. Those should be so that one device can reach other devices. A very poor example would be having all device in a straight line.</p>

<h4 id="rank">Rank</h4>

<p>Rank should be Green and should be &lt; 1000. <br />
Yellow is 1000-1499.
Red is over 1500.</p>

<h4 id="nodepower">Node Power</h4>

<p>NODE POWER will indicate the node D cell battery voltage.
GREEN is > 4.8V
Yellow is between 4.2 and 4.8
Red is below 4.2 volts.
One issue to watch out for it the tilt of the D Cell batteries. Sometimes if the unit get jarred or knocked these batteries may come dislodged. If you see this happening, please contact Davis Instruments for a solution.</p>

<h3 id="addingsensors">Adding Sensors</h3>

<p>If you have the NODE all set up and all the values look good on the phone app, then you should be able to add the sensors. You need to ensure you are using sensors that are supported. 
The latest sensor list can be found here: 
<a href="https://www.davisinstruments.com/product_documents/weather/EM-sensors.pdf">https://www.davisinstruments.com/product_documents/weather/EM-sensors.pdf</a> .</p>

<p>The phone app will have the correct wiring for the sensors. If you have issues with the sensors, 
you typically will find the issue that the wires are not fully seated, the insulation is not removed enough for the screws to bite the bare wires. 
They are not tight, or they are mis-wired. Please check these items very thoroughly.</p>

<p>On the Rain gauge, you MUST use the BARE WIRES and NOT use the Phone jack. This will be documented in the phone app as you are adding the rain collector.</p>

<h2 id="gateway">Gateway</h2>

<h3 id="mygatewayisnotpoweringup">My Gate way is not powering up.</h3>

<p>Make sure that the battery leads are connected to the battery. The unit is shipped without the leads connected.</p>

<p>Power down the unit for 2 minutes and then repower the unit. To do this, remove Main Power Cable from the Main Power Jack on the upper board. 
Wait 2 minutes. Then reconnect. The lamps on the board should go through the startup sequence. 
If they do not come on, try pressing the 2 square pads to activate the lamps.</p>

<img src="./GatewayPower.png" alt="Gateway Power">

<h3 id="makesurethebatteryvoltageisok">Make sure the battery voltage is OK.</h3>

<p>The battery should be over 6v. At 5.2V, the unit will power itself down except for the charging circuit. It will stay powered down until it charges itself to at least 5.7 volts.</p>

<h3 id="mygatewayisnotconnectingtothecelltower">My gateway is not connecting to the cell tower</h3>

<p>Make sure you have registered the device with WeatherLink.com by configuring your Gateway through the EnviroMonitor (EM) app. If the Gate way is not configured, you will see the Cell Status light is a solid red. </p>

<h3 id="thegatewaycannotconnecttothecellnetwork">The Gateway cannot connect to the cell network</h3>

<p>There are several issues that could cause this The first is that you may not have not given it enough time. Wait at least 30 minutes.
Try moving the device to another location. Try this on your property first, also elevate the unit. If it does not work at several location on your property, then try taking it to the nearest town for at least 30 minutes.</p>

<p>Look at the Cell Status Light and compare it to the list on the front cover or under the â€œWhat do the Gateway status LEDs indicate?â€ section
Make sure that your device will work in your location. Not all EnviroMonitors will work everywhere. When you first bought the unit, our sales team will identify the best unit for the area it is going to be placed. Sometime, the unit is not place where we thought it was, or the coverage for the area has changed. If the above steps do not resolve the connect issue, please reverify this with Tech support. </p>

<h3 id="whatdothegatewaystatusledsindicate">What do the Gateway status LEDs indicate?</h3>

<p><img src="./GatewayStatusLEDs.png" alt="LEDs" /></p>

<h3 id="howcanitellifmygatewaybatteryvoltageisgettingtoolow">How can I tell if my Gateway battery voltage is getting too low?</h3>

<p>Our server will monitor your battery voltage and will trigger an e-mail warning if it should get critically low (approximately 14 days of power). The e-mail will go to both the registered customerâ€™s e-mail address as well as the alarm e-mail address (if one has been set up). You can also see the battery power in the app: choose this Gateway, then Gateway Power.
You can also check the status with the EM app. The battery condition will be indicated on the Gateway under Gateway Power. It should be GREEN (> 5.9 volts). It the battery is getting low, but not critical, it will be yellow. This is between 5.75 v and 5.9v This may be normal if there has not been much sunlight recently.  Red indicates critical. Check the battery leads, check the solar panel connections. 
See the Section on â€œMy battery charge does not lastâ€</p>

<h3 id="mybatterychargedoesnotlast">My battery charge does not last</h3>

<p>The battery should last approx 14 days on a full charge. If the battery does not last this long, or the EM app gateway battery status is always in the Yellow or red range, this means your charging system is somehow compromised. Make sure that the solar panel is getting full sun during the day. If portions of the solar panel are blocked by a shadow (from building etc, or from the weather station) you will need to reposition things so that this shadow does not cover the solar panel. Also, aim the solar panel so that it faces the sun in the best manner through out most of the day. In some areas, where the light has a high angle, we do have a special bracket for this. Please reach out to Customer Service to order this item.</p>

<h3 id="whatdoidoifmygatewaybatteryislow">What do I do if my Gateway battery is low?</h3>

<p>The EnviroMonitor features a robust battery and solar panel. It is designed to recharge and last for years. If your battery is low, you need to determine why the solar panel is not recharging the battery. This is usually due to something shading the solar panel (such as vegetation, snow, or dirt), or the solar panel becoming turned away from the sun. Check your installation to make sure sunlight is reaching the solar pane </p>

<h3 id="myinstallationisinalowlightareacaniaddanothersolarpanel">My installation is in a low light area. Can I add another solar panel?</h3>

<p>Yes. You can add an Extra Solar Panel Kit (product number 6616).</p>

<h3 id="caniuseacpowertochargethegatewaybattery">Can I use AC power to charge the Gateway battery?</h3>

<p>If your installation is in a low-light area or an area with prolonged periods of time where temperatures stay below -4Â°F (-20Â°C), charging may be severely diminished. You may use Davisâ€™s Optional AC Charger Kit, product number 6710, to charge the battery. The kit allows you to replace the solar charger with AC power. The adapter has a universal input (100 -240V, 50-60 Hz) and will work anywhere in the world. (A wall-plug adapter may be necessary for use in some countries.) In a cold environment, you will need to bring the Gateway into a warmer environment (above -4Â°F/-20Â°C) to charge the battery with the AC Charger Kit.</p>

<h3 id="imnotgettingdatafrommynodetothegateway">Iâ€™m not getting data from my Node to the Gateway?</h3>

<ul>
<li>Make sure the D batteries in the Node are installed all the way in. Sometimes they appear to be but are actually tilted outward, preventing connection. If your unit does not have the battery retainer, you can order it as part number:7342.326 Retainer, Battery, EnviroMonitor.</li>

<li>Make sure the green sensor adapters in the Node are aligned properly and not offset. </li>

<li>Make sure the screws on the sensor adapters are very tight. </li>

<li>Make sure none of the sensor cables are pinched in the Node door. If these steps donâ€™t solve the problem, consider mounting the Node and Gateway higher above the canopy. See â€œTo get optimal transmission range:â€ on page 2.</li>
</ul>

<h2 id="node">Node</h2>

<h3 id="whatdothenodestatusledsindicate">What do the Node status LEDs indicate?</h3>

<p><img src="./NodeStatusLEDs.png" alt="Node Status LEDs" /></p>

<h3 id="mynodecantconnecttothegatewayormeshparent">My Node canâ€™t connect to the Gateway or mesh parent</h3>

<p>Give the Node more time, at least 15 minutes, to negotiate a connection to the mesh network. If it still cannot connect, the Node is not within transmission distance to a parent. To solve this you can relocate the Node closer to the Gateway or another Node, or you can install another intermediate Node between it and the mesh parent to help it connect to the mesh network.</p>

<h3 id="howcanitellifmynodebatteriesaregettingtoolow">How can I tell if my Node batteries are getting too low?</h3>

<p>The mesh LED will be solid or blinking amber to show that the Nodeâ€™s batteries are low. See the table above. You can also see the battery power in the app: choose this Nodeâ€™s Gateway, then this Node, then Node Power.</p>

<h3 id="mydevicehasarj11connectionyetthenodehasbarewireconnectionsonly">My device has a RJ 11 connection, yet the node has bare wire connections only.</h3>

<p>If the Davis sensor has an RJ-plug on its cable, use the Davis RJ Adapter, product number 6860. Or, you can remove the plug and strip the wires. Try not to strip the covering back so far that the bare wires can touch each other when the connector is plugged in, but make sure the clamp in the sensor port is closing on wire, not plastic. (About 1/4â€ [6.4 mm] of exposed wire is ideal.) </p>

<p><img src="./RjAdapter.png" alt="RJ Adapter" /></p>

<p>Note: The exception to this is the Davis Rain Collectors. These you need to cut the end of and use the BARE WIRE connector.</p>

<h3 id="ihavearaincollectorconnectedtomynodebutiamnotgettingreadings">I have a rain collector connected to my node, but I am not getting readings.</h3>

<p>Make sure that you have the rain collector set up to use BARE WIRE connections you will need to cut the RJ11 connection of and use the wiring diagram in the phone app.</p>

<p><img src="./wiring.png" alt="wiring"/></p>

<h3 id="whatsensorscaniconnecttomynode">What sensors can I connect to my node?</h3>

<p>You can always find the latest sensors here:
<a href="https://www.davisinstruments.com/product_documents/weather/EM-sensors.pdf">https://www.davisinstruments.com/product_documents/weather/EM-sensors.pdf</a>.</p>

<h3 id="thereisasensoriwouldlikebutitisnotonthelist">There is a sensor I would like, but it is not on the list.</h3>

<p>If you have a need for a sensor that we do not support but fits the communication parameters list in the "What format of sensors does the Node support?",<br>

please forward the request to <a href="mailto:support@davisinstruments.com">support@davisinstruments.com</a>.  
Please include a spec sheet for the sensor with your request.Â  We will evaluate it and potentially add it to the future sensor list.</p>

<h3 id="whatformatofsensorsdoesthenodesupport">What format of sensors does the Node support?</h3>

<p>We can support sensors that have:</p>

<ul>
<li>analog voltage output</li>

<li>pulse output (switch closures) Â </li>

<li>SDI-12 communication protocol</li>
</ul>

<h3 id="whatfrequenciesdoesmygatewaytalktothenode">What Frequencies does my Gateway talk to the Node?</h3>

<p><img src="./Frequencies.png" alt="frequencies"/></p>
<br>

<h2 id="howdoireachtechsupport">How do I reach Davis Tech Support?</h2>

<p>You can reach Davis Instruments Technical Support:</p>

<ul>
<li>By phone: Call (510) 732-7814 | M-F 7:00am to 5:30pm PT</li>

<li>By email:  <a href="mailto:support@davisinstruments.com">support@davisinstruments.com</a></li>
<li>By LiveChat. You can access this from our Website and looking for the <img src="./LiveChatIcon_small.png" alt="LiveChatIcon"/> in the lower right hand area.</li>
</ul>


<br>
<br>
</div>
</body>
</html>
