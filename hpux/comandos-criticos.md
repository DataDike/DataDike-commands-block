# 🔴 HP-UX (HPE) - Comandos Críticos

`#HPE` `#HPUX` `#HewlettPackardEnterprise` `#HPEServers` `#UNIX` `#DataDike` `#PAM` `#FSafer`

> Comandos destrutivos e irreversíveis no HP-UX.
>
> ---
>
> ## Tabela de Referência
>
> | Comando | Descrição | Exemplo |
> |---------|-----------|---------|
> | `rm -rf /` | Remove todos os arquivos do sistema | `rm -rf /` |
> | `rm -rf /*` | Remove todos os diretórios na raiz | `rm -rf /*` |
> | `mkfs` | Formata filesystem | `mkfs -F vxfs /dev/vg00/rlvol1` |
> | `newfs` | Cria novo filesystem (formata) | `newfs -F vxfs /dev/vg00/rlvol1` |
> | `dd if=/dev/zero` | Sobrescreve disco com zeros | `dd if=/dev/zero of=/dev/rdsk/c0t0d0 bs=1024k` |
> | `shutdown -h` | Desliga sistema | `shutdown -h now` |
> | `shutdown -r` | Reinicia sistema | `shutdown -r now` |
> | `reboot` | Reinicia imediatamente | `reboot` |
> | `halt` | Para o sistema | `halt` |
> | `init 0` | Desliga o sistema | `init 0` |
> | `init 6` | Reinicia o sistema | `init 6` |
> | `setboot` | Altera dispositivo de boot | `setboot -p /dev/dsk/c0t0d0` |
> | `mk_kernel` | Reconstrói kernel (crítico) | `mk_kernel` |
> | `kmtune` | Altera parâmetros do kernel | `kmtune -s maxdsiz=1073741824` |
> | `kctune` | Altera configuráveis do kernel (11.31+) | `kctune maxdsiz=1073741824` |
> | `swinstall` | Instala software (pode alterar sistema) | `swinstall -s /tmp/patch.depot` |
> | `swremove` | Remove software do sistema | `swremove PatchName` |
> | `make_recovery` | Cria imagem de recovery | `make_recovery -A` |
> | `vgexport` | Exporta volume group | `vgexport vg01` |
> | `lvremove` | Remove logical volume | `lvremove /dev/vg01/lvol1` |
> | `vgremove` | Remove volume group | `vgremove vg01` |
> | `pvremove` | Remove physical volume | `pvremove /dev/dsk/c0t1d0` |
> | `ioinit` | Reinicializa I/O (operação crítica) | `ioinit` |
> | `insf -e` | Instala arquivos de device | `insf -e` |
>
> ---
>
> ## Bloco para Copiar
>
> ```
> rm -rf /
> rm -rf /*
> mkfs
> newfs
> dd if=/dev/zero
> shutdown -h
> shutdown -r
> reboot
> halt
> init 0
> init 6
> setboot
> mk_kernel
> kmtune
> kctune
> swinstall
> swremove
> make_recovery
> vgexport
> lvremove
> vgremove
> pvremove
> ioinit
> insf -e
> ```
>
> ---
>
> `#HPUX` `#CriticalCommands` `#DataDike` `#PAM` `#FSafer` `#PrivilegedAccessManagement` `#CommandControl`
