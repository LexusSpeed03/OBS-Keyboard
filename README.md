# OBS-Keyboard
OBS Keyboard is used to remap a 10 key pad to control aspects of OBS or other software. This will not affect your original keyboard only the secondary.

# Purchase Keyboard / 10 Keypad
You can purchase a wireless 10 Keypad or another keyboard to use. It is highly recommended you purchase a different model than what you own now to avoid conflicts.

# Installing Keyboard Interception
1. Once you have extracted OBS-Keyboard.zip you need to first open cmd.exe as Administrator.  
2. Type install-inception.exe /install  
3. Please reboot your PC once install has finished.  

# Capture Hardware ID of 10 Keypad
1. Open cmd.exe as Administrator  
2. Type remapper.exe  
3. You will then need to hit enter on the 10 Keypad to get the Hardware ID. You will see it listed please copy it as you will need it later. Example of one is HID\VID_1A2C&PID_4224&REV_0110&MI_00  

# Setup Config File
1. You will notice there is a text file name OBS-Keyboard.txt use this as reference when creating yours or modify this one.  
2. The first top line needs to be your Hardware ID.  
3. Leave a blank space below it.  
4. Begin by mapping keys to what you want in OBS. For example I have each numpad doing CTRL+ALT+Num1 etc.  
5. You can create any key combination that is within windows limitations.  

# Config Notes
Windows Keys:
Left Shift S-  
Right Shift rS-  
Left/Alt A-  
Right/Alt rA-  
Left Control C-  
Right Control rC-  
Left Windows W-  
Right Windows rW-  

# Examples
Num1 C-A-1 This would remap Numpad 1 to CTRL-ALT-1 and ETC below.  
Num2 C-A-2   
Num3 C-A-3  
Num4 C-A-4  
Num5 C-A-5  
Num6 C-A-6  
Num7 C-A-7  
Num8 C-A-8  
Num9 C-A-9  

# Configure to Autostart  
1. Open cmd.exe as Administrator  
2. Type nssm.exe install  
3. Please fill in the following information  

Application  
Path: C:\Directory of Extract Zip\remapper.exe  
Startup Directory: Automatically Fills  
Arguments: C:\Directory of Extracted Zip\OBS-Keyboard.txt  
Service Name: OBS-Keyboard  

4. Once you have performed this click Install Service.  
5. You will now have a remapped 10 Keypad when this service is running. You can verify this by doing WindowsKey+R on keyboard and typing services.msc  
6. In this list you will see OBS-Keyboard. Make sure you right click and hit start. Please make sure to right click the service and go to properties and make it Automatically start.  


# OBS Setup
1. You would set Hotkeys in OBS to your corresponding hotkeys for example if you want Num1 to be Live scene you would do CTRL+ALT+1
2. If you press Num1 on your normal keyboard it wouldn't affect anything.


# Information
I do not take credit for all of this just the configuration and using information gathered from the internet. The full article for this can be found below here  

http://www.2112design.com/blog/multi-keyboard-remapper/

This project is based on http://www.oblita.com/interception.html with many thanks to Francisco Lopes for the amazing job he did figuring out all he windows internals. His package does all the magic shit, I just put a control application and config format together.
