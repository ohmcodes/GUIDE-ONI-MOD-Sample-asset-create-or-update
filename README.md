# GUIDE ONI MOD Sample asset create or update

#### Oxygen Not Included MOD change asset or create new building or animation basic guide

## Requirements:
  * [uTinyRipper](https://github.com/mafaca/UtinyRipper)
  * [kanimal SE (KSE)](https://github.com/skairunner/kanimal-SE)
  * [Spriter Pro](https://brashmonkey.com/download-spriter-pro/)
  * Working OS (Windows 10)

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
  1. Open __*TextAsset*__ folder then find __*pumpgas_anim.bytes*__ and __*pumpgas_build.bytes*__ (to search it easily you can use search bar but in my case i just click some file and rapidly pressing __p+u+m+p__ then it will highlight the 1st file with contains __*pump*__
  1. it is safe to copy it to a new folder
  1. Open __*Texture2d*__ and find __*pumpgas_0.png*__ then copy it to your folder with your __*bytes*__ file
  1. Press windows key and search for __*Windows PowerShell*__ run as administrator (optional but better)
  1. Locate your kanimal folder in my case __*C:\Users\<your-user>\Desktop\<your-kanimal-folder>*__
  1. if you are stuck, you can check [kanimal guide](https://github.com/skairunner/kanimal-SE#kanim--scml)
  1. go you your __*pump*__ folder and get the dir location by pressing the dir tab and it will show you the full dir and copy it
  1. in your Windows PowerShell type in: NOTE: change __*<your-user>*__ and __*<your-pump>*__
  ```
  .\kanimal-cli.exe scml C:\Users\<your-user>\Desktop\<your-pump>\pumpgas_0.png C:\Users\<your-user>\Desktop\<your-pump>\pumpgas_anim.bytes C:\Users\<your-user>\Desktop\<your-pump>\pumpgas_build.bytes -o C:\Users\<your-user>\Desktop\<your-pump>\output\
  ```
  1. if you don't set __*-o*__ or output dir it will auto generate in your kanimal folder where kanimal-cli.exe located
  1. after you hit enter if will look like this:
  
  ![tut2](/223.PNG)
  
  1. It will fragmented to multiple files or __*.png*__ and 1 __*.scml*__
  
  ![tut3](/33.PNG)
  
  1. if you have Spriter you can open the pumpGas.scml and if you want to change some animation
  1. if you just want to change the skin you can skip renaming all files inside it but its better to rename everything to avoid conflict
  1. In my case i just rename 3 files *(Note: this will be done after scml->kanim)* 
 
    __*pumpGas_red.png*__

    __*pumpGas_red_anim.bytes*__

    __*pumpGas_red_build_bytes*__
   
   
1. __*scml -> kanim*__ in your __*Windows PowerShell*__ type in:
 ```
  .\kanila-cli.exe kanim pumpGas.scml -o C:\Users\<your-user>\Desktop\<your-pump>\editoutput\
 ```
### Visual Studio
1. Make a folder to your solution __*anim/assets/<your-pump-folder>/*__ Note: make sure you made the directory inside VS not in Windows
1. Open that directory then drag the 3 files 
 
   __*pumpGas_red.png*__
   
   __*pumpGas_red_anim.bytes*__
   
   __*pumpGas_red_build_bytes*__
   
   
1. if your anim string you can call it __*pumpGas_red_kanim*__
1. Enjoy!
  
  
  
Credit to my master:
[Ronivan](https://github.com/Ronivan)
  
  
  
  
  
  
