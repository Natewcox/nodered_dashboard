# nodered_dashboard
Creating a Node-Red dashboard.

## DESCRIPTION

I use HomeKit for my home automations and I wanted to share how I use Node-Red to add each element. This first repository nodered_heater connects my porch heater. Not every user has Apple devices so I use this Raspberry as a dashboard to control the heater and a button to tell my Garage Door Raspberry to open. We will going over the elements of setting up a dashboard and if you have followed nodered_heater, skip down to installing the dashboard.

## GETTING STARTED

![image](https://user-images.githubusercontent.com/97216517/148485561-8359d3a1-3a52-4e5d-8c62-6aa99ab292b6.jpeg)



### MATERIALS

1. Raspberry Pi
2. SD Card


### INSTALLS

Fallow the directions at [RaspberryPi.org](https://www.raspberrypi.org) to:
  * Flash the latest Raspberry Pi imiage to the SDCard
  * Perform initial startup. Network and Update is a must.
***
Install Node-Red. The recommended software for the Raspberry includes Node-Red but is missing a few parts. Use the full install to have all files and updates.

```
bash <(curl -sL https://raw.githubusercontent.com/node-red/linux-installers/master/deb/update-nodejs-and-nodered)
```

Enable Node-Red at boot.

```
sudo systemctl enable nodered.service
```
If you plan to communicate between Pis, I recommend Mosquitto.
  * https://mosquitto.org/blog/2013/01/mosquitto-debian-repository/
***
Locate your IP address.

```
hostname -I
```

### Node-Red

Once Node-red is running, access it through any web browser on the same wifi using the.ip.add:1880

***

In the dropdown, Click Manage Pallets to add dashboard or in terminal


```
npm install node-red-dashboard
```

```
sudo reboot
```




## Help

This is best to be used as an example. I tried to use a mixture of change nodes and function nodes to provide different ways to change the msg.payload

## Authors

Preston - Testing


## Version History

0.1 - Ruff draft
