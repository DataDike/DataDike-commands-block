# 🔵 Linux - Comandos de Usuários

`#Linux` `#Ubuntu` `#RedHat` `#RHEL` `#CentOS` `#Debian` `#SUSE` `#Bash` `#Shell` `#DataDike` `#PAM` `#FSafer`

> Comandos para gestão de contas de usuário, grupos e permissões do sistema.
>
> ---
>
> ## Tabela de Referência
>
> | Comando | Descrição | Exemplo |
> |---------|-----------|---------|
> | `useradd` | Cria novo usuário no sistema | `useradd -m -s /bin/bash joao` |
> | `userdel` | Remove usuário do sistema | `userdel joao` |
> | `userdel -r` | Remove usuário e seu diretório home | `userdel -r joao` |
> | `usermod` | Modifica propriedades de um usuário | `usermod -aG sudo joao` |
> | `usermod -L` | Bloqueia conta de usuário | `usermod -L joao` |
> | `usermod -U` | Desbloqueia conta de usuário | `usermod -U joao` |
> | `usermod -s /sbin/nologin` | Remove acesso shell do usuário | `usermod -s /sbin/nologin joao` |
> | `passwd` | Altera senha de usuário | `passwd joao` |
> | `passwd -l` | Bloqueia senha do usuário | `passwd -l joao` |
> | `passwd -d` | Remove senha do usuário (acesso sem senha) | `passwd -d joao` |
> | `chage` | Altera políticas de expiração de senha | `chage -M 90 joao` |
> | `chage -E` | Define data de expiração da conta | `chage -E 2025-12-31 joao` |
> | `groupadd` | Cria novo grupo | `groupadd desenvolvedores` |
> | `groupdel` | Remove grupo do sistema | `groupdel desenvolvedores` |
> | `groupmod` | Modifica propriedades de um grupo | `groupmod -n novo_nome antigo_nome` |
> | `gpasswd -a` | Adiciona usuário a um grupo | `gpasswd -a joao sudo` |
> | `gpasswd -d` | Remove usuário de um grupo | `gpasswd -d joao sudo` |
> | `chmod` | Altera permissões de arquivos/diretórios | `chmod 700 /home/joao` |
> | `chmod -R` | Altera permissões recursivamente | `chmod -R 755 /var/www` |
> | `chown` | Altera proprietário de arquivos/diretórios | `chown root:root /etc/passwd` |
> | `chown -R` | Altera proprietário recursivamente | `chown -R joao:joao /home/joao` |
> | `chgrp` | Altera grupo de arquivos/diretórios | `chgrp www-data /var/www` |
> | `setfacl` | Define ACLs em arquivos/diretórios | `setfacl -m u:joao:rwx /dados` |
> | `visudo` | Edita configuração do sudoers | `visudo` |
> | `su` | Troca para outro usuário | `su - root` |
> | `sudo` | Executa comando como outro usuário | `sudo comando` |
> | `pkill -u` | Mata todos os processos de um usuário | `pkill -u joao` |
> | `crontab -r` | Remove crontab de um usuário | `crontab -r -u joao` |
> | `loginctl terminate-user` | Encerra todas as sessões de um usuário | `loginctl terminate-user joao` |
> | `faillock --reset` | Reseta contador de falhas de login | `faillock --user joao --reset` |
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
> usermod -s /sbin/nologin
> passwd
> passwd -l
> passwd -d
> chage
> chage -E
> groupadd
> groupdel
> groupmod
> gpasswd -a
> gpasswd -d
> chmod
> chmod -R
> chown
> chown -R
> chgrp
> setfacl
> visudo
> su
> sudo
> pkill -u
> crontab -r
> loginctl terminate-user
> faillock --reset
> ```
>
> ---
>
> `#Linux` `#UserCommands` `#DataDike` `#PAM` `#FSafer` `#PrivilegedAccessManagement` `#CommandControl`
