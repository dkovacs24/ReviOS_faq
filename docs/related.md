---
hide:
  - navigation
---

<style>
    div.admonition p:not(.admonition-title) {
        font-size: 125%;
    }
</style>

# ReviOS related questions

## What is the difference between the versions?

As of this moment (2022-08-31), there are only 2 versions of ReviOS that are supported: `10 22.08` and `11 22.07`. No other versions are supported.

=== "ReviOS 10 22.08"

    Based on the latest Windows 10 Pro (19044.1865), released on 31th of July 2022.

    Recommended for older systems, incompatible with Windows 11.

    [Changelog](https://www.revi.cc/revios/download/changelog#h.5m29vb11epyy){target=_blank}

    [Download](https://www.revi.cc/revios/download#h.vxvav5mpn4w){target=_blank}

    Alternative download links are a work in progess. Stay tuned.


=== "ReviOS 11 22.07"

    Based on the latest Windows 11 Pro (22621.232), released on 24th of July 2022.

    Recommended for newer systems with more recent hardware.

    [Changelog](https://www.revi.cc/revios/download/changelog#h.jjwpsqn2kr){target=_blank}

    [Download](https://www.revi.cc/revios/download#h.kwa7bvvnrtc9){target=_blank}

    Alternative download links on the official [Discord](https://discord.gg/962y4pU){target=_blank} server's [download channel](https://discord.com/channels/619835916139364383/658369065110339640/1000795817705230396){target=_blank}.


**For FACEIT we always recommend to use the latest versions of ReviOS.** [Details below](#is-revios-faceit-compatible-which-version-do-i-need-for-faceit).

### Which version is the best?

Even if you do find **older version of ReviOS, we do not recommend** using those, since they are outdated. Maybe ancient version have better latency or speed, but the number of software that supports those versions are declining day by day.

So always **install the latest**, because that is the best.

### ReviOS 10 or ReviOS 11?

These two versions of ReviOS have very little difference between them, and it mainly boils down to **what do you like more**. Windows 10 or Windows 11. Although **DirectX 12 games** and latest **Intel** processors, like the **12th generation**, might perform better on **Windows 11**, due to [DirectStorage](https://www.thewindowsclub.com/what-is-directstorage-in-windows){target=_blank}, [BypassIO](https://docs.microsoft.com/en-us/windows-hardware/drivers/ifs/bypassio){target=_blank} and [Thread Director](https://www.anandtech.com/show/16881/a-deep-dive-into-intels-alder-lake-microarchitectures/2){target=_blank}, these are not ReviOS related things, these differences are present on stock Windows too.

Also, if you plan on using anti-cheat systems like FACEIT or Vanguard, you must enable Secure Boot and TPM, regardless that ReviOS 11 skips the check when installing, so if your hardware does not support it, use ReviOS 10.

And if you care about latency, Windows 10 still provides a better experience.

<!-- <figure markdown>
  ![graph](img/dc/latency.png){width=600px}
  <figcaption>Graph shows Win10 vs Win11 latency. Tested with Intel i7-10700KF and GTX 1070TI by Muren#6968.<br>Click the image to open it</figcaption>
</figure> -->

### Why are there two ISOs files for each ReviOS version?

One for installing a completely new ReviOS instance, and one for upgrading a previous ReviOS. Read more at [How can I upgrade to the newest build of ReviOS?](#how-can-i-upgrade-to-the-newest-build-of-revios) section.


---

## Unsupported things on ReviOS

As of the **latest** ReviOS

**Disabled:** (can be enabled)

- Automatic Windows Updates
    - With that automatic driver installation too. Install your drivers manually. Help on the [How to install drivers page](drivers.md).

**Removed:**

- Windows Insider Hub
- Intel Indeo Codecs
- Video Compression Manager (VCM) codecs

---

## What is the system requirement for ReviOS?

Refer to our website's section about this, although it is the same as the stock Windows have, but ReviOS usually uses less RAM, and fewer processes run. The Windows 11 versions of ReviOS have the Secure Boot and TPM requirements disabled.

!!! note "TPM and Secure Boot on Windows 11"
    In order to play games or use anti-cheats that require Secure Boot and TPM, you still need to enable those functions.

### ReviOS RAM usage

| Total RAM Capacity | Max Usage                       | Actual Available Amount |
| ------------------ | ------------------------------- | ----------------------- |
| 2 GB               | 1.1 GB down to 0.9, 1.4 GB peak | 600 MB to 1.1 GB        |
| 4 GB               | 0.8 GB                          | 3.2 GB                  |
| 8 GB               | 1 GB                            | 7 GB                    |
| 16 GB              | 1 GB                            | 15 GB                   |
| 24 GB              | 1.3 GB                          | 22.7 GB                 |

Tested on a fresh installation of ReviOS 10 22.01, in VirtualBox, on AMD Ryzen 5900X.

Credit to [Stasium#0001](https://stasium.dev/){target=_blank}.

---

## Is ReviOS FACEIT compatible? Which version do I need for FACEIT?

Since ReviOS is Windows, yes it is compatible.

As of this moment (2022-08-31), the recommended builds of ReviOS are `10 22.08` and `11 22.07`.

The `22.06` builds are probably still compatible with FACEIT, but not for long. Keep in mind, we do not support and recommend those versions anymore.

If you are using one of the recommended versions, and still cannot use FACEIT, since the release of that version probably another update was released by Microsoft, which is required by FACEIT. A new build of ReviOS probably will be released too, soon.

---

## Rufus "Unable to patch/setup files for boot" error

On older versions of Rufus **select Standard at Image options**.

On newer versions when **a window pops up** with the options to remove Secure Boot and TPM or RAM and disk or Microsoft account requirements or disable data collection, **select neither**. **ReviOS skips all of these already.**

==Or just try Ventoy. Help in the [installation tutorial](install.md#ventoy).==

---

## Missing drivers in the installation process

When you arrive to the partition making and selecting part of the installing process, but the installer asks for drivers, you might need Intel Rapid Storage Technology (IRST) drivers. [Here is a helping guide from the Asus Support page.](https://www.asus.com/support/FAQ/1044458/){target=_blank}

---

## Apps taking long time to load on ReviOS

Run this command using **PowerShell in administrator mode**:

```powershell
reg add "HKLM\SOFTWARE\Microsoft\Windows NT\CurrentVersion\Image File Execution Options\smartscreen.exe" /v "Debugger" /t REG_SZ /d "%windir%\System32\taskkill.exe" /f
```

---

## I cannot log into my user

*Update:*

In ReviOS 22.07 (Windows 10 and 11) and above this problem is resolved. Even if you do not set a password at installation, and evade setting a PIN code when logging into your Microsoft account, at the login screen a window will pop up, and after logging in again with your MS account, you have to set a PIN code.

The PIN code forcing can be disabled in `Settings` -> `Accounts` -> `Sign-in options` with `For improved security, only allow Windows Hello sign-in for Microsoft accounts on this device (Recommended)` after loggin in with your MS account and setting a PIN code. Then you can delete the PIN code, if you want to.

*Previously:*

This is happening, because of the connection of a Microsoft account to the local user. Right now the only fix is to reinstall your OS, and after you log into your Microsoft account set a PIN code too.

Other technique to evade the bug, is to log into your Microsoft account in the Microsoft Store. That way you will not be locked out and still can use your PC without a PIN code. Partial solution reported with [this message on our Discord](https://discord.com/channels/619835916139364383/626772969611460619/944214984047616001){target=_blank}.

---

## Can I use Windows Update? Where is the Windows Update menu in Settings?

Not recommended, because **it will revert tweaks**, **reinstall bloatware** and cause setbacks with respect to privacy and other pre-applied features, might even **break your OS**.

**Windows Update** in the latest versions of ReviOS **is not disabled**, so using the **Workspace** enable **.reg file will achieve nothing**. Only the automatic update downloading and installation is disabled, and in Settings the **Windows Update menu is hidden**. It is not disabled completely because half of the OS communicates through this service, for example the Store would not work.

If you still want to update, you can manually install updates with the help of [this guide on the Revision website](https://www.revi.cc/revios/workspace/updating){target=_blank} or reactivate the Windows Update menu in Settings with the Revision Tool. For more information about the tool, please read [the section about it](#how-can-i-enable-windows-defender-or-superfetch-sysmain-or-uac-or-notifications-revision-tool).

!!! warning
    ==**If you update, might as well just use stock Windows.**== Reasons explained above.

Instead, you maybe might want to upgrade your ReviOS instance to a newer build. About that, you can read more here: [How can I upgrade to the newest build of ReviOS?](#how-can-i-upgrade-to-the-newest-build-of-revios)

---

## How can I upgrade to the newest build of ReviOS?

!!! danger
    ==**This is an EXPERIMENTAL method**==. We tested it numerous times, but obviously we cannot cover all the edge cases, so use this with caution!

With newer builds of ReviOS we provide 2 separate ISOs. One for installing a completely new ReviOS instance, and one for upgrading a previous ReviOS version. This way, **the users can update their ReviOS instance without reinstalling and losing files**.

For instructions and more information about upgrading your older ReviOS instance, **please read our [How to upgrade ReviOS](upgrade.md) guide**.

If you want to upgrade because of FACEIT, make sure to check out [the section about it](#is-revios-faceit-compatible-which-version-do-i-need-for-faceit).

---

## How can I enable Windows Defender or Superfetch (SysMain) or UAC or Notifications? Revision Tool

If the **shortcut** of the Revision Tool is not **on the Desktop**, follow this:

1. In the `Documents` folder of the user go to `Workspace` and then `Revision-Tool` folder. To be exact: `%userprofile%\Documents\Workspace\Revision-Tool`
2. Run `Start.bat`
3. Select the desired option
4. After the changes are done, restart your PC

If you cannot find the Revision Tool inside the Documents folder, or you just want to download it, you can do it here:

[:fontawesome-solid-download: Download Revision-Tool.zip](files/Revision-Tool.zip){ .md-button .md-button--primary }

> MD5 checksum: `ba63377d40ac7f72681268e4e91312ae`


!!! warning "Revision Tool on older versions of ReviOS"
    This Revision Tool is fully compatible only with the latest builds of ReviOS, that is right now the `22.07`. If you try to use some or all of the functions of this version of the Revision Tool, they might not work.

    Not exhaustive list of functions that will not work:

    - Windows Defenter before `11 21.12` and `10 22.01`
    - Superfetch before `22.05`
    - Full Screen Optimizations before `10 22.06` and `11 22.07`

    Related: [ReviOS Changelog](https://www.revi.cc/revios/download/changelog){target=_blank}

### Full list of features of the Revision-Tool

=== "On ReviOS 10 (22.08)"

    - Enable/Disable:
        - Defender
        - Superfetch
            - Memory Compression
        - Windows Update features
            - Unhide Windows Updates
            - Enable automatic drivers updating
        - UAC
        - Notifications
        - Inking And Typing Personalization
        - Full Screen Optimizations
    - Installing VC Runtimes


=== "On ReviOS 11 (22.07)"

    - Enable/Disable:
        - Defender
        - Superfetch
        - Windows Update features
            - Unhide Windows Updates
            - Enable automatic drivers updating
        - UAC
        - Notifications
        - Inking And Typing Personalization
        - Full Screen Optimizations
        - Additional Windows 11 tweaks
            - New right-click menu
            - Tabs in File Explorer
    - Installing VC Runtimes



---

## Microsoft Store / Xbox app not working

Run `ctfmon` and `wsreset` commands.

As a last resort, you can try the `wsreset -i` command. It reinstalls the Store app. It must be let running at least 20 minutes.

> *ReviOS 22.05 Store problem (not supported build anymore, so not relevant)*
> 
> 1. Open PowerShell in administrator mode, e.g. ++"Right-click"++ on the Start Menu button (++win++), and select `Windows PowerShell (Admin)`
> 
> 2. Run this command:
> 
>     ```powershell
>     Get-CimInstance -Namespace "Root\cimv2\mdm\dmmap" -ClassName "MDM_EnterpriseModernAppManagement_AppManagement01" | Invoke-CimMethod -MethodName UpdateScanMethod
>     ```
> 
> 3. After this, go inside the Store, and check for app updates.
> 
>     On the older Store UI you can do it by:
> 
>       1. Click the 3 dots in the upper right corner of the window
>       2. Click `Downloads and updates`
> 
>     On the newer Store, you can do it by going inside the Library page.
> 
> If you have updates, the Store should start installing them automatically. If not, click `Get Updates`.

<br>

> *Older, ReviOS 22.01 and 22.02 Xbox app problem (not supported versions anymore):*
>
> If the updating is done, and Xbox login is still not working, go through these steps:
>
> 1. Go to [https://store.rg-adguard.net/](https://store.rg-adguard.net/){target=_blank}
> 2. Change the search options from `URL (link)` to `PackageFamilyName` and `RP` to `Slow`, and search for `Microsoft.GamingApp_8wekyb3d8bbwe`
> 3. Download the following packages:
>     1. `Microsoft.VCLibs.140.00_14.0.30704.0_x64__8wekyb3d8bbwe.appx`
>     2. `Microsoft.VCLibs.140.00.UWPDesktop_14.0.30704.0_x64__8wekyb3d8bbwe.appx`
>     3. `Microsoft.UI.Xaml.2.7_7.2203.17001.0_x64__8wekyb3d8bbwe.appx`
>     4. `Microsoft.GamingApp_2203.1001.4.0_neutral_~_8wekyb3d8bbwe.msixbundle`
> 4. Go where you downloaded the files, ++shift+"Right-click"++ and choose `Open Powershell window here`
> 5. Run `Add-AppxPackage` with the downloaded files. E.g.: `Add-AppxPackage Microsoft.VCLibs.140.00_14.0.30704.0_x64__8wekyb3d8bbwe.appx`.
>
>     **Make sure you install the packages in the order listed above.**
>
> 6. Restart

---

## Cannot toggle Start Menu folders in Settings

If you cannot toggle on Start Menu folders in Settings -> Personalization -> Start -> Folders:

1. Open `regedit`
2. Go to `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\PolicyManager\current\device\Start` 
3. Delete every key **except** `ConfigureStartPins`

---

## Windows Mail not working

1. Open PowerShell in administrator mode, e.g. ++"Right-click"++ on the Start Menu button (++win++), and select `Windows PowerShell (Admin)`
2. Run this command:

    ```powershell
    dism.exe /Online /Add-Capability /CapabilityName:OneCoreUAP.OneSync~~~~0.0.1.0
    ```

3. After this, Open `Settings`
4. Go to `Privacy & security` -> `Contacts`
5. Toggle on `Contact access`, `Let apps access your contacts` and `Mail and Calendar`

---

## Disable old notification balloons

1. Open `regedit`
2. Go to `HKEY_CURRENT_USER\SOFTWARE\Policies\Microsoft\Windows\Explorer`
3. Set `EnableLegacyBalloonNotifications` to `0`

---

## iTunes not detecting any Apple device

It is because ReviOS lacks some Apple drivers, which you could download only by Windows Update, but that is still not recommended. Instead, you can use [3uTools](http://www.3u.com/){target=_blank} to repair the drivers.

Once installed, after opening the software, go to:

1. `Toolbox`
2. `iTunes Utility`
3. `Repair Driver`
4. `Advanced Repair`

There select `Uninstall the old driver files stored in system`. After, iTunes should work.

Link to the original messages on Discord: [Message 1](https://discord.com/channels/619835916139364383/626772969611460619/930729137830789141){target=_blank} and [Message 2](https://discord.com/channels/619835916139364383/626772969611460619/998888988431634512){target=_blank}

---

## Blank screen after logging into ReviOS

1. On the blank screen with cursor, press ++ctrl+alt+delete++, it will bring you the option for Task Manager along with other options. Open Task Manager.

    Alternatively, you can also use the key combination ++ctrl+shift+esc++ to open the Task Manager directly.

2. Click `File`, then `Run new task`.
3. With the new window open `services.msc`.
4. Search for the `App Readiness` service, and open it's properties by double-clicking it.
5. Set the `Startup type` to `Disabled`.
6. In the Task Manager click `File` and `Run new task` again.
7. Run `shutdown /r /f /t 0`. It will restart your PC.

---

## Explorer.exe crashing on ReviOS 11

Open a PowerShell window as administrator, and run this command:

```powershell
Add-AppxPackage -Register -Path C:\Windows\SystemApps\Microsoft.UI.Xaml.CBS_8wekyb3d8bbwe\AppxManifest.xml -DisableDevelopmentMode -ForceApplicationShutdown
```

---

## Valorant CFG error

Either [turn on Windows Defender](#how-can-i-enable-windows-defender-or-superfetch-sysmain-or-uac-or-notifications-revision-tool), and you can enable Control Flow Guard in Windows Security,

or run these commands in a PowerShell terminal as administrator:

```powershell
Set-ProcessMitigation -Name vgc.exe -Enable CFG
Set-ProcessMitigation -Name vgc.exe -Enable DEF
Set-ProcessMitigation -Name vgc.exe -Enable AuditDynamicCode
```

---

## GPU and Network monitoring not working in the Task Manager

They are disabled because of leaking memory.

To reactivate GPU statistics:

1. Open `cmd`
2. Run this:

    ```
    reg add "HKLM\SYSTEM\CurrentControlSet\Services\GraphicsPerfSvc" /v "Start" /t REG_DWORD /d "2" /f
    ```

3. Restart your PC

4. Then run this:

    ```
    sc start GraphicsPerfSvc
    ```

    !!! note
        If this command fails, which is most likely to happen on 22.04 and older versions, download [this zip](files/wscapi.zip), and place the contents of it inside the System32 folder. [Link to the original message and conversation on our Discord](https://discord.com/channels/619835916139364383/626772969611460619/953223236244619274){target=_blank}

If you do not see your GPU in the Performance tab in Task Manager, restart your PC again.


To reactivate Network statistics:

1. Open `regedit`
2. At `HKLM\System\CurrentControlSet\Services\Ndu` set `Start` to `2`
3. Restart
4. Then run this:
    ```
    sc start Ndu
    ```

---

## How to change lock screen background?

Rename your background image to `img100.jpg` and move it to `C:\Windows\Web\Screen` (Taking ownership to the original `img100.jpg` might be mandatory).

---

## AMD driver installation is crashing

It is a Windows 11 bug. Try running the installer in silent mode, with the `/S` flag. [This message on our Discord](https://discord.com/channels/619835916139364383/626772969611460619/932975660392128562){target=_blank} helps with this issue by automatizing it.

If this method is not working, install [Chocolatey](https://chocolatey.org/){target=_blank} and then the `amd-ryzen-chipset` package.

---

## Internet icon bug

[Discord message link with instructions](https://discord.com/channels/619835916139364383/626772969611460619/800174514951684116){target=_blank}

[Zip file with the fix](files/fix-network-icon.zip)

---

## Windows Update icon showed up on the taskbar and/or the "Update and shutdown/restart" option showed up

This was a bug in the `22.01` builds, for now you can use [this fix](files/Fix-Windows-Update-Taskbar.reg){target=_blank} for the taskbar icon. The issue is already fixed in newer ReviOS builds.
