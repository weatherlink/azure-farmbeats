---
title: Connection Status X
permalink: /connectionStatusX
classes: wide
header:
  overlay_color: "#000000"
  overlay_filter: "0.0"
  overlay_image: /assets/vendor/weatherlink/images/landing.jpg
---

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


