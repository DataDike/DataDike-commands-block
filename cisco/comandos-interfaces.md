# 🟠 Cisco IOS / IOS-XE - Comandos de Interfaces

`#Cisco` `#CiscoIOS` `#CiscoIOSXE` `#CiscoRouter` `#CiscoSwitch` `#CiscoNetworking` `#DataDike` `#PAM` `#FSafer`

> Comandos para configuração e shutdown de interfaces no Cisco IOS/IOS-XE.
>
> ---
>
> ## Tabela de Referência
>
> | Comando | Descrição | Exemplo |
> |---------|-----------|---------|
> | `shutdown` | Desabilita interface | `interface GigabitEthernet0/1` + `shutdown` |
> | `no shutdown` | Habilita interface | `interface GigabitEthernet0/1` + `no shutdown` |
> | `ip address` | Configura endereço IP na interface | `ip address 192.168.1.1 255.255.255.0` |
> | `no ip address` | Remove endereço IP da interface | `no ip address` |
> | `description` | Define descrição da interface | `description Link WAN Matriz` |
> | `speed` | Define velocidade da interface | `speed 100` |
> | `duplex` | Define modo duplex | `duplex full` |
> | `switchport mode access` | Configura porta como access | `switchport mode access` |
> | `switchport mode trunk` | Configura porta como trunk | `switchport mode trunk` |
> | `switchport access vlan` | Associa porta a VLAN de acesso | `switchport access vlan 10` |
> | `switchport trunk allowed vlan` | Define VLANs permitidas no trunk | `switchport trunk allowed vlan 10,20,30` |
> | `switchport trunk native vlan` | Define VLAN nativa do trunk | `switchport trunk native vlan 99` |
> | `no switchport` | Remove configuração Layer 2 (torna L3) | `no switchport` |
> | `channel-group` | Associa interface a port-channel | `channel-group 1 mode active` |
> | `no channel-group` | Remove interface do port-channel | `no channel-group 1` |
> | `interface range` | Configura range de interfaces | `interface range GigabitEthernet0/1-24` |
> | `vlan` | Cria VLAN | `vlan 100` |
> | `no vlan` | Remove VLAN | `no vlan 100` |
> | `spanning-tree portfast` | Habilita PortFast na porta | `spanning-tree portfast` |
> | `spanning-tree vlan priority` | Altera prioridade STP da VLAN | `spanning-tree vlan 1 priority 4096` |
> | `ip proxy-arp` | Habilita proxy ARP | `ip proxy-arp` |
> | `no ip proxy-arp` | Desabilita proxy ARP | `no ip proxy-arp` |
> | `bandwidth` | Define bandwidth para cálculos de roteamento | `bandwidth 1000000` |
> | `mtu` | Altera MTU da interface | `mtu 9000` |
> | `encapsulation dot1Q` | Define encapsulamento 802.1Q em subinterface | `encapsulation dot1Q 10` |
>
> ---
>
> ## Bloco para Copiar
>
> ```
> shutdown
> no shutdown
> ip address
> no ip address
> description
> speed
> duplex
> switchport mode access
> switchport mode trunk
> switchport access vlan
> switchport trunk allowed vlan
> switchport trunk native vlan
> no switchport
> channel-group
> no channel-group
> interface range
> vlan
> no vlan
> spanning-tree portfast
> spanning-tree vlan priority
> ip proxy-arp
> no ip proxy-arp
> bandwidth
> mtu
> encapsulation dot1Q
> ```
>
> ---
>
> `#Cisco` `#InterfaceCommands` `#DataDike` `#PAM` `#FSafer` `#PrivilegedAccessManagement` `#CommandControl`
