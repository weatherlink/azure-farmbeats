---
title: Node
permalink: /node
classes: wide
header:
  overlay_color: "#000000"
  overlay_filter: "0.0"
  overlay_image: /assets/vendor/weatherlink/images/landing.jpg
---

<h2 id="node">Node</h2>

<h3 id="whatdothenodestatusledsindicate">What do the Node status LEDs indicate?</h3>

<p><img src="./NodeStatusLEDs.png" alt="Node Status LEDs" /></p>

<h3 id="mynodecantconnecttothegatewayormeshparent">My Node can't connect to the Gateway or mesh parent</h3>

<p>Give the Node more time, at least 15 minutes, to negotiate a connection to the mesh network. If it still cannot connect, the Node is not within transmission distance to a parent. To solve this you can relocate the Node closer to the Gateway or another Node, or you can install another intermediate Node between it and the mesh parent to help it connect to the mesh network.</p>

<h3 id="howcanitellifmynodebatteriesaregettingtoolow">How can I tell if my Node batteries are getting too low?</h3>

<p>The mesh LED will be solid or blinking amber to show that the Node's batteries are low. See the table above. You can also see the battery power in the app: choose this Node's Gateway, then this Node, then Node Power.</p>

<h3 id="mydevicehasarj11connectionyetthenodehasbarewireconnectionsonly">My device has a RJ 11 connection, yet the node has bare wire connections only.</h3>

<p>If the Davis sensor has an RJ-plug on its cable, use the Davis RJ Adapter, product number 6860. Or, you can remove the plug and strip the wires. Try not to strip the covering back so far that the bare wires can touch each other when the connector is plugged in, but make sure the clamp in the sensor port is closing on wire, not plastic. (About 1/4 inchù [6.4 mm] of exposed wire is ideal.) </p>

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
Please include a spec sheet for the sensor with your request.  We will evaluate it and potentially add it to the future sensor list.</p>

<h3 id="whatformatofsensorsdoesthenodesupport">What format of sensors does the Node support?</h3>

<p>We can support sensors that have:</p>

<ul>
<li>analog voltage output</li>

<li>pulse output (switch closures) </li>

<li>SDI-12 communication protocol</li>
</ul>

<h3 id="whatfrequenciesdoesmygatewaytalktothenode">What Frequencies does my Gateway talk to the Node?</h3>

<p><img src="./Frequencies.png" alt="frequencies"/></p>
<br>


