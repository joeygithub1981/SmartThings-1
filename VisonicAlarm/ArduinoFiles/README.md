These files are needed if you have a very old Powermax+ or an American style Powermax Pro (UK style seems to work fine and some American models will also work - I suggest trying without, and if you do not get alarm status or zone names then try adding the Arduino - after discussion on SmartThings forum).

Since the UART pins of the ESP dont reliably work with the Powermax and I have used an Arduino (Nano but could be another option) in between, in order to get clean timing of the Serial data. Without installing Arduino Studio and setting up libraries and burning bootloaders, I have added XLoader into the Github folder (http://www.hobbytronics.co.uk/arduino-xloader) since this should make it easier. This firmware will also toggle the Arduino LED every time a valid command is received, this is really useful in troubleshooting, since you should see the LED flash (either very fast or very slow, based on what data is flowing at the time).

Once you have flashed the Arduino and the Wemos then these are the connections that you need to follow: (Note, it is better to connect the Wemos to 12V since the 12V power supply is stronger than the 5V supply, however the Arduino draws tiny amounts of power, hence can work on the 5V without risk). Do not connect 12V to the Arduino, but you can take 5V off the Wemos and connect this power source to the Arduino if required.
![Wiring Diagram](WemosAndArduinoWiringDiagram.jpg?raw=true)

After you have made these connections, you should have a working communication between the Wemos and Powermax!
