# 🟠 Windows Server - Comandos de Rede

`#Windows` `#WindowsServer` `#PowerShell` `#CMD` `#ActiveDirectory` `#Microsoft` `#DataDike` `#PAM` `#FSafer`

> Comandos para configuração de rede e firewall no Windows Server.
>
> ---
>
> ## Tabela de Referência
>
> | Comando | Descrição | Exemplo |
> |---------|-----------|---------|
> | `netsh interface set interface disable` | Desabilita interface de rede | `netsh interface set interface "Ethernet" disable` |
> | `netsh interface ip set address` | Configura IP estático | `netsh interface ip set address "Ethernet" static 192.168.1.10 255.255.255.0 192.168.1.1` |
> | `netsh interface ip set dns` | Configura servidor DNS | `netsh interface ip set dns "Ethernet" static 8.8.8.8` |
> | `netsh interface ip delete address` | Remove endereço IP | `netsh interface ip delete address "Ethernet" 192.168.1.10` |
> | `netsh advfirewall set allprofiles state off` | Desabilita firewall em todos os perfis | `netsh advfirewall set allprofiles state off` |
> | `netsh advfirewall reset` | Restaura firewall para configuração padrão | `netsh advfirewall reset` |
> | `netsh advfirewall firewall add rule` | Adiciona regra de firewall | `netsh advfirewall firewall add rule name="Bloquear" dir=in action=block` |
> | `netsh advfirewall firewall delete rule` | Remove regra de firewall | `netsh advfirewall firewall delete rule name="Regra1"` |
> | `Set-NetFirewallProfile -Enabled False` | Desabilita firewall via PowerShell | `Set-NetFirewallProfile -Profile Domain,Public,Private -Enabled False` |
> | `New-NetFirewallRule` | Cria regra de firewall (PowerShell) | `New-NetFirewallRule -DisplayName "Block" -Direction Inbound -Action Block` |
> | `Remove-NetFirewallRule` | Remove regra de firewall (PowerShell) | `Remove-NetFirewallRule -DisplayName "Block"` |
> | `Disable-NetAdapter` | Desabilita adaptador de rede | `Disable-NetAdapter -Name "Ethernet" -Confirm:$false` |
> | `Enable-NetAdapter` | Habilita adaptador de rede | `Enable-NetAdapter -Name "Ethernet"` |
> | `Remove-NetIPAddress` | Remove endereço IP (PowerShell) | `Remove-NetIPAddress -InterfaceAlias "Ethernet" -IPAddress 192.168.1.10` |
> | `Remove-NetRoute` | Remove rota de rede | `Remove-NetRoute -InterfaceAlias "Ethernet" -DestinationPrefix 0.0.0.0/0` |
> | `New-NetRoute` | Adiciona rota estática | `New-NetRoute -DestinationPrefix 10.0.0.0/8 -InterfaceAlias "Ethernet" -NextHop 192.168.1.1` |
> | `route delete` | Remove rota (CMD) | `route delete 10.0.0.0` |
> | `route add` | Adiciona rota (CMD) | `route add 10.0.0.0 mask 255.0.0.0 192.168.1.1` |
> | `ipconfig /release` | Libera endereço IP DHCP | `ipconfig /release` |
> | `ipconfig /flushdns` | Limpa cache DNS | `ipconfig /flushdns` |
> | `nbtstat -R` | Limpa cache NetBIOS | `nbtstat -R` |
> | `arp -d *` | Limpa tabela ARP | `arp -d *` |
> | `netsh winsock reset` | Reseta catálogo Winsock | `netsh winsock reset` |
> | `netsh int ip reset` | Reseta pilha TCP/IP | `netsh int ip reset` |
> | `Rename-Computer` | Renomeia o computador | `Rename-Computer -NewName "SRV-WEB01" -Restart` |
>
> ---
>
> ## Bloco para Copiar
>
> ```
> netsh interface set interface disable
> netsh interface ip set address
> netsh interface ip set dns
> netsh interface ip delete address
> netsh advfirewall set allprofiles state off
> netsh advfirewall reset
> netsh advfirewall firewall add rule
> netsh advfirewall firewall delete rule
> Set-NetFirewallProfile -Enabled False
> New-NetFirewallRule
> Remove-NetFirewallRule
> Disable-NetAdapter
> Enable-NetAdapter
> Remove-NetIPAddress
> Remove-NetRoute
> New-NetRoute
> route delete
> route add
> ipconfig /release
> ipconfig /flushdns
> nbtstat -R
> arp -d *
> netsh winsock reset
> netsh int ip reset
> Rename-Computer
> ```
>
> ---
>
> `#Windows` `#NetworkCommands` `#DataDike` `#PAM` `#FSafer` `#PrivilegedAccessManagement` `#CommandControl`
