# Monitoramento de Preços de Gasolina (Python)

Este projeto foi desenvolvido como uma atividade avaliativa para a turma **ADA3**, sob orientação do **Professor Sérgio Monteiro**. O objetivo é analisar a variação de preços da gasolina ao longo de uma semana, classificando-os e gerando métricas estatísticas simples.

## Funcionalidades

O script realiza as seguintes operações:
* **Classificação Automática**: Categoriza os preços em "Baixo", "Moderado" ou "Alto".
* **Cálculo de Métricas**: Soma o valor total acumulado e calcula a média semanal dos preços.
* **Sistema de Alerta**: Identifica se houve uma frequência crítica (mais de 2 dias) de preços altos.

## Regras de Classificação

Para a análise dos dados, foram utilizadas as seguintes faixas de preço (R$/L):

| Faixa de Preço | Classificação |
| :--- | :--- |
| Abaixo de 5.50 | **Baixo** |
| Entre 5.50 e 6.00 | **Moderado** |
| Acima de 6.00 | **Alto** |

## Como funciona o código

O algoritmo percorre uma lista de preços e utiliza estruturas de repetição (`for`) e condicionais (`if/elif/else`) para processar cada valor:

```python
# Exemplo da lógica principal
for p in preços:
    preço_total += p
    if(p < 5.5):
        print(f"preço {p}: Baixo")
    elif(5.5 <= p <= 6.0):
        print(f"preço {p}: Moderado")
    else:
        print(f"preço {p}: Alto")
        quantidade_preços_altos += 1
```

## Tecnologias Utilizadas

* **Linguagem:** Python 3
* **Ambiente:** Google Colab / Jupyter Notebook

---
**Desenvolvido por:** Kayla Rodrigues  
**Turma:** ADA3
