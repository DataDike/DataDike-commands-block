# 🟣 Linux - Comandos de Serviços

`#Linux` `#Ubuntu` `#RedHat` `#RHEL` `#CentOS` `#Debian` `#SUSE` `#Bash` `#Shell` `#DataDike` `#PAM` `#FSafer`

> Comandos para controle de serviços, processos e daemons do sistema.
>
> ---
>
> ## Tabela de Referência
>
> | Comando | Descrição | Exemplo |
> |---------|-----------|---------|
> | `systemctl stop` | Para um serviço | `systemctl stop sshd` |
> | `systemctl start` | Inicia um serviço | `systemctl start httpd` |
> | `systemctl restart` | Reinicia um serviço | `systemctl restart nginx` |
> | `systemctl disable` | Desabilita serviço na inicialização | `systemctl disable firewalld` |
> | `systemctl enable` | Habilita serviço na inicialização | `systemctl enable sshd` |
> | `systemctl mask` | Mascara serviço (impede inicialização) | `systemctl mask iptables` |
> | `systemctl unmask` | Remove máscara de um serviço | `systemctl unmask iptables` |
> | `systemctl daemon-reload` | Recarrega configurações do systemd | `systemctl daemon-reload` |
> | `systemctl set-default` | Altera o target padrão do sistema | `systemctl set-default multi-user.target` |
> | `systemctl isolate` | Muda para outro target imediatamente | `systemctl isolate rescue.target` |
> | `service stop` | Para serviço (SysVinit/legado) | `service httpd stop` |
> | `service start` | Inicia serviço (SysVinit/legado) | `service httpd start` |
> | `chkconfig off` | Desabilita serviço no boot (legado) | `chkconfig httpd off` |
> | `kill` | Envia sinal para processo | `kill -15 1234` |
> | `kill -9` | Mata processo forçadamente (SIGKILL) | `kill -9 1234` |
> | `killall` | Mata todos os processos por nome | `killall httpd` |
> | `killall -9` | Mata forçadamente todos os processos por nome | `killall -9 java` |
> | `pkill` | Mata processos por padrão de nome | `pkill -f tomcat` |
> | `pkill -9` | Mata forçadamente processos por padrão | `pkill -9 -f "java.*tomcat"` |
> | `nice` | Inicia processo com prioridade alterada | `nice -n 19 backup.sh` |
> | `renice` | Altera prioridade de processo em execução | `renice -n -20 -p 1234` |
> | `nohup` | Executa comando imune a hangup | `nohup script.sh &` |
> | `crontab -e` | Edita tarefas agendadas do usuário | `crontab -e` |
> | `crontab -r` | Remove todas as tarefas agendadas | `crontab -r` |
> | `at` | Agenda execução única de comando | `at now + 5 minutes` |
> | `atrm` | Remove job agendado com at | `atrm 5` |
> | `update-rc.d remove` | Remove serviço do init (Debian) | `update-rc.d apache2 remove` |
> | `insserv -r` | Remove serviço do boot (SUSE) | `insserv -r apache2` |
> | `fuser -k` | Mata processos usando um arquivo/porta | `fuser -k 80/tcp` |
> | `lsof -ti -k` | Lista e mata processos em porta/arquivo | `lsof -ti :8080` |
>
> ---
>
> ## Bloco para Copiar
>
> ```
> systemctl stop
> systemctl start
> systemctl restart
> systemctl disable
> systemctl enable
> systemctl mask
> systemctl unmask
> systemctl daemon-reload
> systemctl set-default
> systemctl isolate
> service stop
> service start
> chkconfig off
> kill
> kill -9
> killall
> killall -9
> pkill
> pkill -9
> nice
> renice
> nohup
> crontab -e
> crontab -r
> at
> atrm
> update-rc.d remove
> insserv -r
> fuser -k
> lsof -ti
> ```
>
> ---
>
> `#Linux` `#ServiceCommands` `#DataDike` `#PAM` `#FSafer` `#PrivilegedAccessManagement` `#CommandControl`
