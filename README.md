First github project, sorry in advance for not fully understanding how everything works.

Relevant sections of homelab org chart:
> proxmox cluster
>> debian/docker VM (hostname docky)
>> gotify LXC (used for sonarr messages, struggling with radarr)
>> home assistant VM (hostname haos)
>>> esphome addon

I do the initial esphome flash using the wizard in HA via serial usb, then update via WiFi after it gets an IP. I let the wizard generate the esphome/HA stuff, add a couple pieces up top, then add my code below. Make sure to add the device through the esphome integration after setup.

The displays are capable of touch functions, but I am just using them for an 'always on' screen that has the exact info I want to see (on a dark background). I typically set the screen brightness to 5 or 10 in HA. 

I do my best to understand how the code works, but I do use Claude to generate/troubleshoot some of it.

esp-screen1:

![IMG_1441](https://github.com/user-attachments/assets/8e1a964e-7778-443d-8177-7e677714dc5b)

esp-mini-screen1:

![IMG_1440](https://github.com/user-attachments/assets/d7a8045a-1421-47f3-8865-0654a07b1a7e)


Product List:
* 4.0' ESP32-32E (pictured with separate 3D printed case) - ST7796S Driver - 320x480 TFT LCD - https://a.co/d/0j3O48Uz
* 3D Printed Case from FreshPrintzScranton on Etsy (I'm using this on the 4" screens) - https://www.etsy.com/listing/4389343490
* 2.8 Inch ESP32 (with Acrylic Case) - ILI9341 Driver - 240x320 TFT LCD - https://a.co/d/0eFRdMfB

I haven't found the acrylic case to be super practical. I have one of the devices sitting on a phone stand but it doesn't look great. The 3D printed ones are solid, but end up costing almost as much as the devices did.
