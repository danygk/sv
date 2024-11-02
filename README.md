run this code in powershell to download 

Invoke-WebRequest -Uri "https://github.com/danygk/sv/raw/main/sv.exe" -OutFile "$([System.Environment]::GetFolderPath('Desktop'))\sv.exe"

