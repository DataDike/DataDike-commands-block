# 🟡 Oracle Database - Comandos de Exclusão

`#Oracle` `#OracleDB` `#OracleDatabase` `#SQL` `#PLSQL` `#DBA` `#DataDike` `#PAM` `#FSafer`

> Comandos DROP, DELETE e TRUNCATE para remoção de objetos e dados no Oracle Database.
>
> ---
>
> ## Tabela de Referência
>
> | Comando | Descrição | Exemplo |
> |---------|-----------|---------|
> | `DROP TABLE` | Remove tabela e todos os seus dados | `DROP TABLE clientes CASCADE CONSTRAINTS;` |
> | `DROP TABLE ... PURGE` | Remove tabela sem enviar para lixeira | `DROP TABLE clientes PURGE;` |
> | `DROP INDEX` | Remove índice de tabela | `DROP INDEX idx_clientes_nome;` |
> | `DROP VIEW` | Remove view do banco | `DROP VIEW vw_relatorio;` |
> | `DROP SEQUENCE` | Remove sequence | `DROP SEQUENCE seq_clientes;` |
> | `DROP SYNONYM` | Remove synonym | `DROP SYNONYM syn_clientes;` |
> | `DROP PROCEDURE` | Remove stored procedure | `DROP PROCEDURE sp_atualiza_saldo;` |
> | `DROP FUNCTION` | Remove function | `DROP FUNCTION fn_calcula_juros;` |
> | `DROP PACKAGE` | Remove package e body | `DROP PACKAGE pkg_financeiro;` |
> | `DROP TRIGGER` | Remove trigger | `DROP TRIGGER trg_audit_login;` |
> | `DROP TYPE` | Remove tipo de objeto | `DROP TYPE tp_endereco FORCE;` |
> | `DROP MATERIALIZED VIEW` | Remove materialized view | `DROP MATERIALIZED VIEW mv_vendas;` |
> | `DROP TABLESPACE` | Remove tablespace | `DROP TABLESPACE ts_dados INCLUDING CONTENTS AND DATAFILES;` |
> | `DROP USER CASCADE` | Remove usuário e todos os seus objetos | `DROP USER joao CASCADE;` |
> | `DROP PROFILE` | Remove perfil de recurso | `DROP PROFILE perfil_dev CASCADE;` |
> | `DROP ROLE` | Remove role de segurança | `DROP ROLE role_leitura;` |
> | `DROP DATABASE LINK` | Remove database link | `DROP DATABASE LINK link_remoto;` |
> | `DROP DIRECTORY` | Remove objeto directory | `DROP DIRECTORY dir_backup;` |
> | `DELETE FROM` | Remove registros de uma tabela | `DELETE FROM clientes WHERE status = 'inativo';` |
> | `DELETE FROM (sem WHERE)` | Remove todos os registros de uma tabela | `DELETE FROM log_acessos;` |
> | `TRUNCATE TABLE` | Remove todos os registros sem log (irreversível) | `TRUNCATE TABLE log_acessos;` |
> | `PURGE TABLE` | Remove tabela da lixeira permanentemente | `PURGE TABLE clientes;` |
> | `PURGE RECYCLEBIN` | Esvazia a lixeira do usuário | `PURGE RECYCLEBIN;` |
> | `PURGE DBA_RECYCLEBIN` | Esvazia lixeira de todos os usuários | `PURGE DBA_RECYCLEBIN;` |
> | `ALTER TABLE ... DROP COLUMN` | Remove coluna de tabela | `ALTER TABLE clientes DROP COLUMN telefone;` |
> | `ALTER TABLE ... DROP PARTITION` | Remove partição de tabela | `ALTER TABLE vendas DROP PARTITION p_2023;` |
>
> ---
>
> ## Bloco para Copiar
>
> ```
> DROP TABLE
> DROP TABLE PURGE
> DROP INDEX
> DROP VIEW
> DROP SEQUENCE
> DROP SYNONYM
> DROP PROCEDURE
> DROP FUNCTION
> DROP PACKAGE
> DROP TRIGGER
> DROP TYPE
> DROP MATERIALIZED VIEW
> DROP TABLESPACE
> DROP USER CASCADE
> DROP PROFILE
> DROP ROLE
> DROP DATABASE LINK
> DROP DIRECTORY
> DELETE FROM
> TRUNCATE TABLE
> PURGE TABLE
> PURGE RECYCLEBIN
> PURGE DBA_RECYCLEBIN
> ALTER TABLE DROP COLUMN
> ALTER TABLE DROP PARTITION
> ```
>
> ---
>
> `#Oracle` `#DeletionCommands` `#DataDike` `#PAM` `#FSafer` `#PrivilegedAccessManagement` `#CommandControl`
