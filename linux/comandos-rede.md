# 🟠 Linux - Comandos de Rede

`#Linux` `#Ubuntu` `#RedHat` `#RHEL` `#CentOS` `#Debian` `#SUSE` `#Bash` `#Shell` `#DataDike` `#PAM` `#FSafer`

> Comandos para configuração e manipulação de rede que podem afetar conectividade e segurança.
>
> ---
>
> ## Tabela de Referência
>
> | Comando | Descrição | Exemplo |
> |---------|-----------|---------|
> | `ifconfig` | Configura ou desabilita interfaces de rede | `ifconfig eth0 down` |
> | `ip link set down` | Desabilita interface de rede | `ip link set eth0 down` |
> | `ip addr flush` | Remove todos os endereços IP de uma interface | `ip addr flush dev eth0` |
> | `ip route flush` | Remove todas as rotas da tabela de roteamento | `ip route flush table main` |
> | `ip route del` | Remove uma rota específica | `ip route del default` |
> | `ip route add` | Adiciona rota estática | `ip route add 10.0.0.0/8 via 192.168.1.1` |
> | `iptables -F` | Limpa todas as regras do firewall | `iptables -F` |
> | `iptables -X` | Remove todas as chains customizadas | `iptables -X` |
> | `iptables -P INPUT DROP` | Define política padrão para DROP (bloqueia tudo) | `iptables -P INPUT DROP` |
> | `iptables -P OUTPUT DROP` | Bloqueia todo tráfego de saída | `iptables -P OUTPUT DROP` |
> | `iptables -P FORWARD DROP` | Bloqueia todo encaminhamento de pacotes | `iptables -P FORWARD DROP` |
> | `nft flush ruleset` | Limpa todas as regras do nftables | `nft flush ruleset` |
> | `firewall-cmd --panic-on` | Ativa modo pânico no firewalld (bloqueia tudo) | `firewall-cmd --panic-on` |
> | `ufw disable` | Desabilita o firewall UFW | `ufw disable` |
> | `route del default` | Remove a rota padrão | `route del default` |
> | `route add` | Adiciona rota estática (legado) | `route add -net 10.0.0.0/8 gw 192.168.1.1` |
> | `nmcli con down` | Desativa conexão de rede | `nmcli con down "Wired connection 1"` |
> | `nmcli networking off` | Desabilita toda a rede via NetworkManager | `nmcli networking off` |
> | `hostnamectl set-hostname` | Altera o hostname do sistema | `hostnamectl set-hostname novo-host` |
> | `ethtool -s speed` | Altera velocidade da interface de rede | `ethtool -s eth0 speed 100` |
> | `brctl delbr` | Remove uma bridge de rede | `brctl delbr br0` |
> | `vconfig rem` | Remove interface VLAN | `vconfig rem eth0.100` |
> | `tc qdisc add` | Adiciona controle de tráfego (pode causar lentidão) | `tc qdisc add dev eth0 root netem delay 100ms` |
> | `ss -K` | Mata conexões de socket específicas | `ss -K dst 10.0.0.1` |
> | `arp -d` | Remove entrada da tabela ARP | `arp -d 192.168.1.1` |
>
> ---
>
> ## Bloco para Copiar
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
> `#Linux` `#NetworkCommands` `#DataDike` `#PAM` `#FSafer` `#PrivilegedAccessManagement` `#CommandControl`
