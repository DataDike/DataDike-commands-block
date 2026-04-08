# 🔵 HP-UX (HPE) - Comandos de Usuários

`#HPE` `#HPUX` `#HewlettPackardEnterprise` `#HPEServers` `#UNIX` `#DataDike` `#PAM` `#FSafer`

> Comandos para gestão de contas e segurança no HP-UX.
>
> ---
>
> ## Tabela de Referência
>
> | Comando | Descrição | Exemplo |
> |---------|-----------|---------|
> | `useradd` | Cria novo usuário | `useradd -m -d /home/joao -s /usr/bin/sh joao` |
> | `userdel` | Remove usuário | `userdel joao` |
> | `userdel -r` | Remove usuário e diretório home | `userdel -r joao` |
> | `usermod` | Modifica atributos de usuário | `usermod -s /usr/bin/false joao` |
> | `usermod -L` | Bloqueia conta de usuário | `usermod -L joao` |
> | `usermod -U` | Desbloqueia conta de usuário | `usermod -U joao` |
> | `passwd` | Altera senha de usuário | `passwd joao` |
> | `passwd -l` | Bloqueia senha do usuário | `passwd -l joao` |
> | `passwd -d` | Remove senha do usuário | `passwd -d joao` |
> | `groupadd` | Cria novo grupo | `groupadd desenvolvedores` |
> | `groupdel` | Remove grupo | `groupdel desenvolvedores` |
> | `groupmod` | Modifica atributos de grupo | `groupmod -n novo_nome antigo_nome` |
> | `chmod` | Altera permissões de arquivos | `chmod 750 /home/joao` |
> | `chmod -R` | Altera permissões recursivamente | `chmod -R 755 /dados` |
> | `chown` | Altera proprietário | `chown joao:staff /dados` |
> | `chown -R` | Altera proprietário recursivamente | `chown -R joao:staff /dados` |
> | `chgrp` | Altera grupo de arquivo | `chgrp staff /dados` |
> | `su` | Troca para outro usuário | `su - root` |
> | `sudo` | Executa comando como outro usuário | `sudo command` |
> | `modprpw` | Modifica atributos de segurança do usuário | `modprpw -v -l joao` |
> | `modprpw -k` | Bloqueia conta via Trusted Mode | `modprpw -k joao` |
> | `getprpw` | Consulta atributos de segurança | `getprpw -r -m lockout joao` |
> | `/usr/lbin/tsconvert` | Converte para Trusted System Mode | `/usr/lbin/tsconvert` |
> | `sam` | Interface SAM para gestão de usuários | `sam` |
> | `userdbset` | Define atributos no userdb | `userdbset -u joao DISPLAY_NAME="Joao Silva"` |
> | `userdbget` | Consulta atributos no userdb | `userdbget -u joao` |
> | `pwconv` | Converte /etc/passwd para /etc/shadow | `pwconv` |
>
> ---
>
> ## Bloco para Copiar
>
> ```
> useradd
> userdel
> userdel -r
> usermod
> usermod -L
> usermod -U
> passwd
> passwd -l
> passwd -d
> groupadd
> groupdel
> groupmod
> chmod
> chmod -R
> chown
> chown -R
> chgrp
> su
> sudo
> modprpw
> modprpw -k
> getprpw
> /usr/lbin/tsconvert
> sam
> userdbset
> userdbget
> pwconv
> ```
>
> ---
>
> `#HPUX` `#UserCommands` `#DataDike` `#PAM` `#FSafer` `#PrivilegedAccessManagement` `#CommandControl`
