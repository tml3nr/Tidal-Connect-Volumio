### Hi Audiophile š

<!--
**shawaj/shawaj** is a āØ _special_ āØ repository because its `README.md` (this file) appears on your GitHub profile.

Here are some ideas to get you started:

- š­ Iām currently working on ...
- š± Iām currently learning ...
- šÆ Iām looking to collaborate on ...
- š¤ Iām looking for help with ...
- š¬ Ask me about ...
- š« How to reach me: ...
- š Pronouns: ...
- ā” Fun fact: ...
-->

# Tidal Connect Volumio 2.8x (Debian Jessie) setup instructions

###### Step by Step (10 Steps - Instructables)

This post will tell you how to install Tidal Connect on a Volumio for the Tidal App/Software Streaming HIFI/MQA.

Firstly download the Volumio image and extract it, then flash it to an SDCARD, you can get it here: https://volumio.org/get-started. Now insert that card into your Pi and wait something like 5 minutes. **Need setting your device DAC in Volumio**. Next, enable ssh so that you can setup Tidal Connect. To enable ssh, go http://volumio.local/DEV/ in your browser and click "ENABLE" under SSH. It doesn't report anything but you have just enabled the SSHd daemon. You can now login to your Volumio device with Putty.


#1./ **Enable SSH Volumio**
> http://volumio/dev
> 
> user: volumio
> 
> pass: volumio
> 

####
####
#2./ **Add stretch repo to sources list & apt update**
> chmod -R 777 /etc/apt/sources.list
> 
> echo "deb http://archive.raspbian.org/raspbian stretch main" >> /etc/apt/sources.list
> 
> sudo apt update
> 
####
####
#3./ **Install package**
> ...
####
####
#4./ **Install package needed dependencies**
> ...
####
####
#5./ **Create working folder & Clone git repo**
> sudo mkdir /usr/tid
>
> cd /usr/tid
>
> sudo git clone https://
> 
####
####
#6./ **Correct permissions**
> sudo chmod +x /usr/tid/play
> 
> sudo chmod +x /usr/tid/bin/tidal_connect
> 
> sudo chmod +x /usr/tid/pa_devs/run.sh
> 
####
####
#7./ **Deploy files**
> ./file-deploy.sh 
> 
####
####
#8./ **Check your devices DAC number**
> /usr/tid/pa_devs/bin/pa-devs-get
> 
####
####
#9./ **Setting device in Tidal Connect Service**
> ...
####
####
#10./ **Start service and check on status**
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
You can try setup instructions from https://github.com/shawaj/HiTide

