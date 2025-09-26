# Anotações: Desenvolvendo Soluções de Machine Learning

## 1. O Ciclo de Vida do Desenvolvimento de Machine Learning (ML)

O ciclo de vida de ML refere-se ao processo completo de ponta a ponta para desenvolver, implantar e manter modelos de machine learning.  
É um processo **iterativo**, onde o modelo é continuamente aprimorado à medida que novos dados se tornam disponíveis ou os requisitos mudam, garantindo que ele permaneça preciso e relevante.

### Fases do Ciclo de Vida

#### Fase 1: Identificação de Metas de Negócios e Definição do Problema de ML
- **Objetivo:** Entender o problema de negócio e traduzi-lo em um problema de machine learning.  
- **Processo:** Começa com a identificação de uma meta de negócio clara. Em seguida, essa meta é convertida em um problema técnico que o ML pode resolver, como prever uma categoria (**classificação**) ou um valor (**regressão**).

---

#### Fase 2: Processamento de Dados
- **Objetivo:** Converter dados brutos em um formato utilizável e de alta qualidade para treinar um modelo preciso.  
- **Etapas:**
  - **Coleta e Integração de Dados:** Reunir dados brutos de diversas fontes e centralizá-los.  
  - **Pré-processamento e Visualização:** Transformar e limpar os dados, além de usar visualizações para entender características e distribuições.  
  - **Engenharia de Atributos:** Criar, transformar, extrair e selecionar variáveis mais relevantes para entrada do modelo.  

---

#### Fase 3: Desenvolvimento de Modelos
- **Objetivo:** Treinar, ajustar e avaliar o modelo para atingir o desempenho desejado.  
- **Etapas:**
  - **Divisão dos Dados:**
    - Treinamento (70-80%)
    - Validação (10-15%)
    - Teste (10-15%)  
  - **Treinamento:** O algoritmo aprende padrões a partir dos dados.  
  - **Ajuste (Tuning):** Ajuste de hiperparâmetros e mais engenharia de atributos.  
  - **Avaliação:** Avaliar com o conjunto de teste, evitando usar os mesmos dados de treinamento.  

---

#### Fase 4: Implantação do Modelo
- **Objetivo:** Colocar o modelo treinado e validado em um ambiente de produção.  
- **Processo:** Uma vez que os resultados da avaliação são satisfatórios, o modelo é implantado e passa a realizar previsões com dados reais.  

---

#### Fase 5: Monitoramento de Modelos
- **Objetivo:** Garantir que o modelo em produção continue a ter o desempenho desejado ao longo do tempo.  
- **Processo:** Sistemas de monitoramento são implementados para detectar quedas de performance, depurar problemas e entender o comportamento do modelo.  

---

#### Fase 6: Retreinamento de Modelo
- **Objetivo:** Manter o modelo atualizado e preciso.  
- **Processo:** Quando ocorre o "model drift", o modelo precisa ser retreinado. Isso envolve reanalisar os dados e atributos, além de ajustes de hiperparâmetros.  

---

## 2. Estudo de Caso: Otimização do Call Center da Amazon

**Meta de Negócio:** Melhorar a eficiência do encaminhamento de chamadas de atendimento ao cliente, reduzindo o tempo de espera e o número de transferências. O sistema antigo, baseado em menus ("Pressione 1 para..."), era ineficiente devido à vasta gama de produtos da Amazon.  

**Formulação do Problema de ML:** Converter o problema de negócio em prever qual "habilidade" de atendente resolveria o problema do cliente. Tecnicamente, trata-se de um problema de **classificação multiclasse**.  

### Coleta e Integração de Dados
Baseado em dados históricos de chamadas (aprendizado supervisionado), incluindo:  
- Pedidos recentes do cliente  
- Se o cliente possuía um Kindle  
- Se o cliente era membro Prime  

Os rótulos eram as "habilidades" corretas dos atendentes que resolveram as chamadas no passado.  

### Pré-processamento e Visualização
- **Limpeza e Análise:** Avaliar rótulos imprecisos e combinar rótulos semelhantes.  
- **Exemplo:** Vários rótulos de problemas do Kindle foram agrupados em "habilidade Kindle".  
- **Visualização:** Distribuição das chamadas (ex: 40% devoluções, 30% Prime, etc.).  

### Desenvolvimento e Avaliação
- **Divisão dos Dados:** Treinamento, validação e teste.  
- **Ajuste e Engenharia de Atributos:** Otimização de hiperparâmetros e criação de novos atributos.  
- **Avaliação:** Usar dados de teste "invisíveis". Métrica principal: redução no número de transferências.  

### Implantação e Resultados
- O modelo foi implantado em produção.  
- Houve uma redução significativa no número de transferências, melhorando a experiência do cliente e aumentando a eficiência da empresa.  
