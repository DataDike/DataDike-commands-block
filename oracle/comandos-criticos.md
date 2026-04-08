# 🔴 Oracle Database - Comandos Críticos

`#Oracle` `#OracleDB` `#OracleDatabase` `#SQL` `#PLSQL` `#DBA` `#DataDike` `#PAM` `#FSafer`

> Comandos destrutivos e irreversíveis que podem comprometer todo o banco de dados Oracle.
>
> ---
>
> ## Tabela de Referência
>
> | Comando | Descrição | Exemplo |
> |---------|-----------|---------|
> | `DROP DATABASE` | Remove completamente o banco de dados | `DROP DATABASE;` |
> | `SHUTDOWN ABORT` | Desliga a instância abruptamente sem checkpoint | `SHUTDOWN ABORT;` |
> | `SHUTDOWN IMMEDIATE` | Desliga a instância cancelando transações ativas | `SHUTDOWN IMMEDIATE;` |
> | `ALTER SYSTEM KILL SESSION` | Mata uma sessão de usuário | `ALTER SYSTEM KILL SESSION '12,345' IMMEDIATE;` |
> | `ALTER SYSTEM SWITCH LOGFILE` | Força troca de redo log | `ALTER SYSTEM SWITCH LOGFILE;` |
> | `ALTER DATABASE OPEN RESETLOGS` | Abre banco com reset dos redo logs | `ALTER DATABASE OPEN RESETLOGS;` |
> | `ALTER SYSTEM SET` | Altera parâmetros do sistema em tempo real | `ALTER SYSTEM SET db_recovery_file_dest_size=10G;` |
> | `ALTER SYSTEM FLUSH SHARED_POOL` | Limpa o shared pool (cache de SQL) | `ALTER SYSTEM FLUSH SHARED_POOL;` |
> | `ALTER SYSTEM FLUSH BUFFER_CACHE` | Limpa o buffer cache (cache de dados) | `ALTER SYSTEM FLUSH BUFFER_CACHE;` |
> | `ALTER SYSTEM CHECKPOINT` | Força checkpoint global | `ALTER SYSTEM CHECKPOINT;` |
> | `ALTER SYSTEM ARCHIVE LOG ALL` | Força archiving de todos os redo logs | `ALTER SYSTEM ARCHIVE LOG ALL;` |
> | `ALTER SYSTEM DISABLE RESTRICTED SESSION` | Desabilita modo restrito | `ALTER SYSTEM DISABLE RESTRICTED SESSION;` |
> | `ALTER SYSTEM ENABLE RESTRICTED SESSION` | Habilita modo restrito (bloqueia novos logins) | `ALTER SYSTEM ENABLE RESTRICTED SESSION;` |
> | `ALTER DATABASE NOARCHIVELOG` | Desabilita modo archivelog (risco de perda) | `ALTER DATABASE NOARCHIVELOG;` |
> | `ALTER TABLESPACE OFFLINE` | Coloca tablespace offline | `ALTER TABLESPACE users OFFLINE;` |
> | `DROP TABLESPACE ... INCLUDING CONTENTS` | Remove tablespace e todos os dados | `DROP TABLESPACE users INCLUDING CONTENTS AND DATAFILES;` |
> | `ALTER SYSTEM RESET` | Reseta parâmetro do sistema | `ALTER SYSTEM RESET open_cursors;` |
> | `STARTUP RESTRICT` | Inicia banco em modo restrito | `STARTUP RESTRICT;` |
> | `ALTER PLUGGABLE DATABASE CLOSE` | Fecha um PDB (container database) | `ALTER PLUGGABLE DATABASE pdb1 CLOSE IMMEDIATE;` |
> | `RECOVER DATABASE` | Executa recovery do banco (operação crítica) | `RECOVER DATABASE USING BACKUP CONTROLFILE;` |
>
> ---
>
> ## Bloco para Copiar
>
> ```
> DROP DATABASE
> SHUTDOWN ABORT
> SHUTDOWN IMMEDIATE
> ALTER SYSTEM KILL SESSION
> ALTER SYSTEM SWITCH LOGFILE
> ALTER DATABASE OPEN RESETLOGS
> ALTER SYSTEM SET
> ALTER SYSTEM FLUSH SHARED_POOL
> ALTER SYSTEM FLUSH BUFFER_CACHE
> ALTER SYSTEM CHECKPOINT
> ALTER SYSTEM ARCHIVE LOG ALL
> ALTER SYSTEM DISABLE RESTRICTED SESSION
> ALTER SYSTEM ENABLE RESTRICTED SESSION
> ALTER DATABASE NOARCHIVELOG
> ALTER TABLESPACE OFFLINE
> DROP TABLESPACE INCLUDING CONTENTS
> ALTER SYSTEM RESET
> STARTUP RESTRICT
> ALTER PLUGGABLE DATABASE CLOSE
> RECOVER DATABASE
> ```
>
> ---
>
> `#Oracle` `#CriticalCommands` `#DataDike` `#PAM` `#FSafer` `#PrivilegedAccessManagement` `#CommandControl`
