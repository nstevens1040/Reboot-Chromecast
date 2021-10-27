# Reboot-ChromeCast
Windows PowerShell script that will reboot Chromecast devices on my local network.  
  
This script uses
   - this [gist](https://gist.github.com/rithvikvibhu/952f83ea656c6782fbd0f1645059055d) by [rithvikvibhu](https://github.com/rithvikvibhu) to retrieve the **master_token** and the **access_token**.
   - [grpcurl](https://github.com/fullstorydev/grpcurl) by [fullstorydev](https://github.com/fullstorydev) to retrieve the the response from invoking **RPC** on **googlehomefoyer-pa.googleapis.com:443**  

```ps1
NAME
    Reboot-Chromecast
    
SYNTAX
    Reboot-Chromecast [-DeviceName] {Nick's TV | Google TV}  [<CommonParameters>]
    
    
PARAMETERS
    -DeviceName <string>
        
        Required?                    true
        Position?                    0
        Accept pipeline input?       false
        Parameter set name           (All)
        Aliases                      None
        Dynamic?                     false
```  

