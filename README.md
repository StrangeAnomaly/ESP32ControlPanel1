# ESP32ControlPanel1
This project is a modification of the ever-popular controlling of an LED via wifi. 
The project controls 14 GPIO port pins via a browser. 
This project uses SVG (not HTML). As different browsers render SVG differently use of Firefox is suggested [you've been warned]).
  You should use the Arduino IDE 1.8x (or you could screw around with Visual Studio Code or, horror of all horrors, the Espressif IDE). Why? Because SPIFFS loads the needed files and the new Arduino IDE does not support SPIFFS.
  You could also try the LittleFS file system. Last year it was BIG, this year it seems to have disappeared. hmmmm
  SPIFFS loads three files into your browser: index.svg/script.js/styles.css.
  The .ino files causes SPIFFS to load those files and causes the ESP32 to act right.
  If you do not know how to use the Arduino IDE with SPIFFS look it up, give this project up, find someone besides me to help you, or toil for countless hours, which will probably end up with you giving the project up.
  Line 10 is actually trivial to do.... after you've done it a couple of times. Until then the instructions on how to do it are gibberish and I do not speak or interpret gibberish.
  My original intent was to use my cute little Android phone or my cuter Apple phone to control those LEDs. I have not (yet) achieved acceptable performance. Oh, you can control the LEDs, but the UI sucks. 
  So, I use my desktop. 
  I do NOT use pixel measurements. All locations are given in terms of vh and vw (SVG stuff). Conceptually, ESP32ControlPanel1 should work on any screen size. "Conceptually" is yet another expansive word.
You will need to add a series resistor-LED (use a 330 ohm resistor and a RED or yellow LED. okay?) to each ESP32 GPIO that you want to control. Bias the LEDs correctly, okay? Look it up. Anode toward the GPIO pins. 
Alternatively, or in addition, you could use transistors to control relays. Then you can wire up all kinds of stuff with this puppy. Endeavor not to burn your house down. 3.3V seems safe. 
So, here are my immediate problems:
  I want to force mobile devices that use this program to operate in full-screen, landscape mode. That is sure to pisz a whole lot of people off. But, flipping the phone causes vh and vw locations to flip flop around.
  I do not yet know how to do that.
  Once I can control the screen I can re-space the switches/browser LEDs to make it look better. I know how to do that. 
  I need to test this project on a range of screen sizes. I only have the one desktop screen.
    I added a switch-controlled grid which could be useful. or not. Self-explanatory.
    I also added X and Y coordinates for mouse clicks. I use those more than the grid. No explanation needed (just click in the browser). 
    If you don't like my color scheme let me know. I might change it. or not. 
  
  
