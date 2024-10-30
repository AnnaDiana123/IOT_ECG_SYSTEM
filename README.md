# IOT ECG System

ECG MONITORING SYSTEM:


The goal of this project is to enhance cardiac health monitoring with the help of
technology. The project focuses on developing a system that includes a device for monitoring the
user's heart electrical activity and a web application where both patients and doctors can visualise
and interact with the health information. This system is especially helpful for people who find it
difficult to visit doctors regularly, such as elderly people or those living in remote areas.

Utilising the AD8232 electrocardiogram sensor module connected to the ESP8266
Plusivo development board, the system captures real-time electrocardiogram data through a
wireless and portable setup. Data preprocessing is performed by the Raspberry Pi 4 Model B,
which extracts heart rate variability metrics, such as the heart rate, the root mean square of
successive differences between normal heartbeats, and the standard deviation of the NN
intervals. Then the data is transmitted to the cloud. The system also includes a web application
developed using JavaScript, HTML, CSS, and Firebase services. The applications offer two types
of accounts, for users and an admin/doctor, and ensure secure user authentication, offer live
electrocardiogram data visualisation, enable access to historical data, and facilitate the
generation of medical reports. These reports include reference ranges for the heart rate variability
metrics and medical interpretations, enhancing the utility of the data for both patients and doctors.
The system also sends real-time alert notifications via email for abnormal cardiac activities,
significantly improving responsiveness in emergency situations.

This project not only simplifies cardiac monitoring but also enhances the quality of life by
providing a user-friendly and efficient healthcare monitoring solution.

This project consists of three parts, each with its own repository.

1. ESP8266 Code: https://github.com/AnnaDiana123/ESP8266_ECG_APP.git
2. Raspberry Pi Code: https://github.com/AnnaDiana123/RaspberryPi_ECG_APP.git
3. Web Application Code: https://github.com/AnnaDiana123/ECG_WEB_APP.git


ESP8266 Code:

1. Download Arduino IDE from https://www.arduino.cc/en/software.
2. Install the Arduino IDE.
3. Open Arduino iDE, click on File-> Preferences and in the field Additional Board Manager URLs add http://arduino.esp8266.com/stable/package_esp8266com_index.json and click OK.
4. Open Tools-> Board -> Boards Manager. In the opened window search for ESP8266 and install the package.
5. Open Tools->Board and select NODEMCU 1.0 (ESP - 12E module).
6. Open Sketch-> Include Library-> Manage Libraries search for the following libraries: WifiManager, ESP8266HTTPClient and NTPClient and install them.
7. Open the ESP8266_Reading.ino file and connect the board to a computer via USB.
8. Go to Tools and select the appropriate port.
9. Click on the Upload button.
10. Connect the microcontroller to WiFi by using a phone, tablet, or laptop to connect to the ECGDEVICEAP access point. Once connected, open a web browser and navigate to 192.168.4.1.
11. Enter the wifi network and password in the configuration portal to connect the ESP8266 to the respective wifi.
12. Attach the ECG patches to your chest/arms and leg to capture the ECG signal.

Raspberry Pi Code:

1. Open a terminal on your Raspberry Pi.
2. Set up a virtual environment, install the package: sudo apt-get install python3-venv
3. Create the virtual environment: python3 -m venv my_flask_env
4. Activate the environment: source my_flask_env/bin/activate
5. Install Flask: pip install Flask
6. Install Firebase Admin SDK: pip intall firebase-admin
7. Install numpy and scipy: pip install numpy scipy
8. Run the app: python RaspPi_LocalServer.py

Note: The Raspberry Pi and the ESP8266 need to be connected to the same WiFi network in order to communicate.

Web App Code:

1. Install Node.js from https://nodejs.org/en/download/prebuilt-installer .
2. Install project dependencies: npm install
3. Start the development server: npm run dev
4. Access the web application by opening a browser and going to the URL provided in the terminal.
5. Create a new account and sign in in order to see the ECG data.

The web application can also be accessed at the following link: https://ecgapp-7d874.web.app/