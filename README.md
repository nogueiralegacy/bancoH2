# Banco H2

## Escopo
O projeto Banco H2 é uma aplicação que cria de forma simples um banco de dados gerenciado pelo SGBD H2. A aplicação é voltada para fazer experimentações em um banco de dados SQL.

## Estrutura
### Pré-requisitos
- Maven.
### Descrição
O projeto a partir do Maven faz o download do SGBD e com poucos comandos já está disponível para uso. Caso queira fazer a integração do banco de dados com uma aplicação java será necessário ter o JDK intalado também.

## Criar o banco H2

- `mvn exec:java -P start-shell-h2`

Abre/cria banco para uso via linha de comandos. Para criar o banco de nome `bancoNome` no diretório `dir` forneça `jdbc:h2:dir/bancoNome`. Se existir, apenas será aberto. Adicionalmente, forneça como driver a classe `org.h2.Driver`. Você pode fazer uso do diretório de sua preferência, contudo, a sugestão é criar o banco no diretório `target` (usado pelo comando seguinte). Posteriormente forneça o usuário e senha do banco, caso o banco ainda não exista o usuário e senha fornecido seram armazenados para credenciar acessos futuros. Na shell que é aberta, digite `create table teste (id int primary key, nome varchar(255));` para criar uma tabela de teste. Para inserir um registro, digite `insert into teste values (1, 'teste');`. Para listar os registros, digite `select * from teste;`. Para sair, digite exit


