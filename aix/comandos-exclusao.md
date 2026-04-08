# 🟡 IBM AIX - Comandos de Exclusão

`#IBM` `#AIX` `#IBMAIX` `#PowerSystems` `#UNIX` `#IBMPower` `#DataDike` `#PAM` `#FSafer`

> Comandos para remoção de arquivos e dados no IBM AIX.
>
> ---
>
> ## Tabela de Referência
>
> | Comando | Descrição | Exemplo |
> |---------|-----------|---------|
> | `rm` | Remove arquivos | `rm /tmp/arquivo.txt` |
> | `rm -r` | Remove diretórios recursivamente | `rm -r /tmp/pasta` |
> | `rm -f` | Remove forçadamente sem confirmação | `rm -f /var/log/antigo.log` |
> | `rm -rf` | Remove recursivamente e forçadamente | `rm -rf /var/tmp/*` |
> | `rmdir` | Remove diretório vazio | `rmdir /tmp/vazio` |
> | `unlink` | Remove arquivo (link) | `unlink /tmp/arquivo` |
> | `find ... -exec rm` | Busca e remove por critério | `find /var/log -name "*.gz" -exec rm {} \;` |
> | `find ... -delete` | Busca e remove arquivos | `find /tmp -mtime +30 -delete` |
> | `shred` | Sobrescreve arquivo de forma segura | `shred -vfz -n 5 /dados/sensivel.txt` |
> | `truncate -s 0` | Zera conteúdo de arquivo | `truncate -s 0 /var/log/syslog` |
> | `cat /dev/null >` | Zera arquivo usando redirecionamento | `cat /dev/null > /var/log/messages` |
> | `> arquivo` | Zera conteúdo via redirecionamento | `> /var/adm/wtmp` |
> | `installp -u` | Remove fileset/package AIX | `installp -u bos.adt.include` |
> | `installp -C` | Limpa instalações incompletas | `installp -C` |
> | `lslpp -l / installp -u` | Lista e remove software | `installp -u package.name` |
> | `rmlv` | Remove logical volume | `rmlv lv_temp` |
> | `rmlv -f` | Remove LV forçadamente | `rmlv -f lv_dados` |
> | `rmfs` | Remove filesystem | `rmfs /dados` |
> | `reducevg` | Remove disco de volume group | `reducevg rootvg hdisk1` |
> | `exportvg` | Exporta (remove) volume group | `exportvg datavg` |
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
> find -delete
> shred
> truncate -s 0
> cat /dev/null >
> > arquivo
> installp -u
> installp -C
> rmlv
> rmlv -f
> rmfs
> reducevg
> exportvg
> ```
>
> ---
>
> `#AIX` `#DeletionCommands` `#DataDike` `#PAM` `#FSafer` `#PrivilegedAccessManagement` `#CommandControl`
