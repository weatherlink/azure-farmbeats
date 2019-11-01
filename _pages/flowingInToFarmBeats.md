---
title: Verify Data is Flowing into Azure FarmBeats
permalink: /flowingIntoFarmBeats
classes: wide
header:
  overlay_color: "#000000"
  overlay_filter: "0.0"
  overlay_image: /assets/vendor/weatherlink/images/landing.jpg
---

## Verify Data is Flowing into Azure FarmBeats

Go back to the Account page. Select "Azure FarmBeats" from the pulldown
to show the Azure FarmBeats page.  
It should look something like this:  
  
![UI with data](./images/UI_with_data.png)  
  
Notes:  

  - The Last Telemetry Sent and Connection Status fields. These should
    show (ideally) a green checkmark and a sent date that is pretty
    recent.
  - If you only have 1 EM system and it is on a 15 minute plan (for
    example), then this field would only update every 15 minutes.
  - If you have 5 EM system each on a 5 minute plan (and with
    unrealistically perfect timing), then this field could update every
    minute.
  - If you have (or have shared to you) multiple EM systems, then it
    could be the minimum minutes plan for all of those systems.
  - Note that this is \*not\* an automatically updating page; it shows
    the status for when the page was put up. If you want updated data,
    close the page and bring it back up again.


To learn more about Azure FarmBeats, please visit: [their documentation.](https://aka.ms/FarmBeatsdocumentation)

