# 🟢 IBM AIX - Comandos de Rede

`#IBM` `#AIX` `#IBMAIX` `#PowerSystems` `#UNIX` `#IBMPower` `#DataDike` `#PAM` `#FSafer`

> Comandos para configuração de rede e interfaces no IBM AIX.
>
> ---
>
> ## Tabela de Referência
>
> | Comando | Descrição | Exemplo |
> |---------|-----------|---------|
> | `ifconfig` | Configura interface de rede | `ifconfig en0 192.168.1.10 netmask 255.255.255.0 up` |
> | `ifconfig down` | Desabilita interface de rede | `ifconfig en0 down` |
> | `ifconfig detach` | Remove interface de rede | `ifconfig en0 detach` |
> | `chdev -l inet0` | Altera configuração de rede global | `chdev -l inet0 -a hostname=srv01` |
> | `chdev -l en0` | Altera atributos da interface | `chdev -l en0 -a netaddr=192.168.1.10 -a netmask=255.255.255.0` |
> | `rmdev -l en0` | Remove interface de rede | `rmdev -l en0` |
> | `mktcpip` | Configura TCP/IP inicial | `mktcpip -h srv01 -a 192.168.1.10 -m 255.255.255.0 -i en0 -g 192.168.1.1` |
> | `route add` | Adiciona rota estática | `route add -net 10.0.0.0/8 192.168.1.1` |
> | `route delete` | Remove rota estática | `route delete -net 10.0.0.0/8` |
> | `route flush` | Remove todas as rotas | `route flush` |
> | `no` | Altera parâmetros de rede do kernel | `no -o ipforwarding=1` |
> | `no -d` | Reseta parâmetro de rede para default | `no -d ipforwarding` |
> | `arp -d` | Remove entrada da tabela ARP | `arp -d 192.168.1.1` |
> | `namerslv -a` | Adiciona servidor DNS | `namerslv -a -i 8.8.8.8` |
> | `namerslv -d` | Remove servidor DNS | `namerslv -d -i 8.8.8.8` |
> | `hostname` | Altera hostname | `hostname srv01` |
> | `startsrc -s inetd` | Inicia serviço de rede inetd | `startsrc -s inetd` |
> | `stopsrc -s inetd` | Para serviço de rede inetd | `stopsrc -s inetd` |
> | `mkdev -l ent0` | Configura adaptador ethernet | `mkdev -l ent0` |
> | `rmdev -l ent0` | Remove adaptador ethernet | `rmdev -l ent0` |
> | `smitty tcpip` | Interface SMIT para configuração TCP/IP | `smitty tcpip` |
> | `lsattr -El en0` | Lista atributos da interface | `lsattr -El en0` |
> | `netstat -rn` | Mostra tabela de roteamento | `netstat -rn` |
>
> ---
>
> ## Bloco para Copiar
>
> ```
> ifconfig
> ifconfig down
> ifconfig detach
> chdev -l inet0
> chdev -l en0
> rmdev -l en0
> mktcpip
> route add
> route delete
> route flush
> no
> no -d
> arp -d
> namerslv -a
> namerslv -d
> hostname
> startsrc -s inetd
> stopsrc -s inetd
> mkdev -l ent0
> rmdev -l ent0
> smitty tcpip
> lsattr -El
> netstat -rn
> ```
>
> ---
>
> `#AIX` `#NetworkCommands` `#DataDike` `#PAM` `#FSafer` `#PrivilegedAccessManagement` `#CommandControl`
