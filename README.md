# Tidal Connect Volumio setup instructions

###### Step by Step (10 Steps - Instructables)

This post will tell you how to install Tidal Connect on a Volumio for the Tidal App/Software Streaming HIFI/MQA.

Firstly download the Volumio image and extract it, then flash it to an SDCARD, you can get it here. Now insert that card into your Pi and wait something like 5 minutes. Next, enable ssh so that you can setup the audio driver DAC. To enable ssh, go http://volumio.local/DEV/ in your browser and click "ENABLE" under SSH. It doesn't report anything but you have just enabled the SSHd daemon. You can now login to your Volumio device with Putty.


#1./ Enable SSH Volumio
> http://volumio/dev
> 
> user: volumio
> 
> pass: volumio
> 
####
####
#2./ Add stretch repo to sources list & apt update
> chmod -R 777 /etc/apt/sources.list
> 
> echo "deb http://archive.raspbian.org/raspbian stretch main" >> /etc/apt/sources.list
> 
> sudo apt update
> 
####
####
#3./ Install package
> ...
####
####
#4./ Install package needed dependencies
> ...
####
####
#5./ Create working folder & Clone git repo
> sudo mkdir /usr/tid
>
> cd /usr/tid
>
> sudo git clone https://github.com/shawaj/ifi-tidal-release
> 
####
####
#6./ Correct permissions
> sudo chmod +x /usr/tid/play
> 
> sudo chmod +x /usr/tid/bin/tidal_connect
> 
> sudo chmod +x /usr/tid/pa_devs/run.sh
> 
####
####
#7./ Deploy files
> ./file-deploy.sh 
> 
####
####
#8./ Check your devices (DAC)
> /usr/tid/pa_devs/bin/ifi-pa-devs-get
> 
####
####
#9./ Setting device in Tidal Connect Service
> ...
####
####
#10./ Start service and check on status
> sudo systemctl daemon-reload
>
> sudo systemctl enable tidal-connect.service
>
> sudo systemctl restart tidal-connect.service
>
> sudo systemctl status tidal-connect.service
> 
> 
####
####
I am testing Tidal Connect Volumio now, the setup instructions not yet finish....
