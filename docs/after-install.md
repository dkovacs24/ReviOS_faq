# After installing ReviOS

## The "Do not close the window, otherwise your system won't work properly" not closing

Make sure you did not selected a charcter in the command prompt. (White rectangle) This pauses the running of the script. Press Esc or Enter, and the script will continue.

---

## Internet/Sound/Bluetooth/other hardware... not working

Download the drivers from the manufacturer's website ans install them.

If you can not do that, because you don not have internet driver, somehow (on other computer or something like that) download [Snappy Driver Installer Origin](https://www.snappy-driver-installer.org/). 

Extract it, and start the software with `SDIO_auto.bat`. Then select the `Download Network Drivers Only` option. It will start the download of all the existing network drivers. 

If it finishes (you can monitor the process on the top side of the window), copy the whole folder to the other computer which doesn't have internet. Open on that computer the software, and install the missing network drivers. After restart you can scan the PC for more missing drivers, or better yet, go to the manufacturers website, and download the drivers from there.

---

## Internet icon bug

Fix: [Discord message link with instructions](https://discord.com/channels/619835916139364383/626772969611460619/800174514951684116)

[Zip file](https://cdn.discordapp.com/attachments/626772969611460619/800174514813665290/fix-network-icon.zip)

---

## Second monitor not working/blank or freshrate not desired

Install GPU drivers. [Help to tweak](https://www.revi.cc/revios/post-install#h.p_GR11WmefRS4F)

---

## Can I download other languages?

Yes, in the Settings. If that isn't working, [follow this guide](https://www.revi.cc/revios/workspace/lang).

---

## Can I use Windows Update?

Not recommended, because it will disable tweaks and reinstall bloatware.

But if you still want to update, you can install updates with the help of [this guide](https://www.revi.cc/revios/workspace/updating).

---

## Windows Update icon showed up on the taskbar and/or the "Update and shutdown/restart" option showed up

This is a bug in the `22.01` version, in the next builds it will be fixed. Until that, the taskbar icon can be removed with [this fix](https://cdn.discordapp.com/attachments/626772969611460619/942019507730391050/Fix-Windows-Update-Taskbar.reg).

---

## How can I update to the newest version of ReviOS?

You need to reinstall. Do not forget to backup your data.

### Can I update to the newest version of ReviOS without reinstall?

No. Do not forget to backup your data.

---
## Can I use the Reset this PC feature?

It probably does not work, and even if it does, it is not recommended, because it will disable tweaks and reinstall bloatware.

We recommend to reinstall ReviOS. Do not forget to backup your data.

---

## Which version can I use Faceit? / Faceit is not working

As of this moment (2022-02-07), Faceit only works on the `10 22.01` version.

### You said Faceit only works with 22.01, and I am on 22.01, and it is still not working

Probably since the release of that version another update was released by Microsoft, which is required by Faceit. New build of ReviOS will be released soon.

---

## GPU and Network monitoring not working in the Task Manager

Yes, they were stripped because leaking memory.

To reactivate GPU statistics:

- open `cmd`
- run this: `reg add "HKLM\SYSTEM\CurrentControlSet\Services\GraphicsPerfSvc" /v "Start" /t REG_DWORD /d "2" /f`
- `sc start GraphicsPerfSvc`
- restart

---

## AMD driver installation is crashing

It is a Windows 11 bug. Try running the installer in silent mode, with the `/S` flag. 
[Here is help and a script to automate it](https://discord.com/channels/619835916139364383/626772969611460619/932975660392128562)

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

