**[English](#english)** | **[Português](#português)** | **[Español](#español)**

---

# English

# Linux - Critical Commands

`#Linux` `#Ubuntu` `#RedHat` `#RHEL` `#CentOS` `#Debian` `#SUSE` `#Bash` `#Shell` `#DataDike` `#PAM` `#FSafer`

> Destructive and irreversible commands that can compromise the entire operating system.

---

## Reference Table

| Command | Description | Example |
|---------|-------------|---------|
| `rm -rf /` | Recursively removes all files from root | `rm -rf /` |
| `rm -rf /*` | Removes all directories and files at root | `rm -rf /*` |
| `mkfs` | Formats a partition/disk destroying all data | `mkfs.ext4 /dev/sda1` |
| `mkfs.ext4` | Formats partition with ext4 filesystem | `mkfs.ext4 /dev/sdb1` |
| `mkfs.xfs` | Formats partition with XFS filesystem | `mkfs.xfs /dev/sdc1` |
| `dd if=/dev/zero` | Overwrites disk/partition with zeros | `dd if=/dev/zero of=/dev/sda bs=1M` |
| `dd if=/dev/urandom` | Overwrites disk with random data | `dd if=/dev/urandom of=/dev/sda bs=1M` |
| `:(){ :|:& };:` | Fork bomb - creates infinite processes until crash | `:(){ :|:& };:` |
| `chmod -R 000 /` | Removes all permissions from all files | `chmod -R 000 /` |
| `chown -R nobody:nobody /` | Changes owner of all files to nobody | `chown -R nobody:nobody /` |
| `kill -9 1` | Kills init/systemd process (PID 1) | `kill -9 1` |
| `echo "" > /etc/passwd` | Erases user file contents | `echo "" > /etc/passwd` |
| `echo "" > /etc/shadow` | Erases password file contents | `echo "" > /etc/shadow` |
| `> /etc/fstab` | Erases filesystem mount table | `> /etc/fstab` |
| `shred /dev/sda` | Overwrites disk multiple times, unrecoverable | `shred -vfz -n 5 /dev/sda` |
| `wipefs -a` | Removes filesystem signatures from device | `wipefs -a /dev/sda` |
| `parted rm` | Removes partition from disk | `parted /dev/sda rm 1` |
| `fdisk` | Manipulates partition table (can destroy partitions) | `fdisk /dev/sda` |
| `swapoff -a && swapon -a` | Disables and re-enables swap (may cause OOM) | `swapoff -a` |
| `init 0` | Shuts down system immediately | `init 0` |
| `init 6` | Reboots system immediately | `init 6` |
| `shutdown -h now` | Shuts down server immediately | `shutdown -h now` |
| `reboot -f` | Force reboots without unmounting filesystems | `reboot -f` |
| `halt -f` | Force halts the system | `halt -f` |
| `poweroff -f` | Force powers off | `poweroff -f` |

## Copy Block

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

# Português

# Linux - Comandos Críticos

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

# Español

# Linux - Comandos Críticos

`#Linux` `#Ubuntu` `#RedHat` `#RHEL` `#CentOS` `#Debian` `#SUSE` `#Bash` `#Shell` `#DataDike` `#PAM` `#FSafer`

> Comandos destructivos e irreversibles que pueden comprometer todo el sistema operativo.

---

## Tabla de Referencia

| Comando | Descripción | Ejemplo |
|---------|-------------|---------|
| `rm -rf /` | Elimina recursivamente todos los archivos del sistema desde la raíz | `rm -rf /` |
| `rm -rf /*` | Elimina todos los directorios y archivos en la raíz | `rm -rf /*` |
| `mkfs` | Formatea una partición/disco destruyendo todos los datos | `mkfs.ext4 /dev/sda1` |
| `mkfs.ext4` | Formatea partición con sistema de archivos ext4 | `mkfs.ext4 /dev/sdb1` |
| `mkfs.xfs` | Formatea partición con sistema de archivos XFS | `mkfs.xfs /dev/sdc1` |
| `dd if=/dev/zero` | Sobrescribe disco/partición con ceros, destruyendo datos | `dd if=/dev/zero of=/dev/sda bs=1M` |
| `dd if=/dev/urandom` | Sobrescribe disco con datos aleatorios | `dd if=/dev/urandom of=/dev/sda bs=1M` |
| `:(){ :|:& };:` | Fork bomb - crea procesos infinitos hasta bloquear el sistema | `:(){ :|:& };:` |
| `chmod -R 000 /` | Elimina todos los permisos de todos los archivos del sistema | `chmod -R 000 /` |
| `chown -R nobody:nobody /` | Cambia el propietario de todos los archivos a nobody | `chown -R nobody:nobody /` |
| `kill -9 1` | Mata el proceso init/systemd (PID 1) | `kill -9 1` |
| `echo "" > /etc/passwd` | Borra el contenido del archivo de usuarios | `echo "" > /etc/passwd` |
| `echo "" > /etc/shadow` | Borra el contenido del archivo de contraseñas | `echo "" > /etc/shadow` |
| `> /etc/fstab` | Borra la tabla de montaje de sistemas de archivos | `> /etc/fstab` |
| `shred /dev/sda` | Sobrescribe disco múltiples veces, irrecuperable | `shred -vfz -n 5 /dev/sda` |
| `wipefs -a` | Elimina firmas de filesystem de un dispositivo | `wipefs -a /dev/sda` |
| `parted rm` | Elimina partición de un disco | `parted /dev/sda rm 1` |
| `fdisk` | Manipula tabla de particiones (puede destruir particiones) | `fdisk /dev/sda` |
| `swapoff -a && swapon -a` | Deshabilita y rehabilita swap (puede causar OOM) | `swapoff -a` |
| `init 0` | Apaga el sistema inmediatamente | `init 0` |
| `init 6` | Reinicia el sistema inmediatamente | `init 6` |
| `shutdown -h now` | Apaga el servidor inmediatamente | `shutdown -h now` |
| `reboot -f` | Reinicia forzadamente sin desmontar filesystems | `reboot -f` |
| `halt -f` | Detiene el sistema forzadamente | `halt -f` |
| `poweroff -f` | Apaga forzadamente | `poweroff -f` |

## Bloque para Copiar

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
