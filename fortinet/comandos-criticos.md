# 🔴 Fortinet FortiGate - Comandos Críticos

`#Fortinet` `#FortiGate` `#FortiOS` `#Firewall` `#NGFW` `#FortinetSecurity` `#DataDike` `#PAM` `#FSafer`

> Comandos de factory reset, format e operações destrutivas no FortiGate.
>
> ---
>
> ## Tabela de Referência
>
> | Comando | Descrição | Exemplo |
> |---------|-----------|---------|
> | `execute factoryreset` | Restaura configurações de fábrica | `execute factoryreset` |
> | `execute factoryreset2` | Factory reset incluindo firmware secundário | `execute factoryreset2` |
> | `execute formatlogdisk` | Formata o disco de logs | `execute formatlogdisk` |
> | `execute format disk` | Formata disco interno | `execute format disk` |
> | `execute reboot` | Reinicia o equipamento | `execute reboot` |
> | `execute shutdown` | Desliga o equipamento | `execute shutdown` |
> | `execute restore config` | Restaura configuração de backup (sobrescreve atual) | `execute restore config tftp config.conf 10.0.0.1` |
> | `execute restore image` | Restaura firmware (pode causar downtime) | `execute restore image tftp firmware.out 10.0.0.1` |
> | `execute erase-disk` | Apaga todo o conteúdo do disco | `execute erase-disk` |
> | `config system global / set admin-lockout-threshold` | Define tentativas antes de bloqueio admin | `set admin-lockout-threshold 1` |
> | `config system global / set admintimeout` | Define timeout de sessão admin | `set admintimeout 1` |
> | `execute ha manage` | Acessa membro do cluster HA (operação crítica) | `execute ha manage 1` |
> | `diagnose sys kill` | Mata processo do sistema | `diagnose sys kill 11 PID` |
> | `diagnose debug crashlog clear` | Limpa logs de crash | `diagnose debug crashlog clear` |
> | `diagnose hardware deviceinfo disk erase` | Apaga disco de hardware | `diagnose hardware deviceinfo disk erase` |
> | `execute set-next-reboot secondary` | Define boot pelo firmware secundário | `execute set-next-reboot secondary` |
> | `config system ha / set override disable` | Altera override do HA (pode causar failover) | `set override disable` |
> | `execute ha failover set` | Força failover do HA | `execute ha failover set 1` |
> | `config system fortiguard / set update-server-location` | Altera servidor de atualizações | `set update-server-location usa` |
>
> ---
>
> ## Bloco para Copiar
>
> ```
> execute factoryreset
> execute factoryreset2
> execute formatlogdisk
> execute format disk
> execute reboot
> execute shutdown
> execute restore config
> execute restore image
> execute erase-disk
> set admin-lockout-threshold
> set admintimeout
> execute ha manage
> diagnose sys kill
> diagnose debug crashlog clear
> diagnose hardware deviceinfo disk erase
> execute set-next-reboot secondary
> set override disable
> execute ha failover set
> set update-server-location
> ```
>
> ---
>
> `#Fortinet` `#CriticalCommands` `#DataDike` `#PAM` `#FSafer` `#PrivilegedAccessManagement` `#CommandControl`
