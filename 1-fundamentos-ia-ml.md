# 📘 Domínio 1 – Fundamentos de IA e ML

Este resumo cobre os **conceitos essenciais** de Inteligência Artificial (IA) e Machine Learning (Aprendizado de Máquina), o ciclo de vida de projetos de ML, casos de uso práticos, técnicas, tipos de dados e serviços AWS.

---

## 🔹 1.1 Conceitos e terminologias básicos de IA

- **Inteligência Artificial (IA):** Sistemas que realizam tarefas que normalmente exigem inteligência humana, como raciocínio, aprendizado, percepção e tomada de decisão.  
- **Machine Learning (ML) – Aprendizado de Máquina:** Subcampo da IA em que computadores aprendem padrões a partir de dados, sem programação explícita de regras.  
- **Deep Learning (Aprendizado Profundo):** Subcampo do ML que utiliza redes neurais profundas para aprender padrões complexos e realizar tarefas avançadas.  
- **Redes Neurais (Neural Networks):** Modelos inspirados no cérebro humano, compostos por neurônios artificiais interconectados que processam informações.  
- **Visão Computacional (Computer Vision):** Aplicação de IA para análise de imagens e vídeos, incluindo reconhecimento de objetos, faces e cenários.  
- **Processamento de Linguagem Natural (Natural Language Processing – NLP):** Área da IA voltada para interação com linguagem humana, incluindo análise de texto, tradução e chatbots.  
- **Modelo (Model):** Resultado do treinamento de um algoritmo, usado para realizar previsões ou classificações em novos dados.  
- **Algoritmo (Algorithm):** Conjunto de regras que aprende padrões nos dados.  
- **Treinamento (Training):** Processo de alimentar o algoritmo com dados rotulados ou não para aprender padrões.  
- **Inferência (Inference):** Utilização do modelo treinado para prever resultados em novos dados.  
- **Viés (Bias):** Tendência de um modelo cometer erros sistemáticos devido a dados ou suposições enviesadas.  
- **Imparcialidade (Fairness):** Garantia de que o modelo não produza resultados discriminatórios ou injustos.  
- **Ajuste de Hiperparâmetros (Hyperparameter Tuning):** Processo de otimizar parâmetros que controlam o comportamento do algoritmo para melhorar a performance.  
- **Large Language Model (LLM – Modelo de Linguagem de Grande Porte):** Modelos de Deep Learning treinados em grandes volumes de texto para gerar ou compreender linguagem natural, ex.: GPT.  

### Relações
- IA é o conceito mais amplo.  
- ML é um subconjunto da IA.  
- Deep Learning é um subconjunto do ML.  

### Tipos de Inferência
- **Batch (em lote):** Processamento de grandes volumes de dados simultaneamente, como relatórios mensais.  
- **Tempo Real (Real-Time):** Processamento instantâneo de dados, como detecção de fraude em transações.  

### Tipos de Dados
- **Rotulados x Não Rotulados** – Dados com ou sem resposta conhecida.  
- **Estruturados x Não Estruturados** – Dados organizados (tabelas) versus não organizados (texto, imagens).  
- **Tabulares, Séries Temporais, Imagens, Textos** – Diferentes formatos de dados utilizados em ML.  

### Tipos de Aprendizado
- **Supervisionado:** Dados rotulados são usados para treinar o modelo a prever saídas.  
- **Não Supervisionado:** Dados sem rótulos, usados para descobrir padrões ou agrupamentos.  
- **Por Reforço (Reinforcement Learning):** Agente aprende por tentativa e erro, maximizando recompensas em um ambiente.  

---

## 🔹 1.2 Casos de uso práticos de IA

### Benefícios
- Apoio à tomada de decisão baseada em dados.  
- Escalabilidade de processos e operações.  
- Automação de tarefas repetitivas.  

### Quando NÃO usar IA/ML
- Quando o custo de implementação supera os benefícios.  
- Quando é necessária uma resposta 100% determinística (sem margem de erro).  

### Principais Técnicas
- **Regressão (Regression):** Previsão de valores contínuos, ex.: preço de imóveis.  
- **Classificação (Classification):** Previsão de categorias, ex.: spam x não spam.  
- **Clustering (Agrupamento):** Agrupamento de dados sem rótulos, ex.: segmentação de clientes.  

### Exemplos Reais
- **Visão Computacional:** Reconhecimento facial, carros autônomos.  
- **Processamento de Linguagem Natural:** Chatbots, tradução automática.  
- **Fala:** Assistentes virtuais, transcrição de áudio.  
- **Recomendação:** Netflix, Amazon (sistemas de recomendação).  
- **Detecção de Fraude:** Cartões de crédito.  
- **Previsão (Forecasting):** Demanda de estoque, previsão do tempo.  

### Serviços AWS Citados
- **Amazon SageMaker:** Serviço para construir, treinar e implantar modelos de ML de forma escalável.  
- **Amazon Transcribe:** Converte fala em texto automaticamente (Speech-to-Text).  
- **Amazon Translate:** Serviço de tradução automática de textos entre idiomas.  
- **Amazon Comprehend:** Análise de textos e sentimentos usando NLP.  
- **Amazon Lex:** Criação de chatbots conversacionais com NLP.  
- **Amazon Polly:** Serviço que converte texto em fala (Text-to-Speech).  

---

## 🔹 1.3 Ciclo de vida do desenvolvimento de ML

### Etapas Principais
1. **Coleta de dados** – Obtenção das informações relevantes.  
2. **Análise Exploratória de Dados (Exploratory Data Analysis – EDA)** – Entendimento das características do conjunto de dados.  
3. **Pré-processamento (Preprocessing)** – Limpeza e transformação de dados para treino.  
4. **Engenharia de Atributos (Feature Engineering)** – Criação de novas variáveis ou seleção das mais importantes.  
5. **Treinamento do Modelo (Model Training)** – Aprendizado do algoritmo a partir dos dados.  
6. **Ajuste de Hiperparâmetros (Hyperparameter Tuning)** – Otimização dos parâmetros do modelo.  
7. **Avaliação (Evaluation)** – Medição da performance usando métricas técnicas e de negócio.  
8. **Implantação (Deployment)** – Colocando o modelo em produção.  
9. **Monitoramento (Monitoring)** – Acompanhamento contínuo do desempenho do modelo.  

### Origens de Modelos
- **Pré-treinados (Pre-trained Models):** Modelos já treinados e prontos para uso ou fine-tuning.  
- **Treinados do Zero (From Scratch):** Modelos construídos totalmente do início para personalização máxima. 
- **Transfer Learning (Aprendizado por Transferência):** Processo de usar um modelo pré-treinado como ponto de partida para uma nova tarefa, aproveitando conhecimento já aprendido.

### Formas de Uso em Produção
- **Serviços Gerenciados (Managed Services):** Ex.: SageMaker API.  
- **Self-Hosted (Servidores Próprios):** Modelos hospedados em infraestrutura própria.  

### MLOps
- Aplicação de princípios DevOps ao ML.  
- Princípios: automação, escalabilidade, monitoramento, retreinamento.  

### Métricas de Avaliação
- **Técnicas:** Acurácia, Área sob a Curva (AUC), F1-Score.  
- **De Negócio:** Retorno sobre Investimento (ROI), custo por usuário, aumento de vendas.  

---

## 🔹 Métricas de Avaliação de Modelos de Machine Learning

As métricas são usadas para medir a performance de modelos de **classificação** ou **regressão**. Aqui focamos nas métricas mais comuns em classificação:

---

### 1️⃣ Acurácia (Accuracy)
- **Definição:** Proporção de previsões corretas em relação ao total de previsões.  
- **Fórmula:**  
\[
\text{Acurácia} = \frac{\text{Verdadeiros Positivos + Verdadeiros Negativos}}{\text{Total de Previsões}}
\]  
- **Exemplo:** Se um modelo classificou corretamente 90 de 100 casos, a acurácia = 90%.

- **Observação:** Funciona bem quando as classes estão balanceadas; pode ser enganosa em datasets desbalanceados.

---

### 2️⃣ Área sob a Curva ROC (AUC – Area Under the Curve)
- **Definição:** Mede a capacidade do modelo de **distinguir entre classes** (positiva e negativa).  
- **Intervalo:** 0 a 1 (quanto mais próximo de 1, melhor).  
- **Interpretação:**  
  - 0,5 → modelo aleatório  
  - 0,7–0,8 → bom desempenho  
  - 0,9–1 → excelente desempenho  

- **Uso:** Avaliação de modelos probabilísticos, especialmente em desequilíbrio de classes.

---

### 3️⃣ F1-Score
- **Definição:** Média harmônica entre **precisão** e **recall**, equilibrando os dois.  
- **Fórmula:**  
\[
F1 = 2 \times \frac{\text{Precisão} \times \text{Recall}}{\text{Precisão + Recall}}
\]  

- **Precisão (Precision):** Proporção de previsões positivas corretas sobre todas as previsões positivas.  
\[
\text{Precisão} = \frac{\text{Verdadeiros Positivos}}{\text{Verdadeiros Positivos + Falsos Positivos}}
\]

- **Recall (Sensibilidade):** Proporção de previsões positivas corretas sobre todos os casos realmente positivos.  
\[
\text{Recall} = \frac{\text{Verdadeiros Positivos}}{\text{Verdadeiros Positivos + Falsos Negativos}}
\]

- **Exemplo:**  
  - Verdadeiros Positivos = 80  
  - Falsos Positivos = 20  
  - Falsos Negativos = 10  
  - Precisão = 80 / (80 + 20) = 0,8  
  - Recall = 80 / (80 + 10) = 0,888  
  - F1-Score = 2 * (0,8 * 0,888) / (0,8 + 0,888) ≈ 0,842  

- **Observação:** Indicada quando há **classes desbalanceadas**, ex.: detecção de fraude.

---

Essas métricas ajudam a avaliar **técnica e negócio**, garantindo que o modelo seja eficiente e confiável antes de entrar em produção.


## 📝 Tabela de Revisão Rápida

| Conceito | Significado / Descrição |
|----------|------------------------|
| IA | Inteligência Artificial – sistemas que realizam tarefas inteligentes. |
| ML | Machine Learning – aprendizado de máquina a partir de dados. |
| DL | Deep Learning – aprendizado profundo com redes neurais profundas. |
| Redes Neurais | Modelos inspirados no cérebro para processar dados complexos. |
| PLN / NLP | Processamento de Linguagem Natural – análise de textos e fala. |
| Visão Computacional / Computer Vision | IA aplicada a imagens e vídeos. |
| LLM | Large Language Model – modelos de linguagem treinados em grandes volumes de texto. |
| Batch | Inferência em lote, processando muitos dados simultaneamente. |
| Tempo Real | Inferência instantânea, resposta imediata. |
| Supervisionado | Treinamento com dados rotulados. |
| Não Supervisionado | Treinamento sem dados rotulados, descoberta de padrões. |
| Reforço | Aprendizado por tentativa e erro com recompensas. |
| Regressão | Previsão de valores contínuos. |
| Classificação | Previsão de categorias. |
| Clustering | Agrupamento de dados sem rótulos. |
| SageMaker | Serviço AWS para construir, treinar e implantar modelos ML. |
| Transcribe | Serviço AWS para converter fala em texto. |
| Translate | Serviço AWS de tradução automática. |
| Comprehend | Serviço AWS de análise de texto e sentimentos. |
| Lex | Serviço AWS para criação de chatbots. |
| Polly | Serviço AWS que converte texto em fala. |
| MLOps | DevOps aplicado a ML, incluindo automação e monitoramento. |

