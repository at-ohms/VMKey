# VMKey
VMKey is an usefull tool write in Python to send keystrokes on VMware virtual machine throught vSphere API.

__Requirements__

- vSphere 6.5 or higher
- argparse
- pyvmomi

__Usage__

```
VMKey.py -h

positional arguments:

host                  vSphere IP or Hostname
username              vSphere Username
password              vSphere Password
vm                    VM Name

optional arguments:

-h, --help            show this help message and exit
--port PORT           alternative TCP port to communicate with vSphere API (default: 443)
--timeout TIMEOUT     timeout for VSphere API connection (default: 10s)
--debug               enable debug mode
--key                 key to passed to VM
--string STRING       string to passed to VM (Standard ASCII characters only)
```

__Examples__

```
VMKey.py host username password vm --string "Hello World !"
VMKey.py host username password vm --key CTRL_ALT_DEL
```

__Notes__

Available keys are listed in HIDCode variable.
