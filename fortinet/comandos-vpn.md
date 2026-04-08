# 🟢 Fortinet FortiGate - Comandos de VPN

`#Fortinet` `#FortiGate` `#FortiOS` `#Firewall` `#NGFW` `#FortinetSecurity` `#DataDike` `#PAM` `#FSafer`

> Comandos para configuração e gestão de VPNs no FortiGate.
>
> ---
>
> ## Tabela de Referência
>
> | Comando | Descrição | Exemplo |
> |---------|-----------|---------|
> | `config vpn ipsec phase1-interface / delete` | Remove túnel IPSec fase 1 | `delete tunel_matriz` |
> | `config vpn ipsec phase2-interface / delete` | Remove túnel IPSec fase 2 | `delete tunel_matriz_p2` |
> | `config vpn ipsec phase1-interface / edit` | Edita ou cria túnel IPSec fase 1 | `edit tunel_filial` |
> | `config vpn ipsec phase2-interface / edit` | Edita ou cria túnel IPSec fase 2 | `edit tunel_filial_p2` |
> | `config vpn ssl settings / set status disable` | Desabilita VPN SSL | `set status disable` |
> | `config vpn ssl settings / set port` | Altera porta do VPN SSL | `set port 10443` |
> | `config vpn ssl settings / set source-interface` | Altera interface de origem do SSL VPN | `set source-interface port1` |
> | `config vpn ssl web portal / delete` | Remove portal web SSL VPN | `delete portal_usuarios` |
> | `config vpn ssl web portal / edit` | Edita portal web SSL VPN | `edit portal_usuarios` |
> | `config vpn ssl web user-group-bookmark / delete` | Remove bookmarks de grupo | `delete grp_vpn` |
> | `config user group / delete` | Remove grupo de usuários VPN | `delete grp_vpn_ssl` |
> | `config user local / delete` | Remove usuário local VPN | `delete usuario_vpn` |
> | `config user ldap / delete` | Remove servidor LDAP para VPN | `delete ldap_ad` |
> | `config user radius / delete` | Remove servidor RADIUS | `delete radius_auth` |
> | `diagnose vpn ike gateway flush` | Limpa todas as negociações IKE | `diagnose vpn ike gateway flush` |
> | `diagnose vpn tunnel flush` | Limpa todos os túneis VPN ativos | `diagnose vpn tunnel flush` |
> | `diagnose vpn ike gateway clear` | Limpa gateway IKE específico | `diagnose vpn ike gateway clear name tunel_matriz` |
> | `config vpn ipsec phase1-interface / set status disable` | Desabilita túnel IPSec | `set status disable` |
> | `execute vpn sslvpn del-tunnel` | Remove túnel SSL VPN ativo | `execute vpn sslvpn del-tunnel usuario1` |
> | `config vpn ipsec phase1-interface / set dpd disable` | Desabilita Dead Peer Detection | `set dpd disable` |
>
> ---
>
> ## Bloco para Copiar
>
> ```
> config vpn ipsec phase1-interface delete
> config vpn ipsec phase2-interface delete
> config vpn ipsec phase1-interface edit
> config vpn ipsec phase2-interface edit
> config vpn ssl settings set status disable
> config vpn ssl settings set port
> config vpn ssl settings set source-interface
> config vpn ssl web portal delete
> config vpn ssl web portal edit
> config vpn ssl web user-group-bookmark delete
> config user group delete
> config user local delete
> config user ldap delete
> config user radius delete
> diagnose vpn ike gateway flush
> diagnose vpn tunnel flush
> diagnose vpn ike gateway clear
> config vpn ipsec phase1-interface set status disable
> execute vpn sslvpn del-tunnel
> config vpn ipsec phase1-interface set dpd disable
> ```
>
> ---
>
> `#Fortinet` `#VPNCommands` `#DataDike` `#PAM` `#FSafer` `#PrivilegedAccessManagement` `#CommandControl`
