# GUIDE-ONI-MOD-Sample-asset-create-or-update

## Requirements:
  * [uTinyRipper](https://github.com/mafaca/UtinyRipper)
  * [kanimal SE (KSE)](https://github.com/skairunner/kanimal-SE)
  * [Spriter Pro](https://brashmonkey.com/download-spriter-pro/)
  * Working OS (Windows 10)
  
### Guide

#### Using uTinyRipper
1. Create a folder "ONI Assets" (optional or whatever you want) 
1. Extract [uTinyRipper](https://github.com/mafaca/UtinyRipper) then run uTinyRipper.exe
1. Open Steam and locate ONI
   1. Right Click and Click Local Files Tab
   1. Click Browse Local Files
   1. Open __*OxygenNotIncluded_Data*__ folder
   1. you can do this without steam, in my case the folder is located: __*C:\Program Files (x86)\Steam\steamapps\common\OxygenNotIncluded\OxygenNotIncluded_Data*__
   1. Select all __*.asset*__ filename you can do this by __*Holding shift + click*__
   1. It will look like this and Press Export
   
   ![tut1](/11.PNG)
 
### Using Kanimal SE
1. Extract [kanimal SE (KSE)](https://github.com/skairunner/kanimal-SE) this will generate a folder named __*Windows.NET.dependent*__  you can rename the folder for easy use.
1. For this guide you only look to __*TextAsset*__ and __*Texture2d*__ in your extracted asset folder
1. We'll make a __*Red Gas pump*__
  1. Open __*TextAsset*__ folder then find __*pumpgas_anim.bytes*__ and __*pumpgas_build.bytes*__ (to search it easily you can use search bar but in my case i just click some file and rapidly press __p+u+m+p__ then it will highlight the 1st file with contains __*pump*__
  1. it is safe to copy it to a new folder
  1. Open __*Texture2d*__ and find __*pumpgas_0.png*__ then copy it to your folder with your __*bytes*__ file
  1. Press windows key and search for __*Windows PowerShell*__ run as administrator (optional but better)
  1. Locate your kanimal folder in my case __*C:\Users\<your-user>\Desktop\<your-kanimal-folder>*__
  1. if you are stuck you check [kanimal guide](https://github.com/skairunner/kanimal-SE#kanim--scml)
  1. go you your __*pump*__ folder and get the dir location by pressing the dir tab and it will show you the full dir and copy it
  1. in your Windows PowerShell type in: 
  ```
  kanimal-cli.exe scml C:\Users\__<your-user>__\Desktop\__<your-pump>__\pumpgas_0.png C:\Users\__<your-user>__\Desktop\__<your-pump>__\pumpgas_anim.bytes C:\Users\__<your-user>__\Desktop\__<your-pump>__\pumpgas_build.bytes
  ```
  
  
  
  
  
  
  
  
  
  
  
