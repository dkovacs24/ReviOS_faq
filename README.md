**Before using this faq, please do your own research, look around on the [ReviOS website](https://www.revi.cc/), there specifically in the [Changelogs](https://www.revi.cc/revios/download/changelog), the [Post-install](https://www.revi.cc/revios/post-install) guide and the [Workspace](https://www.revi.cc/revios/workspace). Also use Google (or the search engine of your choice), especially with not ReviOS related questions. You _can_ find here things that are on the ReviOS website, because people are dumb, and going to ask it anyway.**


- [ReviOS frequently asked questions](#revios-frequently-asked-questions)
  - [What's the difference between the versions? What to choose?](#whats-the-difference-between-the-versions-what-to-choose)
  - [Where is the Windows 10 version? / Where are the older versions?](#where-is-the-windows-10-version--where-are-the-older-versions)
  - [How to install ReviOS](#how-to-install-revios)
  - [Downloads not working](#downloads-not-working)
  - [Internet icon bug](#internet-icon-bug)
  - [Internet/sound/touchpad/who knows what else... not working](#internetsoundtouchpadwho-knows-what-else-not-working)
  - [Second monitor not working](#second-monitor-not-working)
  - [Can I download other language?](#can-i-download-other-language)
  - [Can I use Windows Update?](#can-i-use-windows-update)
  - [Which version can I use Faceit? / Faceit not working](#which-version-can-i-use-faceit--faceit-not-working)
  - [You said Faceit works with 21H2/21.12.](#you-said-faceit-works-with-21h22112)
  - [GPU and Network monitoring not working in the Task Manager](#gpu-and-network-monitoring-not-working-in-the-task-manager)
  - [AMD driver installation is crashing](#amd-driver-installation-is-crashing)
  - [There are some visual bugs with ReviOS 11](#there-are-some-visual-bugs-with-revios-11)
  - [Microsoft Store / XBox app not working](#microsoft-store--xbox-app-not-working)
  - [Where is Windows Defender? Can I use it?](#where-is-windows-defender-can-i-use-it)


# ReviOS frequently asked questions


## What's the difference between the versions? What to choose?

As of this moment (2022-01-18), there are 3 versions of ReviOS that are supported: 1709, 21H2 and 21.12. No other versions are supported.

If you are looking for a version:
- more gaming, less latency and less bloatware oriented, choose 1709
- more compatible with latest programs, choose 21H2 or 21.12


***Faceit only works on 21H2 and 21.12.***

---

## Where is the Windows 10 version? / Where are the older versions?

[Alternative downloads](https://www.revi.cc/revios/download/alternative-downloads)

---

## How to install ReviOS

[Tutorial](https://youtu.be/w4Wn25d02iY)

---

## Downloads not working

There are mirror downloads on the official Discord server, invite link: https://discord.gg/962y4pU

---

## Internet icon bug

If not working, try this fix, Discord message link with instructions: https://discord.com/channels/619835916139364383/626772969611460619/800174514951684116. Direct link to the zip file: https://cdn.discordapp.com/attachments/626772969611460619/800174514813665290/fix-network-icon.zip

---

## Internet/sound/touchpad/who knows what else... not working

Download the drivers from the manufacturer's website.

If you can't do that, for example you don't have internet driver, somehow download [Snappy Driver Installer Origin](https://www.snappy-driver-installer.org/) Full. It will download all the drivers they have, about 21 GB. If you have internet access and you need to download other drivers, just choose the Lite version, it will scan your hardware, and only download the drivers you need.

---

## Second monitor not working

Install GPU drivers. Help: https://www.revi.cc/revios/post-install#h.p_GR11WmefRS4F

---

## Can I download other language?

Yes, follow this: https://www.revi.cc/revios/workspace/lang

---

## Can I use Windows Update?

Not recommended, because it can disable tweaks and reinstall bloatware.

---

## Which version can I use Faceit? / Faceit not working

Only works on **21H2** and **21.12** version.

---

## You said Faceit works with 21H2/21.12.

Probably since the release the those versions another update was released by Microsoft, which is required by Faceit. New build of ReviOS will be release soon.

---

## GPU and Network monitoring not working in the Task Manager

Yes, they were stripped because leaking memory.

---

## AMD driver installation is crashing

It's a Windows 11 bug. Try running the installer in silent mode, with the `/S` flag. Here's help and a script to automate it: https://discord.com/channels/619835916139364383/626772969611460619/932975660392128562

---

## There are some visual bugs with ReviOS 11

These bugs came from Windows 11, hope they will be fixed in next Microsoft update releases.

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