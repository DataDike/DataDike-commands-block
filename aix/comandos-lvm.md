# 🟠 IBM AIX - Comandos de LVM

`#IBM` `#AIX` `#IBMAIX` `#PowerSystems` `#UNIX` `#IBMPower` `#DataDike` `#PAM` `#FSafer`

> Comandos para Logical Volume Manager e storage no IBM AIX.
>
> ---
>
> ## Tabela de Referência
>
> | Comando | Descrição | Exemplo |
> |---------|-----------|---------|
> | `mkvg` | Cria volume group | `mkvg -y datavg hdisk1` |
> | `extendvg` | Adiciona disco ao volume group | `extendvg datavg hdisk2` |
> | `reducevg` | Remove disco do volume group | `reducevg datavg hdisk2` |
> | `exportvg` | Exporta volume group (remove do sistema) | `exportvg datavg` |
> | `importvg` | Importa volume group | `importvg -y datavg hdisk1` |
> | `varyonvg` | Ativa volume group | `varyonvg datavg` |
> | `varyoffvg` | Desativa volume group | `varyoffvg datavg` |
> | `chvg` | Altera atributos do volume group | `chvg -a y datavg` |
> | `mklv` | Cria logical volume | `mklv -y lv_dados -t jfs2 datavg 10G` |
> | `rmlv` | Remove logical volume | `rmlv lv_dados` |
> | `rmlv -f` | Remove LV forçadamente | `rmlv -f lv_temp` |
> | `extendlv` | Estende logical volume | `extendlv lv_dados 5G` |
> | `chlv` | Altera atributos do logical volume | `chlv -n lv_novo lv_antigo` |
> | `mklvcopy` | Cria mirror de logical volume | `mklvcopy lv_dados 2` |
> | `rmlvcopy` | Remove cópia mirror de LV | `rmlvcopy lv_dados 1` |
> | `crfs` | Cria filesystem | `crfs -v jfs2 -d lv_dados -m /dados -A yes` |
> | `rmfs` | Remove filesystem | `rmfs /dados` |
> | `chfs` | Altera filesystem (resize) | `chfs -a size=+5G /dados` |
> | `mount` | Monta filesystem | `mount /dados` |
> | `umount` | Desmonta filesystem | `umount /dados` |
> | `umount -f` | Desmonta forçadamente | `umount -f /dados` |
> | `mkfs` | Formata logical volume com filesystem | `mkfs -V jfs2 /dev/lv_dados` |
> | `fsck` | Verifica e repara filesystem | `fsck -y /dev/lv_dados` |
> | `migratepv` | Migra dados entre discos | `migratepv hdisk1 hdisk2` |
> | `replacepv` | Substitui disco no VG | `replacepv hdisk1 hdisk2` |
> | `chpv` | Altera atributos de physical volume | `chpv -a n hdisk1` |
> | `lspv` | Lista physical volumes | `lspv` |
> | `lsvg` | Lista volume groups | `lsvg -l rootvg` |
> | `lslv` | Lista logical volumes | `lslv lv_dados` |
>
> ---
>
> ## Bloco para Copiar
>
> ```
> mkvg
> extendvg
> reducevg
> exportvg
> importvg
> varyonvg
> varyoffvg
> chvg
> mklv
> rmlv
> rmlv -f
> extendlv
> chlv
> mklvcopy
> rmlvcopy
> crfs
> rmfs
> chfs
> mount
> umount
> umount -f
> mkfs
> fsck
> migratepv
> replacepv
> chpv
> lspv
> lsvg
> lslv
> ```
>
> ---
>
> `#AIX` `#LVMCommands` `#DataDike` `#PAM` `#FSafer` `#PrivilegedAccessManagement` `#CommandControl`
