Baby Cry Detection with ESP32 and ThingSpeak

This project uses an ESP32 microcontroller to simulate baby cry detection using a potentiometer sensor. When the system detects a sound level above a threshold, it activates a buzzer and LED and sends the detected value to ThingSpeak for logging and visualization. Data is logged in the cloud via HTTP requests so behavior can be monitored remotely.

Features
*Connects to Wi-Fi and sends data to ThingSpeak using HTTP requests 
*Detects simulated cry input (potentiometer reading)
*Activates buzzer and LED on detection
*Logs sound level to ThingSpeak for remote data visualization

Hardware Required

*ESP32 Development Board
*Potentiometer (simulates sound sensor)
*Buzzer
*LED with suitable resistor
*Jumper wires and breadboard

Installation

1.Open the Arduino IDE.
2.Install the following libraries:
      *WiFi.h (comes with ESP32 board support)
      *HTTPClient.h for HTTP requests
3.Add your Wi-Fi credentials and ThingSpeak Write API Key.
4.If you haven’t created a ThingSpeak channel, log in and create one to obtain the API key. 
5.Random Nerd Tutorials
6.Upload the code to your ESP32 board.

Code Overview 

When the ESP32 reads an analog sound level above the cryThreshold, it will:
    *Ring the buzzer
    *Turn on the LED
    *Send the value to ThingSpeak via a GET request
    *Repeat every 2 seconds
You can adjust the threshold to fit your input sensor’s range.


Usage

1.After uploading code, open the Serial Monitor at 115200 to view debug messages.
2.Turn the potentiometer — values above the threshold simulate a cry event.
3.Visit your ThingSpeak channel to see live updates of the soundLevel field.


Future Enhancements
*Replace potentiometer with an actual microphone sound sensor
*Add machine learning or signal processing to classify different cry patterns
*Integrate notifications (email/SMS) using ThingSpeak Apps

License
       -This project is released under the MIT License.
