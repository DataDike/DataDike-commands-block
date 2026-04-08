# 🔴 Linux - Comandos Críticos

`#Linux` `#Ubuntu` `#RedHat` `#RHEL` `#CentOS` `#Debian` `#SUSE` `#Bash` `#Shell` `#DataDike` `#PAM` `#FSafer`

> Comandos destrutivos e irreversíveis que podem comprometer todo o sistema operacional.

---

## Tabela de Referência

| Comando | Descrição | Exemplo |
|---------|-----------|---------|
| `rm -rf /` | Remove recursivamente todos os arquivos do sistema a partir da raiz | `rm -rf /` |
| `rm -rf /*` | Remove todos os diretórios e arquivos na raiz | `rm -rf /*` |
| `mkfs` | Formata uma partição/disco destruindo todos os dados | `mkfs.ext4 /dev/sda1` |
| `mkfs.ext4` | Formata partição com sistema de arquivos ext4 | `mkfs.ext4 /dev/sdb1` |
| `mkfs.xfs` | Formata partição com sistema de arquivos XFS | `mkfs.xfs /dev/sdc1` |
| `dd if=/dev/zero` | Sobrescreve disco/partição com zeros, destruindo dados | `dd if=/dev/zero of=/dev/sda bs=1M` |
| `dd if=/dev/urandom` | Sobrescreve disco com dados aleatórios | `dd if=/dev/urandom of=/dev/sda bs=1M` |
| `:(){ :|:& };:` | Fork bomb - cria processos infinitos até travar o sistema | `:(){ :|:& };:` |
| `chmod -R 000 /` | Remove todas as permissões de todos os arquivos do sistema | `chmod -R 000 /` |
| `chown -R nobody:nobody /` | Muda dono de todos os arquivos para nobody | `chown -R nobody:nobody /` |
| `kill -9 1` | Mata o processo init/systemd (PID 1) | `kill -9 1` |
| `echo "" > /etc/passwd` | Apaga o conteúdo do arquivo de usuários | `echo "" > /etc/passwd` |
| `echo "" > /etc/shadow` | Apaga o conteúdo do arquivo de senhas | `echo "" > /etc/shadow` |
| `> /etc/fstab` | Apaga a tabela de montagem de sistemas de arquivos | `> /etc/fstab` |
| `shred /dev/sda` | Sobrescreve disco múltiplas vezes, irrecuperável | `shred -vfz -n 5 /dev/sda` |
| `wipefs -a` | Remove assinaturas de filesystem de um dispositivo | `wipefs -a /dev/sda` |
| `parted rm` | Remove partição de um disco | `parted /dev/sda rm 1` |
| `fdisk` | Manipula tabela de partições (pode destruir partições) | `fdisk /dev/sda` |
| `swapoff -a && swapon -a` | Desabilita e reabilita swap (pode causar OOM) | `swapoff -a` |
| `init 0` | Desliga o sistema imediatamente | `init 0` |
| `init 6` | Reinicia o sistema imediatamente | `init 6` |
| `shutdown -h now` | Desliga o servidor imediatamente | `shutdown -h now` |
| `reboot -f` | Reinicia forçadamente sem desmontar filesystems | `reboot -f` |
| `halt -f` | Para o sistema forçadamente | `halt -f` |
| `poweroff -f` | Desliga forçadamente | `poweroff -f` |

---

## Bloco para Copiar

```
rm -rf /
rm -rf /*
mkfs
mkfs.ext4
mkfs.xfs
dd if=/dev/zero
dd if=/dev/urandom
:(){ :|:& };:
chmod -R 000 /
chown -R nobody:nobody /
kill -9 1
echo "" > /etc/passwd
echo "" > /etc/shadow
> /etc/fstab
shred
wipefs -a
parted rm
fdisk
swapoff -a
init 0
init 6
shutdown -h now
reboot -f
halt -f
poweroff -f
```

---

`#Linux` `#CriticalCommands` `#DataDike` `#PAM` `#FSafer` `#PrivilegedAccessManagement` `#CommandControl`
