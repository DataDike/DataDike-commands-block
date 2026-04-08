# 🟡 Windows Server - Comandos de Exclusão

`#Windows` `#WindowsServer` `#PowerShell` `#CMD` `#ActiveDirectory` `#Microsoft` `#DataDike` `#PAM` `#FSafer`

> Comandos Remove-Item, del e remoção de dados no Windows Server.
>
> ---
>
> ## Tabela de Referência
>
> | Comando | Descrição | Exemplo |
> |---------|-----------|---------|
> | `del` | Remove arquivos (CMD) | `del C:\temp\arquivo.txt` |
> | `del /F /Q` | Remove arquivos forçadamente sem confirmação | `del /F /Q C:\temp\*.log` |
> | `del /S /Q` | Remove arquivos recursivamente | `del /S /Q C:\temp\*.*` |
> | `rmdir /S /Q` | Remove diretório e conteúdo sem confirmação | `rmdir /S /Q C:\temp\pasta` |
> | `rd /S /Q` | Remove diretório recursivamente (alias) | `rd /S /Q C:\backup\antigo` |
> | `Remove-Item` | Remove arquivos/diretórios (PowerShell) | `Remove-Item C:\temp\arquivo.txt` |
> | `Remove-Item -Recurse -Force` | Remove recursivamente e forçadamente | `Remove-Item -Path C:\temp\* -Recurse -Force` |
> | `Remove-Item -Filter` | Remove arquivos por filtro | `Remove-Item -Path C:\logs\* -Filter *.log` |
> | `Clear-Content` | Limpa conteúdo de arquivo sem removê-lo | `Clear-Content C:\logs\app.log` |
> | `Clear-RecycleBin` | Esvazia lixeira | `Clear-RecycleBin -Force` |
> | `erase` | Remove arquivos (alias de del) | `erase C:\temp\*.tmp` |
> | `Get-ChildItem ... Remove-Item` | Lista e remove por critério | `Get-ChildItem C:\logs -Recurse -Filter *.gz \| Remove-Item` |
> | `Remove-ItemProperty` | Remove propriedade de item (registro) | `Remove-ItemProperty -Path "HKLM:\SOFTWARE\App" -Name "Config"` |
> | `Uninstall-WindowsFeature` | Remove feature/role do Windows | `Uninstall-WindowsFeature -Name Web-Server` |
> | `Remove-WindowsFeature` | Remove recurso do Windows (alias) | `Remove-WindowsFeature DHCP` |
> | `wmic product uninstall` | Desinstala programa via WMIC | `wmic product where name="App" call uninstall` |
> | `msiexec /x` | Desinstala programa via MSI | `msiexec /x {GUID} /quiet` |
> | `Remove-Printer` | Remove impressora | `Remove-Printer -Name "Impressora1"` |
> | `Remove-PSDrive` | Remove drive mapeado (PowerShell) | `Remove-PSDrive -Name Z` |
> | `net use /delete` | Remove mapeamento de rede | `net use Z: /delete` |
> | `Remove-SmbShare` | Remove compartilhamento SMB | `Remove-SmbShare -Name "Share1" -Force` |
> | `icacls /remove` | Remove permissões de arquivo/pasta | `icacls C:\dados /remove usuario` |
>
> ---
>
> ## Bloco para Copiar
>
> ```
> del
> del /F /Q
> del /S /Q
> rmdir /S /Q
> rd /S /Q
> Remove-Item
> Remove-Item -Recurse -Force
> Remove-Item -Filter
> Clear-Content
> Clear-RecycleBin
> erase
> Get-ChildItem Remove-Item
> Remove-ItemProperty
> Uninstall-WindowsFeature
> Remove-WindowsFeature
> wmic product uninstall
> msiexec /x
> Remove-Printer
> Remove-PSDrive
> net use /delete
> Remove-SmbShare
> icacls /remove
> ```
>
> ---
>
> `#Windows` `#DeletionCommands` `#DataDike` `#PAM` `#FSafer` `#PrivilegedAccessManagement` `#CommandControl`
