I automate things around my home using an ESP32 microcontroller, Blynk app on my iPhone and IFTTT.
I program the ESP32 using the Arduino IDE following the instructions from RandomNerdTutorials.com but use Blynk rather than a Web Client to communicate with the ESP32


##To send data from the ESP32 to the Blynk app on the iPhone
on the hardware code add
make a Blynk timer say 
Add the code below;
timerLightOn() {
Blynk.virtualWrite(V6,1); where V1 is the virtual pin being written to and 1 is the value being written
}
in the setup {} block include the line
????
on the Blynk app add a Value widget, Set the INPUT to V6 and the REFRESH INTERVAL to Push




##To send data from the ESP32 to IFTTT use a Webhook on the Blynk App.
The OUTPUT is set to a virtual pin say V3
The hardware writes to this using the command: Blynk.virtualWrite(V3,1); where 1 is the value that can be sent to IFTTT in the url, the text /pin/ is replaced by the value
METHOD is GET
CONTENT TYPE is application/json
for example:  https://maker.ifttt.com/trigger/Fountain/pin//with/key/de..................K



