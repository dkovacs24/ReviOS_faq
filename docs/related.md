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

## What is the difference between the versions? What to choose?

As of this moment (2022-05-20), there are only 2 versions of ReviOS that are supported: `10 22.05`, `11 21.04`. No other versions are supported.

=== "ReviOS 10 22.05"

    Based on the latest Windows 10 Pro (19044.1737), released on 20th of May 2022.

    [Changelog](https://www.revi.cc/revios/download/changelog#h.5m29vb11epyy){target=_blank}

    [Download](https://www.revi.cc/revios/download#h.vxvav5mpn4w){target=_blank}

    Alternative download links on the official [Discord](https://discord.gg/962y4pU){target=_blank} server's [download channel](https://discord.com/channels/619835916139364383/658369065110339640/977581424125313087){target=_blank}. 


=== "Revios 11 22.04"

    Based on the latest Windows 11 Pro (22000.651), released on 19th of April 2022.

    [Changelog](https://www.revi.cc/revios/download/changelog#h.rhpiak7lkjq1){target=_blank}

    [Download](https://www.revi.cc/revios/download#h.kwa7bvvnrtc9){target=_blank}

    Alternative download links on the official [Discord](https://discord.gg/962y4pU){target=_blank} server's [download channel](https://discord.com/channels/619835916139364383/658369065110339640/965855822372569099){target=_blank}.


**FACEIT only works on `10 22.05`, `11 22.04` and `10 22.04` for a limited time.** [Details below](#which-version-do-i-need-for-faceit).

### But which version is the fastest? Or the better? ReviOS 10 or ReviOS 11?

These two versions of ReviOS have very little difference between them, and it mainly boils down to **what do you like more**. Windows 10 or Windows 11. Although **DirectX 12 games** and latest **Intel** processors, like the **12th generation** are more supported on **Windows 11**, these are not ReviOS related things, these differences are present on the stock Windows too.

Also, if you plan on using anti-cheat systems like FACEIT or Vanguard, you may need to enable Secure Boot and TPM, regardless that ReviOS 11 skips the check when installing, so if your hardware does not support it, use ReviOS 10.

---

## What is the system requirement for ReviOS?

Refer to our website's section about this, although it's the same as the stock Windows have, but ReviOS usually uses less RAM, and fewer processes run. The Windows 11 versions of ReviOS have the Secure Boot and TPM requirements disabled.

???+ note "TPM and Secure Boot on Windows 11"
    If you play games or use anti-cheats that require Secure Boot and TPM, you still need to enable those functions.

### ReviOS RAM usage

| Total RAM Capacity | Max Usage                       | Actual Available Amount |
| ------------------ | ------------------------------- | ------------------------- |
| 2 GB               | 1.1 GB down to 0.9, 1.4 GB peak | 600 MB to 1.1 GB          |
| 4 GB               | 0.8 GB                          | 3.2 GB                    |
| 8 GB               | 1 GB                            | 7 GB                      |
| 16 GB              | 1 GB                            | 15 GB                     |
| 24 GB              | 1.3 GB                          | 22.7 GB                   |

Tested on a fresh installation of ReviOS 10 22.01, in VirtualBox, on AMD Ryzen 5900X.

Credit to [Stasium#0001](https://stasium.dev/){target=_blank}.

---

## Which version do I need for FACEIT?

As of this moment (2022-05-20), FACEIT only works on the `10 22.05` and `11 22.04` versions. The `10 22.04` build is FACEIT compatible for a limited, although we do not support it anymore.

If you are using one of these versions, and still cannot use FACEIT, since the release of that version probably another update was released by Microsoft, which is required by FACEIT. A new build of ReviOS will be released soon. 

---

## Where are the older versions?

On the website, under [Archive Downloads](https://www.revi.cc/revios/download/archive-downloads){target=_blank}.

---

## How to install ReviOS?

The tutorial is [here](install.md).

---

## Can I install ReviOS on a MacBook?

Yes, you can. Follow [this guide](https://jensd.be/1011/windows/install-windows-10-on-a-macbook-air-2019-2020-with-t2-chip){target=_blank}, with the ReviOS iso of course.

---

## I cannot log into my user

This is happening, because of the connection of a Microsoft account to the local user. Right now the only fix is to reinstall your OS, and after you log into your Microsoft account set a PIN code too.

Other technique to evade the bug, is to log into your Microsoft account in the Microsoft Store. That way you will not be locked out and still can use your PC without a PIN code. Solution reported [here](https://discord.com/channels/619835916139364383/626772969611460619/944214984047616001){target=_blank}.

---

## Can I use Windows Update?

Not recommended, because **it will revert tweaks**, **reinstall bloatware** and cause setbacks with respect to privacy and other pre-applied features, might even **break your OS**.

In the latest versions, the Windows Update menu item from Settings was removed, due to users updating without reading the FAQ or asking.

If you still want to update, you can manually install updates with the help of [this guide](https://www.revi.cc/revios/workspace/updating){target=_blank} or reactivate the Windows Update menu item in settings with these steps:

1. Open `regedit`
2. Go to `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows\CurrentVersion\Policies\Explorer`
3. Remove `windowsupdate` and `windowsinsider` from `SettingsPageVisibility`
4. Restart

???+ warning
    ==**If you update, might as well just use stock Windows.**== Reasons explained above.

---

## How can I update to the newest version of ReviOS?

You need to reinstall. Do not forget to backup your data.

If you want to update because of FACEIT, make sure to check out [the section about it](#which-version-do-i-need-for-faceit).

---

## Can I use the Reset this PC feature?

It is probably not working, and even if it would work, using is not recommended , because it probably will disable tweaks and reinstall bloatware.

We recommend reinstalling ReviOS. Do not forget to backup your data.

---

## Valorant CFG error

Either [turn on Windows Defender](#where-is-windows-defender-can-i-use-it), and you can enable Control Flow Guard in Windows Security.

Or run this command in a PowerShell terminal (you may need to start the terminal in administrator mode):

```powershell 
Set-ProcessMitigation -Name vgc.exe -Enable CFG
```

If Vanguard still not working, you can try these two command: (you have to disable CFG to Discord, because it will crash)

```powershell
Set-ProcessMitigation -System -Enable CFG
Set-ProcessMitigation -Name Discord.exe -Disable CFG
```

---

## iTunes not detecting any Apple device

It is because ReviOS misses Apple driver, which you could download only by Windows Update, but that is still not recommended. Instead you can use [3uTools](http://www.3u.com/) to repair the drivers.

Once installed, after opening the software, go to:

1. `Toolbox`
2. `iTunes Utility`
3. `Repair Driver`
4. `Advanced Repair`

There select `Uninstall the old driver files stored in system`. After, iTunes should work.

Link to the original messages on Discord: [Message 1](https://discord.com/channels/619835916139364383/626772969611460619/930729137830789141) and [Message 2](https://discord.com/channels/619835916139364383/650007673626165261/973323621789491230)

---

## GPU and Network monitoring not working in the Task Manager

Yes, they were stripped because leaking memory.

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
        If this command fails, which is most likely to happen on 22.04 and older versions, download [this zip](https://cdn.discordapp.com/attachments/626772969611460619/953223235833589780/wscapi.zip){target=_blank}, and place the contents of it inside the System32 folder. [Link to the original message and conversation](https://discord.com/channels/619835916139364383/626772969611460619/953223236244619274)

If you do not see your GPU in the Performance tab in Task Manager, restart your PC again.


To reactivate Network statistics:

1. Open `regedit`
2. At `HKLM\System\CurrentControlSet\Services\Ndu` set `Start` to `2`
3. Restart

---

## AMD driver installation is crashing

It is a Windows 11 bug. Try running the installer in silent mode, with the `/S` flag. 
[Here](https://discord.com/channels/619835916139364383/626772969611460619/932975660392128562){target=_blank} is help and a script to automate it.

If this method is not working, install [Chocolatey](https://chocolatey.org/){target=_blank} and then the `amd-ryzen-chipset` package.

---

## Microsoft Store / Xbox app not working

Run `ctfmon` and `wsreset` commands.

If still not working, try `wsreset -i`.

If the login not working in the Xbox app, try these steps:

1. Open Microsoft Store
2. Click the 3 dots in the upper right corner of the window
3. Click Downloads and updates
4. Click Get updates
  
If you have updates, it should start installing them automatically.

If the updating is done, and Xbox login is still not working, go through these steps (tested on `22.01` and `22.02`):

1. Go to [https://store.rg-adguard.net/](https://store.rg-adguard.net/){target=_blank}
2. Change the search options from `URL (link)` to `PackageFamilyName` and `RP` to `Slow`, and search for `Microsoft.GamingApp_8wekyb3d8bbwe`
3. Download the following packages:
    1. `Microsoft.VCLibs.140.00_14.0.30704.0_x64__8wekyb3d8bbwe.appx`
    2. `Microsoft.VCLibs.140.00.UWPDesktop_14.0.30704.0_x64__8wekyb3d8bbwe.appx`
    3. `Microsoft.UI.Xaml.2.7_7.2203.17001.0_x64__8wekyb3d8bbwe.appx`
    4. `Microsoft.GamingApp_2203.1001.4.0_neutral_~_8wekyb3d8bbwe.msixbundle`
4. Go where you downloaded the files, ++shift+"Right-click"++ and choose `Open Powershell window here`
5. Run `Add-AppxPackage` with the downloaded files. E.g.: `Add-AppxPackage Microsoft.VCLibs.140.00_14.0.30704.0_x64__8wekyb3d8bbwe.appx`.

    **Make sure you install the packages in the order listed above.**

6. Restart

---

## Where is Windows Defender? Can I use it?

1. Go to `%userprofile%\Documents\Workspace\Windows Defender` folder. On `ReviOS 11 22.04` you can find this folder in `C:\Users\Public\Documents`. Copy it back to your user's Documents folder.
2. Run `Start.bat`
3. Press `1`
4. Restart

---

## Can I enable Superfetch / SysMain?

In older ReviOS versions it was stripped completely, but since ReviOS 10 22.05 it's only disabled.

If you want to enable it:

1. Go to `%userprofile%\Documents\Workspace\Revision-Tool` folder.
2. Run `Start.bat`
3. Restart


---

## How to change lock screen background?

1. Open `regedit`
2. Go to `HKEY_LOCAL_MACHINE\Software\Policies\Microsoft\Windows\Personalization`
3. Set the `NoLockScreen` key's value to `0`
4. Now you should be able to change it in Settings, if not, restart

---

## Internet icon bug

[Discord message link with instructions](https://discord.com/channels/619835916139364383/626772969611460619/800174514951684116){target=_blank}

[Zip file with the fix](https://cdn.discordapp.com/attachments/626772969611460619/800174514813665290/fix-network-icon.zip){target=_blank}

---

## Windows Update icon showed up on the taskbar and/or the "Update and shutdown/restart" option showed up

This is a bug in the `22.01` version, for now you can use [this fix](https://cdn.discordapp.com/attachments/626772969611460619/942019507730391050/Fix-Windows-Update-Taskbar.reg){target=_blank} for the taskbar icon. In the `22.02` version, it is already fixed.