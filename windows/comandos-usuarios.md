# 🔵 Windows Server - Comandos de Usuários

`#Windows` `#WindowsServer` `#PowerShell` `#CMD` `#ActiveDirectory` `#Microsoft` `#DataDike` `#PAM` `#FSafer`

> Comandos para Active Directory e gestão de contas no Windows Server.
>
> ---
>
> ## Tabela de Referência
>
> | Comando | Descrição | Exemplo |
> |---------|-----------|---------|
> | `net user /add` | Cria usuário local | `net user joao Senh@123 /add` |
> | `net user /delete` | Remove usuário local | `net user joao /delete` |
> | `net user /active:no` | Desabilita conta de usuário | `net user joao /active:no` |
> | `net user /active:yes` | Habilita conta de usuário | `net user joao /active:yes` |
> | `net localgroup /add` | Adiciona usuário a grupo local | `net localgroup Administrators joao /add` |
> | `net localgroup /delete` | Remove usuário de grupo local | `net localgroup Administrators joao /delete` |
> | `New-ADUser` | Cria usuário no Active Directory | `New-ADUser -Name "Joao Silva" -SamAccountName joao -Enabled $true` |
> | `Remove-ADUser` | Remove usuário do AD | `Remove-ADUser -Identity joao -Confirm:$false` |
> | `Set-ADUser -Enabled $false` | Desabilita conta no AD | `Set-ADUser -Identity joao -Enabled $false` |
> | `Set-ADUser -Enabled $true` | Habilita conta no AD | `Set-ADUser -Identity joao -Enabled $true` |
> | `Unlock-ADAccount` | Desbloqueia conta no AD | `Unlock-ADAccount -Identity joao` |
> | `Set-ADAccountPassword` | Altera senha no AD | `Set-ADAccountPassword -Identity joao -Reset -NewPassword (ConvertTo-SecureString "NovaSenha" -AsPlainText -Force)` |
> | `Set-ADAccountExpiration` | Define expiração da conta | `Set-ADAccountExpiration -Identity joao -DateTime "12/31/2025"` |
> | `New-ADGroup` | Cria grupo no AD | `New-ADGroup -Name "Desenvolvedores" -GroupScope Global` |
> | `Remove-ADGroup` | Remove grupo do AD | `Remove-ADGroup -Identity "Desenvolvedores" -Confirm:$false` |
> | `Add-ADGroupMember` | Adiciona membro ao grupo AD | `Add-ADGroupMember -Identity "Desenvolvedores" -Members joao` |
> | `Remove-ADGroupMember` | Remove membro do grupo AD | `Remove-ADGroupMember -Identity "Desenvolvedores" -Members joao -Confirm:$false` |
> | `New-ADOrganizationalUnit` | Cria OU no AD | `New-ADOrganizationalUnit -Name "TI" -Path "DC=empresa,DC=local"` |
> | `Remove-ADOrganizationalUnit` | Remove OU do AD | `Remove-ADOrganizationalUnit -Identity "OU=TI,DC=empresa,DC=local" -Confirm:$false` |
> | `Move-ADObject` | Move objeto no AD (usuário, computador) | `Move-ADObject -Identity "CN=joao,OU=TI,DC=empresa,DC=local" -TargetPath "OU=RH,DC=empresa,DC=local"` |
> | `Set-ADUser -PasswordNeverExpires` | Define senha que nunca expira | `Set-ADUser -Identity joao -PasswordNeverExpires $true` |
> | `Disable-ADAccount` | Desabilita conta no AD | `Disable-ADAccount -Identity joao` |
> | `Enable-ADAccount` | Habilita conta no AD | `Enable-ADAccount -Identity joao` |
> | `New-LocalUser` | Cria usuário local (PowerShell) | `New-LocalUser -Name "joao" -Password (ConvertTo-SecureString "Senh@123" -AsPlainText -Force)` |
> | `Remove-LocalUser` | Remove usuário local (PowerShell) | `Remove-LocalUser -Name "joao"` |
> | `Add-LocalGroupMember` | Adiciona a grupo local (PowerShell) | `Add-LocalGroupMember -Group "Administrators" -Member "joao"` |
> | `Remove-LocalGroupMember` | Remove de grupo local (PowerShell) | `Remove-LocalGroupMember -Group "Administrators" -Member "joao"` |
> | `gpupdate /force` | Força atualização de políticas de grupo | `gpupdate /force` |
> | `dsmod user` | Modifica usuário no AD (legado) | `dsmod user "CN=joao,OU=TI,DC=empresa,DC=local" -disabled yes` |
>
> ---
>
> ## Bloco para Copiar
>
> ```
> net user /add
> net user /delete
> net user /active:no
> net user /active:yes
> net localgroup /add
> net localgroup /delete
> New-ADUser
> Remove-ADUser
> Set-ADUser -Enabled $false
> Set-ADUser -Enabled $true
> Unlock-ADAccount
> Set-ADAccountPassword
> Set-ADAccountExpiration
> New-ADGroup
> Remove-ADGroup
> Add-ADGroupMember
> Remove-ADGroupMember
> New-ADOrganizationalUnit
> Remove-ADOrganizationalUnit
> Move-ADObject
> Set-ADUser -PasswordNeverExpires
> Disable-ADAccount
> Enable-ADAccount
> New-LocalUser
> Remove-LocalUser
> Add-LocalGroupMember
> Remove-LocalGroupMember
> gpupdate /force
> dsmod user
> ```
>
> ---
>
> `#Windows` `#UserCommands` `#DataDike` `#PAM` `#FSafer` `#PrivilegedAccessManagement` `#CommandControl`
