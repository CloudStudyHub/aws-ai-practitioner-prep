# Serviços e ferramentas da Amazon para IA responsável

Como líder em tecnologias de nuvem, a AWS oferece serviços como o **Amazon SageMaker** e o **Amazon Bedrock**, com ferramentas integradas para ajudar você a aplicar uma **IA responsável**. Essas ferramentas cobrem tópicos como:

- Avaliação de modelos de base
- Proteções da IA generativa
- Detecção de viés
- Explicações de previsão de modelos
- Monitoramento e revisões humanas
- Melhoria da governança

---

## Amazon SageMaker

O **Amazon SageMaker** é um serviço de machine learning totalmente gerenciado. Ele permite que cientistas de dados e desenvolvedores criem, treinem e implantem modelos de ML de forma rápida e confiável em um ambiente pronto para produção.

### Principais recursos

- Interface de usuário para fluxos de trabalho de ML em diferentes IDEs.
- Armazenamento e compartilhamento de dados sem gerenciar servidores.
- Algoritmos gerenciados para grandes volumes de dados.
- Treinamento distribuído e personalizável.
- Implantação segura e escalável de modelos.

---

## Amazon Bedrock

O **Amazon Bedrock** é um serviço gerenciado que fornece **Foundation Models (FMs)** de alto desempenho por meio de uma API unificada. Ele oferece:

- Variedade de FMs para diferentes casos de uso.
- Desenvolvimento de aplicações de IA generativa com segurança e privacidade.
- Experiência sem servidor para personalizar modelos com dados próprios.
- Integração e implantação seguras em aplicações sem gerenciar infraestrutura.

---

## Ferramentas de IA responsável

### Avaliação de modelo de base

#### Amazon Bedrock
- Avaliação automática: métricas como precisão, robustez e toxicidade.
- Avaliação humana: métricas subjetivas, como estilo e alinhamento com a marca.

#### SageMaker Clarify
- Avalia FMs para IA generativa.
- Métricas: precisão, robustez, toxicidade.
- Suporte para revisão humana sofisticada.

---

### Proteções para IA generativa

#### Guardrails for Amazon Bedrock
- Filtra conteúdo indesejado.
- Redige informações de identificação pessoal (PII).
- Monitoramento contínuo das interações.
- Criação de barreiras de proteção personalizadas.

#### Bloqueio de tópicos indesejáveis
- Definição de tópicos a serem evitados.
- Exemplo: assistente bancário evita consultoria de investimentos.

#### Filtro de conteúdo nocivo
- Limites configuráveis para ódio, insultos, sexo e violência.
- Avaliação automática de interações.

#### Redação de PII
- Detecta e redige dados pessoais nas respostas do modelo.
- Protege a privacidade do usuário.

---

### Detecção de viés

- **SageMaker Clarify**: identifica vieses em datasets e modelos.
- Atributos de entrada: gênero, idade, etc.
- Relatórios visuais com métricas de viés.
- **SageMaker Data Wrangler**: rebalanceamento de dados com subamostragem, sobreamostragem e SMOTE.

---

### Explicação sobre previsão do modelo

- **SageMaker Clarify + SageMaker Experiments**
- Avalia quais atributos contribuem para previsões.
- Visualização de importância agregada dos atributos.
- Ajuda a entender o comportamento do modelo.

---

### Monitoramento e revisões humanas

- **SageMaker Model Monitor**: monitora qualidade de modelos em produção, define alertas para desvios.
- **Amazon Augmented AI (A2I)**: cria fluxos de trabalho para revisão humana de previsões de ML.

---

### Melhoria da governança

Ferramentas de governança do SageMaker:

- **SageMaker Role Manager**: define permissões mínimas rapidamente.
- **SageMaker Model Cards**: captura e compartilha informações essenciais do modelo.
- **SageMaker Model Dashboard**: centraliza informações sobre o comportamento do modelo.

---

### Transparência com AI Service Cards

O **AWS AI Service Cards** fornece:

- Conceitos básicos sobre o serviço.
- Casos de uso intencionais e limitações.
- Considerações sobre design responsável de IA.
- Orientação sobre implantação e otimização.

**Público-alvo:** clientes, tecnólogos, pesquisadores e stakeholders interessados em IA responsável.

