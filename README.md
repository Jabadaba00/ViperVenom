<img src="https://revise7.com/wp-content/uploads/2021/07/Logo2.svg" width="400">

# ViperVenom Spyware Tool for Pentesters

ViperVenom is an open-source cyber offensive tool developed by [Revise7 Security](https://revise7.com)
for pentesters, the tool has the ability to webcam record, screenshot, screenshare and
screen video record in high-quality.
ViperVenom is a great tool when it comes to pentesting assessments, as some sort of a proof
that you broke it to a computer and was able to install ViperVenom to capture the screen

Help us improve the tool by [contacting us](https://revise7.com/contacts/), or by sending an [issue](https://github.com/Revise7/ViperVenom/issues)
Keep in mind, the tool is currently in beta, bugs may happen.

## Install Tool
To create the latest tool for your platform from this source repository:

##### Install Python Extensions for vipervenom.py:
* socket
* time
* platform
* os
* threading
* termcolor
* vidstream

## Error while installing pyaudio
To fix this issue, check out [stackoverflow](https://stackoverflow.com/questions/53866104/pyaudio-failed-to-install-windows-10/53866322)

##### Download and extract the source:
[Download Directly from GitHub](https://github.com/Revise7/ViperVenom/archive/refs/heads/main.zip)
```
$ unzip ViperVenom-main.zip
$ cd ViperVenom-main
```
**NOTE:** Instead of downloading the compressed source, you may instead want to clone the GitHub 
repository:
```
$ https://github.com/Revise7/ViperVenom.git
$ cd ViperVenom
$ pip3 install -r requirements.txt
$ python3 vipervenom.py
```

##### ViperVenom's client.py file: 
```
$ gedit client.py
$ pip3 install -r client_requirements.txt
```
To connect a computer to the listener(you, most likely) you need to edit a few things in the file
and as well as installing a few Python extensions, for now. The client must have the latest Python
installation, and the Python extensions used in the client.py, but you can use the Py2Exe to create
an executable.

#### Edit client.py file
* Line 17, required, put your local or public IP address
* Line 18, optional, default port: 443
* Line 26, 29, optional, default port is: 4444, you can change it to whatever you like.
* Line 40, optional, recommended not to change to other SMTP servers than Gmail, as well as its port.
* Line 42, 44, required for sending screenshots back to you through an email account, change the sender and receiver Gmail account, line 42 requires your Gmail credentials,
  For security reasons, open a new Gmail account, and enable "Less secure apps" in your account settings, use this [helpful arcticle](https://hotter.io/docs/email-accounts/secure-app-gmail/)
* Line 48, recommended, if you ever wanted to record the victim's microphone, you will need to set the amount of time to record, you won't be able to change this option after second into the victim, please keep it in mind.

#### Edit vipervenom.py file
* Line 54, optional, default port: 443
* Line 66, optional, probably keep it as it is, default port: 4444, if you will edit this, you will need to edit client.py, lines 26 and 29 to the same port.

##### To connect your target computer:
```
$ Python3 client.py
```

##### Install Python Extensions for client.py:
* pillow
* vidstream
* socket
* getpass
* smtplib
* base64
* os
* platform
* sounddevice
* scipy
* time
* subprocess
* cv2
* numpy
* pyaudiogui

## Special Commands
```
screenshare
```
Screenshares the victim's computer screen and sends it to the attacker in real-time.
```
webcam_stream
```
Streams victim's webcam.
```
screenshot
```
Screenshots victim's computer and sends it directly to your Gmail account as base64 encoded image, decrypt it using the decode_image.py
that comes with ViperVenom and paste the base64 string in base64.txt and run the Python file
```
$ python dcode_image.py
```
The screenshot should appear in ViperVenom's folder in a .jpg file.
```
mic_record
```
Records victim's microphone input( if the victim has an available microphone) for an amount of time you set.
Known bug: You won't be able to type more commands after executing this command, we're working on a fix.
```
vid_record
```
Record victim's screen for the amount of time you set.
Known bug: You won't be able to type more commands after executing this command, we're working on a fix.

# Contact Us
For more detailed information on developing ViperVenom, please contact us at [our website](https://revise7.com/contacts). 
Revise7 does not take any responsibility in misuse, or for illegal purposes, we cannot control the tool if it goes to the wrong hand as it doesn't have a kill switch.

[Revise7]: https://revise7.com
[Download file]: https://github.com/Revise7/ViperVenom/archive/refs/heads/main.zip
