# Lista de Exercícios — MQE, MQE de Teste e Variância

Resolução da lista de **Introdução à Estatística Computacional**
A lista trabalha o Erro Quadrático Médio (MQE) no treino e no teste, a comparação entre um
modelo linear e um polinomial, e o efeito da variância dos dados na estabilidade da avaliação.

## O que tem em cada parte

- **Parte I** — base original, regressão linear, MQE de treino e de teste e interpretação.
- **Parte II** — polinômio de grau 2 na mesma base e comparação dos erros.
- **Parte III** — base de alta variância avaliada com 7 seeds diferentes.
- **Parte IV** — base de baixa variância, mesma rotina, para contraste.
- **Parte V** — implementação em Python (função reutilizável, repetição por seed, média e
  desvio-padrão do MQE de teste).
- **Parte VI** — questões conceituais (treino x teste, underfitting, overfitting, viés-variância).

## Principais resultados

| Cenário | MQE treino | MQE teste |
|---|---|---|
| Base original — linear (seed 1) | 0,1511 | 1,0327 |
| Base original — polinômio grau 2 (seed 1) | 0,0402 | 1,4613 |
| Alta variância — média nos 7 seeds | 134,17 | 174,65 (desvio 43,48) |
| Baixa variância — média nos 7 seeds | 0,1682 | 0,2287 (desvio 0,099) |

A leitura curta: o modelo mais flexível baixou o erro de treino mas piorou o de teste, e a
base com mais ruído deixou a avaliação muito mais instável entre as divisões.

## Como rodar

```bash
pip install -r requirements.txt
jupyter notebook lista_mqe_variancia.ipynb
```

## Arquivos

- `lista_mqe_variancia.ipynb` — resolução completa (código + respostas).
- `requirements.txt` — bibliotecas usadas.
