# intrusiondetection
Raspberry Pi based intrusion detection system with email notification including webcam and PIR sensor. <br>
## Output <br>
This project sets up an automated system that detects motion using a PIR sensor and captures an image using a webcam whenever motion is detected. It then sends an email alert with the captured image, providing a simple yet effective security system. This could be used to monitor a room, a house, or any other environment where you want to be alerted of any movement. <br>
## To prepare the pie use these commands in the terminal <br>
Step 1: sudo apt-get install python-picamera <br>
Step 2: sudo apt-get update <br>
Step 3: sudo apt-get upgrade <br>
Reboot the system <br>
Step 4: sudo apt-get install ssmtp <br>
Step 5: sudo apt-get install mailutils <br>
Step 6: sudo nano /etc/ssmtp/ssmtp.conf <br>
Edit this config file and add: <br>
  root=requiredemail <br>
  mailhub=smtp.gmail.com:587 <br>
  hostname=raspberrypi <br>
  AuthUser=requiredemail <br>
  AuthPass=password <br>
  FromLineOverride=YES <br>
  UseSTARTTLS=YES <br>
  UseTLS=YES <br>
