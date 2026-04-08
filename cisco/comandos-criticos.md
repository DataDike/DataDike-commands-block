# 🔴 Cisco IOS / IOS-XE - Comandos Críticos

`#Cisco` `#CiscoIOS` `#CiscoIOSXE` `#CiscoRouter` `#CiscoSwitch` `#CiscoNetworking` `#DataDike` `#PAM` `#FSafer`

> Comandos de erase, reload e operações destrutivas no Cisco IOS/IOS-XE.
>
> ---
>
> ## Tabela de Referência
>
> | Comando | Descrição | Exemplo |
> |---------|-----------|---------|
> | `erase startup-config` | Apaga configuração de inicialização | `erase startup-config` |
> | `erase running-config` | Apaga configuração em execução | `erase running-config` |
> | `erase nvram:` | Apaga conteúdo da NVRAM | `erase nvram:` |
> | `erase flash:` | Apaga conteúdo da flash | `erase flash:` |
> | `write erase` | Apaga startup-config (alias) | `write erase` |
> | `reload` | Reinicia o equipamento | `reload` |
> | `reload in` | Agenda reinicialização | `reload in 5` |
> | `delete flash:` | Remove arquivo da flash | `delete flash:vlan.dat` |
> | `format flash:` | Formata a memória flash | `format flash:` |
> | `copy running-config startup-config` | Salva configuração (pode sobrescrever) | `copy running-config startup-config` |
> | `configure replace` | Substitui configuração completa | `configure replace flash:backup.cfg force` |
> | `config-register` | Altera registro de configuração do boot | `config-register 0x2142` |
> | `boot system` | Altera imagem de boot | `boot system flash:c2960-lanbasek9-mz.150-2.SE11.bin` |
> | `license boot module` | Altera licença de boot | `license boot module c2900 technology-package securityk9` |
> | `rommon` | Acessa modo ROMMON (operação crítica) | `reload` + `Ctrl+Break` |
> | `squeeze flash:` | Comprime flash removendo espaços vazios | `squeeze flash:` |
> | `no service password-encryption` | Desabilita criptografia de senhas | `no service password-encryption` |
> | `no enable secret` | Remove senha de enable | `no enable secret` |
> | `no enable password` | Remove senha enable legada | `no enable password` |
> | `clear counters` | Limpa contadores de interfaces | `clear counters` |
> | `clear logging` | Limpa buffer de logs | `clear logging` |
> | `clear crypto sa` | Limpa SAs criptográficas (derruba VPN) | `clear crypto sa` |
> | `clear crypto isakmp` | Limpa sessões ISAKMP | `clear crypto isakmp` |
>
> ---
>
> ## Bloco para Copiar
>
> ```
> erase startup-config
> erase running-config
> erase nvram:
> erase flash:
> write erase
> reload
> reload in
> delete flash:
> format flash:
> copy running-config startup-config
> configure replace
> config-register
> boot system
> license boot module
> squeeze flash:
> no service password-encryption
> no enable secret
> no enable password
> clear counters
> clear logging
> clear crypto sa
> clear crypto isakmp
> ```
>
> ---
>
> `#Cisco` `#CriticalCommands` `#DataDike` `#PAM` `#FSafer` `#PrivilegedAccessManagement` `#CommandControl`
