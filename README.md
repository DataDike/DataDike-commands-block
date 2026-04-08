# PAM Command Catalog - DataDike

Catálogo de comandos sensíveis organizados por **vendor** e **categoria** para uso na plataforma **PAM FSafer** da **DataDike**.

> Cada documento contém a lista completa de comandos com explicação + um bloco pronto para copiar todos os comandos de uma vez.
>
> ---
>
> ## Vendors
>
> ### 🐧 Linux
> `#Linux` `#Ubuntu` `#RedHat` `#RHEL` `#CentOS` `#Debian` `#SUSE` `#Bash` `#Shell`
>
> | Documento | Descrição |
> |-----------|-----------|
> | [Comandos Críticos](./linux/comandos-criticos.md) | Comandos destrutivos e irreversíveis |
> | [Comandos de Exclusão](./linux/comandos-exclusao.md) | Remoção de arquivos, diretórios e dados |
> | [Comandos de Rede](./linux/comandos-rede.md) | Configuração e manipulação de rede |
> | [Comandos de Usuários](./linux/comandos-usuarios.md) | Gestão de contas, grupos e permissões |
> | [Comandos de Serviços](./linux/comandos-servicos.md) | Controle de serviços e processos |
>
> ### 🏢 Oracle Database
> `#Oracle` `#OracleDB` `#OracleDatabase` `#SQL` `#PLSQL` `#DBA`
>
> | Documento | Descrição |
> |-----------|-----------|
> | [Comandos Críticos](./oracle-db/comandos-criticos.md) | DROP DATABASE, SHUTDOWN e operações destrutivas |
> | [Comandos de Exclusão](./oracle-db/comandos-exclusao.md) | DROP, DELETE, TRUNCATE de objetos |
> | [Comandos de Permissões](./oracle-db/comandos-permissoes.md) | GRANT, REVOKE e controle de acesso |
>
> ### 🛡️ Fortinet FortiGate
> `#Fortinet` `#FortiGate` `#FortiOS` `#Firewall` `#NGFW` `#FortinetSecurity`
>
> | Documento | Descrição |
> |-----------|-----------|
> | [Comandos Críticos](./fortinet/comandos-criticos.md) | Factory reset, format e operações destrutivas |
> | [Comandos de Firewall](./fortinet/comandos-firewall.md) | Políticas, regras e objetos de firewall |
> | [Comandos de VPN](./fortinet/comandos-vpn.md) | Configuração e gestão de VPNs |
> | [Comandos de Sistema](./fortinet/comandos-sistema.md) | Configurações globais e administrativas |
>
> ### 🌐 Cisco IOS / IOS-XE
> `#Cisco` `#CiscoIOS` `#CiscoIOSXE` `#CiscoRouter` `#CiscoSwitch` `#CiscoNetworking`
>
> | Documento | Descrição |
> |-----------|-----------|
> | [Comandos Críticos](./cisco/comandos-criticos.md) | Erase, reload e operações destrutivas |
> | [Comandos de Interfaces](./cisco/comandos-interfaces.md) | Configuração e shutdown de interfaces |
> | [Comandos de Routing](./cisco/comandos-routing.md) | Protocolos de roteamento e rotas |
> | [Comandos de ACL](./cisco/comandos-acl.md) | Access Control Lists e segurança |
>
> ### 🪟 Windows Server
> `#Windows` `#WindowsServer` `#PowerShell` `#CMD` `#ActiveDirectory` `#Microsoft`
>
> | Documento | Descrição |
> |-----------|-----------|
> | [Comandos Críticos](./windows-server/comandos-criticos.md) | Format, diskpart e operações destrutivas |
> | [Comandos de Exclusão](./windows-server/comandos-exclusao.md) | Remove-Item, del e remoção de dados |
> | [Comandos de Rede](./windows-server/comandos-rede.md) | Configuração de rede e firewall |
> | [Comandos de Serviços](./windows-server/comandos-servicos.md) | Controle de serviços e processos |
> | [Comandos de Usuários](./windows-server/comandos-usuarios.md) | Active Directory e gestão de contas |
>
> ### 🖥️ IBM AIX
> `#IBM` `#AIX` `#IBMAIX` `#PowerSystems` `#UNIX` `#IBMPower`
>
> | Documento | Descrição |
> |-----------|-----------|
> | [Comandos Críticos](./aix/comandos-criticos.md) | Comandos destrutivos e irreversíveis |
> | [Comandos de Exclusão](./aix/comandos-exclusao.md) | Remoção de arquivos e dados |
> | [Comandos de LVM](./aix/comandos-lvm.md) | Logical Volume Manager e storage |
> | [Comandos de Rede](./aix/comandos-rede.md) | Configuração de rede e interfaces |
> | [Comandos de Usuários](./aix/comandos-usuarios.md) | Gestão de contas e segurança |
>
> ### 🔧 HP-UX (HPE)
> `#HPE` `#HPUX` `#HewlettPackardEnterprise` `#HPEServers` `#UNIX`
>
> | Documento | Descrição |
> |-----------|-----------|
> | [Comandos Críticos](./hpux/comandos-criticos.md) | Comandos destrutivos e irreversíveis |
> | [Comandos de Exclusão](./hpux/comandos-exclusao.md) | Remoção de arquivos e dados |
> | [Comandos de Rede](./hpux/comandos-rede.md) | Configuração de rede e interfaces |
> | [Comandos de Usuários](./hpux/comandos-usuarios.md) | Gestão de contas e segurança |
>
> ---
>
> ## Formato dos Documentos
>
> Cada documento possui duas seções:
>
> 1. **Tabela de Referência** — Comando + Descrição + Exemplo de uso
> 2. 2. **Bloco para Copiar** — Todos os comandos em um bloco de código, prontos para copiar com um clique
>   
>    3. ## Integração com PAM FSafer
>   
>    4. Estes catálogos servem como referência para configurar as políticas de **Command Control** no PAM FSafer da DataDike.
>   
>    5. ---
>
>    6. `#DataDike` `#PAM` `#PrivilegedAccessManagement` `#FSafer` `#CyberSecurity` `#InfoSec` `#CommandControl` `#ZeroTrust`
