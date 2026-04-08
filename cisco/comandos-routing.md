# 🟢 Cisco IOS / IOS-XE - Comandos de Routing

`#Cisco` `#CiscoIOS` `#CiscoIOSXE` `#CiscoRouter` `#CiscoSwitch` `#CiscoNetworking` `#DataDike` `#PAM` `#FSafer`

> Comandos para protocolos de roteamento e rotas no Cisco IOS/IOS-XE.
>
> ---
>
> ## Tabela de Referência
>
> | Comando | Descrição | Exemplo |
> |---------|-----------|---------|
> | `ip route` | Configura rota estática | `ip route 10.0.0.0 255.0.0.0 192.168.1.1` |
> | `no ip route` | Remove rota estática | `no ip route 10.0.0.0 255.0.0.0 192.168.1.1` |
> | `ip default-gateway` | Define gateway padrão (L2) | `ip default-gateway 192.168.1.1` |
> | `router ospf` | Inicia processo OSPF | `router ospf 1` |
> | `no router ospf` | Remove processo OSPF | `no router ospf 1` |
> | `network (OSPF)` | Anuncia rede no OSPF | `network 192.168.1.0 0.0.0.255 area 0` |
> | `router eigrp` | Inicia processo EIGRP | `router eigrp 100` |
> | `no router eigrp` | Remove processo EIGRP | `no router eigrp 100` |
> | `router bgp` | Inicia processo BGP | `router bgp 65000` |
> | `no router bgp` | Remove processo BGP | `no router bgp 65000` |
> | `neighbor (BGP)` | Configura vizinho BGP | `neighbor 10.0.0.2 remote-as 65001` |
> | `no neighbor` | Remove vizinho BGP | `no neighbor 10.0.0.2` |
> | `redistribute` | Redistribui rotas entre protocolos | `redistribute ospf 1 metric 1000 100 255 1 1500` |
> | `no redistribute` | Remove redistribuição de rotas | `no redistribute ospf 1` |
> | `clear ip ospf process` | Reinicia processo OSPF | `clear ip ospf process` |
> | `clear ip bgp *` | Reinicia todas as sessões BGP | `clear ip bgp *` |
> | `clear ip bgp neighbor` | Reinicia sessão BGP com vizinho | `clear ip bgp 10.0.0.2` |
> | `clear ip route *` | Limpa toda a tabela de roteamento | `clear ip route *` |
> | `ip routing` | Habilita roteamento IP | `ip routing` |
> | `no ip routing` | Desabilita roteamento IP | `no ip routing` |
> | `route-map` | Cria ou edita route-map | `route-map RM_FILTER permit 10` |
> | `no route-map` | Remove route-map | `no route-map RM_FILTER` |
> | `ip prefix-list` | Cria prefix-list para filtragem | `ip prefix-list PL_FILTER seq 5 permit 10.0.0.0/8` |
> | `no ip prefix-list` | Remove prefix-list | `no ip prefix-list PL_FILTER` |
> | `passive-interface` | Define interface como passiva | `passive-interface GigabitEthernet0/0` |
> | `default-information originate` | Anuncia rota default no OSPF | `default-information originate` |
>
> ---
>
> ## Bloco para Copiar
>
> ```
> ip route
> no ip route
> ip default-gateway
> router ospf
> no router ospf
> network
> router eigrp
> no router eigrp
> router bgp
> no router bgp
> neighbor
> no neighbor
> redistribute
> no redistribute
> clear ip ospf process
> clear ip bgp *
> clear ip bgp
> clear ip route *
> ip routing
> no ip routing
> route-map
> no route-map
> ip prefix-list
> no ip prefix-list
> passive-interface
> default-information originate
> ```
>
> ---
>
> `#Cisco` `#RoutingCommands` `#DataDike` `#PAM` `#FSafer` `#PrivilegedAccessManagement` `#CommandControl`
