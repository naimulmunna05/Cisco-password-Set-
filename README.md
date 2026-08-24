

# Cisco Router Password Setup & Recovery

| Category / Phase | Sub-Category | Commands / Actions |
| :--- | :--- | :--- |
| 1. Password Setup** | Line Console | `Router(config)#line console 0`<br>`Router(config-line)#password 123`<br>`Router(config-line)#login` |
| | Enable Password | `Router(config)#enable password 123` |
| | Telnet Password | `Router(config)#line vty 0 4`<br>`Router(config-line)#password 123`<br>`Router(config-line)#login`|
| 2. Password Break | Step 1 & 2 | • Set password in any mode (like console)<br>• Physically power off, then power on and press `Ctrl + C`
|
| | Step 3 | • In ROMMON mode, set: `confreg 0x2142`<br>• Then power off and on again|
| | Step 4 | • In default mode, configure: `config-register 0x2101`<br>• Run: `exit`
<br>• Run: `wr`<br>• Run: `reload`
|
