# Prova Técnica — Desenvolvedor Pesquisador Júnior

**Duração estimada:** 4 a 5 horas  
**Formato:** Questões práticas com desenvolvimento de código  
**Observação:** O candidato deve desenvolver o código e estar preparado para explicar cada decisão tomada.

---

## Sessão 1 — Python e Pandas: Análise Exploratória de Dados

> **Dataset utilizado nesta sessão:** [Datasaurus Dozen](https://jumpingrivers.github.io/datasauRus/)  
> O dataset pode ser baixado diretamente via Python usando o pacote `datasaurus`  :  
> ```python
> pip install datasaurus
> from datasaurus.core.models import Datasaurus
> df = Datasaurus.get_all()  # retorna todos os 13 subsets
> ```
> O DataFrame contém as colunas `dataset` (nome do subset), `x` e `y`.

---

### Questão 1

O Datasaurus Dozen é composto por 13 subsets diferentes. Utilizando o dataset completo:

**Tarefas:**
- Carregue os dados utilizando Pandas
- Explore a estrutura geral do DataFrame (tipos de colunas, shape, quantidade de subsets, etc.)
- Verifique se há valores ausentes ou registros duplicados
- Para **cada subset**, calcule as seguintes estatísticas descritivas de `x` e `y`: média, desvio padrão e correlação

**Explique** o que você observou nos resultados estatísticos entre os diferentes subsets. Há algo surpreendente?

---

### Questão 2

Agora, visualize os 13 subsets do Datasaurus Dozen em um único gráfico com subplots, plotando `x` vs `y` para cada dataset.

**Tarefas:**
- Crie uma grade de subplots com todos os 13 datasets
- Cada subplot deve ter o nome do subset como título
- Utilize cores diferentes para cada dataset

**Reflita e explique:** Comparando as estatísticas calculadas na Questão 1 com as visualizações geradas aqui, o que você conclui sobre a importância da visualização na análise de dados? O que poderia ter acontecido se você tivesse tomado decisões baseando-se apenas nas estatísticas descritivas?

---

### Questão 3

Escolha **um subset específico** do Datasaurus Dozen que, na sua opinião, seria o mais desafiador de analisar apenas com estatísticas descritivas. Justifique sua escolha.

Em seguida:
- Filtre apenas os dados desse subset
- Calcule a **média móvel de 5 pontos** sobre os valores de `y` ordenados por `x`
- Visualize os dados originais e a média móvel no mesmo gráfico

**Explique** o que a média móvel revela (ou esconde) sobre os dados desse subset, e quando essa técnica seria útil no contexto de análise de dados de sensores embarcados.

---

## Sessão 2 — Tratamento de Dados e ETL

### Questão 4

Você possui dois arquivos CSV com dados de sensores de dois sistemas embarcados distintos:

- **Arquivo A:** colunas `timestamp`, `temperatura`, `umidade`
- **Arquivo B:** colunas `data_hora`, `temp`, `humidity`

**Tarefas:**
- Una os dois arquivos em um único DataFrame
- Padronize os nomes das colunas
- Padronize os formatos de data e hora

**Explique** o processo de limpeza e transformação que você realizou.

---

### Questão 5

Após unificar os dados da Questão 4, você identifica dois problemas:
1. Alguns valores de temperatura estão armazenados como strings em vez de números
2. Há valores outliers que provavelmente são erros de leitura dos sensores

**Descreva como você trataria cada um desses problemas** e justifique suas decisões de forma clara.

---

### Questão 6

Implemente um **pipeline ETL simples** que:
1. Leia os dados brutos dos dois arquivos CSV
2. Aplique todas as transformações descritas nas Questões 4 e 5
3. Agregue os dados por hora, calculando a média de temperatura e umidade por sensor
4. Salve o resultado em um novo arquivo CSV

**Explique cada etapa do seu pipeline** e as escolhas feitas durante o desenvolvimento.

---

## Sessão 3 — C / C++: Estruturas de Dados Circulares

### Questão 7

Implemente uma **fila circular** em C ou C++ com as seguintes operações:
- Enfileirar (`enqueue`)
- Desenfileirar (`dequeue`)
- Verificar se a fila está cheia ou vazia

**Explique** como essa estrutura é útil em sistemas embarcados, especialmente no contexto de processamento de dados de sensores em tempo real com recursos de memória limitados.

---

### Questão 8

Implemente uma **lista ligada circular** que armazene leituras de sensores contendo `id_sensor`, `timestamp` e `valor`. A lista deve suportar:
- Inserção no início e no final
- Remoção de elementos
- Percorrer e imprimir todos os dados da lista

**Escreva o código completo e explique** as vantagens e desvantagens dessa estrutura em comparação com um vetor simples para esse caso de uso.

---

*Boa sorte ao candidato!*
