# Diabetes Night Guard 

#What is it about?

Night Guard is offshot of famous NightScout project, and also some others (xDrip, Parakeet), which produce little different hardware for similar software.

Intent is to make current solutions less DIY project as it is now. End user just needs to configure himself/herself on our system (for now this can be found under www.atech-software.com/nightguard), set configuration on hardware (we have also partner where you can order NightGuard/NightScout/xDrip/ modules) and start.

# Web site
Like you see our web site is still work in progress. Portal will be available on 1.9. (see Timeplan). If you are interested to be beta tester, then contact us and we will provide you access.

# Timeplan for development of project
- now - Webservice for Parkeet beta testing
- 28.8.2016 - Webservice for Parkeet running 
- 1.9.2016 - Portal beta testing with some basic functionalities (add user, add device, add connector, settintgs)
- 1.10.2016 - Webservice for xDrip bridge running
- 1.11.2016 - Offical opening of Portal (Basic functionalities)
- 1.12.2016 - Display data in portal
- 1.1.2017 - Offical start of project as payable service
- 1.2.2017 - Display data in graph

# Why pay if I can do it myself?
If you can do it yourself, good for you. This project is intended mainly for people who can't. Not everybody can download projects and deploy them to some server, create own database and so on. Currently you need at least some know-how to be able to get solution running, and if you go with offical project, you need to setup MongoDb/Mlab and Azure Web pages (first one is free for now (if you don't have to much data), but second one is not (from my latest info its about 9USD for month if you go with chepest solution). Our service is 2 EUR pro monitored diabetic device (e.g. Dexcom) pro month.

# Priceplan
We have currently one one priceplan planned, which is 2 EUR / diabetic device (monitored device - CGMS) / month. 

# How to start
1. You need to register yourself on website - Portal
2. Build yourself connector (see next chapter), or order one (we have subcontractor who can make you connector, if you can't build it yourself, see Ordering connector).
3. Load correct software to your connector device (see Software for connector)
4. Register your diabetes device (we currently only support Dexcom 4) and connector.
5. Register connector you will use to download data. 
6. Install xDrip+ software (we might create our own version in future, but for now we use this one, see Software for Viewer chapter)
7. And we are done.

# Connector - what is that?
Connector is actually device, that will read data from your diabetes device (e.g. Sensor) and send it to NightGuard webservice. We currently support two such connectors:
1. xDrip/xBridge/xBridge2: Wixel (Processor with Radio Receiver) and BlueTooth module which sends data via your Mobile device to NightGuard webservice. (support active after 1.10.2016)
2. Parakeet: Wixel (Processor with Radio Receiver) and SIM module which send data with help of SIM card to NightGuard webservice.

# Ordering connector
If you are interested in ordering connector, we have some subcontractors who can do this for you. We hope to find several more in the future (if you are interested contact us) to aid us and you.

# Software for connector
Connector has small curcuit called Wixel, where simple software will run (in further text wixel software). You need to build this wixel software (again if you are unable to, let us know, or write to us over Portal (there is option Requests, where you can send all required data). Since your personal data (Serial number of Dexcom receiver, uuid of connector for our WS and in case of Parakeet also APN from your Mobile provider) needs to be compiled in, we can't prepare this wixel software beforehand.

So what do you need?
1. If you will make image yourself (Portal can prepare your settings automatically) you will need compile tools (see link), if not go to point 2.
2. You need drivers and software to upload this wixel software image into your hardware

Here are detailed instructions on both points: https://www.pololu.com/docs/0J46/all#3

# How to create connector
In short you need to do this:
1. Get correct guide
2. Visit amazon.com and buy correct elements (or some other site)
3. Solder everything together
4. Attach battery
5. Upload Wixel image (see guide) and off you go..

Here are relevant guides: 
- Parakeet - https://drive.google.com/file/d/0B6mvYVNVC-fOU2NnV0hJZ3VBeWc/view
- xDrip Bridge - https://github.com/StephenBlackWasAlreadyTaken/xDrip/wiki/xDrip-Wireless-Bridge
- xDrip Bridge V2 (use this one) - https://github.com/jstevensog/wixel-sdk/blob/master/apps/xBridge2/xBridge2.pdf

# Software for Viewer
We are currently supporting only xDrip+ software, available on this site - https://jamorham.github.io

# Links

Here are few links linked with this project (and sub-project)
- Nightscout project - http://www.nightscout.info/ 
- Original xDrip project (home of xDrip and xDrip bridge) - http://stephenblackwasalreadytaken.github.io/xDrip/
- Parakeet/xDrip+ page - https://jamorham.github.io/


