
# Classificação de Câncer de Mama com Random Forest

## Objetivo do Exercício
O objetivo deste projeto é utilizar o dataset de câncer de mama da biblioteca **scikit-learn** para treinar um modelo de aprendizado de máquina que classifique corretamente os tumores em **malignos** ou **benignos**. Para isso, utilizamos o **Random Forest**, um algoritmo de classificação baseado em um conjunto de árvores de decisão.

Além do treinamento do modelo, realizamos a normalização dos dados e avaliamos o desempenho por meio de métricas como **precisão (precision)**, **revocação (recall)**, **F1-score**, e **acurácia**. A matriz de confusão foi usada para uma análise mais detalhada dos acertos e erros.

---

## Como Rodar o Código

1. Certifique-se de ter **Python 3.x** instalado em sua máquina.
2. Instale as bibliotecas necessárias:
   ```bash
   pip install scikit-learn pandas
   ```

3. Execute o código da classe random_forest.ipynb

---

## Análise dos Resultados

### Matriz de Confusão
```
[[ 59   4]
 [  1 107]]
```
- **Verdadeiros Positivos (TP)**: 107
- **Verdadeiros Negativos (TN)**: 59
- **Falsos Positivos (FP)**: 4
- **Falsos Negativos (FN)**: 1

### Relatório de Classificação
| Classe | Precision | Recall | F1-Score | Support |
|--------|-----------|--------|----------|---------|
| 0 (Maligno) | 0.98 | 0.94 | 0.96 | 63 |
| 1 (Benigno) | 0.96 | 0.99 | 0.98 | 108 |

- **Acurácia**: 97%
- **Macro Avg**: 0.97 (média simples das métricas)
- **Weighted Avg**: 0.97 (média ponderada considerando o número de exemplos por classe)

### Interpretação
Os resultados mostram que o modelo **Random Forest** alcançou uma alta acurácia de **97%**, indicando que a maioria dos tumores foi corretamente classificada. A matriz de confusão revela apenas **4 falsos positivos** e **1 falso negativo**, o que é um ótimo resultado para um problema de classificação binária.

- **Precision**: A classe 0 (maligno) teve uma precisão de 98%, significando que, das amostras classificadas como malignas, 98% estavam corretas.
- **Recall**: A classe 1 (benigno) obteve um recall de 99%, ou seja, quase todos os tumores benignos foram corretamente identificados.

---

## Conclusão
Este exercício demonstrou como preparar e treinar um modelo de classificação para prever se um tumor é maligno ou benigno com base em características físicas. O **Random Forest** apresentou um desempenho excelente, com baixa taxa de erros, indicando que é um algoritmo adequado para este tipo de problema.

Futuramente, seria interessante testar outros modelos, como **SVM** ou **Redes Neurais**, para comparar o desempenho e avaliar possíveis melhorias.
