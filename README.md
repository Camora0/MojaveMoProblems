![alt text](https://github.com/Camora0/MojaveMoProblems/blob/main/imagetemp.png)

# Mojave Mo' Problems - A Fallout: New Vegas Survival Overhaul

*"She just needs to realize the only difference between savage and sophisticated is the proper seasoning."* - *Mortimer*

## An Introduction

Welcome to Fallout: New Vegas - Mojave Mo' Problems. Here to make sure you know that the Mojave and it's inhabitants are not your friend. There might be a few souls willing to tolerate you, but the sands and the monsters that lie waiting only have one purpose: to kill you.

*Kill them back.*

The philosophy around MMP is to transform New Vegas into the definitive hardcore survival experience. Including overhauls touching on combat, resource management, self-preservation, and more, Mojave Mo' Problems is guaranteed to make you scared of The Wasteland again.

The following goes over all steps of the installation process as of MMP Public Release 0.7 (25/01/25)

#### Addendum

*for the remainder of this guide, we will assume you have prior knowledge of:*\
Windows file structure\
Mod Organizer 2\
Manual changes to files such as archives and text documents\
PC file-structuring vernacular\
Critical thinking and problem solving skills\

if you lack any of these, we highly recommend [This short, easy to read almanac.](https://www.dummies.com/book/technology/computers/pcs/pcs-for-dummies-13th-edition-281811/)

## Requirements & Prerequisites

### Requirements, Hardware

- CPU: Any Quad Core i5 (or AMD equivalent) made after 2018
- GPU: NVIDIA 3060 / AMD 5500 XT
- Drive: Around 60gb free space
  *Note: it is __absolutely imperative__ that MMP is installed on a Solid State Drive (SSD). Of course, you can install on an HDD, but we are not responsible for any issues related to installation and/or game performance and stability.*

### Requirements, Software

- a ***LEGAL*** Copy of Fallout: New Vegas GOTY (Base Game + all DLC) from Steam, GOG, or EGS.
- Fully updated, Public Release version of Win 10 (or higher), 64 bit
- The latest drivers for your GPU ([NVIDIA](https://www.nvidia.com/en-us/drivers/) / [AMD](https://www.amd.com/en/support/download/drivers.html))
- An archiving program such as [7z](https://7-zip.org/download.html) or [NanaZip](https://github.com/M2Team/NanaZip)\
  ***Latest VC++ Redistributables***
    1. [VC AIO](https://www.techpowerup.com/download/visual-c-redistributable-runtime-package-all-in-one/) (run `install_all.bat` as admin)
    2. [2015-2022 x64](https://aka.ms/vs/17/release/vc_redist.x64.exe)
    3. [2015-2022 x86](https://aka.ms/vs/17/release/vc_redist.x86.exe)
- [Notepad++](https://www.nexusmods.com/) (for text editing)
- A [Nexus mods](https://www.nexusmods.com/) account, preferrably premium for one click install and uncapped download speeds

### Prerequisites
***Disabling Base Address Randomization (BAR)***

Base Address Randomization (or BAR, for short) is a security feature built in to Windows, however, it can cause issues with 32 bit programs, which can and will cause stability issues in MMP and any modded New Vegas List. You can disable it by following these steps.
1. Open Windows Security.
2. Under "**App & Browser Control**", select "**Exploit protection settings**" under "**Exploit Protection**".
3. Set Mandatory ASLR (**Force randomization for images**) to "**Use default (off)**". This is a blanket setting, and will effect every program effected by BAR / Mandatory ASLR.
4. 
***Installing Fallout: New Vegas***
   
1. Either use Steam to create a library outside of `C:\Program Files(x86)`. If you only have one drive, you can use Steam Library Setup Tool to create a new library folder in the root of your C drive (`C:\SteamLibrary...\etc`)
2. Install Fallout: NV + ALL DLC to the path you just created.
3. Launch game to title screen; this will generate files necessary for modlist installation. (More specifically, it creates the falloutNV ini files)
4. Turn off Auto Updates for Fallout: New Vegas. This can be achieved by right-clicking on FoNV in Steam, Clicking Properties, going to the Updates tab, and setting "**Automatic Updates**" to "***Only update when I launch the game***". Since we will be using Mod Organizer 2 for launching MMP, this will prevent Steam from checking for updates.
5. Turn off Steam Overlay for FoNV. This can be achieved by going right-clicking on FoNV in Steam, clicking properties, and turning "***Enable the Steam Overlay while in-game***" off.

***Wabbajack Installation + MMP Pre-install***
1. On the same drive FoNV is installed on, create a folder in the root of the drive named `!Wabbajack Lists` (The exclimation point will keep the folder at the top of the default File Explorer sorting, to keep it easily visible.)
2. Inside the `!Wabbajack Lists` Folder, create three folders named `Wabbajack`, `Fallout NV MMP`, and `FONVMMP Downloads`.
3. Place Wabbajack.exe in the `Wabbajack` folder.
4. Launch Wabbajack.exe
5. Use the gear icon located on the top right of the Wabbajack window to log in to Nexus Mods.
6. In the Wabbajack gallery, enable "Show non-featured lists"
7. Search for Mojave Mo' Problems.
8. Click on the play button to prepare the download for Fallout: New Vegas: Mojave Mo' Problems.

## Installing Mojave Mo' Problems

Wabbajack will now prompt you to select filepaths for MMP. This should be self explanatory, but..
- The game path will be `(Drive)\Wabbajack Lists\Fallout NV MMP`.
- the mod path will be `(Drive)\Wabbajack Lists\FONVMMP Downloads`.

If you have Nexus Premium, you'll be able to sit back and watch Wabbajack do it's thing. However, if you are still a Basic member, Wabbajack will open up a small window for you to click "manually download" on every mod in the list. Unfortunately, there is no way to bypass this.

Wabbajack's bottom right section will change to a light blue, with a few buttons to press when the list finishes. Do not immediately launch MO2, as there are important post install steps to complete.

**Issues with Wabbajack and installing MMP**\
Of course, Wabbajack (and any Windows program) is not without issues. If, at any point during the installation process, *Wabbajack appears to be stuck / doing nothing*, simply close out Wabbajack and restart the install process. This time - and any time you need to restart the download - select "overwrite install" before starting the MMP installation.

**Wabbajack Fails to install, install halts**\
The cause of this can be a few different things. It's recommended to check logs to see where exactly the installation failed, see if you can restart it without issue, and go from there.
Nexus issues: you can attempt to either re-log (log out, log back in) to Nexus through Wabbajack, or, if a mod failed to download, manually downloading and placing in `...\FONVMMP Downloads`, then restarting the process.

A rare issue with Nexus can occur which happens when Wabbajack sends too many API calls (requests to access the download servers) too quickly. This will result in Nexus mods temporarily banning your IP address, for their own security reasons. You'll have to wait ~15-30 minutes before you can proceed with installation. If you try to download anything through Wabbajack before at least 10 minutes, the timer will reset. VPN usage has been known to trigger this issue as well.

Another common failure point will be Wabbajack telling you it *cannot process (x) file because it's open in another location.* From what we understand, the best solution to this is to do the following:
  1. Close Wabbajack
  2. Sign out of Windows (go back to login screen) or reboot your PC
  3. After logging in, go to `(Drive)\Wabbajack Lists\Wabbajack` and delete all files ***EXCEPT** Wabbajack.exe.
  4. You most likely will need to delete any temp files located in `...\Fallout NV MMP and ...\FONVMMP Downloads`.
  5. Restart MMP install as instructed previously.\

     **On the off chance that you get an installation error not pertaining to the above, you can join the [Camora's Wastelands Discord Server](https://discord.com/invite/HVmH8q4nfx), search if other users have had your issue, and if there are no solutions, you may make a Tech-Support thread for (hopefully) quick help.**

## Post install - Additional Setup and Tweaking

Congratulations, you're ready to get your teeth kicked in by an irradiated desert!\
Well, just about. The following instructions are the last steps before Mojave Mo' Problems is ready to be played.

The Tweaking section is an optional read, but could help with performance on low / medium grade hardware.

### Additional Setup

**Creating Exclusions**\
Due to how MO2's file virtualization works, sometimes Windows Defender will block MO2 from operating correctly.
1. Open "**Virus & Threat Protection**" in **Windows Security**
2. Click "**Manage Settings**" under "**Virus & Threat Protection Settings**"
3. Click "**Add or Remove Exclusions**"
4. Add a Folder exclusion and point it to `...\Fallout NV MMP`\
   *Note: If you use a third-party antivirus, ~~don't~~ you'll need to add exclusions through that program. Since it varies per program, we cannot provide blanket instructions.

*There are a few mods / tools that need to be manually placed alongside the game files, such as the 4gb patcher. These are not automatically placed / set up due to the nature of MO2 and what these tools do.*

**Root Mods**
1. in `...\Fallout NV MMP`, copy everything inside the `Manual install` folder into the `Game Root` folder.
2. Run "**FNVpatch.exe**". A command prompt window will open, saying `FalloutNV.exe patched!`.
3. Close the command window.

**BSA Decompressor**
1. In `...\Fallout NV MMP`, run "**FNV BSA Decompressor.exe**" from the "**BSA Decompressor**" folder
2. Click "**Decompress**".
3. Wait for program to finish, then close.\
   *Note: In the off chance the FoNV and Decompressed Archives paths aren't automatically filled, close and re-launch "**...Decompressor.exe**"

**Mod Organizer 2 Setup**
1. Launch "**ModOrganizer.exe**" from the root of your install folder (`...\Fallout NV MMP`)
2. Click yes on both / any pop-ups.

**Graphics Setup**
1. Inside of MO2, click the dropdown next to the Run button, select "**Fallout Launcher**", then hit "**Run**"
2. Select your monitor's native resolution and the **Ultra** preset. You can select **Medium** if you're running on weaker hardware, or prefer the frames.

### Tweaking

While Mojave Mo' Problems is, naturally, intended to be a stable experience, hardware is different and the Gamebryo engine is just absolutely awful. We can't guarantee you'll be locked to 60fps for 100% of your playthrough, so we recommend looking at the [<ins>Fallout: New Vegas Performance Guide<ins/>](https://performance.moddinglinked.com/falloutnv.html).

***After all the above steps have been completed, you may select "New Vegas" in MO2's dropdown menu, and click "Run" to launch the game. This is how you will be launching Mojave Mo' Problems. You may also create a shortcut (under the "Run" button) to bypass MO2.***

# Final Notes & Post Scriptum

### Final Notes

*"This is Mr. New Vegas, and I feel something magic in the air tonight, and I'm not just talking about the gamma radiation."*\
Congratulations, except for real this time around! **Fallout: New Vegas - Mojave Mo' Problems is ready to play!** Bring your Varmint Rifle and your canteen, you're gonna need em.

Any updates to the list are announced via [the Discord](https://discord.com/invite/HVmH8q4nfx)

*Post Scriptum*

Firstly, we'd like to extend our gratitude to you for not only getting through the installation process, but for also taking interest in Mojave Mo' Problems.\
Secondly, we'd like to thank the Wasteland Reborn Discord community. From months of list building and patch making, to weeks of bug testing and squashing, to days of finalization, to now, thank you for the dedication to Camora0, Wasteland Reborn, Mojave Mo' Problems, and any projects TBA<sub>;)</sub>!





Mojave Mo' Problems *Created & Maintained by* ***Camora0***
Install Instructions *Written and Maintained by* ***WiildFiire***
