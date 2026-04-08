# 🔴 Windows Server - Comandos Críticos

`#Windows` `#WindowsServer` `#PowerShell` `#CMD` `#ActiveDirectory` `#Microsoft` `#DataDike` `#PAM` `#FSafer`

> Comandos de format, diskpart e operações destrutivas no Windows Server.
>
> ---
>
> ## Tabela de Referência
>
> | Comando | Descrição | Exemplo |
> |---------|-----------|---------|
> | `format` | Formata volume/partição | `format D: /FS:NTFS /Q` |
> | `diskpart / clean` | Remove todas as partições do disco | `select disk 0` + `clean` |
> | `diskpart / clean all` | Remove partições e sobrescreve com zeros | `select disk 0` + `clean all` |
> | `diskpart / delete partition` | Remove partição específica | `select partition 1` + `delete partition override` |
> | `diskpart / delete volume` | Remove volume específico | `select volume 1` + `delete volume` |
> | `shutdown /s /f /t 0` | Desliga servidor imediatamente | `shutdown /s /f /t 0` |
> | `shutdown /r /f /t 0` | Reinicia servidor imediatamente | `shutdown /r /f /t 0` |
> | `Stop-Computer -Force` | Desliga servidor via PowerShell | `Stop-Computer -Force` |
> | `Restart-Computer -Force` | Reinicia servidor via PowerShell | `Restart-Computer -Force` |
> | `bcdedit` | Edita dados de configuração de boot | `bcdedit /set {default} recoveryenabled No` |
> | `bcdedit /deletevalue` | Remove valor de boot | `bcdedit /deletevalue {default} safeboot` |
> | `sfc /scannow` | Verifica e repara arquivos do sistema | `sfc /scannow` |
> | `DISM /Online /Cleanup-Image` | Repara imagem do Windows | `DISM /Online /Cleanup-Image /RestoreHealth` |
> | `cipher /w` | Sobrescreve espaço livre (irrecuperável) | `cipher /w:D:` |
> | `reg delete` | Remove chave do registro | `reg delete HKLM\SOFTWARE\Chave /f` |
> | `regedit /s` | Importa arquivo .reg silenciosamente | `regedit /s config.reg` |
> | `wmic os set` | Altera configurações do SO via WMIC | `wmic os set enabledisable=false` |
> | `taskkill /F /IM` | Mata processo forçadamente | `taskkill /F /IM sqlservr.exe` |
> | `taskkill /F /PID` | Mata processo por PID | `taskkill /F /PID 1234` |
> | `Stop-Process -Force` | Mata processo via PowerShell | `Stop-Process -Name sqlservr -Force` |
> | `Clear-EventLog` | Limpa logs de eventos | `Clear-EventLog -LogName System` |
> | `wevtutil cl` | Limpa log de eventos específico | `wevtutil cl Security` |
> | `w32tm /config` | Altera configuração de tempo (NTP) | `w32tm /config /manualpeerlist:"time.nist.gov"` |
>
> ---
>
> ## Bloco para Copiar
>
> ```
> format
> diskpart clean
> diskpart clean all
> diskpart delete partition
> diskpart delete volume
> shutdown /s /f /t 0
> shutdown /r /f /t 0
> Stop-Computer -Force
> Restart-Computer -Force
> bcdedit
> bcdedit /deletevalue
> sfc /scannow
> DISM /Online /Cleanup-Image
> cipher /w
> reg delete
> regedit /s
> wmic os set
> taskkill /F /IM
> taskkill /F /PID
> Stop-Process -Force
> Clear-EventLog
> wevtutil cl
> w32tm /config
> ```
>
> ---
>
> `#Windows` `#CriticalCommands` `#DataDike` `#PAM` `#FSafer` `#PrivilegedAccessManagement` `#CommandControl`
