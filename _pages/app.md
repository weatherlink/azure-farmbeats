---
title: App
permalink: /app
classes: wide
header:
  overlay_color: "#000000"
  overlay_filter: "0.0"
  overlay_image: /assets/vendor/weatherlink/images/landing.jpg
---
## App

### Network Status

The Mesh connection will give you a colored value. You would want to see
a GREEN. This indicates the strength is over -90db. If it is less, then
the connections to the nodes are not optimum and tweaking with
placement, elevation or adding nodes will help. Yellow is -90 to -99
medium mesh network status, but you may get reliable data Red is \<
-100. Poor network status you probably will not get data or it will be
spotty.

### Cell Connection

This is an indication of the connection to the CELL TOWER. GOOD will be
a value of \> 9 You should have good consistent data. A value of 5 to 9
will be a mediocre connection and may be spotty. Try moving or raising
the gateway. Red will indicate poor cell connection. This may be caused
by a temporary cell outage, wait and see if it recovers, or contact
support for an update. Try moving the unit, and again, raising the
device. Make there are not pieces of equipment that may be creating EFI
or other interference.

### Gateway Power

The battery indicate should be GREEN. This means you have a good strong
battery and you should be fine to run for several weeks if the sun down
not come out. If the battery indicator is YELLOW, that indicates a weak
battery. The device could be in a state where the battery has been
draining due to lack of solar. Check the panel, has there been cloud
cover for a few days? Check connections from the solar to the charging
board and the battery connections. If it is RED, then the battery is in
a LOW voltage state. This is below 5.75. You unit will be subject to
dropping of line if the battery is not recharged. Check the solar panels
for any shadows, during the main part of the day. Shadows are one of the
biggest causes for poor charging.

Next, you can start adding NODES.

You need to have the NODES and the GATEWAY either above or below the
canopy. For the best distance it should be ABOVE the canopy by a good
SEVERAL feet. The MATURE canopy should be taken into consideration. IF
you place the device 2 feet above the canopy and then the crop grows 3
feet, you would be buried in the canopy and your coverage would be
non-existent.

If your coverage is very weak, raise the devices. For best penetration,
about 8-10 feet above the canopy is best. You can also stretch the
distance by adding more nodes to use as repeaters.

If you are having issues with the NODES, there are several issue that
could occur.

First is no connection or an intermittent connection.

You have some tools on your phone app that can help you with these
issues. There are also tools on the NODE. When you open the door, the
lights should light up. The follow will give you indications of the
connection and other issues.

There are two lights the BLUE (BLE and the one to its right which is a
TRICOLOR LED

The Tricolor is SOLID green means it is connected to a PARENT.

Solid Amber means it is connected to the parent but the batteries are
low. Make sure all of the D Cell are fully seated and then the voltage
on the lithium is over 5.6

A blinking green is that the node is not connecting to a parent. Raise
the unit or move it closer to another device and see if it connects.

A blinking amber is that the node is not connecting to a parent. And the
batteries are low.

Solid RED is that the device is not configured in the APP. Please use
the app to configure.

The BLE light will flash when the BLUETOOTH can connect but is not
currently connected. Us the Phone to connect to the device.

Solid Blue indicated the phone is ready and connected to the node and
you can configure as needed.

The NODE also has some phone tools and they can help trouble shoot. The
NODE Network status has 3 reading we are primarily concerned with: RSSI,
ETX and Rank.

#### RSSI

RSSI is the power of the signal. The reading should be GREEN and in the
range of \>-90 This will give you good solid reading though out. Yellow
is indicating that the RSSI is compromised and is in the range of -90 to
-99 Red is poor. It is for a range of \<-100. Issues that affect RSSI
are distance, height and interference

#### ETX

ETX is the value that references how well it is connecting though a
multi hop network. This should be a low value. Green Anything under \<
1000 is good . Yellow is OK, and is 1000-1499 Red is over 1500. If you
have poor numbers, you can try adding a node as a repeater or moving the
nodes around so that you may have a more optimum "mesh" pattern.
Those should be so that one device can reach other devices. A very poor
example would be having all device in a straight line.

#### Rank

Rank should be Green and should be \< 1000.  
Yellow is 1000-1499. Red is over 1500.

#### Node Power

NODE POWER will indicate the node D cell battery voltage. GREEN is \>
4.8V Yellow is between 4.2 and 4.8 Red is below 4.2 volts. One issue to
watch out for it the tilt of the D Cell batteries. Sometimes if the unit
get jarred or knocked these batteries may come dislodged. If you see
this happening, please contact Davis Instruments for a solution.

### Adding Sensors

If you have the NODE all set up and all the values look good on the
phone app, then you should be able to add the sensors. You need to
ensure you are using sensors that are supported. The latest sensor list
can be found here:
<https://www.davisinstruments.com/product_documents/weather/EM-sensors.pdf>

The phone app will have the correct wiring for the sensors. If you have
issues with the sensors, you typically will find the issue that the
wires are not fully seated, the insulation is not removed enough for the
screws to bite the bare wires. They are not tight, or they are
mis-wired. Please check these items very thoroughly.

On the Rain gauge, you MUST use the BARE WIRES and NOT use the Phone
jack. This will be documented in the phone app as you are adding the
rain collector.


