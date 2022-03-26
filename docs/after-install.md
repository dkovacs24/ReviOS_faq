# After installing ReviOS

## The "Do not close the window, otherwise your system won't work properly" window not closing

Make sure you did not selected a character in the command prompt (a white rectangle). This pauses the running of the script. Press Esc or Enter, and the script will continue.

---

## I cannot log into my user

It is a known bug, and being investigated right now. In the next build of ReviOS, it will be fixed.

So far we know that this is happening, because of the connection of a Microsoft account to the local user. Right now the only fix is to reinstall your OS, and after you log into you Microsoft account set a PIN code too.

Other technique to evade the bug, is to log into your Microsoft account in the Microsoft Store. That way you will not be locked out and still can use your PC without a PIN code. Solution reported [here](https://discord.com/channels/619835916139364383/626772969611460619/944214984047616001).

---

## Internet/Sound/Bluetooth/other hardware... not working

Download the drivers from the manufacturer's website ans install them.

If you can not do that, because you don not have internet driver, somehow (on other computer or something like that) download [Snappy Driver Installer Origin](https://www.snappy-driver-installer.org/). 

Extract it, and start the software with `SDIO_auto.bat`. Then select the `Download Network Drivers Only` option. It will start the download of all the existing network drivers. 

If it finishes (you can monitor the process on the top side of the window), copy the whole folder to the other computer which doesn't have internet. Open on that computer the software, and install the missing network drivers. After restart you can scan the PC for more missing drivers, or better yet, go to the manufacturers website, and download the drivers from there.

---

## Internet icon bug

[Discord message link with instructions](https://discord.com/channels/619835916139364383/626772969611460619/800174514951684116)

[Zip file with the fix](https://cdn.discordapp.com/attachments/626772969611460619/800174514813665290/fix-network-icon.zip)

---

## Second monitor not working/blank or freshrate not desired

Install GPU drivers. [Help to tweak](https://www.revi.cc/revios/post-install#h.p_GR11WmefRS4F)

---

## Can I download other languages?

Yes, in the Settings. If that isn't working, follow [this guide](https://www.revi.cc/revios/workspace/lang).

---

## Can I use Windows Update?

Not recommended, because it will disable tweaks and reinstall bloatware.

In the latest versions it was removed, due to users updating without reading the FAQ or asking.

If you still want to update, you can manually install updates with the help of [this guide](https://www.revi.cc/revios/workspace/updating) or reactivate the Windows Update menu item in settings with this steps:

- Open `regedit`
- Go to `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows\CurrentVersion\Policies\Explorer`
- Remove `windowsupdate` from `SettingsPageVisibility`
- Restart

##### If you update, might as well just use stock Windows.

---

## Windows Update icon showed up on the taskbar and/or the "Update and shutdown/restart" option showed up

This is a bug in the `22.01` version, for now you can use [this fix](https://cdn.discordapp.com/attachments/626772969611460619/942019507730391050/Fix-Windows-Update-Taskbar.reg) for the taskbar icon. In the `22.02` version it is already fixed.

---

## How can I update to the newest version of ReviOS?

You need to reinstall. Do not forget to backup your data.

---

## Can I use the Reset this PC feature?

It is probably not working, and even if it would work, using is not recommended , because it probably will disable tweaks and reinstall bloatware.

We recommend to reinstall ReviOS. Do not forget to backup your data.

---

## GPU and Network monitoring not working in the Task Manager

Yes, they were stripped because leaking memory.

To reactivate GPU statistics:

- Open `cmd`
- Run this: `reg add "HKLM\SYSTEM\CurrentControlSet\Services\GraphicsPerfSvc" /v "Start" /t REG_DWORD /d "2" /f`
- Then run this: `sc start GraphicsPerfSvc`
- Restart

To reactivate Network statistics:

- Open `regedit`
- At `HKLM\System\CurrentControlSet\Services\Ndu` set `Start` to `2`
- Restart

---

## AMD driver installation is crashing

It is a Windows 11 bug. Try running the installer in silent mode, with the `/S` flag. 
[Here](https://discord.com/channels/619835916139364383/626772969611460619/932975660392128562) is help and a script to automate it.

If this method is not working, install [Chocolatey](https://chocolatey.org/) and then the `amd-ryzen-chipset` package.

---

## There are some visual bugs on the taskbar in ReviOS 11

These bugs came from Windows 11, hope they will be fixed in next Microsoft update releases.

In the mean time, try [StartAllBack](https://www.startallback.com/).

---

## Microsoft Store / Xbox app not working

Run `ctfmon` and `wsreset` commands.

If the login not working in the Xbox app, try these steps:

- Open Microsoft Store
- Click the 3 dots in the upper right corner of the window
- Click Downloads and updates
- Click Get updates
  
If you have updates, it should start installing them automatically.

If the updating is done, and Xbox login is still not working, go through these steps:

- Go to [https://store.rg-adguard.net/](https://store.rg-adguard.net/)
- Change the search options from `URL (link)` to `PackageFamilyName` and `RP` to `Slow`, and search for `Microsoft.GamingApp_8wekyb3d8bbwe`
- Download the following packages:
    - `Microsoft.VCLibs.140.00_14.0.30704.0_x64__8wekyb3d8bbwe.appx`
    - `Microsoft.VCLibs.140.00.UWPDesktop_14.0.30704.0_x64__8wekyb3d8bbwe.appx`
    - `Microsoft.UI.Xaml.2.7_7.2203.17001.0_x64__8wekyb3d8bbwe.appx`
    - `Microsoft.GamingApp_2203.1001.4.0_neutral_~_8wekyb3d8bbwe.msixbundle`
- Go where you downloaded the files, Shift + Right click and choose `Open Powershell window here`
- Run `Add-AppxPackage` with the downloaded files. E.g.: `Add-AppxPackage Microsoft.VCLibs.140.00_14.0.30704.0_x64__8wekyb3d8bbwe.appx`. **Make sure you install the packages the order listed above**
- Restart

---

## Where is Windows Defender? Can I use it?

In the Windows 11 and the latest 10 build you can reactivate it.

- Go to`"%userprofile%\Documents\Workspace\Windows Defender"`
- Run `Start.bat`
- Press `1`
- Restart

---

## How to change lock screen background?

- Open `regedit`
- Go to `HKEY_LOCAL_MACHINE\Software\Policies\Microsoft\Windows\Personalization`
- Set the `NoLockScreen` key's value to `0`
- Now you should be able to change it in Settings, if not, restart

---

## Faceit is not working

You are probably using a version of ReviOS which is not supported by Faceit anymore. Details [here](before-install.md#which-version-do-i-need-for-faceit).
