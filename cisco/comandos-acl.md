# 🔵 Cisco IOS / IOS-XE - Comandos de ACL

`#Cisco` `#CiscoIOS` `#CiscoIOSXE` `#CiscoRouter` `#CiscoSwitch` `#CiscoNetworking` `#DataDike` `#PAM` `#FSafer`

> Comandos para Access Control Lists e segurança no Cisco IOS/IOS-XE.
>
> ---
>
> ## Tabela de Referência
>
> | Comando | Descrição | Exemplo |
> |---------|-----------|---------|
> | `access-list (standard)` | Cria ACL padrão numerada | `access-list 10 permit 192.168.1.0 0.0.0.255` |
> | `access-list (extended)` | Cria ACL estendida numerada | `access-list 100 permit tcp any host 10.0.0.1 eq 80` |
> | `no access-list` | Remove ACL numerada completa | `no access-list 100` |
> | `ip access-list standard` | Cria ACL padrão nomeada | `ip access-list standard ACL_PADRAO` |
> | `ip access-list extended` | Cria ACL estendida nomeada | `ip access-list extended ACL_WEB` |
> | `no ip access-list` | Remove ACL nomeada | `no ip access-list extended ACL_WEB` |
> | `permit` | Adiciona regra de permissão na ACL | `permit tcp 192.168.1.0 0.0.0.255 any eq 443` |
> | `deny` | Adiciona regra de negação na ACL | `deny ip any any log` |
> | `no permit` | Remove regra de permissão | `no permit tcp any any eq 80` |
> | `no deny` | Remove regra de negação | `no deny ip host 10.0.0.5 any` |
> | `ip access-group (in)` | Aplica ACL na interface (entrada) | `ip access-group ACL_WEB in` |
> | `ip access-group (out)` | Aplica ACL na interface (saída) | `ip access-group ACL_WEB out` |
> | `no ip access-group` | Remove ACL da interface | `no ip access-group ACL_WEB in` |
> | `line vty / access-class` | Aplica ACL nas linhas VTY (SSH/Telnet) | `access-class 10 in` |
> | `no access-class` | Remove ACL das linhas VTY | `no access-class 10 in` |
> | `line con 0 / login` | Configura autenticação na console | `login local` |
> | `line vty / transport input` | Define protocolos permitidos nas VTY | `transport input ssh` |
> | `no line vty` | Remove configuração de linhas VTY | `no line vty 5 15` |
> | `enable secret` | Define senha criptografada de enable | `enable secret S3nh@F0rt3` |
> | `username / privilege` | Cria usuário com nível de privilégio | `username admin privilege 15 secret S3nh@123` |
> | `no username` | Remove usuário | `no username temp_user` |
> | `aaa new-model` | Habilita modelo AAA | `aaa new-model` |
> | `no aaa new-model` | Desabilita modelo AAA | `no aaa new-model` |
> | `aaa authentication login` | Define método de autenticação | `aaa authentication login default local` |
> | `aaa authorization exec` | Define autorização para exec | `aaa authorization exec default local` |
> | `service password-encryption` | Habilita criptografia de senhas | `service password-encryption` |
> | `ip ssh version 2` | Define versão SSH 2 | `ip ssh version 2` |
> | `crypto key generate rsa` | Gera chaves RSA para SSH | `crypto key generate rsa modulus 2048` |
>
> ---
>
> ## Bloco para Copiar
>
> ```
> access-list
> no access-list
> ip access-list standard
> ip access-list extended
> no ip access-list
> permit
> deny
> ip access-group in
> ip access-group out
> no ip access-group
> access-class
> no access-class
> transport input
> enable secret
> username privilege
> no username
> aaa new-model
> no aaa new-model
> aaa authentication login
> aaa authorization exec
> service password-encryption
> ip ssh version
> crypto key generate rsa
> ```
>
> ---
>
> `#Cisco` `#ACLCommands` `#DataDike` `#PAM` `#FSafer` `#PrivilegedAccessManagement` `#CommandControl`
