This is to share my esp32 displays that I make in Home Assistant/ESPHome. The displays are capable of touch functions, but I am just using them as an 'always on' screen that has the exact info I want to see from HA (on a dark background). This is my first github repo/project, sorry in advance for not fully understanding how everything works. 

**esp-screen1 (4.0 inch, 320x480):**

![IMG_1441](https://github.com/user-attachments/assets/8e1a964e-7778-443d-8177-7e677714dc5b)

**esp-mini-screen1 (2.8 inch, 240x320):**

![IMG_1440](https://github.com/user-attachments/assets/d7a8045a-1421-47f3-8865-0654a07b1a7e)

The ports on the back of these are pretty limited, the referenced entities are not coming directly from the device. The referenced devices include Switchbot Thermo/Hygro sensors in my house/yard, the weather from NWS/Met.No (one gives inches of rain, the other gives % chance), and the AQI from AirVisual Cloud. I was able to attach an SR602 motion sensor to the weird I2C port on the 2.8" device using the 4-pin connector/wire, but am not really utilizing it yet.

I do the initial esphome flash using the device wizard in HA via serial usb, then update via WiFi after it gets an IP. I let the wizard generate the esphome/HA stuff, add the 'on_boot' piece for screen brightness up top, then add my code below the 'captive_portal' line. Make sure you add the device to HA through the esphome integration after setup.

I do my best to understand how the code works, but FYI I use Claude to generate/troubleshoot some of it.

**Potentially relevant sections of my homelab org chart (proxmox cluster):**
- debian/docker VM (hostname docky)
- gotify LXC (HA template entity polls this every 15min for 'Movie Downloaded' or 'Episode Downloaded')
- home assistant VM (hostname haos)
  - esphome addon

**Product List:**
1. 4.0 Inch ESP32-32E - ST7796S Driver - 320x480 TFT LCD - https://a.co/d/0j3O48Uz
2. 3D Printed Case from FreshPrintzScranton on Etsy (purchased separately for the 4" screens) - https://www.etsy.com/listing/4389343490
3. 2.8 Inch ESP32 (purchased with Acrylic Case) - ILI9341 Driver - 240x320 TFT LCD - https://a.co/d/0eFRdMfB

I haven't found the acrylic case included with the 2.8" to be super practical. I have one of the devices sitting on a phone stand but it doesn't look great, and I'm having trouble balancing/tucking the cable. The 3D printed ones are great, but end up costing almost as much as the devices.
