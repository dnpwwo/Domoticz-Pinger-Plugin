# Domoticz-Pinger-Plugin
Python plugin that pings and shows response times for network devices

## Key Features

* Creates two Domoticz devices per specified address
  1. Basic status indicator, On/Off to show device response.
  2. Custom sensor that shows milliseconds per ping.
* When network connectivity is lost the Domoticz UI will optionally show the device(s) with a red banner
* Does not require static IP addresses when DNS names are specified (e.g www.google.com always maps to the same Domoticz devices)
* Domoticz devices can be renamed to anything after initial creation

## Installation

Python version 3.4 or higher required & Domoticz version 3.8xxx or greater.

To install:
* Go in your Domoticz directory, open the plugins directory and create a new one named 'Pinger' or similar.
* Navigate to the directory using a command line
* Run: ```git pull https://github.com/dnpwwo/Domoticz-Pinger-Plugin.git```
* Restart Domoticz.

In the web UI, navigate to the Hardware page.  In the hardware dropdown there will be an entry called "Pinger (ICMP)".

## Configuration

| Field | Information|
| ----- | ---------- |
| Address(es) | Comma separated list, will handle DNS names and IP V4 addresses (e.g 192.168.xxx.xxx) |
| Ping Frequency | Dropdown to allow ping frequency to be set |
| Time Out Lost Devices | When true, the devices in Domoitcz will have a red banner when network connectivity is lost to the Kodi |
| Debug | When true the logging level will be much higher to aid with troubleshooting |

## Change log

| Version | Information|
| ----- | ---------- |
| 3.0.0 | Initial upload version |
