**Before using this FAQ, please do your own research, look around on the [ReviOS website](https://www.revi.cc/), there specifically in the [Changelogs](https://www.revi.cc/revios/download/changelog), the [Post-install](https://www.revi.cc/revios/post-install) guide and the [Workspace](https://www.revi.cc/revios/workspace).**

**Also use Google (or the search engine of your choice), especially with not ReviOS related questions.** 

**You _can_ find here things that are on the ReviOS website, because people are dumb, and going to ask it anyway.**


- [ReviOS frequently asked questions](#revios-frequently-asked-questions)
  - [What is the difference between the versions? What to choose?](#what-is-the-difference-between-the-versions-what-to-choose)
    - [ReviOS 10 22.01](#revios-10-2201)
    - [Revios 11 21.12](#revios-11-2112)
    - [ReviOS 1709](#revios-1709)
  - [Where are the older versions?](#where-are-the-older-versions)
  - [How to install ReviOS?](#how-to-install-revios)
  - [Downloads are not working / Google Drive: "Sorry, you can't view or download this file at this time." / MEGA quota exceeded](#downloads-are-not-working--google-drive-sorry-you-cant-view-or-download-this-file-at-this-time--mega-quota-exceeded)
  - [Driver missing when installing ReviOS](#driver-missing-when-installing-revios)
  - [Internet/Sound/Bluetooth/Touchpad/other hardware... not working](#internetsoundbluetoothtouchpadother-hardware-not-working)
  - [Internet icon bug](#internet-icon-bug)
  - [Second monitor not working/blank or freshrate not desired](#second-monitor-not-workingblank-or-freshrate-not-desired)
  - [Can I download other languages?](#can-i-download-other-languages)
  - [Can I use Windows Update?](#can-i-use-windows-update)
  - [How can I update to the newest version of ReviOS?](#how-can-i-update-to-the-newest-version-of-revios)
    - [Can I update to the newest version of ReviOS without reinstall?](#can-i-update-to-the-newest-version-of-revios-without-reinstall)
  - [Can I use the Reset this PC feature?](#can-i-use-the-reset-this-pc-feature)
  - [Which version can I use Faceit? / Faceit is not working](#which-version-can-i-use-faceit--faceit-is-not-working)
    - [You said Faceit only works with 22.01, and I am on 22.01, and it is still not working](#you-said-faceit-only-works-with-2201-and-i-am-on-2201-and-it-is-still-not-working)
  - [GPU and Network monitoring not working in the Task Manager](#gpu-and-network-monitoring-not-working-in-the-task-manager)
  - [AMD driver installation is crashing](#amd-driver-installation-is-crashing)
  - [There are some visual bugs on the taskbar in ReviOS 11](#there-are-some-visual-bugs-on-the-taskbar-in-revios-11)
  - [Microsoft Store / XBox app not working](#microsoft-store--xbox-app-not-working)
  - [Where is Windows Defender? Can I use it?](#where-is-windows-defender-can-i-use-it)
  - [How to change lock screen background?](#how-to-change-lock-screen-background)


# ReviOS frequently asked questions


## What is the difference between the versions? What to choose?

As of this moment (2022-02-07), there are 3 versions of ReviOS that are supported: `10 22.01`, `11 21.12` and `1709`. No other versions are supported.

### ReviOS 10 22.01

[Changlelog](https://www.revi.cc/revios/download/changelog#h.odb11cheqkzw)

[Download](https://www.revi.cc/revios/download#h.ak1prpz0wx5m)

[Alternative download links](https://www.revi.cc/revios/download#h.cwre5ugg2fhb)

### Revios 11 21.12

[Changelog](https://www.revi.cc/revios/download/changelog#h.kzabahjk03q5)

[Download](https://www.revi.cc/revios/download#h.ywpa5av3hdf3)

Alternative download links on the official Discord server's download channel.

### ReviOS 1709

[Changelog](https://www.revi.cc/revios/download/changelog#h.rfvq0n3k2uk7)

[Download](https://www.revi.cc/revios/download/alternative-downloads#h.ski2fzvfamkj)

Alternative download links on the official Discord server's download channel.


If you are looking for a version:
- more gaming, less latency and less bloatware oriented, choose `1709`
- more compatible with latest programs, choose `22.01` or `21.12`

**_Faceit only works on 22.01._** Details below.

---

## Where are the older versions?

[Here](https://www.revi.cc/revios/download/alternative-downloads)

---

## How to install ReviOS?

[Tutorial](https://youtu.be/w4Wn25d02iY)

---

## Downloads are not working / Google Drive: "Sorry, you can't view or download this file at this time." / MEGA quota exceeded

For the latest version the alternative downloads are on the [website](https://www.revi.cc/revios/download#h.cwre5ugg2fhb).

For the others, ther are mirror downloads on the official Discord server, invite link: https://discord.gg/962y4pU

---

## Driver missing when installing ReviOS

Try plugging the flash drive into another USB port. If sill not working, try using [Ventoy](https://www.ventoy.net/) instead of Rufus.

---

## Internet/Sound/Bluetooth/Touchpad/other hardware... not working

Download the drivers from the manufacturer's website ans install them.

If you can not do that, because you don not have internet driver, somehow (on other computer or something like that) download [Snappy Driver Installer Origin](https://www.snappy-driver-installer.org/). 
Extract it, and start the software with `SDIO_auto.bat`. Then select the `Download Network Drivers Only` option. It will start the download of all the existing network drivers. 
If it finishes (you can monitor the process on the top side of the window), copy the whole folder to the other computer which doesn't have internet. Open on that computer the software, and install the missing network drivers. After restart you can scan the PC for more missing drivers, or better yet, go to the manufacturers website, and download the drivers from there.

---

## Internet icon bug

Fix: Discord message link with instructions: https://discord.com/channels/619835916139364383/626772969611460619/800174514951684116. 
Direct link to the zip file: https://cdn.discordapp.com/attachments/626772969611460619/800174514813665290/fix-network-icon.zip

---

## Second monitor not working/blank or freshrate not desired

Install GPU drivers. Help to tweak: https://www.revi.cc/revios/post-install#h.p_GR11WmefRS4F

---

## Can I download other languages?

Yes, in the Settings. If that isn't working, follow this: https://www.revi.cc/revios/workspace/lang

---

## Can I use Windows Update?

Not recommended, because it will disable tweaks and reinstall bloatware.

But if you still want to update, you can install updates with the help of this guide: https://www.revi.cc/revios/workspace/updating

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
- run this: `reg add "HKLM\SYSTEM\CurrentControlSet\Services\GraphicsPerfSvc" /v "Start" /t REG_DWORD /d "2" /f
- sc start GraphicsPerfSvc`
- restart

---

## AMD driver installation is crashing

It is a Windows 11 bug. Try running the installer in silent mode, with the `/S` flag. 
Here's help and a script to automate it: https://discord.com/channels/619835916139364383/626772969611460619/932975660392128562

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
