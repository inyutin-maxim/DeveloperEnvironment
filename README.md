# Настройка рабочего окружения

Для настройки рабочего окружения выполните в `Powershell` следующие команды:

```powershell
Set-ExecutionPolicy Bypass -Scope Process -Force; Invoke-Expression ((New-Object System.Net.WebClient).DownloadString('https://chocolatey.org/install.ps1'))

choco feature enable -n allowGlobalConfirmation

# Development
cinst dotnetcore-sdk dotnetfx git tortoisegit docker-for-windows docker-compose nuget.commandline nugetpackageexplorer vscode nodejs postman docfx heidisql
# cinst visualstudio2017buildtools --package-parameters "--locale ru-RU" -y
# cinst visualstudio2017-workload-netweb --package-parameters "--productId Microsoft.VisualStudio.Product.Community --channelId VisualStudio.15.Release --includeRecommended --includeOptional --passive --locale ru-RU" -y
cinst sql-server-express
# JetBrains
cinst resharper-clt jetbrainstoolbox -y
# Other
cinst openvpn skype googlechrome 7zip putty teamviewer aimp windjview telegram.portable onedrive notepadplusplus.install libreoffice-fresh thunderbird adobereader

git config --global core.autocrlf true
git config --global core.safecrlf true

# Docker
# docker pull microsoft/mssql-server-windows-developer
# docker pull microsoft/mssql-server-linux
# docker pull sebp/elk
# docker pull jetbrains/teamcity-server
# docker pull microsoft/aspnetcore
# docker pull microsoft/aspnetcore-build
```


# Дополнительную информацию и примеры можно найти [здесь](https://github.com/Microsoft/windows-dev-box-setup-scripts)
