# 🟡 Linux - Comandos de Exclusão

`#Linux` `#Ubuntu` `#RedHat` `#RHEL` `#CentOS` `#Debian` `#SUSE` `#Bash` `#Shell` `#DataDike` `#PAM` `#FSafer`

> Comandos para remoção de arquivos, diretórios e dados que podem causar perda de informações.
>
> ---
>
> ## Tabela de Referência
>
> | Comando | Descrição | Exemplo |
> |---------|-----------|---------|
> | `rm` | Remove arquivos | `rm arquivo.txt` |
> | `rm -r` | Remove diretórios recursivamente | `rm -r /tmp/pasta` |
> | `rm -f` | Remove arquivos forçadamente sem confirmação | `rm -f arquivo.log` |
> | `rm -rf` | Remove recursivamente e forçadamente | `rm -rf /var/log/old/` |
> | `rmdir` | Remove diretórios vazios | `rmdir /tmp/vazio` |
> | `unlink` | Remove um único arquivo (link) | `unlink /tmp/arquivo` |
> | `find ... -delete` | Busca e remove arquivos por critério | `find /tmp -name "*.tmp" -delete` |
> | `find ... -exec rm` | Busca e executa rm em cada resultado | `find /var/log -name "*.gz" -exec rm {} \;` |
> | `shred` | Sobrescreve e remove arquivo de forma segura | `shred -vfz -n 5 arquivo.txt` |
> | `truncate -s 0` | Zera o conteúdo de um arquivo (mantém o arquivo) | `truncate -s 0 /var/log/syslog` |
> | `> arquivo` | Redireciona vazio para arquivo, zerando conteúdo | `> /var/log/messages` |
> | `dd if=/dev/null of=` | Sobrescreve arquivo com null | `dd if=/dev/null of=arquivo.dat` |
> | `cat /dev/null >` | Zera conteúdo de arquivo usando cat | `cat /dev/null > /var/log/auth.log` |
> | `echo "" >` | Substitui conteúdo do arquivo por string vazia | `echo "" > /etc/motd` |
> | `cp /dev/null` | Copia null para arquivo, zerando-o | `cp /dev/null /var/log/syslog` |
> | `rsync --delete` | Sincroniza e remove arquivos no destino não presentes na origem | `rsync -a --delete /vazio/ /dados/` |
> | `find ... -mtime +N -delete` | Remove arquivos mais antigos que N dias | `find /backup -mtime +30 -delete` |
> | `tmpwatch` / `tmpreaper` | Remove arquivos antigos em diretórios temporários | `tmpwatch 720 /tmp` |
> | `srm` | Remoção segura de arquivos (secure remove) | `srm -r /dados/sensivel/` |
> | `wipe` | Apaga arquivos de forma irrecuperável | `wipe -r /dados/antigos/` |
> | `xfs_repair -L` | Zera o log do XFS (pode perder dados) | `xfs_repair -L /dev/sda1` |
> | `tune2fs -O ^has_journal` | Remove journal de filesystem ext (risco de perda) | `tune2fs -O ^has_journal /dev/sda1` |
>
> ---
>
> ## Bloco para Copiar
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
> `#Linux` `#DeletionCommands` `#DataDike` `#PAM` `#FSafer` `#PrivilegedAccessManagement` `#CommandControl`
