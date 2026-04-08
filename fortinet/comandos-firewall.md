# 🟠 Fortinet FortiGate - Comandos de Firewall

`#Fortinet` `#FortiGate` `#FortiOS` `#Firewall` `#NGFW` `#FortinetSecurity` `#DataDike` `#PAM` `#FSafer`

> Comandos para políticas, regras e objetos de firewall no FortiGate.
>
> ---
>
> ## Tabela de Referência
>
> | Comando | Descrição | Exemplo |
> |---------|-----------|---------|
> | `config firewall policy / delete` | Remove política de firewall | `delete 10` |
> | `config firewall policy / edit` | Edita ou cria política de firewall | `edit 10` |
> | `config firewall policy / set action deny` | Define ação da política como negar | `set action deny` |
> | `config firewall policy / set action accept` | Define ação da política como permitir | `set action accept` |
> | `config firewall policy / set status disable` | Desabilita política de firewall | `set status disable` |
> | `config firewall policy / purge` | Remove todas as políticas de firewall | `purge` |
> | `config firewall address / delete` | Remove objeto de endereço | `delete addr_servidor` |
> | `config firewall address / edit` | Edita ou cria objeto de endereço | `edit addr_servidor` |
> | `config firewall addrgrp / delete` | Remove grupo de endereços | `delete grp_servidores` |
> | `config firewall service custom / delete` | Remove serviço customizado | `delete svc_app` |
> | `config firewall service group / delete` | Remove grupo de serviços | `delete grp_servicos` |
> | `config firewall schedule onetime / delete` | Remove agendamento | `delete sched_manutencao` |
> | `config firewall ippool / delete` | Remove IP pool de NAT | `delete pool_nat` |
> | `config firewall vip / delete` | Remove Virtual IP (DNAT) | `delete vip_webserver` |
> | `config firewall vip / edit` | Edita ou cria Virtual IP | `edit vip_webserver` |
> | `config firewall central-snat-map / delete` | Remove regra de SNAT central | `delete 1` |
> | `config firewall shaper traffic-shaper / delete` | Remove traffic shaper | `delete shaper_limite` |
> | `config firewall DoS-policy / delete` | Remove política de DoS | `delete 1` |
> | `config firewall multicast-policy / delete` | Remove política de multicast | `delete 1` |
> | `config firewall ssl-ssh-profile / delete` | Remove perfil de inspeção SSL | `delete perfil_ssl` |
> | `config firewall profile-protocol-options / delete` | Remove perfil de opções de protocolo | `delete perfil_proto` |
>
> ---
>
> ## Bloco para Copiar
>
> ```
> config firewall policy delete
> config firewall policy edit
> config firewall policy set action deny
> config firewall policy set action accept
> config firewall policy set status disable
> config firewall policy purge
> config firewall address delete
> config firewall address edit
> config firewall addrgrp delete
> config firewall service custom delete
> config firewall service group delete
> config firewall schedule onetime delete
> config firewall ippool delete
> config firewall vip delete
> config firewall vip edit
> config firewall central-snat-map delete
> config firewall shaper traffic-shaper delete
> config firewall DoS-policy delete
> config firewall multicast-policy delete
> config firewall ssl-ssh-profile delete
> config firewall profile-protocol-options delete
> ```
>
> ---
>
> `#Fortinet` `#FirewallCommands` `#DataDike` `#PAM` `#FSafer` `#PrivilegedAccessManagement` `#CommandControl`
