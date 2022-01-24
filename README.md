**Before using this FAQ, please do your own research, look around on the [ReviOS website](https://www.revi.cc/), there specifically in the [Changelogs](https://www.revi.cc/revios/download/changelog), the [Post-install](https://www.revi.cc/revios/post-install) guide and the [Workspace](https://www.revi.cc/revios/workspace).**

**Also use Google (or the search engine of your choice), especially with not ReviOS related questions.** 

**You _can_ find here things that are on the ReviOS website, because people are dumb, and going to ask it anyway.**


- [ReviOS frequently asked questions](#revios-frequently-asked-questions)
  - [What is the difference between the versions? What to choose?](#what-is-the-difference-between-the-versions-what-to-choose)
  - [Where is the Windows 10 version? / Where are the older versions?](#where-is-the-windows-10-version--where-are-the-older-versions)
  - [How to install ReviOS?](#how-to-install-revios)
  - [Downloads are not working / Google Drive said: "Sorry, you can't view or download this file at this time." / MEGA quota exceeded](#downloads-are-not-working--google-drive-said-sorry-you-cant-view-or-download-this-file-at-this-time--mega-quota-exceeded)
  - [Internet icon bug](#internet-icon-bug)
  - [Internet/Sound/Bluetooth/Touchpad/other hardware... not working](#internetsoundbluetoothtouchpadother-hardware-not-working)
  - [Second monitor not working/blank](#second-monitor-not-workingblank)
  - [Can I download other languages?](#can-i-download-other-languages)
  - [Can I use Windows Update?](#can-i-use-windows-update)
  - [Which version can I use Faceit? / Faceit is not working](#which-version-can-i-use-faceit--faceit-is-not-working)
  - [You said Faceit only works with 21H2/21.12, and I am on 21H2/21.12, and it is still not working](#you-said-faceit-only-works-with-21h22112-and-i-am-on-21h22112-and-it-is-still-not-working)
  - [GPU and Network monitoring not working in the Task Manager](#gpu-and-network-monitoring-not-working-in-the-task-manager)
  - [AMD driver installation is crashing](#amd-driver-installation-is-crashing)
  - [There are some visual bugs on the taskbar in ReviOS 11](#there-are-some-visual-bugs-on-the-taskbar-in-revios-11)
  - [Microsoft Store / XBox app not working](#microsoft-store--xbox-app-not-working)
  - [Where is Windows Defender? Can I use it?](#where-is-windows-defender-can-i-use-it)
  - [Driver missing when installing ReviOS](#driver-missing-when-installing-revios)


# ReviOS frequently asked questions


## What is the difference between the versions? What to choose?

As of this moment (2022-01-21), there are 3 versions of ReviOS that are supported: `1709`, `21H2` and `21.12`. No other versions are supported.

If you are looking for a version:
- more gaming, less latency and less bloatware oriented, choose `1709`
- more compatible with latest programs, choose `21H2` or `21.12`

**_Faceit only works on 21H2 and 21.12._** Details below.

---

## Where is the Windows 10 version? / Where are the older versions?

[Alternative downloads](https://www.revi.cc/revios/download/alternative-downloads)

---

## How to install ReviOS?

[Tutorial](https://youtu.be/w4Wn25d02iY)

---

## Downloads are not working / Google Drive said: "Sorry, you can't view or download this file at this time." / MEGA quota exceeded

There are mirror downloads on the official Discord server, invite link: https://discord.gg/962y4pU

---

## Internet icon bug

Fix: Discord message link with instructions: https://discord.com/channels/619835916139364383/626772969611460619/800174514951684116. 
Direct link to the zip file: https://cdn.discordapp.com/attachments/626772969611460619/800174514813665290/fix-network-icon.zip

---

## Internet/Sound/Bluetooth/Touchpad/other hardware... not working

Download the drivers from the manufacturer's website ans install them.

If you can't do that, for example you don't have internet driver, somehow (on other computer or something like that) download [Snappy Driver Installer Origin](https://www.snappy-driver-installer.org/). 
Extract it, and start the software with `SDIO_auto.bat`. Then select the `Download Network Drivers Only` option. It will start the download of all the existing network drivers. 
If it finishes (you can monitor the process on the top side of the window), copy the whole folder to the other computer which doesn't have internet. Open on that computer the software, and install the missing network drivers. After restart you can scan the PC for more missing drivers, or better yet, go to the manufacturers website, and download the drivers from there.

((this section needs more detailing, because in my VM all the drivers up to date, so I can't go though the whole process))

---

## Second monitor not working/blank

Install GPU drivers. Help: https://www.revi.cc/revios/post-install#h.p_GR11WmefRS4F

---

## Can I download other languages?

Yes, in the Settings. If that isn't working, follow this: https://www.revi.cc/revios/workspace/lang

---

## Can I use Windows Update?

Not recommended, because it will disable tweaks and reinstall bloatware.

But you can install update with the help of this guide: https://www.revi.cc/revios/workspace/updating

---

## Which version can I use Faceit? / Faceit is not working

Only works on `21H2` and `21.12` version.

---

## You said Faceit only works with 21H2/21.12, and I am on 21H2/21.12, and it is still not working

Probably since the release the those versions another update was released by Microsoft, which is required by Faceit. New build of ReviOS will be released soon.

---

## GPU and Network monitoring not working in the Task Manager

Yes, they were stripped because leaking memory.

---

## AMD driver installation is crashing

It's a Windows 11 bug. Try running the installer in silent mode, with the `/S` flag. 
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

From the Windows 10 builds it was removed.

In the Windows 11 build you can reactivate it.
- go to`"%userprofile%\Documents\Workspace\Windows Defender"`
- run `Start.bat`
- press `1`
- restart

---

## Driver missing when installing ReviOS

Try plugging the flash drive into another USB port. If sill not working, try using [Ventoy](https://www.ventoy.net/) instead of Rufus.
