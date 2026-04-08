**[English](#english)** | **[Português](#português)** | **[Español](#español)**

---

# English

# Linux - Network Commands

`#Linux` `#Ubuntu` `#RedHat` `#RHEL` `#CentOS` `#Debian` `#SUSE` `#Bash` `#Shell` `#DataDike` `#PAM` `#FSafer`

> Commands for network configuration and manipulation that can affect connectivity and security.
>
> ---
>
> ## Reference Table
>
> | Command | Description | Example |
> |---------|-------------|---------|
> | `ifconfig` | Configures or disables network interfaces | `ifconfig eth0 down` |
> | `ip link set down` | Disables network interface | `ip link set eth0 down` |
> | `ip addr flush` | Removes all IP addresses from an interface | `ip addr flush dev eth0` |
> | `ip route flush` | Removes all routes from routing table | `ip route flush table main` |
> | `ip route del` | Removes a specific route | `ip route del default` |
> | `ip route add` | Adds static route | `ip route add 10.0.0.0/8 via 192.168.1.1` |
> | `iptables -F` | Flushes all firewall rules | `iptables -F` |
> | `iptables -X` | Removes all custom chains | `iptables -X` |
> | `iptables -P INPUT DROP` | Sets default policy to DROP (blocks everything) | `iptables -P INPUT DROP` |
> | `iptables -P OUTPUT DROP` | Blocks all outbound traffic | `iptables -P OUTPUT DROP` |
> | `iptables -P FORWARD DROP` | Blocks all packet forwarding | `iptables -P FORWARD DROP` |
> | `nft flush ruleset` | Flushes all nftables rules | `nft flush ruleset` |
> | `firewall-cmd --panic-on` | Activates panic mode on firewalld (blocks everything) | `firewall-cmd --panic-on` |
> | `ufw disable` | Disables UFW firewall | `ufw disable` |
> | `route del default` | Removes default route | `route del default` |
> | `route add` | Adds static route (legacy) | `route add -net 10.0.0.0/8 gw 192.168.1.1` |
> | `nmcli con down` | Deactivates network connection | `nmcli con down "Wired connection 1"` |
> | `nmcli networking off` | Disables all networking via NetworkManager | `nmcli networking off` |
> | `hostnamectl set-hostname` | Changes system hostname | `hostnamectl set-hostname novo-host` |
> | `ethtool -s speed` | Changes network interface speed | `ethtool -s eth0 speed 100` |
> | `brctl delbr` | Removes a network bridge | `brctl delbr br0` |
> | `vconfig rem` | Removes VLAN interface | `vconfig rem eth0.100` |
> | `tc qdisc add` | Adds traffic control (can cause slowness) | `tc qdisc add dev eth0 root netem delay 100ms` |
> | `ss -K` | Kills specific socket connections | `ss -K dst 10.0.0.1` |
> | `arp -d` | Removes ARP table entry | `arp -d 192.168.1.1` |
>
> ## Copy Block
>
> ```
> ifconfig
> ip link set down
> ip addr flush
> ip route flush
> ip route del
> ip route add
> iptables -F
> iptables -X
> iptables -P INPUT DROP
> iptables -P OUTPUT DROP
> iptables -P FORWARD DROP
> nft flush ruleset
> firewall-cmd --panic-on
> ufw disable
> route del default
> route add
> nmcli con down
> nmcli networking off
> hostnamectl set-hostname
> ethtool -s
> brctl delbr
> vconfig rem
> tc qdisc add
> ss -K
> arp -d
> ```
>
> ---
>
> # Português
>
> # Linux - Comandos de Rede
>
> `#Linux` `#Ubuntu` `#RedHat` `#RHEL` `#CentOS` `#Debian` `#SUSE` `#Bash` `#Shell` `#DataDike` `#PAM` `#FSafer`
>
> > Comandos para configuração e manipulação de rede que podem afetar conectividade e segurança.
> >
> > ---
> >
> > ## Tabela de Referência
> >
> > | Comando | Descrição | Exemplo |
> > |---------|-----------|---------|
> > | `ifconfig` | Configura ou desabilita interfaces de rede | `ifconfig eth0 down` |
> > | `ip link set down` | Desabilita interface de rede | `ip link set eth0 down` |
> > | `ip addr flush` | Remove todos os endereços IP de uma interface | `ip addr flush dev eth0` |
> > | `ip route flush` | Remove todas as rotas da tabela de roteamento | `ip route flush table main` |
> > | `ip route del` | Remove uma rota específica | `ip route del default` |
> > | `ip route add` | Adiciona rota estática | `ip route add 10.0.0.0/8 via 192.168.1.1` |
> > | `iptables -F` | Limpa todas as regras do firewall | `iptables -F` |
> > | `iptables -X` | Remove todas as chains customizadas | `iptables -X` |
> > | `iptables -P INPUT DROP` | Define política padrão para DROP (bloqueia tudo) | `iptables -P INPUT DROP` |
> > | `iptables -P OUTPUT DROP` | Bloqueia todo tráfego de saída | `iptables -P OUTPUT DROP` |
> > | `iptables -P FORWARD DROP` | Bloqueia todo encaminhamento de pacotes | `iptables -P FORWARD DROP` |
> > | `nft flush ruleset` | Limpa todas as regras do nftables | `nft flush ruleset` |
> > | `firewall-cmd --panic-on` | Ativa modo pânico no firewalld (bloqueia tudo) | `firewall-cmd --panic-on` |
> > | `ufw disable` | Desabilita o firewall UFW | `ufw disable` |
> > | `route del default` | Remove a rota padrão | `route del default` |
> > | `route add` | Adiciona rota estática (legado) | `route add -net 10.0.0.0/8 gw 192.168.1.1` |
> > | `nmcli con down` | Desativa conexão de rede | `nmcli con down "Wired connection 1"` |
> > | `nmcli networking off` | Desabilita toda a rede via NetworkManager | `nmcli networking off` |
> > | `hostnamectl set-hostname` | Altera o hostname do sistema | `hostnamectl set-hostname novo-host` |
> > | `ethtool -s speed` | Altera velocidade da interface de rede | `ethtool -s eth0 speed 100` |
> > | `brctl delbr` | Remove uma bridge de rede | `brctl delbr br0` |
> > | `vconfig rem` | Remove interface VLAN | `vconfig rem eth0.100` |
> > | `tc qdisc add` | Adiciona controle de tráfego (pode causar lentidão) | `tc qdisc add dev eth0 root netem delay 100ms` |
> > | `ss -K` | Mata conexões de socket específicas | `ss -K dst 10.0.0.1` |
> > | `arp -d` | Remove entrada da tabela ARP | `arp -d 192.168.1.1` |
> >
> > ## Bloco para Copiar
> >
> > ```
> > ifconfig
> > ip link set down
> > ip addr flush
> > ip route flush
> > ip route del
> > ip route add
> > iptables -F
> > iptables -X
> > iptables -P INPUT DROP
> > iptables -P OUTPUT DROP
> > iptables -P FORWARD DROP
> > nft flush ruleset
> > firewall-cmd --panic-on
> > ufw disable
> > route del default
> > route add
> > nmcli con down
> > nmcli networking off
> > hostnamectl set-hostname
> > ethtool -s
> > brctl delbr
> > vconfig rem
> > tc qdisc add
> > ss -K
> > arp -d
> > ```
> >
> > ---
> >
> > # Español
> >
> > # Linux - Comandos de Red
> >
> > `#Linux` `#Ubuntu` `#RedHat` `#RHEL` `#CentOS` `#Debian` `#SUSE` `#Bash` `#Shell` `#DataDike` `#PAM` `#FSafer`
> >
> > > Comandos para configuración y manipulación de red que pueden afectar conectividad y seguridad.
> > >
> > > ---
> > >
> > > ## Tabla de Referencia
> > >
> > > | Comando | Descripción | Ejemplo |
> > > |---------|-------------|---------|
> > > | `ifconfig` | Configura o deshabilita interfaces de red | `ifconfig eth0 down` |
> > > | `ip link set down` | Deshabilita interfaz de red | `ip link set eth0 down` |
> > > | `ip addr flush` | Elimina todas las direcciones IP de una interfaz | `ip addr flush dev eth0` |
> > > | `ip route flush` | Elimina todas las rutas de la tabla de enrutamiento | `ip route flush table main` |
> > > | `ip route del` | Elimina una ruta específica | `ip route del default` |
> > > | `ip route add` | Agrega ruta estática | `ip route add 10.0.0.0/8 via 192.168.1.1` |
> > > | `iptables -F` | Limpia todas las reglas del firewall | `iptables -F` |
> > > | `iptables -X` | Elimina todas las chains personalizadas | `iptables -X` |
> > > | `iptables -P INPUT DROP` | Define política predeterminada a DROP (bloquea todo) | `iptables -P INPUT DROP` |
> > > | `iptables -P OUTPUT DROP` | Bloquea todo el tráfico de salida | `iptables -P OUTPUT DROP` |
> > > | `iptables -P FORWARD DROP` | Bloquea todo el reenvío de paquetes | `iptables -P FORWARD DROP` |
> > > | `nft flush ruleset` | Limpia todas las reglas de nftables | `nft flush ruleset` |
> > > | `firewall-cmd --panic-on` | Activa modo pánico en firewalld (bloquea todo) | `firewall-cmd --panic-on` |
> > > | `ufw disable` | Deshabilita el firewall UFW | `ufw disable` |
> > > | `route del default` | Elimina la ruta predeterminada | `route del default` |
> > > | `route add` | Agrega ruta estática (legado) | `route add -net 10.0.0.0/8 gw 192.168.1.1` |
> > > | `nmcli con down` | Desactiva conexión de red | `nmcli con down "Wired connection 1"` |
> > > | `nmcli networking off` | Deshabilita toda la red vía NetworkManager | `nmcli networking off` |
> > > | `hostnamectl set-hostname` | Cambia el hostname del sistema | `hostnamectl set-hostname novo-host` |
> > > | `ethtool -s speed` | Cambia velocidad de la interfaz de red | `ethtool -s eth0 speed 100` |
> > > | `brctl delbr` | Elimina un bridge de red | `brctl delbr br0` |
> > > | `vconfig rem` | Elimina interfaz VLAN | `vconfig rem eth0.100` |
> > > | `tc qdisc add` | Agrega control de tráfico (puede causar lentitud) | `tc qdisc add dev eth0 root netem delay 100ms` |
> > > | `ss -K` | Mata conexiones de socket específicas | `ss -K dst 10.0.0.1` |
> > > | `arp -d` | Elimina entrada de la tabla ARP | `arp -d 192.168.1.1` |
> > >
> > > ## Bloque para Copiar
> > >
> > > ```
> > > ifconfig
> > > ip link set down
> > > ip addr flush
> > > ip route flush
> > > ip route del
> > > ip route add
> > > iptables -F
> > > iptables -X
> > > iptables -P INPUT DROP
> > > iptables -P OUTPUT DROP
> > > iptables -P FORWARD DROP
> > > nft flush ruleset
> > > firewall-cmd --panic-on
> > > ufw disable
> > > route del default
> > > route add
> > > nmcli con down
> > > nmcli networking off
> > > hostnamectl set-hostname
> > > ethtool -s
> > > brctl delbr
> > > vconfig rem
> > > tc qdisc add
> > > ss -K
> > > arp -d
> > > ```
> > >
> > > ---
> > >
> > > `#Linux` `#NetworkCommands` `#DataDike` `#PAM` `#FSafer` `#PrivilegedAccessManagement` `#CommandControl`
