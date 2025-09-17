# 🔹 Domínio 3: Aplicação de Modelos de Base (Foundation Models)

Este domínio aborda as decisões práticas de design, engenharia de prompts, personalização e avaliação de modelos de base para criar aplicações eficazes e alinhadas aos objetivos de negócio.

---

## Tarefa 3.1: Descrever as considerações sobre design de aplicações

Esta seção foca em como escolher, configurar e arquitetar soluções usando modelos de base pré-treinados.

### Critérios de Seleção para Modelos Pré-treinados

A escolha do modelo correto é fundamental e envolve analisar diversas características para encontrar o equilíbrio ideal entre desempenho e custo.

- **Custo e Complexidade:** Avalia o custo por token, de hospedagem e de ajuste fino. Modelos mais complexos e maiores geralmente são mais capazes, mas também mais caros e lentos.

- **Modalidade:** Determina se o modelo trabalha com um único tipo de dado (texto, imagem) ou se é multimodal, ou seja, capaz de processar múltiplos tipos de dados combinados.

- **Latência e Velocidade de Inferência:** Mede a rapidez com que o modelo responde. É um critério crítico para aplicações em tempo real, como chatbots interativos ou assistentes em veículos autônomos.

- **Tamanho da Janela de Contexto (Context Window):** Refere-se à quantidade máxima de tokens que o modelo pode processar em uma única chamada. Um contexto maior permite analisar documentos mais longos ou manter conversas mais complexas.

- **Suporte a Idiomas:** Verifica se o modelo suporta os idiomas necessários para a aplicação.

- **Capacidade de Personalização:** Confirma se o modelo permite ajuste fino (fine-tuning) para adaptá-lo a tarefas específicas.

### Parâmetros de Inferência: Controlando a Resposta do Modelo

São configurações usadas no momento da chamada do modelo (inferência) para influenciar o estilo e o formato da resposta gerada.

- **Temperatura (Temperature):** Controla a aleatoriedade da resposta.  
  - Temperatura Baixa (ex: 0.1): Gera respostas mais previsíveis, focadas e consistentes. Ideal para tarefas factuais como extração de informação ou resumo.  
  - Temperatura Alta (ex: 0.9): Produz respostas mais criativas, diversas e, por vezes, inesperadas. Útil para tarefas como escrita de marketing ou brainstorming.

- **Tamanho Máximo da Saída (Max Tokens):** Define o comprimento máximo da resposta gerada. Um valor muito baixo pode fazer com que a resposta seja cortada no meio.

---

### Geração Aumentada de Recuperação (RAG - Retrieval-Augmented Generation)

É uma técnica que aprimora os LLMs, permitindo que eles acessem e utilizem conhecimento de uma fonte externa e atualizada durante a geração da resposta.

- **Conceito e Funcionamento:** Em vez de depender apenas do seu conhecimento interno (que pode estar desatualizado), o sistema primeiro busca informações relevantes em uma base de conhecimento externa (como documentos da empresa) e, em seguida, insere essas informações no prompt como contexto para o LLM gerar a resposta.

- **Benefícios:** Ajuda a evitar alucinações, fundamentando as respostas em dados confiáveis, e resolve o problema de conhecimento desatualizado do modelo.

- **Implementação na AWS:** O recurso **Knowledge Bases for Amazon Bedrock** simplifica a implementação de RAG. O processo requer um banco de dados de vetores para armazenar os embeddings dos documentos. Serviços AWS compatíveis incluem:  
  - **Amazon OpenSearch Service:** Com a funcionalidade k-NN (k-Nearest Neighbors ou k-vizinhos mais próximos), um método para busca de similaridade em dados vetoriais.  
  - **Amazon Aurora e Amazon RDS (PostgreSQL):** Com a extensão pgvector, que habilita a busca por similaridade de vetores no PostgreSQL.  
  - **Amazon Neptune e Amazon DocumentDB:** Com capacidade de busca vetorial.

---

### Agentes (Agents)

São sistemas que usam um LLM como um "cérebro" para realizar tarefas complexas de múltiplas etapas que exigem interação com sistemas externos.

- **Conceito e Função:** Enquanto um LLM pode responder a uma pergunta, um agente pode executar uma ação no mundo real. Ele decompõe um pedido complexo (ex: "planeje minhas férias") em tarefas menores, chama APIs (para buscar voos, reservar hotéis) e orquestra o fluxo de trabalho até a conclusão.

- **Serviço AWS:** **Agents for Amazon Bedrock** é a capacidade que permite criar e gerenciar esses agentes para automatizar processos de negócio.

---

### Comparativo de Custos e Esforço de Personalização

Existem diferentes níveis de personalização, cada um com um custo e complexidade associados:

- **Pré-treinamento (do zero):** Custo mais alto. Raramente necessário, exige enormes volumes de dados e poder computacional, mas oferece personalização total.  

- **Ajuste Fino (Fine-Tuning):** Custo alto. Adapta um modelo pré-treinado a um domínio específico (ex: jurídico, médico) usando um dataset menor e rotulado. Melhora significativamente o desempenho em tarefas de nicho.

- **RAG:** Custo moderado. O custo vem do armazenamento de vetores e chamadas ao banco de dados, mas é muito mais barato que o ajuste fino. Excelente para fornecer conhecimento factual e atualizado.

- **Aprendizado em Contexto (In-context learning / Prompting):** Custo mais baixo. A "personalização" ocorre a cada chamada de API, fornecendo exemplos e contexto diretamente no prompt (few-shot prompting). Não altera os pesos do modelo, apenas guia sua resposta.

---

## Tarefa 3.2: Escolher técnicas eficazes de engenharia de prompts

É a prática de criar e otimizar os prompts para guiar o modelo a gerar a resposta mais apropriada e de alta qualidade.

### Técnicas Comuns de Engenharia de Prompts

- **Zero-shot Prompting:** Pedir ao modelo para realizar uma tarefa sem fornecer nenhum exemplo em que se basear.

- **Few-shot Prompting:** Incluir um ou alguns exemplos ("shots") de entrada e saída desejada diretamente no prompt para ajudar o modelo a entender o padrão e calibrar sua resposta.

- **Cadeia de Pensamento (CoT - Chain-of-Thought):** Instruir o modelo a "pensar passo a passo" ou detalhar seu raciocínio antes de dar a resposta final. Essa técnica melhora drasticamente o desempenho em problemas lógicos e matemáticos.

- **Prompts Negativos:** Instruções sobre o que o modelo deve evitar gerar em sua resposta.

### Riscos e Ameaças de Segurança

- **Exposição de Dados:** Risco de vazar informações sensíveis se forem incluídas no prompt enviado a uma API de terceiros.

- **Prompt Hijacking (Sequestro):** Um usuário mal-intencionado insere instruções em uma parte do prompt para fazer o modelo ignorar as instruções originais e executar uma tarefa diferente e não intencional.

- **Jailbreaking:** Tentativas de criar prompts que contornam os filtros de segurança e as barreiras de proteção (guardrails) do modelo para gerar conteúdo proibido ou malicioso.

---

## Tarefa 3.3: Descrever o processo de treinamento e ajuste fino

Esta seção aborda como os modelos são treinados e adaptados para tarefas específicas.

- **Pré-treinamento:** Fase inicial e massiva onde o modelo aprende padrões de linguagem, fatos e raciocínio a partir de um dataset geral e não estruturado, como a internet.

- **Ajuste Fino (Fine-Tuning):** Um segundo estágio de treinamento supervisionado. Ele adapta o modelo pré-treinado a um conjunto de dados menor e específico de uma tarefa ou domínio (ex: documentos jurídicos) para melhorar seu desempenho.

- **Aprendizado por Transferência (Transfer Learning):** É o conceito geral que fundamenta o ajuste fino, onde o conhecimento de um modelo pré-treinado é "transferido" para uma nova tarefa.

- **Limitação - Catastrophic Forgetting (Esquecimento Catastrófico):** O ajuste fino em uma única tarefa pode fazer com que o modelo "esqueça" ou degrade seu desempenho em outras tarefas que ele sabia executar.

- **PEFT (Parameter-Efficient Fine-Tuning ou Ajuste Fino Eficiente de Parâmetros):** Um conjunto de técnicas que congelam a maioria dos pesos do LLM original e treinam apenas um pequeno número de novos parâmetros. Isso reduz significativamente os custos de computação e memória.  

  - **LORA (Low-Rank Adaptation ou Adaptação de Baixo Rank):** Uma técnica popular de PEFT.

- **RLHF (Reinforcement Learning from Human Feedback ou Aprendizado por Reforço com Feedback Humano):** Uma técnica avançada para alinhar o comportamento do modelo com as preferências humanas, tornando-o mais útil e seguro. Humanos classificam as respostas do modelo, e um "modelo de recompensa" é treinado com base nessas preferências para, em seguida, ajustar o LLM original.

---

## Tarefa 3.4: Descrever os métodos para avaliar o desempenho

A avaliação mede se um modelo é "bom" tanto do ponto de vista técnico quanto do impacto no negócio.

### Abordagens de Avaliação

- **Avaliação Humana:** Considerado o "padrão ouro". Pessoas avaliam a qualidade das respostas com base em critérios como precisão, coerência e segurança. É eficaz, mas lento e caro.

- **Benchmarks (Conjuntos de Dados de Referência):** Avaliação automática do modelo em conjuntos de dados padronizados onde as respostas corretas são conhecidas. Permite uma comparação objetiva entre diferentes modelos. Exemplos incluem:  
  - GLUE (General Language Understanding Evaluation)  
  - MMLU (Massive Multitask Language Understanding)  
  - HELM (Holistic Evaluation of Language Models)

### Métricas de Avaliação Técnica

- **ROUGE (Recall-Oriented Understudy for Gisting Evaluation):** Usado para avaliar a qualidade de resumos, comparando o texto gerado com um resumo de referência.

- **BLEU (Bilingual Evaluation Understudy):** Usado para avaliar a qualidade de traduções automáticas, medindo a semelhança com traduções humanas.

- **BERTScore:** Uma métrica mais avançada que avalia a similaridade semântica (de significado) entre o texto gerado e o de referência, em vez de apenas contar palavras sobrepostas.

### Avaliação de Objetivos de Negócio

O impacto final é medido por indicadores de negócio:

- **Produtividade:** O modelo está ajudando os funcionários a economizar tempo ou a completar tarefas mais rapidamente?  

- **Envolvimento dos Usuários:** A satisfação do cliente aumentou? Os usuários estão interagindo mais com a aplicação?

# Tabelas de Resumo: Domínio 3 – Aplicação de Modelos de Base

---

## Tabela 1: Critérios de Seleção de Modelos de Base
Esta tabela resume os fatores a serem considerados ao escolher um modelo pré-treinado.

| Critério                     | Descrição / Considerações |
|-------------------------------|---------------------------|
| Custo e Complexidade          | Avalia o custo por token, de hospedagem e de ajuste fino. Modelos maiores e mais complexos são mais caros e lentos, mas geralmente mais capazes. |
| Modalidade                    | Define se o modelo trabalha com texto, imagem, áudio (unimodal) ou uma combinação deles (multimodal). |
| Latência                      | Mede a rapidez com que o modelo responde, um fator crítico para aplicações em tempo real. |
| Janela de Contexto            | Refere-se à quantidade máxima de tokens que o modelo pode processar em uma única chamada. Um contexto maior permite analisar documentos mais longos ou manter conversas complexas. |
| Capacidade de Personalização  | Verifica se o modelo permite ajuste fino (fine-tuning) para ser adaptado a tarefas ou domínios específicos. |
| Suporte a Idiomas             | Confirma se o modelo suporta os idiomas necessários para a aplicação. |

---

## Tabela 2: Comparativo de Métodos de Personalização de Modelos
Esta tabela compara as principais abordagens para adaptar um modelo, do mais simples ao mais complexo.

| Método                          | Custo / Esforço | Principal Vantagem e Caso de Uso |
|---------------------------------|----------------|---------------------------------|
| Aprendizado em Contexto (Prompting) | O mais baixo. A personalização ocorre a cada chamada de API. | Rápido e barato para guiar o comportamento do modelo em tempo real, sem alterar seus pesos. |
| RAG (Retrieval-Augmented Generation) | Moderado. O custo está no armazenamento de vetores e chamadas à base de dados. | Excelente para fornecer conhecimento factual, atualizado e específico do domínio, evitando alucinações. |
| Ajuste Fino (Fine-Tuning)       | Alto. Adapta um modelo pré-treinado usando um dataset menor e específico. | Melhora significativamente o desempenho para tarefas ou domínios específicos (ex: jurídico, médico). |
| Pré-treinamento (do zero)       | O mais alto. Exige enormes quantidades de dados e poder computacional. | Oferece personalização total, mas raramente é necessário para a maioria das aplicações de negócio. |

---

## Tabela 3: Técnicas de Engenharia de Prompts
Um resumo das principais técnicas para criar prompts eficazes.

| Técnica                            | Descrição |
|-----------------------------------|-----------|
| Zero-shot Prompting               | A tarefa é solicitada ao modelo sem fornecer nenhum exemplo de como realizá-la. |
| Few-shot Prompting                | O prompt inclui um ou alguns exemplos ("shots") de entrada e saída para guiar o modelo a calibrar sua resposta. |
| Cadeia de Pensamento (CoT - Chain-of-Thought) | O modelo é instruído a decompor seu raciocínio em etapas intermediárias antes de dar a resposta final, o que melhora o desempenho em tarefas lógicas e matemáticas. |

---

## Tabela 4: Riscos e Ameaças de Segurança em Prompts
Principais vulnerabilidades associadas à engenharia de prompts.

| Risco                        | Descrição |
|-------------------------------|-----------|
| Prompt Hijacking (Sequestro) | Um usuário mal-intencionado insere instruções no prompt para fazer o modelo ignorar as ordens originais e executar uma tarefa diferente. |
| Jailbreaking                  | Uma tentativa de criar prompts que contornam as barreiras de segurança (guardrails) do modelo para gerar conteúdo proibido ou malicioso. |
| Exposição de Dados            | Risco de vazar dados sensíveis se eles forem incluídos no prompt enviado a uma API de terceiros. |
| Prompt Injection              | Ataques de manipulação onde uma entrada não confiável de um usuário produz uma resposta maliciosa do modelo. |

---

## Tabela 5: Abordagens de Avaliação de Modelos
Comparativo entre os principais métodos para avaliar o desempenho de um modelo de base.

| Abordagem         | Descrição | Vantagens | Desvantagens |
|------------------|-----------|-----------|--------------|
| Avaliação Humana  | Pessoas avaliam a qualidade das respostas do modelo com base em critérios como precisão, coerência e segurança. | É o "padrão ouro" para medir a qualidade real e o alinhamento com as preferências humanas. | É um processo lento, caro e difícil de escalar. |
| Benchmarks        | Avaliação automática do modelo em conjuntos de dados padronizados (ex: GLUE, MMLU) onde as respostas corretas são conhecidas. | Permite uma comparação objetiva, rápida e escalável entre diferentes modelos. | Pode não capturar nuances de qualidade ou o alinhamento com os objetivos específicos do negócio. |

---

## Tabela 6: Métricas de Avaliação Técnica
Métricas comuns para medir o desempenho de tarefas específicas de IA Generativa.

| Métrica  | Significado | Principal Caso de Uso |
|----------|------------|---------------------|
| ROUGE    | Recall-Oriented Understudy for Gisting Evaluation | Avaliar a qualidade de resumos de texto gerados automaticamente. |
| BLEU     | Bilingual Evaluation Understudy | Avaliar a qualidade de textos traduzidos por máquina. |
| BERTScore | N/A | Avalia a similaridade semântica (de significado) entre o texto gerado e o de referência. |
