# NoGaurdian
A advanced bypass for the school management extension GoGaurdian.

<a href="https://example.com">
  <button style="background-color: #4CAF50; border: none; color: white; padding: 10px 20px; text-align: center; text-decoration: none; display: inline-block; margin: 4px 2px; cursor: pointer;">Advanced bypass technology</button>
</a>


HOW TO BYPASS?

1. Open notepad
<img src="https://www.startpage.com/av/proxy-image?piurl=https%3A%2F%2Fthurrott-assets.nyc3.digitaloceanspaces.com%2Fweb%2Fwp-content%2Fuploads%2Fsites%2F2%2F2021%2F12%2F09181515%2Fnotepad-hero-cropped.jpg&amp;sp=1763590461T12c74a681beb02be98d02713716ffa6ec13a84636a5913cc3a70a6cf91ace6a7" alt="Hands-On with the Redesigned Notepad for Windows 11 - Thurrott.com"/><img width="1066" height="599" alt="image" src="https://github.com/user-attachments/assets/d1525c13-70b9-488b-907b-e3c4396088c4" />

2. Paste this code into notepad:
@echo off

REM Disable Group Policy for Microsoft Edge
reg add "HKLM\SOFTWARE\Policies\Microsoft\Edge" /v "BrowserManagementPolicy" /t REG_DWORD /d 0 /f
reg add "HKLM\SOFTWARE\Policies\Microsoft\Edge" /v "DefaultPopupsSetting" /t REG_DWORD /d 1 /f
reg add "HKLM\SOFTWARE\Policies\Microsoft\Edge" /v "HomepageIsNewTabPage" /t REG_DWORD /d 0 /f
reg add "HKLM\SOFTWARE\Policies\Microsoft\Edge" /v "DefaultBrowserSettingEnabled" /t REG_DWORD /d 0 /f
reg add "HKLM\SOFTWARE\Policies\Microsoft\Edge" /v "RestoreOnStartup" /t REG_DWORD /d 4 /f
reg add "HKLM\SOFTWARE\Policies\Microsoft\Edge" /v "DisableDeveloperModeExtensions" /t REG_DWORD /d 0 /f
reg add "HKLM\SOFTWARE\Policies\Microsoft\Edge" /v "DisableSafeBrowsing" /t REG_DWORD /d 0 /f

REM Disable Managed Mode
reg delete "HKLM\SOFTWARE\Policies\Microsoft\Edge" /v "ManagedMode" /f

REM Delete existing extensions
del /q "%LOCALAPPDATA%\Microsoft\Edge\User Data\Default\Extensions\*"
del /q "%LOCALAPPDATA%\Microsoft\Edge\User Data\Profile 1\Extensions\*"

REM Remove from allow list (without admin privileges)
reg delete "HKCU\Software\Classes\*\shell\open\command" /v "(Default)" /f
reg delete "HKCU\Software\Classes\Directory\shell\open\command" /v "(Default)" /f
reg delete "HKCU\Software\Classes\Directory\Background\shell\open\command" /v "(Default)" /f
reg delete "HKCU\Software\Classes\Drive\shell\open\command" /v "(Default)" /f

REM Disable additional security features
reg add "HKCU\Software\Microsoft\Windows\CurrentVersion\Explorer\Advanced" /v "Start_TrackProgs" /t REG_DWORD /d 0 /f
reg add "HKCU\Software\Microsoft\Windows\CurrentVersion\Explorer\Advanced" /v "EnableBalloonTips" /t REG_DWORD /d 0 /f

REM Restart Edge to apply changes
taskkill /F /IM msedge.exe
start msedge.exe

echo Organization control for Microsoft Edge has been disabled and extensions removed.
pause
<script>
function copyToClipboard(text) {
  const tempInput = document.createElement('textarea');
  tempInput.value = text;
  document.body.appendChild(tempInput);
  tempInput.select();
  document.execCommand('copy');
  document.body.removeChild(tempInput);
}
</script>

<button onclick="copyToClipboard('@echo off

REM Disable Group Policy for Microsoft Edge
reg add "HKLM\SOFTWARE\Policies\Microsoft\Edge" /v "BrowserManagementPolicy" /t REG_DWORD /d 0 /f
reg add "HKLM\SOFTWARE\Policies\Microsoft\Edge" /v "DefaultPopupsSetting" /t REG_DWORD /d 1 /f
reg add "HKLM\SOFTWARE\Policies\Microsoft\Edge" /v "HomepageIsNewTabPage" /t REG_DWORD /d 0 /f
reg add "HKLM\SOFTWARE\Policies\Microsoft\Edge" /v "DefaultBrowserSettingEnabled" /t REG_DWORD /d 0 /f
reg add "HKLM\SOFTWARE\Policies\Microsoft\Edge" /v "RestoreOnStartup" /t REG_DWORD /d 4 /f
reg add "HKLM\SOFTWARE\Policies\Microsoft\Edge" /v "DisableDeveloperModeExtensions" /t REG_DWORD /d 0 /f
reg add "HKLM\SOFTWARE\Policies\Microsoft\Edge" /v "DisableSafeBrowsing" /t REG_DWORD /d 0 /f

REM Disable Managed Mode
reg delete "HKLM\SOFTWARE\Policies\Microsoft\Edge" /v "ManagedMode" /f

REM Delete existing extensions
del /q "%LOCALAPPDATA%\Microsoft\Edge\User Data\Default\Extensions\*"
del /q "%LOCALAPPDATA%\Microsoft\Edge\User Data\Profile 1\Extensions\*"

REM Remove from allow list (without admin privileges)
reg delete "HKCU\Software\Classes\*\shell\open\command" /v "(Default)" /f
reg delete "HKCU\Software\Classes\Directory\shell\open\command" /v "(Default)" /f
reg delete "HKCU\Software\Classes\Directory\Background\shell\open\command" /v "(Default)" /f
reg delete "HKCU\Software\Classes\Drive\shell\open\command" /v "(Default)" /f

REM Disable additional security features
reg add "HKCU\Software\Microsoft\Windows\CurrentVersion\Explorer\Advanced" /v "Start_TrackProgs" /t REG_DWORD /d 0 /f
reg add "HKCU\Software\Microsoft\Windows\CurrentVersion\Explorer\Advanced" /v "EnableBalloonTips" /t REG_DWORD /d 0 /f

REM Restart Edge to apply changes
taskkill /F /IM msedge.exe
start msedge.exe

echo Organization control for Microsoft Edge has been disabled and extensions removed.
pause')">Copy Text</button>
