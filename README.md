## Banco de Dados
 Repositório destinado a prática sobre introdução ao estudo de Banco de Dados

## O que é Banco de Dados?
Pode ser definido como um local de armazenamento de dados, onde esses dados, são organizados de maneira estrutura, e que podem ser consultados a qualquer momento, para extração de informações.

## Qual a função do BD?
Dentre as muitas funções e utilidades de um banco de dados, destaca-se seu uso para registrar e armazenar informações, de maneira que os dados fiquem seguros, integros e organizados.

## Sistema de Gerenciamento de Banco de Dados
Um banco de dados é controlado/administrado por meio de um SGBD, que em resumo pode ser definido como uma coleção de programas que
permite que um usuário crie e manipule (consultando, inserindo, alterando ou deletando dados) um banco de dados. 

## Modelos de Banco de Dados
Cada BD possui suas caraceristícas e usos específicos. Desta forma existem 2 modelos de BDs:
- Banco de Dados Relacional: Este é o tipo mais comum de banco de dados. Os dados são organizados em tabelas com linhas e colunas, e a relação entre os dados é estabelecida por meio de chaves primárias e estrangeiras. Exemplos de BDs populares nesse modelos incluem MySQL, PostgreSQL, Oracle e Microsoft SQL Server.
Em resumo, um banco de dados relacional organiza os dados em tabelas com relações definidas, mantendo a integridade dos dados e suportando transações seguras. É uma estrutura robusta e amplamente utilizada para armazenar e manipular informações em muitos sistemas de software.

- Banco de Dados Não-Relacional:
Bancos de dados não relacionais, também conhecidos como NoSQL (Not Only SQL), são sistemas de armazenamento de dados que diferem dos tradicionais bancos de dados relacionais em sua estrutura e forma de armazenamento. Em resumo, os bancos de dados não relacionais oferecem flexibilidade, escalabilidade e desempenho para uma variedade de casos de uso, mas também têm suas próprias limitações em termos de suporte a transações complexas e modelagem de dados. Sua escolha entre um banco de dados relacional e não relacional dependerá das necessidades específicas do seu aplicativo ou projeto.

## SQL
O SQL é basicamente uma linguagem de consulta, onde seu uso ao dar comandos/instruções no meio ambiente de um SGBD obter respostar ao que foi solicitado.

A linguagem SQL serve para interagir com os nossos dados que estão armazenados dentro de um banco de dados relacional, permitindo a criação, a recuperação, a atualização e a exclusão desses dados.

O SQL funciona, portanto, por meio de vários componentes e processos que trabalham juntos para gerenciar bancos de dados relacionais, como:

- Analisador: analisa a instrução SQL, verificando sua sintaxe e convertendo palavras-chave em símbolos especiais.
- Exatidão: garante que a instrução esteja em conformidade com as regras da SQL, como o uso correto de pontos e vírgulas.
- Mecanismo Relacional: cria um plano eficiente para acessar os dados, otimizando a consulta e verificando consultas semelhantes.
- Mecanismo de Armazenamento:** executa a instrução SQL, lendo e gravando os dados nos arquivos de armazenamento físico.

Os componentes de uma SQL trabalham juntos para permitir a criação, a manutenção** e a consulta de bancos de dados relacionais:

- Tabelas: as tabelas são estruturas fundamentais em um banco de dados SQL. Elas são usadas para armazenar os dados em formato tabular, com colunas representando atributos e linhas representando registros.
- Procedimentos Armazenados: os procedimentos armazenados são blocos de código SQL que podem ser definidos e armazenados no banco de dados. Eles são usados para realizar tarefas específicas, como cálculos complexos, validações de dados e processamento personalizado.
- Comandos SQL: Os comandos SQL, como SELECT, INSERT, UPDATE e DELETE, são usadas para manipular os dados em tabelas. As instruções SQL permitem que os usuários realizem consultas, insiram novos dados, atualizem registros existentes e excluam dados.

## CRUD
CRUD (acrônimo para operações essenciais em um bd) :

- Create   (Criar)
- Read     (Ler)
- Update  (Atualizar)
- Delete   (Apagar)

### Os principais tipos de dados são:

- INT  -> Número inteiro
- SERIAL  -> Número inteiro com autoincremento
- LOAT  -> Número fracionário
- VARCHAR-> Texto com tamanho variável (É possível fixar valor máximo)
- DATATIME-> Data e hora
- BOOLEAN  -> Valor booleano (True/False)

### Criação

CREATE TABLE Pessoa (
ID INT PRIMARY KEY,
Nome VARCHAR(100),
Idade INT
);

### Inserir dados

INSERT INTO Pessoa (ID, Nome, Idade) VALUES (1, 'João Silva', 30);

### Buscar dados

SELECT Nome, Idade FROM Pessoa;

### Filtrar dados com WHERE:

SELECT * FROM Pessoa WHERE Idade > 18;

### Atualizar Dados (UPDATE):

UPDATE Pessoa SET Idade = 31 WHERE ID = 1;

### Deletar dados:

DELETE FROM Pessoa WHERE ID = 1;

### Cláusulas Complementares:

- FROM: Especifica a tabela de onde os dados serão selecionados ou excluídos.
- WHERE: Filtra registros com base em uma condição.
- AND/OR: Usados dentro de **`WHERE`** para combinar múltiplas condições.


## Desafio: Instituto do Coração Zurique 
![cristina-yang](img.greys.jpg)

### Contexto-Problema

O consultório de Cristina Yang era conhecido por sua eficiência implacável e sua abordagem meticulosa para lidar com todos os aspectos do trabalho. Desde a precisão cirúrgica até a organização dos registros dos pacientes, nada escapava ao olhar afiado da Dra. Yang.

Certo dia, ao observar a bagunça aparente na mesa da recepcionista, Cristina decidiu intervir. Com um olhar penetrante, ela abordou a funcionária responsável pela organização de sua agenda.

"Francyne, precisamos ter uma conversa sobre a maneira como estamos gerenciando os dados dos nossos pacientes aqui. Não podemos nos dar ao luxo de perder tempo procurando números de telefone, buscar por informações importantes ou se quer correr risco de perder os dados de nossos pacientes por algum erro inesperado."

Francyne, acostumada com a abordagem direta da Dra. Yang, assentiu, pronta para ouvir as instruções.

"A partir de agora, quero que todos os nossos contatos sejam digitalizados e organizados em um banco de dados acessível a todos do Instituo Zurique. Nada de agendas desorganizadas ou papéis perdidos! Quero eficiência, quero precisão."

Francyne absorveu as palavras de sua chefe, reconhecendo a importância da mudança. "Entendi, Dra. Yang. Vou começar a digitalizar imediatamente e garantir que todos os contatos estejam devidamente catalogados e fiquem seguros e salvos em um Banco de Dados."

Cristina Yang sorriu satisfeita. "Ótimo. Lembre-se, a organização é a chave para o sucesso. Não podemos nos dar ao luxo de cometer erros quando se trata da saúde e do bem-estar de nossos pacientes."

### Instruções

1. Uma tabela precisará ser construida, para armazenar os dados dos pacientes, dispondo das seguintes categorias:

● Nome do Paciente;
● Idade;
● Sexo;
● Email;
● Telefone;
● Endereço;
● Data da última consulta;

2. Pacientes precisam ser criados.
3. Busque por pacientes em que a data da última consulta tenha sido a mais de 3 meses e tenham mais de 30 anos.
4. Atualize a data de consulta de um paciente para a semana atual.
5. Exclua o cadastro de pacientes que possuem menos de 30 anos de idade.


