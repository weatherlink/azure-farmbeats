---
title: What NOT to do
permalink: /whatNotToDo
classes: wide
header:
  overlay_color: "#000000"
  overlay_filter: "0.0"
  overlay_image: /assets/vendor/weatherlink/images/landing.jpg
---

## What NOT to do

Do **NOT** delete (and then recreate) your Azure FarmBeats Account Integration **unless** you also have "clean data" on the Microsoft side.

## Why Not?

Let's assume:

- You have a Microsoft Azure Farmbeats Installation

- You have done the WeatherLink Azure FarmBeats Account Integration

- Something is not working

- So you decide to delete/unlink the WeatherLink "side" from the Microsoft "side" and try again.
  
  DO NOT DO THIS.
  
  Every time you do the "WeatherLink Azure FarmBeats Account Integration", the WeatherLink side goes through, looks at all your sensors and assigns them unique ids; an example id is "b52ac6d4-fc9f-4687-9772-d46ca66c0488".  The WeatherLink software then describes this sensor (say, a temperature sensor) and then tells the Azure/Microsoft code "I'm going to refer to this sensor as "b52ac6d4-fc9f-4687-9772-d46ca66c0488".  So it does this for all of your sensors.
  
  However, when you delete the WeatherLink side and recreate it, the WeatherLink side does not KNOW that the Azure side ALREADY has ids for all the sensors.  So the WeatherLink side assigns ALL NEW ids.  And then it uses these NEW ids to send the telemetry data.
  
  On the Microsoft side, they see now that they have twice as many sensors, because each sensor has an old id and a new id.  But there is no way to "link" the old id to the new id.  So now, on the Microsoft side, you have old telemetry with old ids and new telemetry with new ids.  A mess.

## How to Fix This?

 For now, you can't; all you can do is to start over ... cleanly this time.

 Whenever you create a new "WeatherLink" connection, you must ensure that the Microsoft side has NO sensors, NO devices and NO telemetry.  If any of that exists, then it must be PURGED *before* you create the WeatherLink connection, or a new Azure FarmBeats account must be used.  



 Note, that when you create the WeatherLink side (aka do the "WeatherLink Azure FarmBeats Account Integration"), you can set the "Telemetry Start Date" as far back in time as you'd like (limited by when the sensors were originally added to WeatherLink, of course.) 

## How do I clean/purge the Azure Microsoft Data?

To learn more about Azure FarmBeats, please visit:  please visit: [Azure FarmBeats Documentation](https://aka.ms/FarmBeatsdocumentation).
