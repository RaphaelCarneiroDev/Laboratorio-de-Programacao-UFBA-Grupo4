# Laboratório de Programação UFBA  Grupo 4


## Repositório destinado a conclusão de atividades propostas pela disciplina de Laboratório de Programação I.

# Membros:
```text
Ana Lívia Abreu
Breno Almeida
João Pedro Gonçalves
Kit Meng Ng
Tiago Souza
Raphael Carneiro
Sthefany dos Santos
Thales Sena
Thaise Adrielle Martins
```
# Lista de Exercícios

## Atividade 1 - Soma de Dois Inteiros
**Dificuldade:** Simples (1 ponto)

### Descrição
Construa uma função para calcular a soma de dois números inteiros.

### Exemplo
```text
a = 7
b = 3
```

Retorno:

```text
10
```

### Assinatura da Função
```python
def soma(a, b):
```

### Parâmetros
| Parâmetro | Tipo | Descrição |
|-----------|------|-----------|
| a | int | Primeiro valor |
| b | int | Segundo valor |

### Retorno
| Tipo | Descrição |
|--------|-----------|
| int | Soma de `a` e `b` |

### Restrições
```text
1 ≤ a, b ≤ 1000
```

### Entrada de Exemplo
```text
a = 2
b = 3
```

### Saída de Exemplo
```text
5
```

### Explicação
```text
2 + 3 = 5
```

---

## Atividade 2 - Soma dos Elementos de um Array
**Dificuldade:** Simples (1 ponto)

### Descrição
Dado um array de inteiros, encontre a soma de seus elementos.

### Exemplo
```text
ar = [1, 2, 3]
```

Retorno:

```text
6
```

### Assinatura da Função
```python
def somaArray(ar):
```

### Parâmetros
| Parâmetro | Tipo | Descrição |
|-----------|------|-----------|
| ar | int[] | Array de inteiros |

### Retorno
| Tipo | Descrição |
|------|-----------|
| int | Soma dos elementos do array |

### Formato de Entrada
A primeira linha contém um inteiro `n`, indicando o tamanho do array.

A segunda linha contém `n` inteiros separados por espaço.

### Restrições
```text
0 < n, ar[i] ≤ 1000
```

### Entrada de Exemplo
```text
6
1 2 3 4 10 11
```

### Saída de Exemplo
```text
31
```

### Explicação
```text
1 + 2 + 3 + 4 + 10 + 11 = 31
```

---

## Atividade 3 - Próxima Palavra Lexicográfica
**Dificuldade:** Intermediária (1 ponto)

### Descrição
Dada uma palavra, encontre a menor palavra lexicograficamente maior que pode ser formada reorganizando seus caracteres.

Caso não exista uma palavra maior possível, retorne:

```text
no answer
```

### Exemplo
Entrada:

```text
abcd
```

Saída:

```text
abdc
```

### Assinatura da Função
```python
def biggerIsGreater(w):
```

### Parâmetros
| Parâmetro | Tipo | Descrição |
|-----------|------|-----------|
| w | string | Palavra de entrada |

### Retorno
| Tipo | Descrição |
|------|-----------|
| string | Menor string lexicograficamente maior ou `"no answer"` |

### Formato de Entrada
A primeira linha contém um inteiro `T`, número de casos de teste.

As próximas `T` linhas contêm uma string `w`.

### Restrições
```text
1 ≤ T ≤ 10⁵
1 ≤ |w| ≤ 100
w ∈ [a-z]
```

### Entrada de Exemplo 0
```text
5
ab
bb
hefg
dhck
dkhc
```

### Saída de Exemplo 0
```text
ba
no answer
hegf
dhkc
hcdk
```

### Entrada de Exemplo 1
```text
6
lmno
dcba
dcbb
abdc
abcd
fedcbabcd
```

### Saída de Exemplo 1
```text
lmon
no answer
no answer
acbd
abdc
fedcbabdc
```

---

## Atividade 4 - Organizando Contêineres de Bolas
**Dificuldade:** Avançada (7 pontos)

### Descrição
David possui diversos contêineres contendo bolas de diferentes tipos.

Ele pode realizar trocas entre bolas localizadas em contêineres distintos.

O objetivo é verificar se é possível reorganizar as bolas de forma que:

- Cada contêiner contenha apenas um único tipo de bola.
- Todas as bolas de um mesmo tipo estejam em um único contêiner.

### Exemplo

```text
containers = [
    [1, 4],
    [2, 3]
]
```

Resultado:

```text
Impossible
```

### Assinatura da Função
```python
def organizingContainers(containers):
```

### Parâmetros
| Parâmetro | Tipo | Descrição |
|-----------|------|-----------|
| containers | int[][] | Matriz representando as quantidades de bolas |

### Retorno
| Tipo | Descrição |
|------|-----------|
| string | `"Possible"` ou `"Impossible"` |

### Formato de Entrada

A primeira linha contém um inteiro `q`, indicando o número de consultas.

Para cada consulta:

- A primeira linha contém um inteiro `n`.
- As próximas `n` linhas contêm `n` inteiros cada.

### Restrições

```text
1 ≤ q ≤ 10
1 ≤ n ≤ 100
0 ≤ containers[i][j] ≤ 10⁹
```

### Pontuação

```text
33% dos testes: 1 ≤ n ≤ 10
100% dos testes: 1 ≤ n ≤ 100
```

### Entrada de Exemplo 0

```text
2
2
1 1
1 1
2
0 2
1 1
```

### Saída de Exemplo 0

```text
Possible
Impossible
```

### Entrada de Exemplo 1

```text
2
3
1 3 1
2 1 2
3 3 3
3
0 2 1
1 1 1
2 0 0
```

### Saída de Exemplo 1

```text
Impossible
Possible
```

### Explicação
A solução é possível quando o conjunto das capacidades totais dos contêineres é igual ao conjunto das quantidades totais de cada tipo de bola.

Caso contrário, a reorganização é impossível.
