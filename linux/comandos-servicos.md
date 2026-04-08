**[English](#english)** | **[Português](#português)** | **[Español](#español)**

---

# English

# Linux - Service Commands

`#Linux` `#Ubuntu` `#RedHat` `#RHEL` `#CentOS` `#Debian` `#SUSE` `#Bash` `#Shell` `#DataDike` `#PAM` `#FSafer`

> Commands for controlling services, processes and system daemons.

---

## Reference Table

| Command | Description | Example |
|---------|-------------|---------|
| `systemctl stop` | Stops a service | `systemctl stop sshd` |
| `systemctl start` | Starts a service | `systemctl start httpd` |
| `systemctl restart` | Restarts a service | `systemctl restart nginx` |
| `systemctl disable` | Disables service at boot | `systemctl disable firewalld` |
| `systemctl enable` | Enables service at boot | `systemctl enable sshd` |
| `systemctl mask` | Masks service (prevents startup) | `systemctl mask iptables` |
| `systemctl unmask` | Removes mask from a service | `systemctl unmask iptables` |
| `systemctl daemon-reload` | Reloads systemd configurations | `systemctl daemon-reload` |
| `systemctl set-default` | Changes default system target | `systemctl set-default multi-user.target` |
| `systemctl isolate` | Switches to another target immediately | `systemctl isolate rescue.target` |
| `service stop` | Stops service (SysVinit/legacy) | `service httpd stop` |
| `service start` | Starts service (SysVinit/legacy) | `service httpd start` |
| `chkconfig off` | Disables service at boot (legacy) | `chkconfig httpd off` |
| `kill` | Sends signal to process | `kill -15 1234` |
| `kill -9` | Forcefully kills process (SIGKILL) | `kill -9 1234` |
| `killall` | Kills all processes by name | `killall httpd` |
| `killall -9` | Forcefully kills all processes by name | `killall -9 java` |
| `pkill` | Kills processes by name pattern | `pkill -f tomcat` |
| `pkill -9` | Forcefully kills processes by pattern | `pkill -9 -f "java.*tomcat"` |
| `nice` | Starts process with altered priority | `nice -n 19 backup.sh` |
| `renice` | Changes priority of running process | `renice -n -20 -p 1234` |
| `nohup` | Executes command immune to hangup | `nohup script.sh &` |
| `crontab -e` | Edits user scheduled tasks | `crontab -e` |
| `crontab -r` | Removes all scheduled tasks | `crontab -r` |
| `at` | Schedules single command execution | `at now + 5 minutes` |
| `atrm` | Removes scheduled at job | `atrm 5` |
| `update-rc.d remove` | Removes service from init (Debian) | `update-rc.d apache2 remove` |
| `insserv -r` | Removes service from boot (SUSE) | `insserv -r apache2` |
| `fuser -k` | Kills processes using a file/port | `fuser -k 80/tcp` |
| `lsof -ti -k` | Lists and kills processes on port/file | `lsof -ti :8080` |

## Copy Block

```
systemctl stop
systemctl start
systemctl restart
systemctl disable
systemctl enable
systemctl mask
systemctl unmask
systemctl daemon-reload
systemctl set-default
systemctl isolate
service stop
service start
chkconfig off
kill
kill -9
killall
killall -9
pkill
pkill -9
nice
renice
nohup
crontab -e
crontab -r
at
atrm
update-rc.d remove
insserv -r
fuser -k
lsof -ti
```

---

# Português

# Linux - Comandos de Serviços

`#Linux` `#Ubuntu` `#RedHat` `#RHEL` `#CentOS` `#Debian` `#SUSE` `#Bash` `#Shell` `#DataDike` `#PAM` `#FSafer`

> Comandos para controle de serviços, processos e daemons do sistema.

---

## Tabela de Referência

| Comando | Descrição | Exemplo |
|---------|-----------|---------|
| `systemctl stop` | Para um serviço | `systemctl stop sshd` |
| `systemctl start` | Inicia um serviço | `systemctl start httpd` |
| `systemctl restart` | Reinicia um serviço | `systemctl restart nginx` |
| `systemctl disable` | Desabilita serviço na inicialização | `systemctl disable firewalld` |
| `systemctl enable` | Habilita serviço na inicialização | `systemctl enable sshd` |
| `systemctl mask` | Mascara serviço (impede inicialização) | `systemctl mask iptables` |
| `systemctl unmask` | Remove máscara de um serviço | `systemctl unmask iptables` |
| `systemctl daemon-reload` | Recarrega configurações do systemd | `systemctl daemon-reload` |
| `systemctl set-default` | Altera o target padrão do sistema | `systemctl set-default multi-user.target` |
| `systemctl isolate` | Muda para outro target imediatamente | `systemctl isolate rescue.target` |
| `service stop` | Para serviço (SysVinit/legado) | `service httpd stop` |
| `service start` | Inicia serviço (SysVinit/legado) | `service httpd start` |
| `chkconfig off` | Desabilita serviço no boot (legado) | `chkconfig httpd off` |
| `kill` | Envia sinal para processo | `kill -15 1234` |
| `kill -9` | Mata processo forçadamente (SIGKILL) | `kill -9 1234` |
| `killall` | Mata todos os processos por nome | `killall httpd` |
| `killall -9` | Mata forçadamente todos os processos por nome | `killall -9 java` |
| `pkill` | Mata processos por padrão de nome | `pkill -f tomcat` |
| `pkill -9` | Mata forçadamente processos por padrão | `pkill -9 -f "java.*tomcat"` |
| `nice` | Inicia processo com prioridade alterada | `nice -n 19 backup.sh` |
| `renice` | Altera prioridade de processo em execução | `renice -n -20 -p 1234` |
| `nohup` | Executa comando imune a hangup | `nohup script.sh &` |
| `crontab -e` | Edita tarefas agendadas do usuário | `crontab -e` |
| `crontab -r` | Remove todas as tarefas agendadas | `crontab -r` |
| `at` | Agenda execução única de comando | `at now + 5 minutes` |
| `atrm` | Remove job agendado com at | `atrm 5` |
| `update-rc.d remove` | Remove serviço do init (Debian) | `update-rc.d apache2 remove` |
| `insserv -r` | Remove serviço do boot (SUSE) | `insserv -r apache2` |
| `fuser -k` | Mata processos usando um arquivo/porta | `fuser -k 80/tcp` |
| `lsof -ti -k` | Lista e mata processos em porta/arquivo | `lsof -ti :8080` |

## Bloco para Copiar

```
systemctl stop
systemctl start
systemctl restart
systemctl disable
systemctl enable
systemctl mask
systemctl unmask
systemctl daemon-reload
systemctl set-default
systemctl isolate
service stop
service start
chkconfig off
kill
kill -9
killall
killall -9
pkill
pkill -9
nice
renice
nohup
crontab -e
crontab -r
at
atrm
update-rc.d remove
insserv -r
fuser -k
lsof -ti
```

---

# Español

# Linux - Comandos de Servicios

`#Linux` `#Ubuntu` `#RedHat` `#RHEL` `#CentOS` `#Debian` `#SUSE` `#Bash` `#Shell` `#DataDike` `#PAM` `#FSafer`

> Comandos para control de servicios, procesos y daemons del sistema.

---

## Tabla de Referencia

| Comando | Descripción | Ejemplo |
|---------|-------------|---------|
| `systemctl stop` | Detiene un servicio | `systemctl stop sshd` |
| `systemctl start` | Inicia un servicio | `systemctl start httpd` |
| `systemctl restart` | Reinicia un servicio | `systemctl restart nginx` |
| `systemctl disable` | Deshabilita servicio en el arranque | `systemctl disable firewalld` |
| `systemctl enable` | Habilita servicio en el arranque | `systemctl enable sshd` |
| `systemctl mask` | Enmascara servicio (impide inicio) | `systemctl mask iptables` |
| `systemctl unmask` | Elimina máscara de un servicio | `systemctl unmask iptables` |
| `systemctl daemon-reload` | Recarga configuraciones de systemd | `systemctl daemon-reload` |
| `systemctl set-default` | Cambia el target predeterminado del sistema | `systemctl set-default multi-user.target` |
| `systemctl isolate` | Cambia a otro target inmediatamente | `systemctl isolate rescue.target` |
| `service stop` | Detiene servicio (SysVinit/legado) | `service httpd stop` |
| `service start` | Inicia servicio (SysVinit/legado) | `service httpd start` |
| `chkconfig off` | Deshabilita servicio en el arranque (legado) | `chkconfig httpd off` |
| `kill` | Envía señal a proceso | `kill -15 1234` |
| `kill -9` | Mata proceso forzadamente (SIGKILL) | `kill -9 1234` |
| `killall` | Mata todos los procesos por nombre | `killall httpd` |
| `killall -9` | Mata forzadamente todos los procesos por nombre | `killall -9 java` |
| `pkill` | Mata procesos por patrón de nombre | `pkill -f tomcat` |
| `pkill -9` | Mata forzadamente procesos por patrón | `pkill -9 -f "java.*tomcat"` |
| `nice` | Inicia proceso con prioridad alterada | `nice -n 19 backup.sh` |
| `renice` | Cambia prioridad de proceso en ejecución | `renice -n -20 -p 1234` |
| `nohup` | Ejecuta comando inmune a hangup | `nohup script.sh &` |
| `crontab -e` | Edita tareas programadas del usuario | `crontab -e` |
| `crontab -r` | Elimina todas las tareas programadas | `crontab -r` |
| `at` | Programa ejecución única de comando | `at now + 5 minutes` |
| `atrm` | Elimina tarea programada con at | `atrm 5` |
| `update-rc.d remove` | Elimina servicio del init (Debian) | `update-rc.d apache2 remove` |
| `insserv -r` | Elimina servicio del arranque (SUSE) | `insserv -r apache2` |
| `fuser -k` | Mata procesos usando un archivo/puerto | `fuser -k 80/tcp` |
| `lsof -ti -k` | Lista y mata procesos en puerto/archivo | `lsof -ti :8080` |

## Bloque para Copiar

```
systemctl stop
systemctl start
systemctl restart
systemctl disable
systemctl enable
systemctl mask
systemctl unmask
systemctl daemon-reload
systemctl set-default
systemctl isolate
service stop
service start
chkconfig off
kill
kill -9
killall
killall -9
pkill
pkill -9
nice
renice
nohup
crontab -e
crontab -r
at
atrm
update-rc.d remove
insserv -r
fuser -k
lsof -ti
```

---

`#Linux` `#ServiceCommands` `#DataDike` `#PAM` `#FSafer` `#PrivilegedAccessManagement` `#CommandControl`# 🟣 Linux - Comandos de Serviços

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
