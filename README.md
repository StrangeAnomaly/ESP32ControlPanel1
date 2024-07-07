# ESP32ControlPanel1
This project controls 14 GPIO port pins via a browser and wifi. It incorporates websocket and SVG technology. Firefox is recommended [you've been warned]).

Use Arduino IDE version 1.8x (the latest Arduino IDE does NOT support SPIFFS, which is used to load browser files, you have been warned).

The .ino files causes SPIFFS to load three files: index.svg/script.js/styles.css.

If you do not know how to use the Arduino IDE with SPIFFS look it up, give this project up, find someone besides me to help you, use VS Code w/ Platform I/O, or toil for countless hours, which will probably end with you giving the project up.

This project is incomplete in that I want it to work with Android and Apple mobile devices. I have not (yet) achieved acceptable performance. 

So, I use my desktop. A screen shot of it in operation is provided.

Conceptually, as the SVG file only uses vw and vw percentages ESP32ControlPanel1 should work on any screen size.

To control the LEDs you will have to add a series resistor-LED circuit to each GPIO port that you want to control (suggest a 330 ohm resistor and a RED LED). Alternatively, you could use relay drivers to control relays. 

My immediate issues:

  I want to force mobile devices to operate in full-screen, landscape mode. 
  
  I need to test this project on a range of screen sizes.
  
  
