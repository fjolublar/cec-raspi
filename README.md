# cec-raspi
Turn the TV On and Off with a Raspberry Pi and a Flask app

# Guides

  - [Raspberry Pi Power TV over CEC](https://www.linuxuprising.com/2019/07/raspberry-pi-power-on-off-tv-connected.html)
  - [How to enable hdmi cec on TV](https://www.howtogeek.com/207186/how-to-enable-hdmi-cec-on-your-tv-and-why-you-should/)
  - [CEC commands over HDMI](https://elinux.org/CEC_(Consumer_Electronics_Control)_over_HDMI)

Keep in mind that TV-audio can not be controlled via CEC-HDMI

---

# TLDR:

-1. Install **cec-utils** library in the Raspberry Pi
  >`sudo apt install cec-utils`
-2. List devices that support cec
  >`echo 'scan' | cec-client -s -d 1`
-3. Check **Power Status** of TV
  >`echo 'pow <DEVICE #>' | cec-client -s -d 1s`
-4. **Power ON** TV
  >`echo 'on <DEVICE #>' | cec-client -s -d 1`
-5. **Power OFF** TV
  >`echo 'standby <DEVICE #>' | cec-client -s -d 1`
-6. Make Rapsi the active source
  >`echo 'as' | cec-client -s -d 1`
-7. List all the available commands of HDMI-CEC
  >`echo h | cec-client -s -d 1`
 
 
 
