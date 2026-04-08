**[English](#english)** | **[Português](#português)** | **[Español](#español)**

---

# English

# Linux - Deletion Commands

`#Linux` `#Ubuntu` `#RedHat` `#RHEL` `#CentOS` `#Debian` `#SUSE` `#Bash` `#Shell` `#DataDike` `#PAM` `#FSafer`

> Commands for removing files, directories and data that can cause information loss.
>
> ---
>
> ## Reference Table
>
> | Command | Description | Example |
> |---------|-------------|---------|
> | `rm` | Removes files | `rm arquivo.txt` |
> | `rm -r` | Removes directories recursively | `rm -r /tmp/pasta` |
> | `rm -f` | Removes files forcefully without confirmation | `rm -f arquivo.log` |
> | `rm -rf` | Removes recursively and forcefully | `rm -rf /var/log/old/` |
> | `rmdir` | Removes empty directories | `rmdir /tmp/vazio` |
> | `unlink` | Removes a single file (link) | `unlink /tmp/arquivo` |
> | `find ... -delete` | Finds and removes files by criteria | `find /tmp -name "*.tmp" -delete` |
> | `find ... -exec rm` | Finds and executes rm on each result | `find /var/log -name "*.gz" -exec rm {} \;` |
> | `shred` | Overwrites and removes file securely | `shred -vfz -n 5 arquivo.txt` |
> | `truncate -s 0` | Zeroes out file content (keeps the file) | `truncate -s 0 /var/log/syslog` |
> | `> arquivo` | Redirects empty to file, zeroing content | `> /var/log/messages` |
> | `dd if=/dev/null of=` | Overwrites file with null | `dd if=/dev/null of=arquivo.dat` |
> | `cat /dev/null >` | Zeroes file content using cat | `cat /dev/null > /var/log/auth.log` |
> | `echo "" >` | Replaces file content with empty string | `echo "" > /etc/motd` |
> | `cp /dev/null` | Copies null to file, zeroing it | `cp /dev/null /var/log/syslog` |
> | `rsync --delete` | Syncs and removes files at destination not present in source | `rsync -a --delete /vazio/ /dados/` |
> | `find ... -mtime +N -delete` | Removes files older than N days | `find /backup -mtime +30 -delete` |
> | `tmpwatch / tmpreaper` | Removes old files in temporary directories | `tmpwatch 720 /tmp` |
> | `srm` | Secure file removal (secure remove) | `srm -r /dados/sensivel/` |
> | `wipe` | Erases files irrecoverably | `wipe -r /dados/antigos/` |
> | `xfs_repair -L` | Zeroes XFS log (may lose data) | `xfs_repair -L /dev/sda1` |
> | `tune2fs -O ^has_journal` | Removes ext filesystem journal (risk of loss) | `tune2fs -O ^has_journal /dev/sda1` |
>
> ## Copy Block
>
> ```
> rm
> rm -r
> rm -f
> rm -rf
> rmdir
> unlink
> find -delete
> find -exec rm
> shred
> truncate -s 0
> > arquivo
> dd if=/dev/null
> cat /dev/null >
> echo "" >
> cp /dev/null
> rsync --delete
> find -mtime -delete
> tmpwatch
> tmpreaper
> srm
> wipe
> xfs_repair -L
> tune2fs -O ^has_journal
> ```
>
> ---
>
> # Português
>
> # Linux - Comandos de Exclusão
>
> `#Linux` `#Ubuntu` `#RedHat` `#RHEL` `#CentOS` `#Debian` `#SUSE` `#Bash` `#Shell` `#DataDike` `#PAM` `#FSafer`
>
> > Comandos para remoção de arquivos, diretórios e dados que podem causar perda de informações.
> >
> > ---
> >
> > ## Tabela de Referência
> >
> > | Comando | Descrição | Exemplo |
> > |---------|-----------|---------|
> > | `rm` | Remove arquivos | `rm arquivo.txt` |
> > | `rm -r` | Remove diretórios recursivamente | `rm -r /tmp/pasta` |
> > | `rm -f` | Remove arquivos forçadamente sem confirmação | `rm -f arquivo.log` |
> > | `rm -rf` | Remove recursivamente e forçadamente | `rm -rf /var/log/old/` |
> > | `rmdir` | Remove diretórios vazios | `rmdir /tmp/vazio` |
> > | `unlink` | Remove um único arquivo (link) | `unlink /tmp/arquivo` |
> > | `find ... -delete` | Busca e remove arquivos por critério | `find /tmp -name "*.tmp" -delete` |
> > | `find ... -exec rm` | Busca e executa rm em cada resultado | `find /var/log -name "*.gz" -exec rm {} \;` |
> > | `shred` | Sobrescreve e remove arquivo de forma segura | `shred -vfz -n 5 arquivo.txt` |
> > | `truncate -s 0` | Zera o conteúdo de um arquivo (mantém o arquivo) | `truncate -s 0 /var/log/syslog` |
> > | `> arquivo` | Redireciona vazio para arquivo, zerando conteúdo | `> /var/log/messages` |
> > | `dd if=/dev/null of=` | Sobrescreve arquivo com null | `dd if=/dev/null of=arquivo.dat` |
> > | `cat /dev/null >` | Zera conteúdo de arquivo usando cat | `cat /dev/null > /var/log/auth.log` |
> > | `echo "" >` | Substitui conteúdo do arquivo por string vazia | `echo "" > /etc/motd` |
> > | `cp /dev/null` | Copia null para arquivo, zerando-o | `cp /dev/null /var/log/syslog` |
> > | `rsync --delete` | Sincroniza e remove arquivos no destino não presentes na origem | `rsync -a --delete /vazio/ /dados/` |
> > | `find ... -mtime +N -delete` | Remove arquivos mais antigos que N dias | `find /backup -mtime +30 -delete` |
> > | `tmpwatch / tmpreaper` | Remove arquivos antigos em diretórios temporários | `tmpwatch 720 /tmp` |
> > | `srm` | Remoção segura de arquivos (secure remove) | `srm -r /dados/sensivel/` |
> > | `wipe` | Apaga arquivos de forma irrecuperável | `wipe -r /dados/antigos/` |
> > | `xfs_repair -L` | Zera o log do XFS (pode perder dados) | `xfs_repair -L /dev/sda1` |
> > | `tune2fs -O ^has_journal` | Remove journal de filesystem ext (risco de perda) | `tune2fs -O ^has_journal /dev/sda1` |
> >
> > ## Bloco para Copiar
> >
> > ```
> > rm
> > rm -r
> > rm -f
> > rm -rf
> > rmdir
> > unlink
> > find -delete
> > find -exec rm
> > shred
> > truncate -s 0
> > > arquivo
> > dd if=/dev/null
> > cat /dev/null >
> > echo "" >
> > cp /dev/null
> > rsync --delete
> > find -mtime -delete
> > tmpwatch
> > tmpreaper
> > srm
> > wipe
> > xfs_repair -L
> > tune2fs -O ^has_journal
> > ```
> >
> > ---
> >
> > # Español
> >
> > # Linux - Comandos de Eliminación
> >
> > `#Linux` `#Ubuntu` `#RedHat` `#RHEL` `#CentOS` `#Debian` `#SUSE` `#Bash` `#Shell` `#DataDike` `#PAM` `#FSafer`
> >
> > > Comandos para eliminación de archivos, directorios y datos que pueden causar pérdida de información.
> > >
> > > ---
> > >
> > > ## Tabla de Referencia
> > >
> > > | Comando | Descripción | Ejemplo |
> > > |---------|-------------|---------|
> > > | `rm` | Elimina archivos | `rm arquivo.txt` |
> > > | `rm -r` | Elimina directorios recursivamente | `rm -r /tmp/pasta` |
> > > | `rm -f` | Elimina archivos forzadamente sin confirmación | `rm -f arquivo.log` |
> > > | `rm -rf` | Elimina recursivamente y forzadamente | `rm -rf /var/log/old/` |
> > > | `rmdir` | Elimina directorios vacíos | `rmdir /tmp/vazio` |
> > > | `unlink` | Elimina un único archivo (link) | `unlink /tmp/arquivo` |
> > > | `find ... -delete` | Busca y elimina archivos por criterio | `find /tmp -name "*.tmp" -delete` |
> > > | `find ... -exec rm` | Busca y ejecuta rm en cada resultado | `find /var/log -name "*.gz" -exec rm {} \;` |
> > > | `shred` | Sobrescribe y elimina archivo de forma segura | `shred -vfz -n 5 arquivo.txt` |
> > > | `truncate -s 0` | Vacía el contenido de un archivo (mantiene el archivo) | `truncate -s 0 /var/log/syslog` |
> > > | `> arquivo` | Redirige vacío al archivo, vaciando contenido | `> /var/log/messages` |
> > > | `dd if=/dev/null of=` | Sobrescribe archivo con null | `dd if=/dev/null of=arquivo.dat` |
> > > | `cat /dev/null >` | Vacía contenido de archivo usando cat | `cat /dev/null > /var/log/auth.log` |
> > > | `echo "" >` | Sustituye contenido del archivo por cadena vacía | `echo "" > /etc/motd` |
> > > | `cp /dev/null` | Copia null al archivo, vaciándolo | `cp /dev/null /var/log/syslog` |
> > > | `rsync --delete` | Sincroniza y elimina archivos en destino no presentes en origen | `rsync -a --delete /vazio/ /dados/` |
> > > | `find ... -mtime +N -delete` | Elimina archivos más antiguos que N días | `find /backup -mtime +30 -delete` |
> > > | `tmpwatch / tmpreaper` | Elimina archivos antiguos en directorios temporales | `tmpwatch 720 /tmp` |
> > > | `srm` | Eliminación segura de archivos (secure remove) | `srm -r /dados/sensivel/` |
> > > | `wipe` | Borra archivos de forma irrecuperable | `wipe -r /dados/antigos/` |
> > > | `xfs_repair -L` | Vacía el log de XFS (puede perder datos) | `xfs_repair -L /dev/sda1` |
> > > | `tune2fs -O ^has_journal` | Elimina journal de filesystem ext (riesgo de pérdida) | `tune2fs -O ^has_journal /dev/sda1` |
> > >
> > > ## Bloque para Copiar
> > >
> > > ```
> > > rm
> > > rm -r
> > > rm -f
> > > rm -rf
> > > rmdir
> > > unlink
> > > find -delete
> > > find -exec rm
> > > shred
> > > truncate -s 0
> > > > arquivo
> > > dd if=/dev/null
> > > cat /dev/null >
> > > echo "" >
> > > cp /dev/null
> > > rsync --delete
> > > find -mtime -delete
> > > tmpwatch
> > > tmpreaper
> > > srm
> > > wipe
> > > xfs_repair -L
> > > tune2fs -O ^has_journal
> > > ```
> > >
> > > ---
> > >
> > > `#Linux` `#DeletionCommands` `#DataDike` `#PAM` `#FSafer` `#PrivilegedAccessManagement` `#CommandControl`
