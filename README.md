# Predição do risco de inadimplência com aprendizado de máquina

Trabalho de Conclusão de Curso (UNIVESP, Ciência de Dados, 2026).
Comparação de Regressão Logística, Random Forest e XGBoost na predição de
inadimplência de clientes, usando o dataset Home Credit Default Risk.

## Dados
Base `application_train.csv` do Kaggle: https://www.kaggle.com/competitions/home-credit-default-risk/data
Os dados não estão neste repositório (termos de uso do Kaggle e tamanho do arquivo).
Baixe o arquivo no link acima e envie no Colab quando solicitado.

## Como reproduzir
1. Abra o notebook `TCC_Inadimplencia_01_Coleta.ipynb` no Google Colab.
2. Execute as células em ordem (Ambiente de execução → Executar tudo).
3. Envie o `application_train.csv` quando solicitado.

Semente aleatória fixa (SEED = 42). Tempo total estimado: cerca de 20 minutos.

## Metodologia
- Divisão estratificada treino/teste (80/20)
- Pré-processamento ajustado apenas no treino (imputação, padronização, one-hot)
- Desbalanceamento tratado por ponderação de classes
- Validação cruzada estratificada (5 partições)
- Métricas: AUC-ROC, recall, precisão, F1 e acurácia

## Resultados (conjunto de teste)
| Modelo | AUC-ROC | Recall | Precisão | F1 | Acurácia |
|---|---|---|---|---|---|
| Regressão Logística | 0,7482 | 0,6763 | 0,1610 | 0,2601 | 0,6894 |
| Random Forest | 0,7339 | 0,5831 | 0,1717 | 0,2653 | 0,7393 |
| XGBoost | 0,7598 | 0,6846 | 0,1678 | 0,2695 | 0,7004 |

## Autores
Eduardo Thomaz e Dionatan Willian Rodrigues Oliveira.
Orientador: Me. Januario Ernesto António Domingos.
