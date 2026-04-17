# Experimentos de Avaliação de Desempenho


## Elaboração das Consultas SQL

Para cada consulta, traduzi-la para SQL e adcionar que operações ela abrange.

*Nota: o postgree trata tabelas e colunas como case-sensitive, então vamos padronizar usar eles entre aspas duplas (O MySql entende)*

**Experimento I.** Criação de novo registro de teste na tabela users.
```
codigo_sql
```
Operações utilizadas: insersão.

**Experimento II.** Remoção do último registro de teste na tabela users.
```
codigo_sql
```
Operações utilizadas: remoção, busca por atributo não-chave primária, condição de seleção composta.

**Experimento III.**  Alteração de recompensa em +10 para um usuário e post específico que possue voto do tipo BountyStart
```
codigo_sql
```
Operações utilizadas: alteração, busca por faixa de chaves, condição de seleção.

**Experimento IV.** Listar todas as postagens que contenham a palavra SQL no título ou nas tags. Ordenar por pontuação.
```
codigo_sql
```
Operações utilizadas: busca com sql, ordenação.

**Experimento V.** Listar a postagem, a tag da postagem e o seu número de comentários que contenham a palavra SQL no texto. Ordenado pelo score.
```
codigo_sql
```
Operações utilizadas: busca com sql, ordenação, junção.

**Experimento VI.** Calcular pontuação média dos posts por usuário.
```
código_sql
```
Operações utilizadas: agrupamento, agregação.

**Experimento VII.** Listar usuários que fizeram posts votados como 12-spam, trazer o indentificador de perfil e seus respectivos posts (Title, Body, CreationDate, ClosedDate)
```
código_sql
```
Operações utilizadas:

**Experimento VIII.** Buscar todos os usuários com idade 65 que tenha feito alguma postagem no último mês
```
código_sql
```
Operações utilizadas:

**Experimento IX.** Buscar usuários que possuam mais distintivos(badges)
```
código_sql
```
Operações utilizadas: 


**Experimento X.** Trazer titulo, nome do tipo, número de comentários, número de vezes que foi referenciado, soma dos votos postivos e soma dos votos negativos do post do tipo resposta que possue maior número de vizualiações.
```
código_sql
```
Operações utilizadas: 



## Criação de Índices e Definição de Cenários

Cenário I. Cenário Base sem índices utilizando o MySQL

Cenário II. Cenário Base sem índices utilizando o PostgreSQL


1. **Banco de dados sem índices**
- Cenário I. Cenário Base sem índices utilizando o MySQL
- Cenário II. Cenário Base sem índices utilizando o PostgreSQL
2. Cenários com índices:
   - Criados sobre diferentes atributos
   - Utilizando diferentes estruturas:
     - **Árvore B+**
     - **Hash**

- Identificar **quais índices trazem maior ganho de desempenho**.
   1. Pesquisar sobre ferramentas de testes de índices 

---

## Execução dos Experimentos

- Cada consulta deve ser executada **múltiplas vezes em cada cenário**.
- O tempo de execução pode variar devido a fatores como:
  - Carga da máquina
  - Paginação do sistema operacional
  - Cache do SGBD/SO

### Recomendação importante:
- **Minimizar interferências externas**, como outros programas em execução.

---
## Coleta de Dados

- Desenvolver **programas ou scripts** para:
  - Executar as operações nos SGBDs
  - Coletar os **tempos de execução**

- Para cada:
  - **SGBD**
  - **Cenário**
  
  Executar cada operação **pelo menos 20 vezes**.
