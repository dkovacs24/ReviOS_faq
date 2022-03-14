# After installing ReviOS

## The "Do not close the window, otherwise your system won't work properly" window not closing

Make sure you did not selected a character in the command prompt (a white rectangle). This pauses the running of the script. Press Esc or Enter, and the script will continue.

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

Yes, in the Settings. If that isn't working, [follow this guide](https://www.revi.cc/revios/workspace/lang).

---

## Can I use Windows Update?

Not recommended, because it will disable tweaks and reinstall bloatware.

In the latest versions it was removed, due to users updating without reading the FAQ or asking.

If you still want to update, you can manually install updates with the help of [this guide](https://www.revi.cc/revios/workspace/updating) or reactivate the Windows Update menu item in settings with this steps:

- open `regedit`
- go to `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows\CurrentVersion\Policies\Explorer`
- remove `windowsupdate` from `SettingsPageVisibility`
- restart

##### If you update, might as well just use stock Windows.

---

## Windows Update icon showed up on the taskbar and/or the "Update and shutdown/restart" option showed up

This is a bug in the `22.01` version, for now you can use [this fix](https://cdn.discordapp.com/attachments/626772969611460619/942019507730391050/Fix-Windows-Update-Taskbar.reg) for the taskbar icon. In the `22.02` version it is already fixed.

---

## How can I update to the newest version of ReviOS?

You need to reinstall. Do not forget to backup your data.

---

## Can I use the Reset this PC feature?

It probably does not work, and even if it does, it is not recommended, because it will disable tweaks and reinstall bloatware.

We recommend to reinstall ReviOS. Do not forget to backup your data.

---

## GPU and Network monitoring not working in the Task Manager

Yes, they were stripped because leaking memory.

To reactivate GPU statistics:

- open `cmd`
- run this: `reg add "HKLM\SYSTEM\CurrentControlSet\Services\GraphicsPerfSvc" /v "Start" /t REG_DWORD /d "2" /f`
- then run this: `sc start GraphicsPerfSvc`
- restart

To reactivate Network statistics:

- open `regedit`
- at `HKLM\System\CurrentControlSet\Services\Ndu` set `Start` to `2`
- restart

---

## AMD driver installation is crashing

It is a Windows 11 bug. Try running the installer in silent mode, with the `/S` flag. 
[Here is help and a script to automate it](https://discord.com/channels/619835916139364383/626772969611460619/932975660392128562).

If this method is not working, install [Chocolatey](https://chocolatey.org/) and then the `amd-ryzen-chipset` package.

---

## There are some visual bugs on the taskbar in ReviOS 11

These bugs came from Windows 11, hope they will be fixed in next Microsoft update releases.

In the mean time, try [StartAllBack](https://www.startallback.com/).

---

## Microsoft Store / XBox app not working

Run `ctfmon` and `wsreset` commands.

---

## Where is Windows Defender? Can I use it?

In the Windows 11 and the latest 10 build you can reactivate it.

- go to`"%userprofile%\Documents\Workspace\Windows Defender"`
- run `Start.bat`
- press `1`
- restart

---

## How to change lock screen background?

- open `regedit`
- go to `HKEY_LOCAL_MACHINE\Software\Policies\Microsoft\Windows\Personalization`
- set the `NoLockScreen` key's value to `0`
- now you should be able to change it in Settings, if not, restart

---

## Faceit is not working

You are probably using a version of ReviOS which is not supported by Faceit anymore. [Details here](before-install.md#which-version-do-i-need-for-faceit).