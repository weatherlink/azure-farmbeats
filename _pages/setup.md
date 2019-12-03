---
title: Setup
permalink: /setup
classes: wide
header:
  overlay_color: "#000000"
  overlay_filter: "0.0"
  overlay_image: /assets/vendor/weatherlink/images/landing.jpg
---

## Setting up your Azure FarmBeats Connection

Click on the Account icon (the leftmost of these in the right side
navigation bar).  
  
![AccountIcon](./images/AccountIcon.png)  

  
From there, click on the Account Integration pulldown and select "Azure
FarmBeats".  
  
![AccountIntegration](./images/AccountIntegration2.png)  
  
This should bring up the Azure FarmBeats window. If you have yet to set
up your connection, the window will look like this:  
  
![UI\_without\_data](./images/UI_without_data.png)  
  
  
Let's go through each of the fields and the selections.

**NOTE**  It is important that (if copying and pasting this data), that you **NOT** inadvertenly add any trailing whitespace (e.g., space) characters!!

### Documentation

That would be this document that you are currently reading.  
  

### Display Name

This is a free-form field to describe your setup. It could be something
like "Dave's Farm".  
  

### API Endpoint

This is a field that should be provided from your Azure FarmBeats
account. It is a custom URL for your account.  

### Tenant Id

This is a field that should be provided from your Azure FarmBeats
account. This is basically a "group ID".  
  

### Client Id

This is a field that should be provided from your Azure FarmBeats
account. This is basically your "account Id".  
  

### Client Secret

This is a field that should be provided from your Azure FarmBeats
account. This is considered to be the confidential "account password".  
It is normally shown as asterisks ("\*\*\*"). The eye icon will
show/hide the actual value.  
  

### EventHub aka EventHub Connection String

This is a field that should be provided from your Azure FarmBeats
account.  
This is also considered to be confidential.  
This is a long, string containing several snippets of
"someName=someValue"-type sections.  
  

### Telemetry Start Date

This is the date from which you want Historical Data to be sent. Say you
are filling out this form on December 1 2019.  
However, you're equipment had been setup and collecting data since July
3rd 2019.  
If you want all that data from July 3rd until now to be sent to
FarmBeats, select July 3rd 2019 as the Telemetry Start Date.  
Once your connection is fully established, then both LIVE telemetry data
as well as the "Historical" telemetry data (from July 3rd until now)
will be sent to FarmBeats.  
  
Note that this historical data can easily generate massive amounts of
data.  
The record count is grossly like: (num stations \* num records/day \*
num days).  
Under certain situations, this could be 10s of thousands of records
which could take days to be generated and then sent to Azure
FarmBeats.

### Available EM Stations

This alerts you to the total number of EM stations that you currently
own or are shared to your accounts.  
If this number is not what you expect, go back and check your
configuration.  
  

### Last Telemetry Sent

This value shows the datetime of the last telemetry record sent to
FarmBeats for this account.  
If nothing has yet to be sent, then "--" will be displayed.  
  

### Connection Status

This shows the current condition of the connection to your FarmBeats
installation.  
There are 3 different statusses:  

  - None or "--"
  - ![greenCheck](./images/greenCheck.png)
  - ![redX](./images/redX.png)

### Unlink

Clicking on this will terminate the link or connection from WeatherLink
to Azure FarmBeats for your data.  
  
This effectively stops data from ever being sent from WeatherLink to
Azure FarmBeats again.

### Exit

Exit the page.  
  

### Save

Clicking on this does:  

  - Check data validity
  - Connection Test
  - Save data to the database
  - Success Message

### Waiting to Add

Once you've entered data into all the fields and have successfully saved
your data, you must then wait for the "backend servers" to process this
request.  
While this request is being processed, we cannot allow you to edit or
change any data.  
Therefore, you will see the following graphic anytime you click on the
"Azure FarmBeats" pulldown:  
  
![AddInProgress](./images//AddInProgress.png)

