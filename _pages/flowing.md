
---
title: App
permalink: /app
classes: wide
header:
  overlay_color: "#000000"
  overlay_filter: "0.0"
  overlay_image: /assets/vendor/weatherlink/images/landing.jpg
---

<h2 id="wl_dataTab">Verifying Data is Flowing into FarmBeats</h2>

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


