---
hide:
  - navigation
---

<style>
    details > p {
        font-size: 14pt;
    }
</style>

# ReviOS related questions

## What is the difference between the versions?

As of this moment (2022-07-24), there are only 2 versions of ReviOS that are supported: `11 22.07`, `10 22.07`. No other versions are supported.

=== "ReviOS 11 22.07"

    Based on the latest Windows 11 Pro (22621.232), released on 24th of July 2022.

    [Changelog](https://www.revi.cc/revios/download/changelog#h.jjwpsqn2kr){target=_blank}

    [Download](https://www.revi.cc/revios/download#h.kwa7bvvnrtc9){target=_blank}

    Alternative download links on the official [Discord](https://discord.gg/962y4pU){target=_blank} server's [download channel](https://discord.com/channels/619835916139364383/658369065110339640/1000795817705230396){target=_blank}. 


=== "ReviOS 10 22.07"

    Based on the latest Windows 10 Pro (19044.1865), released on 28th of July 2022.

    [Changelog](https://www.revi.cc/revios/download/changelog#h.5m29vb11epyy){target=_blank}

    [Download](https://www.revi.cc/revios/download#h.vxvav5mpn4w){target=_blank}

    Alternative download links on the official [Discord](https://discord.gg/962y4pU){target=_blank} server's [download channel](https://discord.com/channels/619835916139364383/658369065110339640/1002273626910904470){target=_blank}. 


**For FACEIT we always recommend to use the latest versions of ReviOS.** [Details below](#which-version-do-i-need-for-faceit).

### Which version is the best? 

Even if you do find **older version of ReviOS, we do not recommend** using those, since they are outdated. Maybe ancient version have better latency or speed, but the number of software that supports those versions are declining day by day.

So always **install the latest**, because that is the best.

### ReviOS 10 or ReviOS 11?

These two versions of ReviOS have very little difference between them, and it mainly boils down to **what do you like more**. Windows 10 or Windows 11. Although **DirectX 12 games** and latest **Intel** processors, like the **12th generation** are more supported on **Windows 11**, these are not ReviOS related things, these differences are present on the stock Windows too.

Also, if you plan on using anti-cheat systems like FACEIT or Vanguard, you may need to enable Secure Boot and TPM, regardless that ReviOS 11 skips the check when installing, so if your hardware does not support it, use ReviOS 10.

---

## Unsupported things on ReviOS

Disabled:

- Automatic Windows Updates
    - With that automatic driver installation too. Install your drivers manually. [Help here](not-related.md#internetsoundbluetoothother-hardware-not-working)

Not working:

- Phone calls *(fixed in ReviOS 22.07 and above)*
- Microsoft email client *(fixed in ReviOS 22.07 and above)*
- Mixed Reality *(fixed in ReviOS 22.07 and above)*

---

## What is the system requirement for ReviOS?

Refer to our website's section about this, although it's the same as the stock Windows have, but ReviOS usually uses less RAM, and fewer processes run. The Windows 11 versions of ReviOS have the Secure Boot and TPM requirements disabled.

???+ note "TPM and Secure Boot on Windows 11"
    If you play games or use anti-cheats that require Secure Boot and TPM, you still need to enable those functions.

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

## Which version do I need for FACEIT?

As of this moment (2022-07-24), FACEIT only works on the `11 22.07` and `10 22.07` versions. 

The `22.05` and `22.06` builds are probably still compatible with FACEIT, but not for long. Keep in mind that we do not support those versions anymore.

If you are using one of these versions, and still cannot use FACEIT, since the release of that version probably another update was released by Microsoft, which is required by FACEIT. A new build of ReviOS will be released soon. 

---

## Rufus "Unable to patch/setup files for boot" error

On older versions of Rufus **select Standard at Image options**.

On newer versions when **a window pops up** with the options to remove Secure Boot and TPM or RAM and disk or Microsoft account requirements or disable data collection, **select neither**. **ReviOS skips all of these already.**

==Or just try Ventoy. Help in the [installation tutorial](install.md#ventoy).==

---

## I cannot log into my user

*Update:* 

In ReviOS 11 22.07 and above this problem is resolved. Even if you do not set a password at installation, and evade setting a PIN code when logging into your Microsoft account, at the login screen a window will pop up, and after logging in again with your MS account, you have to set a PIN code.

The PIN code forcing can be disabled in `Settings` -> `Accounts` -> `Sign-in options` with `For improved security, only allow Windows Hello sign-in for Microsoft accounts on this device (Recommended)`.

*Previously:*

This is happening, because of the connection of a Microsoft account to the local user. Right now the only fix is to reinstall your OS, and after you log into your Microsoft account set a PIN code too.

Other technique to evade the bug, is to log into your Microsoft account in the Microsoft Store. That way you will not be locked out and still can use your PC without a PIN code. Partial solution reported [here](https://discord.com/channels/619835916139364383/626772969611460619/944214984047616001){target=_blank}.

---

## Can I use Windows Update?

Not recommended, because **it will revert tweaks**, **reinstall bloatware** and cause setbacks with respect to privacy and other pre-applied features, might even **break your OS**.

**Windows Update** in the latest versions of ReviOS **is not disabled**, so using the **Workspace** enable **.reg file will achieve nothing**. Only the automatic update downloading and installation is disabled, and in Settings the **Windows Update menu is hidden**. It is not disabled completely because half of the OS communicates through this service, for example the Store would not work.

If you still want to update, you can manually install updates with the help of [this guide](https://www.revi.cc/revios/workspace/updating){target=_blank} or reactivate the Windows Update menu in Settings with the Revision Tool. For more information about the tool, please read [the section about it](#how-can-i-enable-windows-defender-or-superfetch-sysmain-or-uac-or-notifications-revision-tool).

???+ warning
    ==**If you update, might as well just use stock Windows.**== Reasons explained above.

---

## How can I update to the newest version of ReviOS?

You need to reinstall. Do not forget to backup your data.

Also, you do not need to update just because a new version of ReviOS is released. If your system is stable, and you do not need newer updates for certain anti-cheat systems, you can stay on your older ReviOS version. But please note that we might not provide you support.

If you want to update because of FACEIT, make sure to check out [the section about it](#which-version-do-i-need-for-faceit).

---

## How can I enable Windows Defender or Superfetch (SysMain) or UAC or Notifications? Revision Tool

If the **shortcut** of the Revision Tool is not **on the Desktop**, follow this:

1. In the `Documents` folder of the user go to `Workspace` and then `Revision-Tool` folder. To be exact: `%userprofile%\Documents\Workspace\Revision-Tool`
2. Run `Start.bat`
3. Select the desired option
4. After the changes are done, restart your PC

### Full list of features of the Revision-Tool

#### On ReviOS 11 (22.07):

Installing VC Runtimes.

Enable/Disable:

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

#### On ReviOS 10 (22.07):

Installing VC Runtimes.

Enable/Disable:

- Defender
- Superfetch
- Windows Update features
  - Unhide Windows Updates
  - Enable automatic drivers updating
- UAC
- Notifications
- Inking And Typing Personalization
- Full Screen Optimizations

---

## Explorer.exe crashing on ReviOS 11

Open a PowerShell window, and run this command:

```powershell
Add-AppxPackage -Register -Path C:\Windows\SystemApps\Microsoft.UI.Xaml.CBS_8wekyb3d8bbwe\AppxManifest.xml -DisableDevelopmentMode -ForceApplicationShutdown
```

---

## GPU and Network monitoring not working in the Task Manager

They were disabled because leaking memory.

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
  
    ???+ note
        If this command fails, which is most likely to happen on 22.04 and older versions, download [this zip](files/wscapi.zip), and place the contents of it inside the System32 folder. [Link to the original message and conversation](https://discord.com/channels/619835916139364383/626772969611460619/953223236244619274)

If you do not see your GPU in the Performance tab in Task Manager, restart your PC again.


To reactivate Network statistics:

1. Open `regedit`
2. At `HKLM\System\CurrentControlSet\Services\Ndu` set `Start` to `2`
3. Restart

---

## Microsoft Store / Xbox app not working

Run `ctfmon` and `wsreset` commands.

On ReviOS 10 22.05 try this:

1. Open PowerShell in administrator mode, e.g. ++"Right-click"++ on the Start Menu button (++win++), and select `Windows PowerShell (Admin)`

2. Run this command:
   
    ```powershell
    Get-CimInstance -Namespace "Root\cimv2\mdm\dmmap" -ClassName "MDM_EnterpriseModernAppManagement_AppManagement01" | Invoke-CimMethod -MethodName UpdateScanMethod
    ```

3. After this, go inside the Store, and check for app updates.
    
    On the older Store UI you can do it by:

      1. Click the 3 dots in the upper right corner of the window
      2. Click `Downloads and updates`

    On the newer Store, you can do it by going inside the Library page.
  
If you have updates, the Store should start installing them automatically. If not, click `Get Updates`.

As a last resort, you can try the `wsreset -i` command. It reinstalls the Store app. It must be let running at least 20 minutes.

> *Older, ReviOS 22.01 and 22.02 Xbox app problem (not supported versions):*
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

## iTunes not detecting any Apple device

It is because ReviOS misses Apple driver, which you could download only by Windows Update, but that is still not recommended. Instead you can use [3uTools](http://www.3u.com/) to repair the drivers.

Once installed, after opening the software, go to:

1. `Toolbox`
2. `iTunes Utility`
3. `Repair Driver`
4. `Advanced Repair`

There select `Uninstall the old driver files stored in system`. After, iTunes should work.

Link to the original messages on Discord: [Message 1](https://discord.com/channels/619835916139364383/626772969611460619/930729137830789141) and [Message 2](https://discord.com/channels/619835916139364383/626772969611460619/998888988431634512)

---

## Valorant CFG error

Either [turn on Windows Defender](#how-can-i-enable-windows-defender-or-superfetch-sysmain-or-uac-or-notifications-revision-tool), and you can enable Control Flow Guard in Windows Security.

Or run this command in a PowerShell terminal (you may need to start the terminal in administrator mode):

```powershell 
Set-ProcessMitigation -Name vgc.exe -Enable CFG
Set-ProcessMitigation -Name vgc.exe -Enable DEF
Set-ProcessMitigation -Name vgc.exe -Enable AuditDynamicCode
```

If Vanguard still not working, you can try these two command: (you have to disable CFG to Discord, because it will crash)

```powershell
Set-ProcessMitigation -System -Enable CFG
Set-ProcessMitigation -Name Discord.exe -Disable CFG
```

---

## How to change lock screen background?

1. Open `regedit`
2. Go to `HKEY_LOCAL_MACHINE\Software\Policies\Microsoft\Windows\Personalization`
3. Set the `NoLockScreen` key's value to `0`
4. Now you should be able to change it in Settings, if not, restart

---

## AMD driver installation is crashing

It is a Windows 11 bug. Try running the installer in silent mode, with the `/S` flag. 
[Here](https://discord.com/channels/619835916139364383/626772969611460619/932975660392128562){target=_blank} is help and a script to automate it.

If this method is not working, install [Chocolatey](https://chocolatey.org/){target=_blank} and then the `amd-ryzen-chipset` package.

---

## Internet icon bug

[Discord message link with instructions](https://discord.com/channels/619835916139364383/626772969611460619/800174514951684116){target=_blank}

[Zip file with the fix](files/fix-network-icon.zip)

---

## Windows Update icon showed up on the taskbar and/or the "Update and shutdown/restart" option showed up

This is a bug in the `22.01` version, for now you can use [this fix](files/Fix-Windows-Update-Taskbar.reg){target=_blank} for the taskbar icon. In the `22.02` version, it is already fixed.