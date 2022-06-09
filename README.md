# Reboot-Chromecast
Windows PowerShell script that will reboot Chromecast devices on my local network.  
You will likely need to edit this script if you want to use it.  
  
This script uses
   - [gpsoauth](https://github.com/simon-weber/gpsoauth) by [simon-weber](https://github.com/simon-weber)
   - this [gist](https://gist.github.com/rithvikvibhu/952f83ea656c6782fbd0f1645059055d) by [rithvikvibhu](https://github.com/rithvikvibhu) to retrieve the **master_token** and the **access_token**.
   - [grpcurl](https://github.com/fullstorydev/grpcurl) by [fullstorydev](https://github.com/fullstorydev) to invoke **RPC** on **googlehomefoyer-pa.googleapis.com:443**  
# Usage
```ps1

NAME
    Reboot-Chromecast
    
SYNTAX
    Reboot-Chromecast [-DeviceName] <string>  [<CommonParameters>]
    
    
PARAMETERS
    -DeviceName <string>
        
        Required?                    true
        Position?                    0
        Accept pipeline input?       false
        Parameter set name           (All)
        Aliases                      None
        Dynamic?                     false
        
    <CommonParameters>
        This cmdlet supports the common parameters: Verbose, Debug,
        ErrorAction, ErrorVariable, WarningAction, WarningVariable,
        OutBuffer, PipelineVariable, and OutVariable. For more information, see 
        about_CommonParameters (https:/go.microsoft.com/fwlink/?LinkID=113216). 
    
    
INPUTS
    None
    
    
OUTPUTS
    System.Object
    
ALIASES
    None
    

REMARKS
    None

```

