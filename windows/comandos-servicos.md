# 🟣 Windows Server - Comandos de Serviços

`#Windows` `#WindowsServer` `#PowerShell` `#CMD` `#ActiveDirectory` `#Microsoft` `#DataDike` `#PAM` `#FSafer`

> Comandos para controle de serviços e processos no Windows Server.
>
> ---
>
> ## Tabela de Referência
>
> | Comando | Descrição | Exemplo |
> |---------|-----------|---------|
> | `net stop` | Para um serviço | `net stop "SQL Server (MSSQLSERVER)"` |
> | `net start` | Inicia um serviço | `net start W3SVC` |
> | `sc stop` | Para serviço via SC | `sc stop MSSQLSERVER` |
> | `sc start` | Inicia serviço via SC | `sc start MSSQLSERVER` |
> | `sc config start= disabled` | Desabilita serviço na inicialização | `sc config MSSQLSERVER start= disabled` |
> | `sc config start= auto` | Habilita serviço na inicialização | `sc config MSSQLSERVER start= auto` |
> | `sc delete` | Remove serviço permanentemente | `sc delete ServicoAntigo` |
> | `Stop-Service` | Para serviço (PowerShell) | `Stop-Service -Name W3SVC -Force` |
> | `Start-Service` | Inicia serviço (PowerShell) | `Start-Service -Name W3SVC` |
> | `Restart-Service` | Reinicia serviço (PowerShell) | `Restart-Service -Name W3SVC -Force` |
> | `Set-Service -StartupType Disabled` | Desabilita serviço (PowerShell) | `Set-Service -Name W3SVC -StartupType Disabled` |
> | `Set-Service -StartupType Automatic` | Habilita serviço (PowerShell) | `Set-Service -Name W3SVC -StartupType Automatic` |
> | `taskkill /F /IM` | Mata processo por nome | `taskkill /F /IM w3wp.exe` |
> | `taskkill /F /PID` | Mata processo por PID | `taskkill /F /PID 4567` |
> | `Stop-Process -Force` | Mata processo (PowerShell) | `Stop-Process -Name w3wp -Force` |
> | `Stop-Process -Id` | Mata processo por ID (PowerShell) | `Stop-Process -Id 4567 -Force` |
> | `schtasks /create` | Cria tarefa agendada | `schtasks /create /tn "Backup" /tr "backup.bat" /sc daily /st 02:00` |
> | `schtasks /delete` | Remove tarefa agendada | `schtasks /delete /tn "Backup" /f` |
> | `schtasks /change /disable` | Desabilita tarefa agendada | `schtasks /change /tn "Backup" /disable` |
> | `Register-ScheduledTask` | Cria tarefa agendada (PowerShell) | `Register-ScheduledTask -TaskName "Backup" -Action $action` |
> | `Unregister-ScheduledTask` | Remove tarefa agendada (PowerShell) | `Unregister-ScheduledTask -TaskName "Backup" -Confirm:$false` |
> | `iisreset /stop` | Para o IIS | `iisreset /stop` |
> | `iisreset /start` | Inicia o IIS | `iisreset /start` |
> | `iisreset /restart` | Reinicia o IIS | `iisreset /restart` |
> | `wmic service call stopservice` | Para serviço via WMIC | `wmic service where name="W3SVC" call stopservice` |
> | `Install-WindowsFeature` | Instala role/feature do Windows | `Install-WindowsFeature -Name Web-Server` |
>
> ---
>
> ## Bloco para Copiar
>
> ```
> net stop
> net start
> sc stop
> sc start
> sc config start= disabled
> sc config start= auto
> sc delete
> Stop-Service
> Start-Service
> Restart-Service
> Set-Service -StartupType Disabled
> Set-Service -StartupType Automatic
> taskkill /F /IM
> taskkill /F /PID
> Stop-Process -Force
> Stop-Process -Id
> schtasks /create
> schtasks /delete
> schtasks /change /disable
> Register-ScheduledTask
> Unregister-ScheduledTask
> iisreset /stop
> iisreset /start
> iisreset /restart
> wmic service call stopservice
> Install-WindowsFeature
> ```
>
> ---
>
> `#Windows` `#ServiceCommands` `#DataDike` `#PAM` `#FSafer` `#PrivilegedAccessManagement` `#CommandControl`
