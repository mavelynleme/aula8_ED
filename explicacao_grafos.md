# Grafos — Explicação Completa e Simples

## 1. O que são grafos?

Grafos são estruturas usadas na Matemática e na Ciência da Computação para representar **relações entre elementos**.

Um grafo é formado por:

- **Vértices** ou **nós**: representam os elementos.
- **Arestas**: representam as ligações entre os elementos.

Exemplo simples:

```text
1 ----- 2
```

Nesse exemplo:

- `1` e `2` são vértices.
- A linha entre eles é uma aresta.

Podemos dizer que o vértice `1` está ligado ao vértice `2`.

---

## 2. Representação formal de um grafo

Um grafo geralmente é representado assim:

```text
G = (V, E)
```

Onde:

- `G` é o grafo.
- `V` é o conjunto de vértices.
- `E` é o conjunto de arestas.

Exemplo:

```text
V = {1, 2, 3}
E = {(1, 2), (2, 3)}
```

Isso significa que temos os vértices `1`, `2` e `3`, com ligações entre:

```text
1 -- 2
2 -- 3
```

---

## 3. Onde os grafos são usados?

Grafos podem representar muitos problemas do mundo real, como:

- Redes sociais.
- Rotas de ônibus, aviões e estradas.
- Mapas e caminhos mais curtos.
- Ligações elétricas.
- Redes de computadores.
- Relações profissionais.
- Jogos, como xadrez e damas.
- Horários de aula e escalas de trabalho.

Exemplo em rede social:

```text
João ----- Maria
  \        /
   \      /
    Paulo
```

Nesse caso:

- As pessoas são os vértices.
- As amizades são as arestas.

---

## 4. Grafo não orientado

Um **grafo não orientado** é aquele em que as ligações não têm direção.

Exemplo:

```text
1 ----- 2
```

Isso significa que:

```text
1 está ligado a 2
2 está ligado a 1
```

A ligação vale nos dois sentidos.

---

## 5. Grafo orientado

Um **grafo orientado** é aquele em que as ligações têm direção, representadas por setas.

Exemplo:

```text
1 ----> 2
```

Isso significa que existe uma ligação saindo de `1` e chegando em `2`.

Nesse caso:

```text
1 aponta para 2
```

Mas não significa necessariamente que `2` aponta para `1`.

---

## 6. Grau de um vértice

O **grau de um vértice** é a quantidade de arestas ligadas a ele.

Exemplo:

```text
1 ----- 2 ----- 3
```

Graus:

```text
Vértice 1: grau 1
Vértice 2: grau 2
Vértice 3: grau 1
```

O vértice `2` tem grau `2` porque está ligado ao vértice `1` e ao vértice `3`.

---

## 7. Maior grau e menor grau

Depois de calcular o grau de cada vértice, podemos identificar:

- **Maior grau**: o maior número de conexões de um vértice.
- **Menor grau**: o menor número de conexões de um vértice.

Exemplo:

```text
Vértice 1: grau 2
Vértice 2: grau 3
Vértice 3: grau 2
Vértice 4: grau 3
Vértice 5: grau 3
Vértice 6: grau 1
```

Resultado:

```text
Maior grau = 3
Menor grau = 1
```

---

## 8. Grau de entrada e grau de saída

Em grafos orientados, usamos dois tipos de grau:

### Grau de entrada

É a quantidade de setas que **chegam** em um vértice.

Também pode ser escrito como:

```text
d-(v)
```

### Grau de saída

É a quantidade de setas que **saem** de um vértice.

Também pode ser escrito como:

```text
d+(v)
```

Exemplo:

```text
1 ----> 2
```

Resultado:

```text
Vértice 1:
Grau de saída = 1
Grau de entrada = 0

Vértice 2:
Grau de saída = 0
Grau de entrada = 1
```

---

## 9. Lista de adjacência

A **lista de adjacência** mostra, para cada vértice, quais vértices estão ligados a ele.

Exemplo de grafo:

```text
1 ----- 2
|       |
3 ----- 4
```

Arestas:

```text
(1, 2)
(1, 3)
(2, 4)
(3, 4)
```

Lista de adjacência:

```text
1: [2, 3]
2: [1, 4]
3: [1, 4]
4: [2, 3]
```

Ou seja, para cada vértice, escrevemos seus vizinhos.

---

## 10. Matriz de adjacência

A **matriz de adjacência** representa as ligações do grafo usando uma tabela.

A regra é:

```text
1 = existe ligação
0 = não existe ligação
```

Exemplo com vértices `1`, `2`, `3` e `4`:

```text
Arestas:
(1, 2)
(1, 3)
(2, 4)
```

Matriz de adjacência:

|   | 1 | 2 | 3 | 4 |
|---|---|---|---|---|
| 1 | 0 | 1 | 1 | 0 |
| 2 | 1 | 0 | 0 | 1 |
| 3 | 1 | 0 | 0 | 0 |
| 4 | 0 | 1 | 0 | 0 |

Explicação:

- Linha `1`, coluna `2` tem valor `1`, porque existe ligação entre `1` e `2`.
- Linha `1`, coluna `4` tem valor `0`, porque não existe ligação entre `1` e `4`.

---

## 11. Diferença entre lista e matriz de adjacência

### Lista de adjacência

Mostra diretamente os vizinhos de cada vértice.

Exemplo:

```text
1: [2, 3]
2: [1, 4]
3: [1]
4: [2]
```

### Matriz de adjacência

Mostra as conexões em formato de tabela com `0` e `1`.

Exemplo:

|   | 1 | 2 | 3 | 4 |
|---|---|---|---|---|
| 1 | 0 | 1 | 1 | 0 |
| 2 | 1 | 0 | 0 | 1 |
| 3 | 1 | 0 | 0 | 0 |
| 4 | 0 | 1 | 0 | 0 |

---

## 12. Como resolver uma atividade de grafos

Para resolver uma atividade de grafos, siga esta ordem:

### Passo 1 — Identifique os vértices

Veja quais são os pontos do grafo.

Exemplo:

```text
V = {1, 2, 3, 4, 5}
```

### Passo 2 — Identifique as arestas

Veja quais pontos estão ligados por linhas.

Exemplo:

```text
E = {(1, 2), (1, 3), (2, 5), (3, 4)}
```

### Passo 3 — Calcule os graus

Conte quantas linhas encostam em cada vértice.

### Passo 4 — Monte a lista de adjacência

Para cada vértice, escreva os vértices ligados a ele.

### Passo 5 — Monte a matriz de adjacência

Crie uma tabela com todos os vértices nas linhas e nas colunas.

Depois preencha:

```text
1 = tem ligação
0 = não tem ligação
```

---

## 13. Exemplo completo

Grafo:

```text
1 ----- 2
|       |
3 ----- 4
```

### Vértices

```text
V = {1, 2, 3, 4}
```

### Arestas

```text
E = {(1, 2), (1, 3), (2, 4), (3, 4)}
```

### Graus

```text
d(1) = 2
d(2) = 2
d(3) = 2
d(4) = 2
```

### Lista de adjacência

```text
1: [2, 3]
2: [1, 4]
3: [1, 4]
4: [2, 3]
```

### Matriz de adjacência

|   | 1 | 2 | 3 | 4 |
|---|---|---|---|---|
| 1 | 0 | 1 | 1 | 0 |
| 2 | 1 | 0 | 0 | 1 |
| 3 | 1 | 0 | 0 | 1 |
| 4 | 0 | 1 | 1 | 0 |

---

## 14. Código simples em Python para desenhar grafos

```python
import networkx as nx
import matplotlib.pyplot as plt

G = nx.Graph()

arestas = [
    (1, 2),
    (1, 3),
    (2, 4),
    (3, 4)
]

G.add_edges_from(arestas)

nx.draw(
    G,
    with_labels=True,
    node_color="lightblue",
    node_size=1000,
    font_weight="bold"
)

plt.show()
```

---

## 15. Código para calcular graus

```python
import networkx as nx

G = nx.Graph()

arestas = [
    (1, 2),
    (1, 3),
    (2, 4),
    (3, 4)
]

G.add_edges_from(arestas)

graus = dict(G.degree())

for vertice, grau in sorted(graus.items()):
    print(f"Vértice {vertice}: Grau {grau}")
```

---

## 16. Código para lista de adjacência

```python
import networkx as nx

G = nx.Graph()

arestas = [
    (1, 2),
    (1, 3),
    (2, 4),
    (3, 4)
]

G.add_edges_from(arestas)

for vertice in sorted(G.nodes()):
    vizinhos = sorted(list(G.neighbors(vertice)))
    print(f"{vertice}: {vizinhos}")
```

---

## 17. Código para matriz de adjacência

```python
import networkx as nx
import pandas as pd

G = nx.Graph()

arestas = [
    (1, 2),
    (1, 3),
    (2, 4),
    (3, 4)
]

G.add_edges_from(arestas)

matriz = nx.to_pandas_adjacency(G, nodelist=sorted(G.nodes()), dtype=int)
display(matriz)
```

---

## 18. Resumo final

| Conceito | Significado |
|---|---|
| Grafo | Estrutura formada por vértices e arestas |
| Vértice | Ponto ou nó do grafo |
| Aresta | Ligação entre dois vértices |
| Grau | Quantidade de arestas ligadas a um vértice |
| Grafo orientado | Grafo com setas |
| Grau de entrada | Quantidade de setas que chegam em um vértice |
| Grau de saída | Quantidade de setas que saem de um vértice |
| Lista de adjacência | Lista dos vizinhos de cada vértice |
| Matriz de adjacência | Tabela com `0` e `1` indicando as ligações |

---

## 19. Ideia principal

A ideia mais importante é:

```text
Um grafo representa relações.
```

Se existem elementos conectados entre si, podemos representar isso com grafos.

Exemplos:

```text
Pessoas conectadas por amizade
Cidades conectadas por estradas
Computadores conectados por rede
Disciplinas conectadas por pré-requisitos
Páginas conectadas por links
```

Por isso, grafos são muito usados na computação, na matemática e em problemas do mundo real.
