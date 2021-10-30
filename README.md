# bettyproject
Smart Home Automation display and control for Vanlifers, RVers, tiny homers, and general off-gridders.

STAGE 1:
- STATUS: Power system (JBD BMS, Inverter), Temperature/Humidity
- CONTROL: Zone lighting, Diesel heater, Fan
- INTERACTION: Touchscreen (Fully Kiosk on Fire Tablet), LAN Webpage, Voice (Rhasspy)
- MEDIA: Basic SAMBA NAS
- 

STAGE X:
**Central Hub for off-grid / tiny homes / van dwellings** 
- Shows STATUS of home and logs data for analysis and preemptive warnings. (ie. (You’re getting low on water”) Solar/battery/water/fuel. Also uses sensors for awareness of environment and calculate efficiency. (Inside/outside temp, humidity)
- CONTROLS zone lighting/heating/cooling/battery management 
- INTERACTION via touchscreen, voice, phone, remote control
- NETWORK control and WiFi AP for phone hotspot, LTE modem/jetpack, external WiFi networks (McD’s, WF)
- MEDIA/ENTERTAINMENT hub. Store and distribute movies/pictures across network as NAS. HTPC via Kodi to secondary monitors or projectors. Game system via Retropie. Function as Bluetooth speaker / HiFi / streaming destination from phone. 
* Functions well offline/local, enhanced online
* Minimal and scaleable cost based on progressive functionality 
* Extensible 
* Beautiful and elegant to use for anyone 
* Low EMF, minimal wireless
* Compact/portable 

Abilities:
    - Power
        - Solar
            - Victron MPPT tracking
                - https://github.com/victronenergy/venus/wiki
                - https://community.victronenergy.com/questions/16842/raspberry-pi-the-very-basic-please.html
                - Ve.direct https://www.sv-zanshin.com/r/manuals/victron-ve-direct-protocol.pdf
            - MPP Solar
                - https://github.com/ned-kelly/docker-voltronic-homeassistant
        - Battery
            - SOC, voltage, net current, load 
            - JBD BMS: https://diysolarforum.com/threads/jbd-bms-wi-fi-module.17252/page-10
        - Data logging/analysis/warning
    - Control
        - Lights
            - Zoned/dimmable/sceneable lighting on touchscreen or voice
            - Wake sunrise light alarm with music 
            - SAD light
            - Bluetooth yongnuo
                - https://github.com/kenkeiter/lantern
                - https://medium.com/@urish/reverse-engineering-a-bluetooth-lightbulb-56580fcb7546
                - https://learn.adafruit.com/reverse-engineering-a-bluetooth-low-energy-light-bulb/overview
            - IR strip lights
            - Individually addressable zone lighting
                - https://tutorials-raspberrypi.com/connect-control-raspberry-pi-ws2812-rgb-led-strips/
                - https://youtu.be/9KI36GTgwuQ
                - https://quinled.info/2018/08/23/my-favorite-warm-white-led-strip/
                - https://www.alconlighting.com/blog/residential-led-lighting/how-do-i-determine-how-many-led-lumens-i-need-for-a-space/
        - MaxxFan IR
            - Open, close, speed, direction 
        - Diesel heater
            - Afterburner
    - Sensor
        - Temperature/ humidity inside and out
            - https://projects.raspberrypi.org/en/projects/build-your-own-weather-station/2
            - https://www.raspberrypi.org/forums/viewtopic.php?t=201333
            - https://github.com/alex-konshin/f007th-rpi
        - Proximity 
            - Inside enter vehicle
            - Outside, for animal/human video
        - Tilt for leveling
            - “Hey Betty, help me level” “Ok, nose up 5”, tilt left 3”
        - Propane level
            - https://mopeka.com
    - Connection
        - WiFi access point for LTE modems/hotspots
        - WiFi repeater for McD’s/Starbucks/library networks
            - https://raspap.com
    - Media
        - NAS
            - Movies
            - Photo backup
                - PhotoSync – transfer photos by touchbyte GmbH
                    - https://apps.apple.com/us/app/photosync-transfer-photos/id415850124
            - https://youtu.be/s0Sc2n3gUqA
        - Kodi client
        - Airplay / Chromecast receiver
            - https://github.com/FD-/RPiPlay
    - Gaming
        - Emulator of Retropi consoles
            - https://youtu.be/7fmiUWmCi3Q
    - Interaction
        - Remote (phone access)
            - https://youtu.be/S_32H-CKTCs
        - Touchscreen
            - To fully turn off black light to usb screen https://github.com/mvp/uhubctl/blob/master/README.md
        - Voice control
            - https://medium.com/better-programming/building-your-custom-voice-assistants-an-overview-of-the-current-solutions-and-integrations-d8db227a325
            - http://docs.kitt.ai/snowboy/
            - https://www.hackster.io/dmitrywat/offline-speech-recognition-on-raspberry-pi-4-with-respeaker-c537e7
            - https://www.seeedstudio.com/blog/2020/01/23/offline-speech-recognition-on-raspberry-pi-4-with-respeaker/
            - https://hacks.mozilla.org/2019/12/deepspeech-0-6-mozillas-speech-to-text-engine/
            - https://www.slanglabs.in/blog/how-to-build-python-transcriber-using-mozilla-deepspeech?ref=hackernoon.com
            - https://hackaday.com/2017/05/30/diy-google-aiy/
            - https://rhasspy.readthedocs.io/en/latest/
        - Security
        - Code word checkin on person detection
        - If unauthorized, “you are trespassing, calling police. Ring ring ring, this is the police, hi, I’d like to report a robbery. White Ram Promaster van, sending gps coordinates now. Got it, we are sending a unit your way. Ok, will update you on vehicle location. 

- Bluetooth speaker?
    - https://www.instructables.com/id/Turn-your-Raspberry-Pi-into-a-Portable-Bluetooth-A/



HARDWARE:
    - Magic Mirror
        - https://youtu.be/RWjvJq4Zabk
- Raspberry Pi 4 B 4GB
- 5V 3A (15W) usb-c 12V cigarette
- 32 or 64GB SD card
- Case (Argon One)
- 7” touchscreen
- Audio speaker / mic
    - PS3 Eye mic/Ir
        - https://www.cnx-software.com/2019/08/30/using-sony-ps3-eye-camera-as-an-inexpensive-microphone-array/
- (1) Micro HDMI - HDMI cable

INTEGRATION:
Node
Hass.io Home Automation 
    - https://youtu.be/XntGFVeg2eE
    - Kodi & Retropie & Home Automation 
https://community.home-assistant.io/t/ha-and-kodi-on-same-raspberry-pi/13181/18

    - UI examples 
        - https://marcelliot.net/home-assistant-lovelace-theme/
        - https://awesomeopensource.com/project/bbbenji/synthwave-hass
        - https://youtu.be/gKoBwl7QUds
        - https://youtu.be/weZFfrjF-k4
    - UI possibilities 
        - https://youtu.be/LsFUwqb-6As
HomeKit 
    - https://medium.com/@adamargo/how-i-use-raspberry-pis-for-homekit-automation-ed69df8d8be7
- Mozilla IoT 
    - https://github.com/mozilla-iot/gateway

Interaction
    - Keyboard touchpad combo
    - Gaming controller
    - Remote access
        - MacOs App Store Microsoft RDP
    - Voice
        - Google AIY
        - Core microphone array
        - Hey Betty, good evening - evening light
        - “Hey Betty, shh” - turn off all lights, touchscreen, pause media, no response for stealth situations
            - “Coast is clear” - resume “Got it”
        - “Hey Betty, lets go!” “Let’s drive” “Batten down the hatches”
        - “It’s hot!”
        - “I’m cold.”
        - “I’m lonely” - Play it’s not easy being green
        - “Hey Betty, let me know when I’m in service.” 
        - “How level am I?” You’re close, nose up a little ... keep going ... a little more ... got it” 
        - “How many rocks do I need to be level?” 3” front left, 4” front right. 

MISCELLANEOUS 
Auto accept terms of service for public wifi
    - https://www.freecodecamp.org/news/how-i-created-a-python-bot-to-automatically-log-into-a-captive-portal-3d4ba04dee9f/
Bluetooth sniffing 
http://nilhcem.com/iot/reverse-engineering-simple-bluetooth-devices
https://www.polidea.com/blog/bluetooth-low-energy-sniffing-guide/
https://www.novelbits.io/best-bluetooth-low-energy-sniffer-tutorial-connections/
https://reverse-engineering-ble-devices.readthedocs.io/en/latest/protocol_reveng/00_protocol_reveng.html

Raspberry Pi revision code checking
cat /proc/cpuinfo | grep "Revision"
root@pi4:/home/pi# cat /proc/cpuinfo
—  Revision	: c03112
https://www.raspberrypi.org/forums/viewtopic.php?t=259629
Solar Controller Hacks and Arduino Integration
