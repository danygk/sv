run this code in powershell to download 

Invoke-WebRequest -Uri "https://github.com/danygk/sv/raw/main/nw.exe" -OutFile "$([System.Environment]::GetFolderPath('Desktop'))\nw.exe"

