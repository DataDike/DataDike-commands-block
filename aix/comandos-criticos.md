# 🔴 IBM AIX - Comandos Críticos

`#IBM` `#AIX` `#IBMAIX` `#PowerSystems` `#UNIX` `#IBMPower` `#DataDike` `#PAM` `#FSafer`

> Comandos destrutivos e irreversíveis no IBM AIX.
>
> ---
>
> ## Tabela de Referência
>
> | Comando | Descrição | Exemplo |
> |---------|-----------|---------|
> | `rm -rf /` | Remove todos os arquivos do sistema | `rm -rf /` |
> | `rm -rf /*` | Remove todos os diretórios na raiz | `rm -rf /*` |
> | `mkfs` | Formata filesystem | `mkfs -V jfs2 /dev/lv_dados` |
> | `dd if=/dev/zero` | Sobrescreve disco/LV com zeros | `dd if=/dev/zero of=/dev/hdisk0 bs=1M` |
> | `bosboot` | Recria boot image (crítico se falhar) | `bosboot -a -d /dev/hdisk0` |
> | `shutdown -F` | Desliga sistema imediatamente | `shutdown -F` |
> | `halt` | Para o sistema | `halt` |
> | `reboot` | Reinicia o sistema | `reboot` |
> | `shutdown -r now` | Reinicia imediatamente | `shutdown -r now` |
> | `mksysb` | Cria backup do sistema (pode impactar) | `mksysb -i /dev/rmt0` |
> | `alt_disk_install` | Instalação em disco alternativo | `alt_disk_install -d hdisk1` |
> | `installp -u` | Desinstala filesets/packages | `installp -u bos.net.tcp.client` |
> | `instfix -k` | Remove fix/patch | `instfix -k IJ12345` |
> | `rmdev -dl` | Remove device permanentemente | `rmdev -dl hdisk2` |
> | `cfgmgr` | Reconfigura dispositivos (pode causar mudanças) | `cfgmgr` |
> | `chdev` | Altera atributos de device | `chdev -l sys0 -a maxuproc=4096` |
> | `bootlist` | Altera lista de boot | `bootlist -m normal hdisk0 hdisk1` |
> | `smitty` | Interface de administração (acesso total) | `smitty` |
> | `diag` | Diagnóstico de hardware | `diag` |
> | `savebase` | Salva configuração de devices na base | `savebase` |
>
> ---
>
> ## Bloco para Copiar
>
> ```
> rm -rf /
> rm -rf /*
> mkfs
> dd if=/dev/zero
> bosboot
> shutdown -F
> halt
> reboot
> shutdown -r now
> mksysb
> alt_disk_install
> installp -u
> instfix -k
> rmdev -dl
> cfgmgr
> chdev
> bootlist
> smitty
> diag
> savebase
> ```
>
> ---
>
> `#AIX` `#CriticalCommands` `#DataDike` `#PAM` `#FSafer` `#PrivilegedAccessManagement` `#CommandControl`
