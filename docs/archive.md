---
hide:
  - navigation
---

<style>
    div.admonition p:not(.admonition-title) {
        font-size: 125%;
    }
    .center {
        display: block;
        margin-left: auto;
        margin-right: auto;
    }
</style>

# Archived questions

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
        If this command fails, which is most likely to happen on 22.04 and older builds, download [this zip](files/wscapi.zip), and place the contents of it inside the System32 folder. [Link to the original message and conversation on our Discord](https://discord.com/channels/619835916139364383/626772969611460619/953223236244619274){target=_blank}

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

## I cannot log into my user

*Update:*

In ReviOS 22.07 (Windows 10 and 11) and above this problem is resolved. Even if you do not set a password at installation, and evade setting a PIN code when logging into your Microsoft account, at the login screen a window will pop up, and after logging in again with your MS account, you have to set a PIN code.

The PIN code forcing can be disabled in `Settings` -> `Accounts` -> `Sign-in options` with `For improved security, only allow Windows Hello sign-in for Microsoft accounts on this device (Recommended)` after loggin in with your MS account and setting a PIN code. Then you can delete the PIN code, if you want to.

*Previously:*

This is happening, because of the connection of a Microsoft account to the local user. Right now the only fix is to reinstall your OS, and after you log into your Microsoft account set a PIN code too.

Other technique to evade the bug, is to log into your Microsoft account in the Microsoft Store. That way you will not be locked out and still can use your PC without a PIN code. Partial solution reported with [this message on our Discord](https://discord.com/channels/619835916139364383/626772969611460619/944214984047616001){target=_blank}.

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

## Apps taking long time to load on ReviOS

Run this command using **PowerShell in administrator mode**:

```powershell
reg add "HKLM\SOFTWARE\Microsoft\Windows NT\CurrentVersion\Image File Execution Options\smartscreen.exe" /v "Debugger" /t REG_SZ /d "%windir%\System32\taskkill.exe" /f
```

---

## Explorer.exe crashing on ReviOS 11

Open a PowerShell window as administrator, and run this command:

```powershell
Add-AppxPackage -Register -Path C:\Windows\SystemApps\Microsoft.UI.Xaml.CBS_8wekyb3d8bbwe\AppxManifest.xml -DisableDevelopmentMode -ForceApplicationShutdown
```

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

## Cannot toggle Start Menu folders in Settings

If you cannot toggle on Start Menu folders in Settings -> Personalization -> Start -> Folders:

1. Open `regedit`
2. Go to `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\PolicyManager\current\device\Start` 
3. Delete every key **except** `ConfigureStartPins`

---

## There are some visual bugs on the taskbar in ReviOS 11

These bugs came from Windows 11, hope they will be fixed in next Microsoft update releases.

In the meantime, try [StartAllBack](https://www.startallback.com/){target=_blank}.


---

## AMD driver installation is crashing

It is a Windows 11 bug. Try running the installer in silent mode, with the `/S` flag. [This message on our Discord](https://discord.com/channels/619835916139364383/626772969611460619/932975660392128562){target=_blank} helps with this issue by automatizing it.

If this method is not working, install [Chocolatey](https://chocolatey.org/){target=_blank} and then the `amd-ryzen-chipset` package.

---

## Internet icon bug

[Discord message link with instructions](https://discord.com/channels/619835916139364383/626772969611460619/800174514951684116){target=_blank}

[Zip file with the fix](files/fix-network-icon.zip)

---

## Windows Update icon on the taskbar and/or the "Update and shutdown/restart" option showed up

This was a bug in the `22.01` builds, for now you can use [this fix](files/Fix-Windows-Update-Taskbar.reg){target=_blank} for the taskbar icon. The issue is already fixed in newer ReviOS builds.