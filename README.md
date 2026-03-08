# 🪟 Windows Fix Commands You Must Know

> **Essential CMD & PowerShell Commands for Troubleshooting Windows**  
> A comprehensive reference guide covering system repair, networking, security, disk management, and more.

---

## 📋 Table of Contents

- [System Repair & Health](#-system-repair--health)
- [Network Troubleshooting](#-network-troubleshooting)
- [Disk & File Management](#-disk--file-management)
- [Boot & Startup Repair](#-boot--startup-repair)
- [User & Account Management](#-user--account-management)
- [System Configuration & Services](#-system-configuration--services)
- [Windows Update & Activation](#-windows-update--activation)
- [Security & Firewall](#-security--firewall)
- [PowerShell Admin Tools](#-powershell-admin-tools)
- [Misc & Utilities](#-misc--utilities)

---

## 🔧 System Repair & Health

| Command | Description |
|---------|-------------|
| `sfc /scannow` | Scan and repair system files |
| `DISM /Online /Cleanup-Image /RestoreHealth` | Repair Windows image |
| `chkdsk C: /f /r` | Check and repair disk errors |
| `systeminfo` | Display system information |
| `ver` | Show Windows version |
| `shutdown /r /f /t 0` | Force restart |
| `shutdown /s /f /t 0` | Force shutdown |
| `powercfg /energy` | Generate energy report |
| `powercfg /batteryreport` | Battery health report |
| `cleanmgr` | Open Disk Cleanup |

---

## 🌐 Network Troubleshooting

| Command | Description |
|---------|-------------|
| `ipconfig /all` | Display all IP info |
| `ipconfig /release` | Release IP address |
| `ipconfig /renew` | Renew IP address |
| `ipconfig /flushdns` | Clear DNS cache |
| `netsh winsock reset` | Reset Winsock |
| `netsh int ip reset` | Reset TCP/IP |
| `ping 8.8.8.8` | Test internet connection |
| `tracert google.com` | Trace route |
| `nslookup google.com` | DNS lookup |
| `netstat -an` | List all network connections |
| `route print` | Display routing table |
| `arp -a` | Display ARP cache |
| `netsh wlan show profile` | Show WiFi profiles |
| `netsh wlan delete profile name=profile` | Delete WiFi profile |
| `netsh wlan export profile key=clear` | Export WiFi keys |
| `netsh interface show interface` | Show network interfaces |
| `netsh advfirewall reset` | Reset firewall rules |
| `net stop dhcp` | Stop DHCP service |
| `net start dhcp` | Start DHCP service |
| `netsh firewall show state` | Show firewall state |

---

## 💾 Disk & File Management

| Command | Description |
|---------|-------------|
| `diskmgmt.msc` | Open Disk Management |
| `defrag C:` | Defragment disk |
| `format D: /fs:ntfs` | Format drive D |
| `robocopy source destination /E` | Copy files with structure |
| `xcopy source destination /E /H /C /I` | Copy directories |
| `del /f /s /q C:\Windows\Temp\*.*` | Delete temp files |
| `rmdir /s /q foldername` | Delete folder |
| `attrib -h -r -s /s /d *.*` | Remove hidden attributes |
| `fsutil dirty query C:` | Check dirty bit |
| `sdelete -p 3 filename` | Securely delete file |

---

## 🚀 Boot & Startup Repair

| Command | Description |
|---------|-------------|
| `bcdedit /enum all` | Display boot entries |
| `bootrec /fixmbr` | Repair MBR |
| `bootrec /fixboot` | Repair boot sector |
| `bootrec /scanos` | Scan installations |
| `bootrec /rebuildbcd` | Rebuild boot configuration |
| `bcdboot C:\Windows` | Recreate boot files |
| `reagentc /enable` | Enable recovery environment |
| `bcdedit /set {default} safeboot minimal` | Safe mode boot |
| `bcdedit /deletevalue {default} safeboot` | Exit safe mode |
| `srttrail.txt` | View startup repair log |

---

## 👤 User & Account Management

| Command | Description |
|---------|-------------|
| `net user` | List users |
| `net user username password /add` | Add user |
| `net localgroup administrators username /add` | Make admin |
| `net user username /delete` | Delete user |
| `net user administrator /active:yes` | Enable admin |
| `net user administrator /active:no` | Disable admin |
| `control userpasswords2` | Advanced account settings |
| `lusrmgr.msc` | Local Users and Groups |
| `whoami /groups` | Display user groups |
| `rundll32.exe user32.dll,LockWorkStation` | Lock PC |
| `net accounts /minpwlen:8` | Set minimum password length |
| `net accounts /maxpwage:30` | Set password expiry |

---

## ⚙️ System Configuration & Services

| Command | Description |
|---------|-------------|
| `msconfig` | System configuration |
| `services.msc` | Manage services |
| `taskmgr` | Task Manager |
| `eventvwr` | Event Viewer |
| `perfmon` | Performance Monitor |
| `resmon` | Resource Monitor |
| `gpedit.msc` | Group Policy Editor |
| `secpol.msc` | Local Security Policy |
| `compmgmt.msc` | Computer Management |
| `sysdm.cpl` | System Properties |

---

## 🔄 Windows Update & Activation

| Command | Description |
|---------|-------------|
| `wuauclt /detectnow` | Force update check |
| `wuauclt /updatenow` | Start updates |
| `usoclient startscan` | Scan for updates |
| `usoclient startinstall` | Install updates |
| `control update` | Open Windows Update |
| `slmgr /ipk XXXXX-XXXXX-XXXXX-XXXXX-XXXXX` | Install key |
| `slmgr /ato` | Activate Windows |
| `slmgr /xpr` | Check activation status |
| `slmgr /rearm` | Reset activation timer |
| `sc query wuauserv` | Check update service status |

---

## 🔒 Security & Firewall

| Command | Description |
|---------|-------------|
| `wf.msc` | Windows Firewall settings |
| `netsh advfirewall show allprofiles` | Show firewall profiles |
| `netsh advfirewall set allprofiles state off` | Disable firewall |
| `netsh advfirewall set allprofiles state on` | Enable firewall |
| `rstrui` | System Restore |
| `WindowsDefender:` | Open Windows Security |
| `explorer ms-settings:windowsdefender` | Defender settings |

---

## 💻 PowerShell Admin Tools

| Command | Description |
|---------|-------------|
| `Get-EventLog -LogName System -Newest 20` | Show latest 20 system logs |
| `Get-Service \| Where-Object {$_.Status -eq 'Running'}` | Show running services |
| `Restart-Service Spooler` | Restart print spooler |
| `Stop-Process -Name notepad` | Stop Notepad process |
| `Get-Process \| Sort CPU -Descending \| Select -First 10` | Show top CPU processes |
| `Get-Disk` | Show disks |
| `Get-NetAdapter` | Show network adapters |
| `Test-Connection google.com` | Test connectivity |
| `Get-WindowsFeature` | List Windows features |
| `Restart-Computer -Force` | Force restart computer |
| `Get-ChildItem Env:` | Show environment variables |
| `Get-Command *network*` | Find network commands |
| `Get-Help Get-Process` | Show help for Get-Process |
| `Set-ExecutionPolicy RemoteSigned` | Allow local scripts |
| `Get-WmiObject Win32_OperatingSystem` | Show OS info |
| `Get-HotFix` | List installed updates |
| `Get-LocalUser` | List local users |
| `Enable-LocalUser -Name Administrator` | Enable Administrator |
| `Disable-LocalUser -Name Guest` | Disable Guest account |
| `Get-ComputerInfo` | Show full computer info |

---

## 🛠️ Misc & Utilities

| Command | Description |
|---------|-------------|
| `calc` | Calculator |
| `notepad` | Notepad |
| `mspaint` | Paint |
| `osk` | On-screen keyboard |
| `magnify` | Magnifier |
| `snippingtool` | Snipping Tool |
| `write` | WordPad |
| `control printers` | Printers folder |
| `hdwwiz.cpl` | Add Hardware Wizard |
| `timedate.cpl` | Date and Time settings |
| `ncpa.cpl` | Network connections |
| `inetcpl.cpl` | Internet options |
| `main.cpl` | Mouse settings |
| `desk.cpl` | Display settings |
| `appwiz.cpl` | Programs and Features |
| `joy.cpl` | Game controllers |

---

## 🚦 Quick Tips

> 💡 **Run as Administrator** — Most repair and system commands require elevated privileges. Right-click CMD or PowerShell and select **"Run as administrator"**.

> 💡 **CMD vs PowerShell** — Commands starting with capital verbs (e.g., `Get-`, `Set-`, `Stop-`) are PowerShell cmdlets. All others are typically CMD commands.

> 💡 **Safe Mode** — Use `bcdedit /set {default} safeboot minimal` to boot into Safe Mode for advanced troubleshooting. Always undo with `bcdedit /deletevalue {default} safeboot` afterward.

> ⚠️ **Warning** — Commands like `format`, `del`, `rmdir`, and firewall disablement are destructive or security-sensitive. Use with caution.

---

## 📂 Categories at a Glance

```
Windows Fix Commands
├── System Repair & Health      (10 commands)
├── Network Troubleshooting     (20 commands)
├── Disk & File Management      (10 commands)
├── Boot & Startup Repair       (10 commands)
├── User & Account Management   (12 commands)
├── System Config & Services    (10 commands)
├── Windows Update & Activation (10 commands)
├── Security & Firewall          (7 commands)
├── PowerShell Admin Tools      (20 commands)
└── Misc & Utilities            (16 commands)
```

---

## 📄 License

This reference guide is provided for educational and professional IT use. Feel free to fork, star ⭐, and share.

---

*Maintained with ❤️ for IT professionals, sysadmins, and Windows power users.*
