# JavaDatabase

java构建SQL数据库系统。与下面以BNF形式列出的SQL语法一起使用。 该系统不使用任何外部库来设置数据库或解析SQL查询。 用DBServer在客户端上启动数据库，然后用client可以访问它。 运行后，可以在命令行中输入SQL查询。

基本数据结构创建：

CREATE DATABASE coursework; Server response: OK

USE coursework; Server response: OK

CREATE TABLE marks (name, mark); Server response: OK

将数据添加到表时，其他查询包括：

SELECT * FROM marks; Server response: id name mark 1 Steve 65 2 Dave 55 3 Bob 35 4 Clive 20

DELETE FROM marks WHERE name == 'Dave'; Server response: OK

还能够处理JOIN查询和多个WHERE条件。

<sqlCompiler.sqlCommands> ::= ;

::= | | | | | | | | ::= USE ::= | ::= CREATE DATABASE ::= CREATE TABLE | CREATE TABLE ( ) ::= DROP ::= DATABASE | TABLE ::= ALTER TABLE ::= INSERT INTO VALUES ( ) ::= SELECT FROM | SELECT FROM WHERE

::= UPDATE SET WHERE

::= DELETE FROM WHERE

::= JOIN AND ON AND

::= | ,

::= =

::= ADD | DROP

::= | ,

::= '' | | |

::= true | false

::= | *

::= | ,

::= ( ) AND ( ) | ( ) OR ( ) |

::= == | > | < | >= | <= | != | LIKE
