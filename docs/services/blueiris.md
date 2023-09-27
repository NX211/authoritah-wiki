# Blue Iris

## Enable Automatic Login

Windows + R  `regedit`

Navigate to `Computer\HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\WindowsNT\CurrentVersion\Winlogon`

### Create new Registry Keys

`Edit > New > String Value`

```bash
DefaultUserName = $BLUEIRIS_USERNAME
DefaultPassword = $BLUEIRIS_USER_PASSWORD
AutoAdminLogon = 1
```

## Turn off User Access Control

Control Panel > User Account > User Access Control

## Create PowerShell Script

```powershell
C:\Users\blueiris\plusiris.ps1

Start-Sleep -s 15
Start-Process "C:\Program Files\Blue Iris 5\BlueIris.exe"
```

## Create Batch file to Autorun Blue Iris

Create blueiris.cmd file in  Startup folder using Windows + R  `shell:startup`

```powershell
PowerShell -Command "Set-ExecutionPolicy Unrestricted" >> "C:\Windows\Temp\StartupLog.txt" 2>%1
PowerShell "C:\Users\blueiris\plusiris.ps1" >> "C:\Windows\Temp\StartupLog.txt" 2>%1
```
