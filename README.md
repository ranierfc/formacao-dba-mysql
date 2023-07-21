# Formação DBA do MySQL

Esta formação tem como objetivo passar pelos principais tópicos para se tornar um DBA do MySQL.

**Tópicos abordados**: 
1. [Instalação do MySQL Community](#1-instalação-do-mysql-community)
2. [Contecatando e criando novo usuário](#2-contecatando-e-criando-novo-usuário)

## 1. Instalação do MySQL Community

Começaremos com a instalação do MySQL no Ubuntu.

```shell
sudo apt update
sudo apt upgrade -y
sudo apt install mysql-server
mysql --version
```

Verificando status do processo

```shell
service mysql status
```

## 2. Contecatando e criando novo usuário
Conectando com usuário `root`

```shell
sudo mysql -u root -p
```

Criando novo usuário

```sql
create user ['username']@['host'] identified by 'password';
```

Concedendo todos os privilégios para o novo usuário

```sql
grant all privileges on *.* to [username];
```