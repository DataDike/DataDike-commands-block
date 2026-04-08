# 🟣 Fortinet FortiGate - Comandos de Sistema

`#Fortinet` `#FortiGate` `#FortiOS` `#Firewall` `#NGFW` `#FortinetSecurity` `#DataDike` `#PAM` `#FSafer`

> Comandos para configurações globais e administrativas do FortiGate.
>
> ---
>
> ## Tabela de Referência
>
> | Comando | Descrição | Exemplo |
> |---------|-----------|---------|
> | `config system global / set hostname` | Altera hostname do equipamento | `set hostname FGT-MATRIZ` |
> | `config system global / set timezone` | Altera fuso horário | `set timezone 12` |
> | `config system global / set admin-sport` | Altera porta HTTPS de administração | `set admin-sport 8443` |
> | `config system global / set admin-ssh-port` | Altera porta SSH de administração | `set admin-ssh-port 2222` |
> | `config system global / set admin-server-cert` | Altera certificado do servidor admin | `set admin-server-cert Fortinet_Factory` |
> | `config system interface / edit` | Edita interface de rede | `edit port1` |
> | `config system interface / set ip` | Define IP da interface | `set ip 192.168.1.1/24` |
> | `config system interface / set allowaccess` | Define acessos permitidos na interface | `set allowaccess ping https ssh` |
> | `config system interface / set status down` | Desabilita interface | `set status down` |
> | `config system dns / set primary` | Altera DNS primário | `set primary 8.8.8.8` |
> | `config system ntp / set ntpsync disable` | Desabilita sincronização NTP | `set ntpsync disable` |
> | `config system admin / delete` | Remove administrador | `delete admin_temp` |
> | `config system admin / edit` | Edita ou cria administrador | `edit admin_novo` |
> | `config system admin / set password` | Altera senha de administrador | `set password Nova_Senha_123` |
> | `config system admin / set accprofile` | Altera perfil de acesso do admin | `set accprofile super_admin` |
> | `config system accprofile / delete` | Remove perfil de acesso | `delete perfil_leitura` |
> | `config system snmp community / delete` | Remove comunidade SNMP | `delete 1` |
> | `config system syslogd / set status disable` | Desabilita envio de syslog | `set status disable` |
> | `config log memory setting / set status disable` | Desabilita log em memória | `set status disable` |
> | `config log disk setting / set status disable` | Desabilita log em disco | `set status disable` |
> | `config system replacemsg / delete` | Remove mensagem de substituição | `delete utm` |
> | `config router static / delete` | Remove rota estática | `delete 1` |
> | `config router static / edit` | Edita ou cria rota estática | `edit 1` |
> | `config system dhcp server / delete` | Remove servidor DHCP | `delete 1` |
> | `execute backup config` | Exporta configuração (operação sensível) | `execute backup config tftp config.conf 10.0.0.1` |
> | `config system ha / set mode standalone` | Remove equipamento do cluster HA | `set mode standalone` |
>
> ---
>
> ## Bloco para Copiar
>
> ```
> config system global set hostname
> config system global set timezone
> config system global set admin-sport
> config system global set admin-ssh-port
> config system global set admin-server-cert
> config system interface edit
> config system interface set ip
> config system interface set allowaccess
> config system interface set status down
> config system dns set primary
> config system ntp set ntpsync disable
> config system admin delete
> config system admin edit
> config system admin set password
> config system admin set accprofile
> config system accprofile delete
> config system snmp community delete
> config system syslogd set status disable
> config log memory setting set status disable
> config log disk setting set status disable
> config system replacemsg delete
> config router static delete
> config router static edit
> config system dhcp server delete
> execute backup config
> config system ha set mode standalone
> ```
>
> ---
>
> `#Fortinet` `#SystemCommands` `#DataDike` `#PAM` `#FSafer` `#PrivilegedAccessManagement` `#CommandControl`
