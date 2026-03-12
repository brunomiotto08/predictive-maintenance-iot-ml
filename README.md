# Sistema Inteligente de Manutenção Preditiva com Algoritmos Não-Lineares para IoT Industrial

Este projeto consiste em uma Prova de Conceito (PoC) de um modelo de Machine Learning voltado para a manutenção preditiva de ativos industriais críticos, especificamente uma Autoclave de produção. O objetivo central é identificar padrões sutis de desgaste nos dados dos sensores antes que ocorram falhas e paradas não programadas.

##  Contexto do Projeto
O trabalho foi desenvolvido em parceria com a empresa **Habilita Soluções em Automação** para resolver a ineficiência da manutenção tradicional, que gera altos custos operacionais com interrupções imprevistas.

O sistema utiliza um CLP (Controlador Lógico Programável) que envia dados via protocolo **MQTT** para um broker Mosquitto, permitindo o monitoramento em tempo real.

##  Tecnologias e Ferramentas
- **Linguagem:** Python
- **Bibliotecas de ML:** Scikit-learn (Random Forest, PCA, StandardScaler)
- **Análise de Dados:** Pandas, NumPy
- **Visualização:** Matplotlib, Seaborn
- **Infraestrutura:** Supabase (PostgreSQL), Protocolo MQTT (Mosquitto) 

##   Metodologia de Machine Learning
O pipeline de dados implementado no projeto segue as seguintes etapas:

1. **Pré-processamento:** Escalonamento de dados com `StandardScaler` e tratamento de valores nulos.
2. **Redução de Dimensionalidade:** Aplicação de **PCA** (Principal Component Analysis) para reduzir os dados a 3 componentes principais.
3. **Modelagem:** Utilização do algoritmo **Random Forest Classifier** com pesos de classe balanceados.
4. **Validação:** Técnica de **K-Fold Cross-Validation** (5 folds) para garantir a robustez dos resultados.

## Resultados Alcançados
O modelo demonstrou uma alta capacidade de identificar riscos de falha, alcançando métricas de desempenho excelentes:
- **Recall Médio:** ~0.9657 (96,57%) na validação cruzada.
- **Acurácia:** Alta precisão na distinção entre estado normal e risco elevado.

O projeto foi validado tecnicamente e considerado com alto potencial de aplicação prática no setor industrial pela empresa parceira.

##  Estrutura de Arquivos
- `aplicacao_final.ipynb`: Notebook com o pipeline completo de treinamento e avaliação.
- `dados_20000_para_ml.csv`: Conjunto de dados utilizado para o desenvolvimento do modelo.
- `Relatorio_tecnico_final.pdf`: Documentação detalhada da fundamentação teórica e arquitetura.
- `parecer_tecnico_assinado.pdf`: Avaliação e validação da empresa parceira.

##  Como Executar
1. Certifique-se de ter as dependências instaladas:
   ```bash
   pip install pandas numpy matplotlib seaborn scikit-learn joblib
