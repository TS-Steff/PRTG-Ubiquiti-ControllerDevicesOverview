# PRTG-Ubiquiti Overview
This script is for PRTG from Paessler to monitor the AP's, Switches and Gateways. You can define which site or sites you want to monitor, or if you would like to monitor all sites and exclude specific sites.

It returns the sum of all APs, Switches and Gateways. How many are connected, online, offline and how many do need upgrades.

### Screenshots (Outdated)
Sensor view
![PRTG Screenshot](/Screenshots/prtg.png?raw=true "PRTG Screenshot")

The settings page may look like this
![PRTG Settings](/Screenshots/settings.png?raw=true "PRTG Sensor Settings")

## Config
Add an EXE/Script Advanced sensor to your PRTG Site

You have to pass six parameters
| parameter    | Value                                        | Comment                                                                     |
| ------------ | -------------------------------------------- | --------------------------------------------------------------------------- |
| server       | IP or hostname of your controller            | you can add %host% to for localhost                                         |
| port         | TCP port on which your cotntroller runs      |                                                                             |
| sites        | the site IDs you would like to get data from | you find the site ID in the url of each site                                |
| excludeSite  | the site ID                                  | site IDs you want to exclude if you leave sites empty                       |
| username     | The username to connect the controller       | this user only needs read rights on the sites defined in the sites variable |
| password     | the users password                           |                                                                             |
| debug        | debug mode                                   | writes the json to the disk if set true                                     |

## History
| Date       | Description                                                                             |
| ---------- | --------------------------------------------------------------------------------------- |
| 2023-04-12 | Added counter for disconnected devices                                                  |
|            | Updated readme.md                                                                       |

## Credits
Many thants to Luciano Lingnau [Paessler Support]
- <https://kb.paessler.com/users/Luciano%20Lingnau%20%5BPaessler%20Support%5D>
- <https://kb.paessler.com/en/topic/71263-can-i-monitor-ubiquiti-unifi-network-devices-with-prtg#reply-243681>

He wrote the most part of this script. We just adopted and changed the script to fit our needs