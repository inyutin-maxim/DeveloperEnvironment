# Настройка рабочего окружения

Для настройки рабочего окружения выполните в `Powershell` следующие команды:

```powershell
Set-ExecutionPolicy Bypass -Scope Process -Force; Invoke-Expression ((New-Object System.Net.WebClient).DownloadString('https://chocolatey.org/install.ps1'))

choco feature enable -n allowGlobalConfirmation

# Development
cinst dotnetcore-sdk netfx-4.7.1-devpack git tortoisegit docker-for-windows docker-compose nuget.commandline nugetpackageexplorer vscode nodejs postman docfx heidisql cygwin -y
cinst visualstudio2017buildtools --package-parameters "--allWorkloads --includeRecommended --includeOptional --passive --locale ru-RU" -y
cinst visualstudio2017-workload-netcoretools --package-parameters "--productId Microsoft.VisualStudio.Product.Community --channelId VisualStudio.15.Release --includeRecommended --includeOptional --passive --locale ru-RU" -y
cinst visualstudio2017-workload-netweb --package-parameters "--productId Microsoft.VisualStudio.Product.Community --channelId VisualStudio.15.Release --includeRecommended --includeOptional --passive --locale ru-RU" -y
# JetBrains
cinst resharper-clt jetbrainstoolbox -y
# Other
cinst openvpn skype googlechrome 7zip putty teamviewer aimp windjview telegram onedrive -y

# Docker
docker pull microsoft/mssql-server-windows-developer
# docker pull microsoft/mssql-server-linux
docker pull sebp/elk
docker pull jetbrains/teamcity-server
docker pull microsoft/aspnetcore
docker pull microsoft/aspnetcore-build
```
