# Experimentos de Avaliação de Desempenho

## 1. Definição Geral
Para os experimentos de avaliação de desempenho, o grupo deverá:

- Especificar um conjunto de **operações e consultas** sobre o banco de dados do **StackOverflow**.
- Implementar essas operações utilizando **SQL**.

---

## 2. Tipos de Operações a Avaliar

As operações obrigatórias incluem:

1. **Operações básicas de dados:**
   - Consultas simples
      - Trazer o detalhamento de cada base, 50 primeiras linhas
   - Inserção
      - Inserir um novo usuário U1 na base Users
      - Inserir um novo usuário U2 na base Users
      - Inserir um novo post A do user U1 com tipo 1-Question + Add comments 
      - Inserir um novo post B do user U1 com tipo 1-Question + Add comments
      - Inserir um novo post C do user U2 com tipo 2-Answer referenciando uma outra postagem (B) respondendo post A + Add comments
   - Remoção
      - Remover referencia do post B para se referir a nenhum post
   - Alteração  
      - Alterar tipo do posto B
   *(em diferentes tabelas)*

2. **Buscas por chave primária:**
   - Busca por **uma única chave**
      - Buscar title_post quando id = A
   - Busca por **faixa de valores**
      - buscar todos os posts de uma respectiva data do usuário id=U1

3. **Buscas por atributos não-chave:**
   - Consultas em atributos não-chave
      - buscar todos os usuários com idade 65 
   - Uso de **condições compostas**
      - Buscar todos os usuários com idade 65 que tenha feito alguma postagem no último mês

4. **Buscas por padrões de string:**
   - Utilização do operador **`LIKE`**
      - Buscar posts que possuem tags especificas para linguagens de programação
      - Filtragem de usuários na Location X 
5. **Consultas com relacionamentos:**
   - Junções (**JOIN**)
   - Múltiplas junções
      - Buscar usuários que possuem distintivos
      - Buscar usuários que possuem mais distintivos
      - Buscar posts do tipo "Perguntas" feitos pelo usuário A em certo intervalo de tempo além de todos e todos os comentários com score positivo
      - Listar usuários que fizeram posts votados como 12-spam, trazer o indentificador de perfil
      - Listar usuários que fizeram posts votados como 12-spam, trazer o indentificador de perfil e seus respectivos posts (Title, Body, CreationDate, ClosedDate)

6. **Consultas com subconsultas**

7. **Operações com agrupamento e agregação:**
   - **Soma (SUM)**
   - **Média (AVG)**
   - **Mínimo (MIN)**
   - **Máximo (MAX)**
   - **Contagem (COUNT)**

---

## 3. Planejamento dos Experimentos

O grupo deverá:

- Projetar experimentos considerando **diferentes cenários de execução**.

### Cenários obrigatórios:

1. **Banco de dados sem índices**
2. Cenários com índices:
   - Criados sobre diferentes atributos
   - Utilizando diferentes estruturas:
     - **Árvore B+**
     - **Hash**

- Identificar **quais índices trazem maior ganho de desempenho**.
   1. Pesquisar sobre ferramentas de testes de índices 

---

## 4. Execução dos Experimentos

- Cada consulta deve ser executada **múltiplas vezes em cada cenário**.
- O tempo de execução pode variar devido a fatores como:
  - Carga da máquina
  - Paginação do sistema operacional
  - Cache do SGBD/SO

### Recomendação importante:
- **Minimizar interferências externas**, como outros programas em execução.

---

## 5. Coleta de Dados

- Desenvolver **programas ou scripts** para:
  - Executar as operações nos SGBDs
  - Coletar os **tempos de execução**

- Para cada:
  - **SGBD**
  - **Cenário**
  
  Executar cada operação **pelo menos 20 vezes**.

---

## 6. Padronização dos Experimentos

- Todos os experimentos devem ser realizados:
  - **Na mesma máquina**

⚠️ Caso contrário, os resultados **não serão comparáveis**.

---

## 7. Análise dos Resultados

- Comparar os tempos obtidos em cada cenário
- Avaliar o impacto dos índices no desempenho
- Identificar **melhores estratégias de otimização**
