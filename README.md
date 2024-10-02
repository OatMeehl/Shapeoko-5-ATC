# Shapeoko 5 Pro 4x4 ATC
![Shapeoko5 ATC](https://github.com/user-attachments/assets/4debbb05-b612-4f68-82fa-ab4cc2f4993e)
<img width="750" alt="Tool Print+Render" src="https://github.com/user-attachments/assets/a906cb31-705a-4400-9f26-af173bee5635">

### Things needed to buy;

2.2kw water cooled spindle with VFD - https://www.aliexpress.us/item/3256802808501425.html?spm=a2g0o.order_list.order_list_main.5.53451802R5zNQh&gatewayAdapt=glo2usa

80mm Spindle Mount - I machined my own but it looks like Carbide3D has one now. https://shop.carbide3d.com/products/80mm-spindle-mount-s5

Cooling System - either a tank of water with a submersible pump or a small chiller.

Air compressor - The quiet ones are nice - https://www.harborfreight.com/1-gallon-135-psi-ultra-quiet-oil-free-hand-carry-jobsite-air-compressor-64592.html

Air Pump - Creates constant positive pressure to keep dust out of spindle bearings. https://a.co/d/5YxAlrj

Qty 7 - Proximity Sensors - https://a.co/d/2bBb0iI

ISO20 Tool Holders - https://a.co/d/e9mtsC4

Timer Relay - https://a.co/d/9uUspSC

24V Power Supply - https://a.co/d/etT1WPE

Solenoid Valve - https://a.co/d/fbD1gJ7

Tool Release Button - https://a.co/d/0YxQrxa

Cable Glands - https://a.co/d/78sGWZN

6mm Flow Control - https://a.co/d/1PORBhs

6mm Y Splitter - https://a.co/d/9BAZi52

Terminal Block - https://a.co/d/eLBwwW1


This is a fairly involved project to take on. The requirement to install a 220V circuit for the spindle and do the wiring and VFD setup might be a bit much for some people. If you're the adventurous type and have some mechanical and electrical skills you should be good to go. I'll show what I did as much as I can but I'm sure I'll be missing some stuff since I did most of this over a year ago. Use common sense and build at your own risk!

***This will only work if you are using the Fusion360 payed version since the free one doesn't allow tool changes. If Carbide3D would open up their Carbide Create posts for editing I could maybe add the Gcode that would be needed to make this work, but currently that isn't the case. Even if you don't use automated tool changing, the convenience and speed of manual tool changes is still worth it in my opinion.

This is a project for an automated tool changing system for the Shapeoko 5 Pro CNC router. It uses an Aliexpress ATC spindle and other components to make it happen. The tool holder stations mount directly to the table and should be printed out of ABS. This system is run on Carbide Motion software. The tool changes are controlled by G code output from a Fusion 360 Post processor. When the spindle goes to a tool location and gets within range of the proximity sensor, the solenoid is activated and is latched in by a timer relay with a 3 second latch time. During that time the spindle will fully lower into the tool position. If we want the tool to stay in the spindle we simply stay in the position longer than the timer relay time and if we want to leave a tool we leave before that time. The G code then issues an M6 which will cause Carbide Motion to give a confirmation dialog. I use Dialog Demon https://dair.com/ddevil/ to auto-confirm that dialog. Then our tool measure cycle can commence and we're ready to party! 
