# 📘 Domínio 4 – Diretrizes para IA Responsável

Este domínio foca nos princípios e práticas para o desenvolvimento de sistemas de Inteligência Artificial (IA) que sejam éticos, justos, transparentes e confiáveis, abordando os riscos e as ferramentas para mitigá-los.

---

## 🔹 Tarefa 4.1: Explicar o desenvolvimento de sistemas de IA que são éticos e justos

Esta seção aborda os pilares da IA Responsável, desde a análise de viés nos dados até os riscos específicos da IA Generativa.

### Definição e Dimensões da IA Responsável

IA Responsável é um conjunto de diretrizes e princípios para garantir que os sistemas de IA operem de maneira segura, confiável e ética. Suas dimensões principais são:

- **Justiça (Fairness):** Garante que os modelos tratem todos os indivíduos de forma equitativa e imparcial, independentemente de idade, gênero, etnia ou outras características, evitando perpetuar ou amplificar vieses sociais.

- **Explicabilidade (Explainability):** Capacidade de explicar em termos humanos por que um modelo tomou uma decisão específica, como o motivo da rejeição de um pedido de empréstimo.

- **Robustez e Segurança (Robustness and Safety):** Assegura que os sistemas de IA sejam resistentes a falhas, ataques, comportamentos inesperados e minimizem erros.

- **Privacidade e Segurança (Privacy and Security):** Foca na proteção da privacidade do usuário e na não exposição de Informações de Identificação Pessoal (PII - Personally Identifiable Information).

- **Governança (Governance):** Cumprimento e auditoria de padrões da indústria e melhores práticas para mitigar riscos e garantir a conformidade.

- **Transparência (Transparency):** Fornece informações claras sobre as capacidades, limitações e riscos do modelo, garantindo que os usuários saibam quando estão interagindo com uma IA.

- **Inclusão:** Desenvolvimento de sistemas que sejam acessíveis e funcionem bem para uma ampla gama de usuários.

- **Veracidade (Truthfulness):** Garante que o modelo forneça informações precisas e evite gerar desinformação, como as alucinações.

---

### Viés (Bias) e Justiça (Fairness) em Modelos de IA

O viés ocorre quando há disparidades no desempenho de um modelo entre diferentes grupos, com resultados distorcidos a favor ou contra uma classe específica.

- **Origens do Viés:** Geralmente surge de problemas nos dados de treinamento.
- **Desequilíbrio de Classe:** Um grupo sub-representado nos dados (ex: 70% homens, 30% mulheres) pode gerar desempenho melhor para o grupo majoritário.
- **Dados Não Representativos:** Se os dados não refletem a diversidade do mundo real, o modelo pode sofrer de sobreajuste (overfitting) ou subajuste (underfitting).

---

### Riscos da IA Generativa e Ferramentas de Mitigação

- **Alucinações:** Informações factualmente incorretas geradas pelo modelo.
- **Violação de Propriedade Intelectual (PI):** Conteúdo muito semelhante a dados protegidos por direitos autorais.
- **Conteúdo Tóxico:** Geração de conteúdo ofensivo ou inadequado.
- **Privacidade de Dados:** Vazamento de dados sensíveis (PII ou segredos comerciais) para a saída do modelo.

**Ferramenta de Mitigação: Guardrails for Amazon Bedrock**

- Permite implementar políticas para controlar interações com modelos de IA Generativa.
- Define tópicos a evitar, filtra conteúdo prejudicial e remove PII.

---

### Ferramentas da AWS para Medir e Monitorar Viés

**Amazon SageMaker Clarify:** Ajuda a mitigar o viés, detectando-o em várias fases do ciclo de vida do ML:

- **Desequilíbrio de Classe e Rótulos:** Verifica se dados e resultados favorecem um grupo em detrimento de outro.
- **Disparidade Demográfica:** Mede se certos grupos enfrentam resultados enviesados.
- **Diferença de Acurácia e Recall:** Mede diferenças de desempenho entre grupos.

---

## 🔹 Tarefa 4.2: Reconhecer a importância de modelos transparentes e explicáveis

Esta seção aborda por que é crucial ser capaz de interpretar, explicar e confiar nas decisões de um modelo de IA.

### Diferenças entre Transparência e Explicabilidade

- **Modelos Transparentes (ou Interpretáveis):** Lógica interna fácil de entender (ex: regressão linear, árvores de decisão). Modelos de base complexos não são interpretáveis.
- **Modelos Explicáveis:** Modelos complexos tratados como "caixa-preta" (black-box), onde explicações são geradas por técnicas específicas.

### Trade-offs (Compromissos) da Transparência

- **Desempenho vs. Transparência:** Modelos mais complexos geralmente têm melhor desempenho; modelos simples podem sacrificar poder preditivo.
- **Segurança vs. Transparência:** Modelos muito transparentes podem ser mais vulneráveis a ataques.

---

### IA Centrada no Humano (Human-Centered AI)

- Design de sistemas que priorizam necessidades e valores humanos, aprimorando habilidades em vez de substituí-las.
- **Ferramenta:** Amazon Augmented AI (Amazon A2I) – fluxos de revisão humana automáticos para inferências de baixa confiança.

---

### Técnica: RLHF (Reinforcement Learning from Human Feedback)

- Alinha um LLM (Large Language Model ou Modelo de Linguagem de Grande Porte) com preferências humanas.
- Humanos classificam respostas do modelo; um modelo de recompensa é treinado com base nessas preferências e usado para ajustar o LLM.

---

### Ferramentas para Transparência e Explicabilidade

- **Amazon SageMaker Clarify e Valores de Shapley:** Detecta viés e determina importância de cada característica nas previsões.
- **SageMaker Model Cards (Cartões de Modelos):** Documentam dados de treinamento, usos, limitações e métricas.
- **AI Service Cards:** Documentação de serviços de IA, mostrando casos de uso e limitações.

---

# 📘 Domínio 4 – Resumos em Tabelas

---

## 🔹 Dimensões da IA Responsável

| Dimensão | Descrição |
|----------|-----------|
| Justiça (Fairness) | Garantir que o modelo trate todos de forma equitativa, evitando vieses sociais. |
| Explicabilidade (Explainability) | Capacidade de explicar decisões do modelo em termos humanos. |
| Robustez e Segurança (Robustness and Safety) | Sistemas resistentes a falhas, ataques e comportamentos inesperados. |
| Privacidade e Segurança (Privacy and Security) | Proteção da privacidade do usuário e dados sensíveis (PII). |
| Governança (Governance) | Cumprimento de padrões, auditoria e conformidade regulatória. |
| Transparência (Transparency) | Informações claras sobre capacidades, limitações e riscos do modelo. |
| Inclusão | Sistemas acessíveis e funcionais para diversos tipos de usuários. |
| Veracidade (Truthfulness) | Garantia de informações precisas, evitando alucinações. |

---

## 🔹 Viés e Justiça em Modelos de IA

| Conceito | Explicação |
|-----------|-----------|
| Desequilíbrio de Classe | Grupos sub-representados geram desempenho desigual nos modelos. |
| Dados Não Representativos | Treinamento com dados que não refletem diversidade do mundo real. |
| Overfitting | Modelo se ajusta demais aos dados de treinamento, falhando em generalizar. |
| Underfitting | Modelo simples demais para capturar padrões dos dados. |

---

## 🔹 Riscos da IA Generativa e Mitigações

| Risco | Descrição | Ferramenta de Mitigação |
|-------|-----------|------------------------|
| Alucinações | Informações incorretas ou inventadas pelo modelo. | Guardrails for Amazon Bedrock |
| Violação de PI | Conteúdo gerado muito semelhante a dados protegidos. | Guardrails, políticas de conteúdo |
| Conteúdo Tóxico | Geração de material ofensivo ou inadequado. | Guardrails, filtros de categorias |
| Privacidade de Dados | Vazamento de PII ou dados sensíveis. | Guardrails, remoção de PII |

---

## 🔹 Ferramentas da AWS para Medir e Monitorar Viés

| Ferramenta | Função | Métricas |
|------------|--------|----------|
| Amazon SageMaker Clarify | Detecta e mitiga viés em diferentes fases do ML | Desequilíbrio de Classe, Disparidade Demográfica, Diferença de Acurácia/Recall |
| Valores de Shapley | Explicabilidade | Determina importância de cada característica na previsão |
| SageMaker Model Cards | Documentação do modelo | Dados de treino, usos pretendidos, limitações, métricas de desempenho |
| AI Service Cards | Documentação de serviços de IA | Casos de uso e limitações dos serviços |

---

## 🔹 Transparência e Explicabilidade

| Conceito | Descrição | Exemplos |
|-----------|-----------|----------|
| Modelos Transparentes | Lógica interna fácil de entender | Regressão Linear, Árvores de Decisão |
| Modelos Explicáveis | Caixa-preta, mas com técnicas para gerar explicações | Redes Neurais Profundas, LLMs ajustados por RLHF |
| Trade-offs | Compromissos entre desempenho, transparência e segurança | Modelos simples vs complexos |

---

## 🔹 Human-Centered AI e Técnicas

| Técnica/Ferramenta | Descrição |
|-------------------|-----------|
| Amazon Augmented AI (A2I) | Revisão humana automática para inferências de baixa confiança |
| RLHF (Reinforcement Learning from Human Feedback) | Alinhamento de LLMs com preferências humanas usando feedback humano |
| Amazon SageMaker Ground Truth | Coleta de preferências humanas para treinar modelos de recompensa |

---


