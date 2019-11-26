---
title: Connection Status X
permalink: /connectionStatusX
classes: wide
header:
  overlay_color: "#000000"
  overlay_filter: "0.0"
  overlay_image: /assets/vendor/weatherlink/images/landing.jpg
---

## What to do if Connection Status shows as an X?

Let us assume that your connection status shows this:  
  
![connectionStatus](./images/connectionStatus.png)  
  
This shows that:

  - Connection is currently BAD
  - We have not sent telemetry data since Oct 24th

A bad connection typically means either:

  - A temporary bad Internet connection
  - Something has happened to your Azure Farmbeats installation
  - You changed your Azure FarmBeats credentials

Close and reopen this page several times over a couple of minutes,
checking the Connection Status field.  If the problem doesn't clear up, then it may not be a temporary issue.  

Try clicking the Save button. This would cause the webpage to retry the
connection with the current data.  If you get an error, that means that the website could not build a
connection (using your credentials) to your Azure FarmBeats installation.  
  
At this time, it may make sense to investigate from the Azure FarmBeats
side. The "top" of their general documentation can found found at: [their documentation.](https://aka.ms/FarmBeatsdocumentation).

However, this link will show you information on how to generate the credentials you need to enter into WeatherLink to make the WeatherLink-FarmBeats connection.
That documentation can be found: [here](https://docs.microsoft.com/en-us/azure/industry/agriculture/get-sensor-data-from-sensor-partner).


