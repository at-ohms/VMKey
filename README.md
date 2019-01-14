# VMKey
VMKey is an usefull tool write in Python to send keystrokes on VMware virtual machine throught vSphere API.

__Requirements__

- vSphere 6.5 or higher
- argparse
- pyvmomi

__Usage__

VMKey.py -h

positional arguments:
  host                  vSphere IP or Hostname
  username              vSphere Username
  password              vSphere Password
  vm                    VM Name

optional arguments:
  -h, --help            show this help message and exit
  --port PORT           alternative TCP port to communicate with vSphere API
                        (default: 443)
  --timeout TIMEOUT     timeout for VSphere API connection (default: 10s)
  --debug               enable debug mode
  --key                 key to passed to VM
  
 Available :
    {KEY_A,KEY_B,KEY_C,KEY_D,KEY_E,KEY_F,KEY_G,KEY_H,KEY_I,KEY_J,KEY_K,KEY_L,KEY_M,KEY_N,KEY_O,KEY_P,KEY_Q,KEY_R,KEY_S,KEY_T,KEY_U,KEY_V,KEY_W,KEY_X,KEY_Y,KEY_Z,KEY_1,KEY_2,KEY_3,KEY_4,KEY_5,KEY_6,KEY_7,KEY_8,KEY_9,KEY_0,KEY_ENTER,KEY_ESC,KEY_BACKSPACE,KEY_TAB,KEY_SPACE,KEY_MINUS,KEY_EQUAL,KEY_LEFTBRACE,KEY_RIGHTBRACE,KEY_BACKSLASH,KEY_SEMICOLON,KEY_APOSTROPHE,KEY_GRAVE,KEY_COMMA,KEY_DOT,KEY_SLASH,KEY_CAPSLOCK,KEY_F1,KEY_F2,KEY_F3,KEY_F4,KEY_F5,KEY_F6,KEY_F7,KEY_F8,KEY_F9,KEY_F10,KEY_F11,KEY_F12,KEY_DELETE,CTRL_ALT_DEL,CTRL_C}
  
  --string STRING       string to passed to VM (Standard ASCII characters only)

__Examples__

VMKey.py host username password vm --string "Hello World !"
VMKey.py host username password vm --key CTRL_ALT_DEL
