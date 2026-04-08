# 🔵 IBM AIX - Comandos de Usuários

`#IBM` `#AIX` `#IBMAIX` `#PowerSystems` `#UNIX` `#IBMPower` `#DataDike` `#PAM` `#FSafer`

> Comandos para gestão de contas e segurança no IBM AIX.
>
> ---
>
> ## Tabela de Referência
>
> | Comando | Descrição | Exemplo |
> |---------|-----------|---------|
> | `mkuser` | Cria novo usuário | `mkuser -a home=/home/joao joao` |
> | `rmuser` | Remove usuário | `rmuser joao` |
> | `rmuser -p` | Remove usuário e limpa entrada do /etc/passwd | `rmuser -p joao` |
> | `chuser` | Altera atributos de usuário | `chuser login=false joao` |
> | `chuser account_locked=true` | Bloqueia conta de usuário | `chuser account_locked=true joao` |
> | `chuser account_locked=false` | Desbloqueia conta de usuário | `chuser account_locked=false joao` |
> | `chuser login=false` | Desabilita login do usuário | `chuser login=false joao` |
> | `chuser login=true` | Habilita login do usuário | `chuser login=true joao` |
> | `passwd` | Altera senha de usuário | `passwd joao` |
> | `pwdadm -c` | Limpa flags de senha (força troca) | `pwdadm -c joao` |
> | `mkgroup` | Cria novo grupo | `mkgroup desenvolvedores` |
> | `rmgroup` | Remove grupo | `rmgroup desenvolvedores` |
> | `chgroup` | Altera atributos de grupo | `chgroup users=joao,maria desenvolvedores` |
> | `chgrpmem -m +` | Adiciona membro ao grupo | `chgrpmem -m + joao staff` |
> | `chgrpmem -m -` | Remove membro do grupo | `chgrpmem -m - joao staff` |
> | `chmod` | Altera permissões de arquivos | `chmod 750 /home/joao` |
> | `chmod -R` | Altera permissões recursivamente | `chmod -R 755 /dados` |
> | `chown` | Altera proprietário | `chown joao:staff /dados/arquivo` |
> | `chown -R` | Altera proprietário recursivamente | `chown -R joao:staff /dados` |
> | `su` | Troca para outro usuário | `su - root` |
> | `sudo` | Executa comando como outro usuário | `sudo command` |
> | `chsec` | Altera atributos de segurança | `chsec -f /etc/security/user -s joao -a maxage=90` |
> | `setsenv` | Define ambiente de segurança | `setsenv` |
> | `lsuser` | Lista atributos de usuário | `lsuser ALL` |
> | `lsgroup` | Lista atributos de grupo | `lsgroup ALL` |
> | `smitty user` | Interface SMIT para gestão de usuários | `smitty user` |
> | `smitty security` | Interface SMIT para segurança | `smitty security` |
>
> ---
>
> ## Bloco para Copiar
>
> ```
> mkuser
> rmuser
> rmuser -p
> chuser
> chuser account_locked=true
> chuser account_locked=false
> chuser login=false
> chuser login=true
> passwd
> pwdadm -c
> mkgroup
> rmgroup
> chgroup
> chgrpmem -m +
> chgrpmem -m -
> chmod
> chmod -R
> chown
> chown -R
> su
> sudo
> chsec
> setsenv
> lsuser
> lsgroup
> smitty user
> smitty security
> ```
>
> ---
>
> `#AIX` `#UserCommands` `#DataDike` `#PAM` `#FSafer` `#PrivilegedAccessManagement` `#CommandControl`
