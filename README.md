<h1>Zigbee Home Enargy Monitor</h1> 

<h2>SAFETY FIRST!</h2>
This project requires you to deal with mains voltage, which is extremely dangerous and can cause severe injuries and even death.

Connecting this equipment to your home electrical wiring might void its certification, and your insurance can and will refuse to pay if something bad happens.

If you believe you lack the necessary skills and knowledge, I strongly advise you to hire a professional electrician and DO NOT ATTEMPT IT YOURSELF!

I take no responsibility. You have been warned!

<h2>Description</h2>
The project consists of a ZigBee device which use to monitor home energy consumption and relay that data into smart home platforms like Home Assistant and Openhab. It uses Zigbee protocol rather than wifi for better range and stability. It uses a CC2530 Zigbee chip and Pzem-004t with a custom-made PCB. It also can be operated with AC and DC power supply.also, it work with Zigbee2mqtt and zha framework 



<h2>Essential Components</h2>

- <b>CC2530</b> 
- <b>PZEM-004T</b>
- <b>Hi-link 5V 2W AC to DC Power Supply Module</b>
- <b>Mini 360 Step-Down Buck Converter Power Module</b>
- <b>Custom PCB (optional)</b>





<h2>Software  Used </h2>

- <b>[Zigbee Configurable Firmware](https://ptvo.info/zigbee-switch-configurable-firmware-v2-210/)</b>
- <b>[Programing CC2530](https://blog.boris-wach.de/permalink/265)</b>


 <h2>PTVO firmware Configuration </h2>

 This is custom device which work both with ZHA and z2m,Inorder to work with them For ZHA a cuystom quirk shoud load
 
 <b>For Home Assistant Quirks </b>[More](https://www.home-assistant.io/integrations/zha/)

 For ZHA [File](https://github.com/delta010/Zigbee-Energy-Monitor/blob/main/pzem004t.py)
 
```zha:
  enable_quirks: true
  custom_quirks_path: /config/custom_zha_quirks
```
 <b>For Zigbee2mqtt Device Handiler </b>[More](https://www.home-assistant.io/integrations/zha/)

 For Z2M [File](https://github.com/delta010/Zigbee-Energy-Monitor/blob/main/PZEMENERGY.js)
 
 ```
external_converters:
       - PZEMENERGY.js
       
```

Custom PCB Gerber [File](https://github.com/delta010/Zigbee-Energy-Monitor/blob/main/zigbeepzem.zip)
 
 

<p align="center">
 <br/>
<img src="https://github.com/delta010/Zigbee-Energy-Monitor/assets/29528880/5a0b0df7-fcdf-4106-926f-9a0a39c8d6a9" />
<br />
<br />

<img src="https://github.com/delta010/Zigbee-Energy-Monitor/assets/29528880/def497b7-8cd3-48a2-bcf2-04cbe828027e"/>
<br />
<br />


</p>

<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
