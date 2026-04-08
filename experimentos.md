# Experimentos de Avaliação de Desempenho

## 1. Definição Geral
Para os experimentos de avaliação de desempenho, o grupo deverá:

- Especificar um conjunto de **operações e consultas** sobre o banco de dados do **StackOverflow**.
- Implementar essas operações utilizando **SQL**.

---

## 2. Tipos de Operações a Avaliar

As operações obrigatórias incluem:

1. **Operações básicas de dados:**
   - Inserção
   - Remoção
   - Alteração  
   *(em diferentes tabelas)*

2. **Buscas por chave primária:**
   - Busca por **uma única chave**
   - Busca por **faixa de valores**

3. **Buscas por atributos não-chave:**
   - Consultas em atributos não-chave
   - Uso de **condições compostas**

4. **Buscas por padrões de string:**
   - Utilização do operador **`LIKE`**

5. **Consultas com relacionamentos:**
   - Junções (**JOIN**)
   - Múltiplas junções

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
