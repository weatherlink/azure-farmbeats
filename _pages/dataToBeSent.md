---
title: Data to Be Sent
permalink: /dataToBeSent
classes: wide
header:
  overlay_color: "#000000"
  overlay_filter: "0.0"
  overlay_image: /assets/vendor/weatherlink/images/landing.jpg
---
  
## What Data will be sent to Azure FarmBeats?

FarmBeats is currently an EnviroMonitor-based system. Therefore, only
data related to EnviroMonitors (EMs) will be sent to FarmBeats. This
applies to any and all EMs that:

  - you own and are registered under your account
  - that are pro-shared to your account.

The graphic below shows where you can view both the Owned as well as
Shared stations.  
  
![Stations](./images/Stations.png)

## What does the data look like?

Although this is not meant to be a technical document, it is sometimes useful to get a feel for data.  Below is an actual telemetry record that has been sent to Azure FarmBeats.  It is a text record in JSON format.

```

{
	"deviceid": "333da51d-9834-4c2a-9b2e-08ff523cde8e",
	"timestamp": "2019-11-01T23:50:00Z",
	"version": "1",
	"sensors": [{
		"id": "33366c2a-3820-434a-9168-63394466ebb4",
		"sensordata": [{
			"moist_soil_4in": 31.9542,
			"timestamp": "2019-11-01T23:50:00Z"
		}, {
			"moist_soil_8in": 42.8048,
			"timestamp": "2019-11-01T23:50:00Z"
		}, {
			"moist_soil_12in": 64.4298,
			"timestamp": "2019-11-01T23:50:00Z"
		}, {
			"moist_soil_16in": 73.3719,
			"timestamp": "2019-11-01T23:50:00Z"
		}, {
			"moist_soil_24in": 78.9054,
			"timestamp": "2019-11-01T23:50:00Z"
		}, {
			"moist_soil_32in": 79.1097,
			"timestamp": "2019-11-01T23:50:00Z"
		}, {
			"temp_4in": 62.6,
			"timestamp": "2019-11-01T23:50:00Z"
		}, {
			"temp_8in": 61.88,
			"timestamp": "2019-11-01T23:50:00Z"
		}, {
			"temp_12in": 63.32,
			"timestamp": "2019-11-01T23:50:00Z"
		}, {
			"temp_16in": 64.76,
			"timestamp": "2019-11-01T23:50:00Z"
		}, {
			"temp_24in": 62.6,
			"timestamp": "2019-11-01T23:50:00Z"
		}, {
			"temp_32in": 63.32,
			"timestamp": "2019-11-01T23:50:00Z"
		}]
	}]
}

```

