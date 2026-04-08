# 🔵 Oracle Database - Comandos de Permissões

`#Oracle` `#OracleDB` `#OracleDatabase` `#SQL` `#PLSQL` `#DBA` `#DataDike` `#PAM` `#FSafer`

> Comandos GRANT, REVOKE e controle de acesso no Oracle Database.
>
> ---
>
> ## Tabela de Referência
>
> | Comando | Descrição | Exemplo |
> |---------|-----------|---------|
> | `GRANT DBA` | Concede role DBA a um usuário | `GRANT DBA TO joao;` |
> | `GRANT SYSDBA` | Concede privilégio SYSDBA | `GRANT SYSDBA TO joao;` |
> | `GRANT SYSOPER` | Concede privilégio SYSOPER | `GRANT SYSOPER TO joao;` |
> | `GRANT ALL PRIVILEGES` | Concede todos os privilégios de sistema | `GRANT ALL PRIVILEGES TO joao;` |
> | `GRANT SELECT` | Concede permissão de leitura em tabela | `GRANT SELECT ON clientes TO joao;` |
> | `GRANT INSERT` | Concede permissão de inserção | `GRANT INSERT ON clientes TO joao;` |
> | `GRANT UPDATE` | Concede permissão de atualização | `GRANT UPDATE ON clientes TO joao;` |
> | `GRANT DELETE` | Concede permissão de exclusão | `GRANT DELETE ON clientes TO joao;` |
> | `GRANT EXECUTE` | Concede permissão de execução em procedure/function | `GRANT EXECUTE ON pkg_financeiro TO joao;` |
> | `GRANT CREATE SESSION` | Permite que usuário conecte ao banco | `GRANT CREATE SESSION TO joao;` |
> | `GRANT CREATE TABLE` | Permite criação de tabelas | `GRANT CREATE TABLE TO joao;` |
> | `GRANT CREATE USER` | Permite criação de usuários | `GRANT CREATE USER TO joao;` |
> | `GRANT DROP ANY TABLE` | Permite remover qualquer tabela | `GRANT DROP ANY TABLE TO joao;` |
> | `GRANT ALTER ANY TABLE` | Permite alterar qualquer tabela | `GRANT ALTER ANY TABLE TO joao;` |
> | `GRANT SELECT ANY TABLE` | Permite ler qualquer tabela | `GRANT SELECT ANY TABLE TO joao;` |
> | `GRANT WITH ADMIN OPTION` | Concede privilégio com direito de repassar | `GRANT DBA TO joao WITH ADMIN OPTION;` |
> | `GRANT WITH GRANT OPTION` | Concede privilégio de objeto com direito de repassar | `GRANT SELECT ON clientes TO joao WITH GRANT OPTION;` |
> | `REVOKE DBA` | Remove role DBA de um usuário | `REVOKE DBA FROM joao;` |
> | `REVOKE ALL PRIVILEGES` | Remove todos os privilégios | `REVOKE ALL PRIVILEGES FROM joao;` |
> | `REVOKE SELECT` | Remove permissão de leitura | `REVOKE SELECT ON clientes FROM joao;` |
> | `REVOKE CREATE SESSION` | Remove permissão de conexão | `REVOKE CREATE SESSION FROM joao;` |
> | `CREATE ROLE` | Cria nova role de segurança | `CREATE ROLE role_leitura;` |
> | `ALTER USER ... IDENTIFIED BY` | Altera senha de usuário | `ALTER USER joao IDENTIFIED BY nova_senha;` |
> | `ALTER USER ... ACCOUNT LOCK` | Bloqueia conta de usuário | `ALTER USER joao ACCOUNT LOCK;` |
> | `ALTER USER ... ACCOUNT UNLOCK` | Desbloqueia conta de usuário | `ALTER USER joao ACCOUNT UNLOCK;` |
> | `ALTER USER ... PROFILE` | Altera perfil de recurso do usuário | `ALTER USER joao PROFILE perfil_restrito;` |
> | `ALTER USER ... DEFAULT TABLESPACE` | Altera tablespace padrão do usuário | `ALTER USER joao DEFAULT TABLESPACE ts_dados;` |
> | `ALTER USER ... QUOTA` | Altera cota de espaço do usuário | `ALTER USER joao QUOTA UNLIMITED ON ts_dados;` |
> | `CREATE PROFILE` | Cria perfil de recurso e senha | `CREATE PROFILE perfil_restrito LIMIT FAILED_LOGIN_ATTEMPTS 3;` |
> | `ALTER PROFILE` | Altera perfil de recurso | `ALTER PROFILE perfil_restrito LIMIT PASSWORD_LIFE_TIME 90;` |
> | `AUDIT` | Ativa auditoria em operações | `AUDIT SELECT ON clientes BY ACCESS;` |
> | `NOAUDIT` | Desativa auditoria | `NOAUDIT SELECT ON clientes;` |
>
> ---
>
> ## Bloco para Copiar
>
> ```
> GRANT DBA
> GRANT SYSDBA
> GRANT SYSOPER
> GRANT ALL PRIVILEGES
> GRANT SELECT
> GRANT INSERT
> GRANT UPDATE
> GRANT DELETE
> GRANT EXECUTE
> GRANT CREATE SESSION
> GRANT CREATE TABLE
> GRANT CREATE USER
> GRANT DROP ANY TABLE
> GRANT ALTER ANY TABLE
> GRANT SELECT ANY TABLE
> GRANT WITH ADMIN OPTION
> GRANT WITH GRANT OPTION
> REVOKE DBA
> REVOKE ALL PRIVILEGES
> REVOKE SELECT
> REVOKE CREATE SESSION
> CREATE ROLE
> ALTER USER IDENTIFIED BY
> ALTER USER ACCOUNT LOCK
> ALTER USER ACCOUNT UNLOCK
> ALTER USER PROFILE
> ALTER USER DEFAULT TABLESPACE
> ALTER USER QUOTA
> CREATE PROFILE
> ALTER PROFILE
> AUDIT
> NOAUDIT
> ```
>
> ---
>
> `#Oracle` `#PermissionCommands` `#DataDike` `#PAM` `#FSafer` `#PrivilegedAccessManagement` `#CommandControl`
