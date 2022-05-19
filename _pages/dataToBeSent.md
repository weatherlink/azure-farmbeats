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

### What does the data look like?

Although this is not meant to be a technical document, it is sometimes useful to get a feel for data.  Below is an actual telemetry record that has been sent to Azure FarmBeats.  It is a text record in JSON format.

```

{
	"temp": 70.7,
	"rainfall": 0,
	"wind_speed_avg": 0,
	"rainfall_rate_hi": null,
	"wind_speed_hi": 0,
	"wind_dir_of_hi": null,
	"evapotranspiration": 0,
	"solar_rad_hi": 0,
	"wind_dir_of_prevail": null,
	"bar": 29.986,
	"temperature_lo": 70.6,
	"humidity": 57,
	"wind_num_samples": 117,
	"temperature_hi": 70.7,
	"archive_interval": 300,
	"timestamp": "2022-05-19T18:10:00Z",
	"solar_rad_avg": 0
}


```

