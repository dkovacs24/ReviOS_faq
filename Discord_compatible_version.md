**Before using this FAQ, please do your own research, look around on the `ReviOS website` (https://www.revi.cc/), there specifically in the  `Changelogs` (https://www.revi.cc/revios/download/changelog), the `Post-install` (https://www.revi.cc/revios/post-install) guide and the `Workspace` (https://www.revi.cc/revios/workspace).**
**Also use Google (or the search engine of your choice), especially with not ReviOS related questions.** 
**You _can_ find here things that are on the ReviOS website, because people are dumb, and going to ask it anyway.**
<:blank:934095223045374033>

##ReviOS frequently asked questions##
<:blank:934095223045374033>

**What is the difference between the versions? What to choose?**
> As of this moment (2022-01-21), there are 3 versions of ReviOS that are supported: `1709`, `21H2` and `21.12`. No other versions are supported.
> 
> If you are looking for a version:
> - more gaming, less latency and less bloatware oriented, choose `1709`
> - more compatible with latest programs, choose `21H2` or `21.12`
> 
> **_Faceit only works on 21H2 and 21.12._** Details below.
<:blank:934095223045374033>

**Where is the Windows 10 version? / Where are the older versions?**
> https://www.revi.cc/revios/download/alternative-downloads
<:blank:934095223045374033>

**How to install ReviOS?**
> https://youtu.be/w4Wn25d02iY
<:blank:934095223045374033>

**Downloads are not working / Google Drive said: "Sorry, you can't view or download this file at this time." / MEGA quota exceeded**
> Mirror downloads in <#658369065110339640>
<:blank:934095223045374033>

**Internet icon bug**
> Fix: https://discord.com/channels/619835916139364383/626772969611460619/800174514951684116. 
> Direct link to the zip file: https://cdn.discordapp.com/attachments/626772969611460619/800174514813665290/fix-network-icon.zip
<:blank:934095223045374033>

**Internet/Sound/Bluetooth/Touchpad/other hardware... not working**
> Download the drivers from the manufacturer's website.
> If you can't do that, for example you don't have internet driver, somehow (on other computer or something like that) download [Snappy Driver Installer Origin](https://www.snappy-driver-installer.org/). 
> Extract it, and start the software with `SDIO_auto.bat`. Then select the `Download Network Drivers Only` option. It will start the download of all the existing network drivers. 
> If it finishes (you can monitor the process on the top side of the window), copy the whole folder to the other computer which doesn't have internet. Open on that computer the software, and install the missing network drivers. After restart you can scan the PC for more missing drivers, or better yet, go to the manufacturers website, and download the drivers from there.
<:blank:934095223045374033>

**Second monitor not working/blank**
> Install GPU drivers. Help: https://www.revi.cc/revios/post-install#h.p_GR11WmefRS4F
<:blank:934095223045374033>

**Can I download other languages?**
> Yes, in the Settings. If that isn't working, follow this: https://www.revi.cc/revios/workspace/lang
<:blank:934095223045374033>

**Can I use Windows Update?**
> Not recommended, because it will disable tweaks and reinstall bloatware.
> But you can install update with the help of this guide: https://www.revi.cc/revios/workspace/updating
<:blank:934095223045374033>

**Which version can I use Faceit? / Faceit is not working**
> Only works on `21H2` and `21.12` version.
<:blank:934095223045374033>

**You said Faceit only works with 21H2/21.12, and I am on 21H2/21.12, and it is still not working**
> Probably since the release the those versions another update was released by Microsoft, which is required by Faceit. New build of ReviOS will be released soon.
<:blank:934095223045374033>

**GPU and Network monitoring not working in the Task Manager**
> Yes, they were stripped because leaking memory.
<:blank:934095223045374033>

**AMD driver installation is crashing**
> It's a Windows 11 bug. Try running the installer in silent mode, with the `/S` flag. 
> Here's help and a script to automate it: https://discord.com/channels/619835916139364383/626772969611460619/932975660392128562
<:blank:934095223045374033>

**There are some visual bugs on the taskbar in ReviOS 11**
> These bugs came from Windows 11, hope they will be fixed in next Microsoft update releases.
> In the mean time, try StartAllBack (https://www.startallback.com/).
<:blank:934095223045374033>

**Microsoft Store / XBox app not working**
> Run `ctfmon` and `wsreset` commands.
<:blank:934095223045374033>

**Where is Windows Defender? Can I use it?**
> From the Windows 10 builds it was removed.
> In the Windows 11 build you can reactivate it.
> - go to`"%userprofile%\Documents\Workspace\Windows Defender"`
> - run `Start.bat`
> - press `1`
> - restart
<:blank:934095223045374033>

**Driver missing when installing ReviOS**
> Try plugging the flash drive into another USB port. If sill not working, try using Ventoy (https://www.ventoy.net/) instead of Rufus.
<:blank:934095223045374033>

##Jump to the start of the list:## 
https://discord.com/channels/619835916139364383/779558805422735402/934169999222919178

##Table of Contents:##

**What is the difference between the versions? What to choose?**
https://discord.com/channels/619835916139364383/779558805422735402/934170066386296852

**Where is the Windows 10 version? / Where are the older versions?**
https://discord.com/channels/619835916139364383/779558805422735402/934170087844380712

**How to install ReviOS?**
https://discord.com/channels/619835916139364383/779558805422735402/934170107398213682

**Downloads are not working / Google Drive said: "Sorry, you can't view or download this file at this time." / MEGA quota exceeded**
https://discord.com/channels/619835916139364383/779558805422735402/934170142319984730

**Internet icon bug**
https://discord.com/channels/619835916139364383/779558805422735402/934170163979370506

**Internet/Sound/Bluetooth/Touchpad/other hardware... not working**
https://discord.com/channels/619835916139364383/779558805422735402/934170196283883591

**Second monitor not working/blank**
https://discord.com/channels/619835916139364383/779558805422735402/934170238486999040

**Can I download other languages?**
https://discord.com/channels/619835916139364383/779558805422735402/934170255587164180

**Can I use Windows Update?**
https://discord.com/channels/619835916139364383/779558805422735402/934170289569402960

**Which version can I use Faceit? / Faceit is not working**
https://discord.com/channels/619835916139364383/779558805422735402/934170309819519036

**You said Faceit only works with 21H2/21.12, and I am on 21H2/21.12, and it is still not working**
https://discord.com/channels/619835916139364383/779558805422735402/934170342023381033

**GPU and Network monitoring not working in the Task Manager**
https://discord.com/channels/619835916139364383/779558805422735402/934170361933750332

**AMD driver installation is crashing**
https://discord.com/channels/619835916139364383/779558805422735402/934170381181399081

**There are some visual bugs on the taskbar in ReviOS 11**
https://discord.com/channels/619835916139364383/779558805422735402/934170399791542372

**Microsoft Store / XBox app not working**
https://discord.com/channels/619835916139364383/779558805422735402/934170417843806229

**Where is Windows Defender? Can I use it?**
https://discord.com/channels/619835916139364383/779558805422735402/934170442640551976

**Driver missing when installing ReviOS**
https://discord.com/channels/619835916139364383/779558805422735402/934170459023495168