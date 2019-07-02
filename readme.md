# ***Super-NFZ Eraser***

*Tool to erase GeoZone entries from the nfz database on Mavic Pro/MPP/MP Artic White running a stock firmware version v01.04.0300 or a DJI_Super-Patcher https://github.com/brett8883/DJI_Super-Patcher patched firmware* 

By Jezzab and Brett8883

Note: THERE MAY BE OTHER FIRMWARE VERSIONS OR OTHER AIRCRAFT THIS WILL WORK FOR BUT THESE ARE THE ONLY ONES I HAVE PERSONALLY TRIED IT ON. WILL UPDATE AS CONFIRMATION COMES IN OF COMPATIBILITY WITH OTHER FIRMWARE AND AIRCRAFT

Super-NFZ Eraser will replace the NFZ database that lives on the Mavic with an empty database effectively erasing all GeoZones inside it. 

Included is a special moddified version of DULMdore v3.03 which I have renammed DUMLdore_for_NFZ_Eraser_only, it CANNOT be used to upgrade and downgrade firmware. REPEAT. It CANNOT be used to upgrade and downgrade firmware. IT has been renamed to reflect this. IF you need a standard copy of DUMLdore get it from https://github.com/jezzab/DUMLdore

**BACKGROUND:** On firmware version 01.04.0300 there is an anti-tamper mechanism that prevents flight of a Mavic if the nfz.db has been removed. Instead, by replacing the nfz.db with an empty one we satisfy the requirement to have a nfz.db even though there are no entries and no geozones in the database which has the same effect as removing it if we could. 

**Step-by-step**
1. Download full repository and keep all files in original folders
2. Turn on Mavic and connect to PC 
3. Double click “DUML_for_nfz_removal_only.exe”
4. [alt] [click] on “load firmware” and choose “Clear_nfzdb_dji_system.bin”
5. Click “flash firmware” 
6. Allow it to do its thing which can take several minutes. 
7. Once flashing is complete restart Mavic and done!

**VERIFICATION**

To verify NFZ.db has been erased you can reconnect your bird once it restarts and then open DULMdore 3.2. Close DULMdore once the "enable ADB" process is done  

Then double click the pull_nfz_db.bat to make a copy of the nfz.db on the drone and save it to the nfz_db folder 

This will copy the nfz.db from the Mavic into the folder you made.

You can then browse the db to ensure there are no entries in it with a DB browser like https://sqlitebrowser.org/dl/#windows

**Acknowlegments**

 First of all I did not create the ingenious mod behind this project it was created by jezzab https://github.com/jezzab and all I did was bring an under appreciated mod from the celler, slapped a nice dress on it, made into a single cohesive package, and created the "verify" steps. Other than that it was all Jezzab https://github.com/jezzab 

Includes a modified version of the DUMLdore https://github.com/jezzab/DUMLdore by @jezzab
Includes a non-modified version of the DUMLdore project https://github.com/jezzab/DUMLdore by @jezzab

Thanks to https://sqlitebrowser.org/dl/#windows for making a lightweight DB browser I was able to include in this program. 

Thanks to the OGs who, by making their work open, have enabled me to liberate myself from the bondage imposed by DJI and inspired me to help others to liberate themselves. Their past work has gone into this project and they continually have helped me get better at making projects. 

Thanks and shout out to digdat0 who I barrowed the GUI design from. 

