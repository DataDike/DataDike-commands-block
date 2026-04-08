# 🟡 HP-UX (HPE) - Comandos de Exclusão

`#HPE` `#HPUX` `#HewlettPackardEnterprise` `#HPEServers` `#UNIX` `#DataDike` `#PAM` `#FSafer`

> Comandos para remoção de arquivos e dados no HP-UX.
>
> ---
>
> ## Tabela de Referência
>
> | Comando | Descrição | Exemplo |
> |---------|-----------|---------|
> | `rm` | Remove arquivos | `rm /tmp/arquivo.txt` |
> | `rm -r` | Remove diretórios recursivamente | `rm -r /tmp/pasta` |
> | `rm -f` | Remove forçadamente sem confirmação | `rm -f /var/adm/syslog/syslog.log` |
> | `rm -rf` | Remove recursivamente e forçadamente | `rm -rf /var/tmp/*` |
> | `rmdir` | Remove diretório vazio | `rmdir /tmp/vazio` |
> | `unlink` | Remove arquivo (link) | `unlink /tmp/arquivo` |
> | `find ... -exec rm` | Busca e remove por critério | `find /var/adm -name "*.old" -exec rm {} \;` |
> | `shred` | Sobrescreve arquivo de forma segura | `shred -vfz -n 5 /dados/sensivel.txt` |
> | `cat /dev/null >` | Zera conteúdo de arquivo | `cat /dev/null > /var/adm/syslog/syslog.log` |
> | `> arquivo` | Zera conteúdo via redirecionamento | `> /var/adm/wtmp` |
> | `truncate -s 0` | Zera arquivo (se disponível) | `truncate -s 0 /var/log/messages` |
> | `swremove` | Remove software/patch do sistema | `swremove PatchName` |
> | `lvremove` | Remove logical volume | `lvremove /dev/vg01/lvol1` |
> | `lvremove -f` | Remove LV forçadamente | `lvremove -f /dev/vg01/lvol1` |
> | `vgremove` | Remove volume group | `vgremove vg01` |
> | `pvremove` | Remove physical volume | `pvremove /dev/dsk/c0t1d0` |
> | `vgreduce` | Remove disco do volume group | `vgreduce vg01 /dev/dsk/c0t1d0` |
> | `vgexport` | Exporta (remove) volume group | `vgexport vg01` |
> | `fsadm -d` | Reduz filesystem (pode causar perda) | `fsadm -d -b 5242880 /dados` |
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
> find -exec rm
> shred
> cat /dev/null >
> > arquivo
> truncate -s 0
> swremove
> lvremove
> lvremove -f
> vgremove
> pvremove
> vgreduce
> vgexport
> fsadm -d
> ```
>
> ---
>
> `#HPUX` `#DeletionCommands` `#DataDike` `#PAM` `#FSafer` `#PrivilegedAccessManagement` `#CommandControl`
