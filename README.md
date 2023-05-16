# intrusiondetection
Raspberry Pi based intrusion detection system with email notification including webcam and PIR sensor.
# To prepare the pie use these commands in the terminal
Step 1: sudo apt-get install python-picamera
Step 2: sudo apt-get update
Step 3: sudo apt-get upgrade
Reboot the system
Step 4: sudo apt-get install ssmtp
Step 5: sudo apt-get install mailutils
Step 6: sudo nano /etc/ssmtp/ssmtp.conf
Edit this config file and add:
  root=requiredemail
  mailhub=smtp.gmail.com:587
  hostname=raspberrypi
  AuthUser=requiredemail
  AuthPass=password
  FromLineOverride=YES
  UseSTARTTLS=YES
  UseTLS=YES
