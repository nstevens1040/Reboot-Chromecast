# Reboot-Chromecast
Windows PowerShell script that will reboot Chromecast devices on my local network.  
You will likely need to edit this script if you want to use it.  
  
This script uses
   - [gpsoauth](https://github.com/simon-weber/gpsoauth) by [simon-weber](https://github.com/simon-weber)
   - this [gist](https://gist.github.com/rithvikvibhu/952f83ea656c6782fbd0f1645059055d) by [rithvikvibhu](https://github.com/rithvikvibhu) to retrieve the **master_token** and the **access_token**.
   - [grpcurl](https://github.com/fullstorydev/grpcurl) by [fullstorydev](https://github.com/fullstorydev) to invoke **RPC** on **googlehomefoyer-pa.googleapis.com:443**  
  
The script assumes that you have
   - set an environment variable named **HOMEGRAPH_SERVICE_ACCOUNT** to your Google service account's **email address** ```<service-account-name>@<project-id>.iam.gserviceaccount.com```
   - hard-coded your Google master token by setting the environment variable **GOOGLE_MASTER_TOKEN** to the value of your master token
   - In this case, I have set an environment variable entitled **CHROMECASTMAC** to my Chromecast MAC address. This isn't necessary, but it was convenient for me during testing as a way to quickly retrieve that value.

*You will need to remove the parameter DeviceName's default value unless you also happen to have a Chromecast named Nick's Bedroom TV*

## Quick Start
Once you have set your environment variables, you can make **Reboot-Chromecast** available in a **Windows PowerShell** session by running the commands below.
```ps1
Set-ExecutionPolicy Bypass -Scope Process -Force;
[System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072;
iex (irm https://raw.githubusercontent.com/nstevens1040/Reboot-Chromecast/main/Reboot-Chromecast.ps1)
```  
  
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

