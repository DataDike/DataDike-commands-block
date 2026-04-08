# 🟠 HP-UX (HPE) - Comandos de Rede

`#HPE` `#HPUX` `#HewlettPackardEnterprise` `#HPEServers` `#UNIX` `#DataDike` `#PAM` `#FSafer`

> Comandos para configuração de rede e interfaces no HP-UX.
>
> ---
>
> ## Tabela de Referência
>
> | Comando | Descrição | Exemplo |
> |---------|-----------|---------|
> | `ifconfig` | Configura interface de rede | `ifconfig lan0 192.168.1.10 netmask 255.255.255.0 up` |
> | `ifconfig down` | Desabilita interface de rede | `ifconfig lan0 down` |
> | `ifconfig unplumb` | Remove configuração da interface | `ifconfig lan0 unplumb` |
> | `set_parms ip_address` | Configura IP via set_parms | `set_parms ip_address` |
> | `set_parms hostname` | Altera hostname | `set_parms hostname` |
> | `set_parms addl_netwrk` | Configura rede adicional | `set_parms addl_netwrk` |
> | `route add default` | Adiciona rota padrão | `route add default 192.168.1.1` |
> | `route add` | Adiciona rota estática | `route add -net 10.0.0.0/8 192.168.1.1` |
> | `route delete` | Remove rota | `route delete default` |
> | `route flush` | Remove todas as rotas | `route flush` |
> | `ndd -set` | Altera parâmetros de rede do kernel | `ndd -set /dev/ip ip_forwarding 1` |
> | `ndd -get` | Consulta parâmetros de rede | `ndd -get /dev/ip ip_forwarding` |
> | `lanscan` | Lista adaptadores de rede | `lanscan` |
> | `linkloop` | Testa conectividade de link | `linkloop -i 0 0x080009ABCDEF` |
> | `lanadmin` | Administra adaptadores LAN | `lanadmin` |
> | `nwmgr` | Gerenciador de rede (11.31+) | `nwmgr` |
> | `arp -d` | Remove entrada ARP | `arp -d 192.168.1.1` |
> | `hostname` | Altera hostname do sistema | `hostname srv01` |
> | `nslookup` | Consulta DNS | `nslookup servidor.empresa.local` |
> | `sam` | Interface SAM para configuração de rede | `sam` |
> | `inetd -c` | Recarrega configuração do inetd | `inetd -c` |
>
> ---
>
> ## Bloco para Copiar
>
> ```
> ifconfig
> ifconfig down
> ifconfig unplumb
> set_parms ip_address
> set_parms hostname
> set_parms addl_netwrk
> route add default
> route add
> route delete
> route flush
> ndd -set
> ndd -get
> lanscan
> linkloop
> lanadmin
> nwmgr
> arp -d
> hostname
> nslookup
> sam
> inetd -c
> ```
>
> ---
>
> `#HPUX` `#NetworkCommands` `#DataDike` `#PAM` `#FSafer` `#PrivilegedAccessManagement` `#CommandControl`
