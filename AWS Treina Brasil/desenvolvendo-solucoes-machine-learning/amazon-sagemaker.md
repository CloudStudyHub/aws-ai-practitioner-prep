# Anotações: Amazon SageMaker

## Visão Geral

O **Amazon SageMaker** é um serviço de Machine Learning (ML) totalmente gerenciado.  
Ele foi projetado para simplificar o ciclo de vida do desenvolvimento de ML em uma **interface visual unificada**, permitindo:

- Coletar e preparar dados  
- Criar e treinar modelos de ML  
- Implantar modelos  
- Monitorar o desempenho das previsões  

Com o SageMaker, é possível realizar todas as etapas do ciclo de vida de ML, desde a coleta de dados até a implantação e monitoramento em produção.

---

## Fases do Ciclo de Vida de ML com SageMaker

### 1. Coletar, Analisar e Preparar Dados
Ferramentas disponíveis:  

- **Amazon SageMaker Data Wrangler**  
  Ferramenta LCNC (low-code/no-code) para importar, preparar, transformar, caracterizar e analisar dados em interface web.  
  - Permite personalização com scripts em Python.  

- **Amazon SageMaker Studio Classic**  
  Voltado para preparação em larga escala, com integração a **Amazon EMR** e **AWS Glue**, permitindo fluxos de dados e ML em grande escala.  

- **API de Processamento do SageMaker**  
  Possibilita executar scripts e cadernos para processamento e análise de dados.  
  - Suporta frameworks como **Scikit-learn, MXNet, PyTorch**, em ambientes totalmente gerenciados.  

**Resultado esperado:** atributos e dados organizados para definir e treinar o modelo.

---

### 2. Gerenciamento de Atributos
- **Amazon SageMaker Feature Store**  
  Ajuda cientistas de dados e engenheiros de ML a **criar, compartilhar e gerenciar atributos**.  
  - Os atributos armazenados podem ser recuperados e enriquecidos antes de alimentar os modelos.  

---

### 3. Treinamento e Avaliação de Modelos

**Treinamento**
- O SageMaker cria um **trabalho de treinamento** para usar algoritmos integrados ou personalizados.  
- Ele gerencia as instâncias de computação, executa o código e treina o modelo com os dados fornecidos.  
- Os artefatos resultantes ficam armazenados em **Amazon S3**.  

**Ferramentas adicionais:**
- **Amazon SageMaker Canvas:** opção LCNC para gerar previsões sem código.  
- **Amazon SageMaker JumpStart:** acesso a modelos pré-treinados e de código aberto para vários tipos de problemas.  

**Avaliação de Modelos**
- **Amazon SageMaker Experiments:** possibilita comparar diferentes combinações de dados, algoritmos e parâmetros.  
- **Amazon SageMaker Automatic Model Tuning:** ajusta hiperparâmetros automaticamente, testando várias combinações e avaliando resultados com base em métricas definidas.  

---

### 4. Implantação
- O SageMaker permite **implantar modelos treinados** para realizar previsões (inferência).  
- Oferece diferentes opções de infraestrutura e estratégias de implantação para atender a requisitos de produção.  

---

### 5. Monitoramento
- **Amazon SageMaker Model Monitor:** supervisiona a qualidade dos modelos em produção.  
- Suporta monitoramento **contínuo ou agendado**.  
- Detecta desvios em:  
  - Qualidade dos dados  
  - Qualidade do modelo  
  - Viés  
  - Atribuição de atributos  

---

## Ambientes e Ferramentas do SageMaker

### SageMaker Studio
Interface baseada na web, **recomendada como ponto central** para todo o ciclo de vida de ML.  
- Permite preparar dados, treinar, implantar e monitorar modelos.  

### Aplicações dentro do Studio
- **JupyterLab:** cadernos interativos para código e análise de dados.  
- **Amazon SageMaker Canvas:** ferramenta sem código para previsões.  
- **RStudio:** ambiente para programadores R.  
- **Editor de Código (VS Code):** editor baseado no Visual Studio Code com suporte a milhares de extensões.  

---

## ML Automatizado (AutoML)

- **SageMaker JumpStart:** oferece modelos de código aberto pré-treinados para acelerar projetos de ML.  
- **AutoML no SageMaker Canvas:** automatiza a criação e implantação de modelos.  
- **Avaliações de Modelos:** analisam **LLMs (Large Language Models)** e soluções de **IA generativa**, avaliando qualidade e responsabilidade.  

## Implementações de Modelos

O Amazon SageMaker oferece suporte a diferentes formas de criar e implantar modelos de Machine Learning:

- **Modelos pré-treinados**  
  - Exigem o mínimo esforço.  
  - Podem ser implantados diretamente ou ajustados e implantados usando o **SageMaker JumpStart**.  

- **Modelos integrados (algoritmos prontos do SageMaker)**  
  - Exigem mais esforço.  
  - São indicados para grandes conjuntos de dados e quando há necessidade de atributos significativos para treinar e implantar o modelo.  

- **Modelos com imagens pré-fabricadas**  
  - Suporte a frameworks populares como **Scikit-learn, TensorFlow, PyTorch, MXNet** e **Chainer**.  
  - Úteis quando não há solução integrada adequada.  

- **Imagens personalizadas do Docker**  
  - Permitem configurar e instalar pacotes ou softwares específicos necessários para o seu caso de uso.  

---

## Algoritmos Integrados do SageMaker

Os algoritmos integrados são oferecidos em diferentes categorias de problemas de Machine Learning.  
Aqui estão alguns exemplos comuns (consulte a documentação oficial para lista completa):

### Aprendizado Supervisionado
- Classificação  
- Regressão  

### Aprendizado Não Supervisionado
- Agrupamento (clustering)  
- Redução de dimensionalidade  
- Modelagem de tópicos  
- Reconhecimento de padrões  
- Detecção de anomalias  

### Processamento de Imagem
- Classificação de imagens  
- Detecção de objetos  
- Visão computacional  
- Séries temporais  

### Análise de Texto
- Processamento de linguagem natural (PLN)  
- Classificação ou resumo de documentos  
- Modelagem ou classificação de tópicos  
- Transcrição e tradução de idiomas  

---

## SageMaker JumpStart

O **SageMaker JumpStart** fornece acesso rápido a **modelos pré-treinados de código aberto** e soluções para problemas comuns de ML.

### Recursos do JumpStart
- Implantar, ajustar e avaliar modelos pré-treinados dos principais hubs de modelos.  
- Permite treinar e ajustar incrementalmente modelos antes da implantação.  
- Oferece **modelos de solução** que já configuram a infraestrutura necessária para casos de uso recorrentes.  
- Inclui **cadernos de exemplo executáveis**, facilitando o aprendizado e experimentação com ML no SageMaker.  

