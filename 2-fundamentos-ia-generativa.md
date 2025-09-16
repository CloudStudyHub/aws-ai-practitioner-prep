# 📘 Domínio 2 – Fundamentos de IA Generativa 

Este domínio aprofunda os conceitos que definem a Inteligência Artificial (IA) Generativa, suas capacidades, aplicações, limitações e a infraestrutura que a AWS oferece para construir e desenvolver soluções.

---

## 🔹 Tarefa 2.1: Explicar os conceitos básicos de IA generativa

O objetivo desta seção é construir um vocabulário sólido sobre os componentes e processos da IA Generativa.

### IA Generativa (Generative AI)
É um subconjunto do deep learning (aprendizado profundo) focado em gerar conteúdo novo e original, como textos, imagens e músicas, em vez de apenas classificar ou analisar dados existentes.

### Modelos de Base (Foundation Models - FMs)
São modelos de rede neural de grande escala e complexidade, pré-treinados em vastas quantidades de dados. Eles podem ser adaptados (com ajuste fino) para uma ampla variedade de tarefas.

### Modelos de Linguagem de Grande Porte (Large Language Models - LLMs)
Quando um Modelo de Base é focado especificamente em tarefas de linguagem, ele é chamado de LLM.

### Conceitos Essenciais

**Tokens e Fragmentação (Tokenization):** Modelos de linguagem não processam palavras inteiras, mas sim "tokens". Tokens são as menores unidades de informação, como palavras, partes de palavras ou pontuação. A fragmentação é o processo de quebrar um texto nesses pedaços menores. O custo de uso de um LLM é frequentemente medido pela quantidade de tokens processados na entrada e na saída.

**Incorporações (Embeddings) e Vetores:** São representações numéricas (vetores) de tokens, palavras ou frases. Essas representações capturam o significado semântico e as relações entre as palavras. Palavras com significados semelhantes terão vetores matematicamente próximos.

**Prompt:** É a entrada de texto fornecida ao modelo para guiá-lo a gerar uma resposta.

**Engenharia de Prompts (Prompt Engineering):** É a arte e a ciência de criar e otimizar prompts eficazes para guiar um modelo de IA Generativa a produzir a saída desejada. Um bom prompt é claro, específico e fornece contexto.

**Arquitetura Transformer:** É a tecnologia fundamental por trás da maioria dos LLMs modernos. Introduzida em 2017, sua principal inovação é o "mecanismo de atenção", que permite ao modelo pesar a importância de diferentes palavras em uma sequência, compreendendo o contexto de forma muito mais eficaz.

### Tipos de Modelos

**Modelos Unimodais e Multimodais:** Modelos unimodais trabalham com apenas um tipo de dado (como texto). Modelos multimodais podem processar e entender múltiplos tipos de dados simultaneamente, como texto e imagens.

**Modelos de Difusão (Diffusion Models):** Uma classe de modelos generativos muito eficazes na geração de imagens de alta qualidade. Eles funcionam adicionando ruído a uma imagem e, em seguida, aprendem a reverter o processo para gerar uma nova imagem, guiados por um prompt de texto.

### Casos de Uso Comuns

- **Geração de Conteúdo:** Criação de imagens, áudio, música e vídeos.  
- **Resumo:** Condensação de longos documentos e conversas.  
- **Chatbots e Atendentes Virtuais:** Criação de assistentes de conversação mais naturais.  
- **Tradução:** Realização de traduções de alta qualidade que capturam nuances.  
- **Geração de Código:** Escrita, preenchimento e depuração de código de programação.

---

## 🔹 Tarefa 2.2: Entender os recursos e as limitações da IA generativa

### Vantagens e Capacidades

- **Adaptabilidade:** Modelos de base podem ser rapidamente adaptados para diversas tarefas (processo chamado de fine-tuning ou ajuste fino), em vez de construir um modelo do zero para cada problema.  
- **Simplicidade e Acessibilidade:** A interação baseada em prompts de linguagem natural simplifica o acesso a funcionalidades complexas.  
- **Capacidade de Resposta:** Permitem a criação de interações mais dinâmicas e contextuais com usuários.

### Desvantagens, Riscos e Limitações

- **Alucinações:** A principal limitação, onde o modelo gera uma resposta que soa convincente, mas é factualmente incorreta ou completamente inventada.  
- **Vieses (Bias) e Toxicidade:** Os modelos podem reproduzir vieses ou linguagem tóxica presentes em seus dados de treinamento.  
- **Falta de Interpretabilidade:** É difícil entender por que o modelo gerou uma resposta específica, sendo considerados "caixas-pretas" (black boxes).  
- **Não Determinismo:** Para um mesmo prompt, o modelo pode gerar respostas diferentes a cada vez, o que é um desafio para processos que exigem consistência.

### Fatores para Escolha de um Modelo

- **Tipos de Modelo:** Se o foco é texto, imagem, código ou multimodal.  
- **Requisitos de Desempenho:** Latência (velocidade de resposta) e throughput (requisições por segundo).  
- **Recursos:** Se o modelo suporta o tamanho de contexto (quantidade de tokens) necessário.  
- **Conformidade:** Restrições de custo e conformidade com leis como GDPR e LGPD.

### Métricas de Valor Comercial

- **Métricas de Desempenho Técnico:** Acurácia e eficiência em benchmarks.  
- **Métricas de Negócio:** Taxa de Conversão, Receita Média por Usuário (ARPU), Valor da Vida Útil do Cliente (CLV) e Redução de Custos.

---

## 🔹 Tarefa 2.3: Descrever a infraestrutura e as tecnologias da AWS

### Serviços e Recursos da AWS

- **Amazon SageMaker JumpStart:** Atua como um hub de modelos, oferecendo acesso rápido a centenas de Modelos de Base pré-treinados para implantação e ajuste fino.  
- **Amazon Bedrock:** É um serviço totalmente gerenciado que fornece acesso aos principais Modelos de Base por meio de uma única API, eliminando a necessidade de gerenciar a infraestrutura.  
- **PartyRock (um Amazon Bedrock Playground):** Uma ferramenta online intuitiva que permite a qualquer pessoa criar e experimentar pequenos aplicativos de IA Generativa usando prompts, sem necessidade de conhecimento técnico.  
- **Amazon Q:** Um assistente de IA generativa projetado para o ambiente de trabalho, capaz de auxiliar em tarefas no ecossistema AWS.

### Vantagens de Usar os Serviços AWS

- **Acessibilidade e Menor Barreira de Entrada:** Serviços como Bedrock simplificam drasticamente o acesso a modelos poderosos.  
- **Eficiência e Custo-Benefício:** O modelo de pagamento é "pague pelo que usar", evitando o alto custo de treinar e hospedar FMs do zero.  
- **Velocidade de Comercialização (Time-to-Market):** Acelera o desenvolvimento de protótipos e aplicações.  
- **Segurança e Conformidade:** Aproveita os robustos recursos de segurança e as diversas certificações de conformidade da AWS.

### Compensações e Modelos de Custos

- **Preços Baseados em Tokens:** O custo é calculado pela quantidade de tokens de entrada e saída.  
- **Throughput de Provisão (Provisioned Throughput):** Opção de pagar por capacidade dedicada para garantir desempenho estável, a um custo fixo.  
- **Modelos Personalizados:** O ajuste fino (fine-tuning) e a hospedagem de modelos personalizados geram custos adicionais.

### Aprofundando em Conceitos-Chave

#### Ciclo de Vida do Modelo de Base

- **Seleção de Dados:** Coletar e filtrar datasets massivos e diversificados para o treinamento inicial.  
- **Seleção de Modelos:** Escolher a arquitetura e o tamanho do modelo de base que será treinado ou utilizado.  
- **Pré-treinamento:** O processo, computacionalmente intensivo, de treinar o modelo de base nos dados massivos coletados.  
- **Ajuste Fino (Fine-Tuning):** Adaptar o modelo pré-treinado a uma tarefa específica usando um dataset menor e mais focado.  
- **Avaliação:** Medir o desempenho e a segurança do modelo usando métricas e benchmarks específicos para a tarefa.  
- **Implantação:** Disponibilizar o modelo para uso em aplicações, geralmente através de uma API.  
- **Feedback:** Coletar dados sobre o desempenho do modelo em produção para orientar melhorias e futuros retreinamentos.

#### Métricas de Avaliação para Modelos Generativos

- **ROUGE (Recall-Oriented Understudy for Gisting Evaluation):** Utilizada principalmente para avaliar a qualidade de resumos de texto.  
- **BLEU (Bilingual Evaluation Understudy):** Usada para medir a qualidade de textos traduzidos automaticamente.

#### Infraestrutura de Hardware Otimizada da AWS

- **AWS Trainium:** Chips projetados especificamente para o treinamento de modelos de deep learning de forma mais rápida e com menor custo.  
- **AWS Inferentia:** Chips projetados para acelerar a inferência (a etapa de fazer previsões com um modelo já treinado), oferecendo alto desempenho com baixa latência.

---

# 🔹 Tabelas de Resumo

## Tabela 1 – Conceitos Básicos de IA Generativa

| Conceito | Definição / Descrição |
|----------|----------------------|
| IA Generativa | Subconjunto de deep learning focado em gerar conteúdo novo e original (texto, imagem, áudio, música) |
| Modelos de Base (FMs) | Modelos de rede neural grandes e pré-treinados, adaptáveis a várias tarefas |
| LLMs | Modelos de base focados especificamente em linguagem |
| Tokens / Tokenization | Quebra de texto em unidades menores; custo medido por tokens processados |
| Embeddings | Representações numéricas que capturam significado semântico e relações |
| Prompt | Entrada de texto fornecida ao modelo |
| Engenharia de Prompts | Arte de criar prompts claros e específicos |
| Transformer | Tecnologia de atenção que permite compreensão de contexto |
| Modelos Unimodais | Trabalham com um tipo de dado (texto) |
| Modelos Multimodais | Trabalham com múltiplos tipos de dados (texto + imagem) |
| Modelos de Difusão | Adição e remoção de ruído para gerar imagens guiadas por prompt |

## Tabela 2 – Casos de Uso Comuns

| Aplicação | Descrição |
|------------|-----------|
| Geração de Conteúdo | Criação de imagens, áudio, música e vídeos |
| Resumo | Condensação de longos documentos ou conversas |
| Chatbots / Assistentes | Assistentes de conversação mais naturais |
| Tradução | Tradução de alta qualidade que captura nuances |
| Geração de Código | Escrita, preenchimento e depuração de código |

## Tabela 3 – Vantagens e Limitações

| Categoria | Pontos Principais |
|-----------|-----------------|
| Vantagens | Adaptabilidade, simplicidade e acessibilidade, capacidade de resposta |
| Desvantagens / Riscos | Alucinações, vieses, falta de interpretabilidade, não determinismo |
| Fatores para Escolha | Tipo de modelo, desempenho, recursos, conformidade |
| Métricas de Valor Comercial | Técnica: acurácia e benchmarks; Negócio: conversão, ARPU, CLV, redução de custos |

## Tabela 4 – Serviços AWS para IA Generativa

| Serviço / Recurso | Descrição |
|------------------|-----------|
| SageMaker JumpStart | Hub de modelos pré-treinados para implantação e ajuste fino |
| Amazon Bedrock | Acesso a FMs via API sem gerenciar infraestrutura |
| PartyRock | Ferramenta online para criar apps de IA sem conhecimento técnico |
| Amazon Q | Assistente de IA generativa para tarefas na AWS |

## Tabela 5 – Vantagens e Custos AWS

| Categoria | Detalhes |
|-----------|----------|
| Vantagens | Acessibilidade, custo-eficiência, time-to-market, segurança e conformidade |
| Custos / Compensações | Preço por tokens, throughput provisionado, ajuste fino/modelos personalizados |

## Tabela 6 – Ciclo de Vida de um Modelo de Base

| Etapa | Descrição |
|-------|-----------|
| Seleção de Dados | Coletar e filtrar datasets massivos e diversificados |
| Seleção de Modelos | Escolher arquitetura e tamanho do modelo |
| Pré-Treinamento | Treinar modelo com dados massivos (intensivo) |
| Ajuste Fino | Adaptar modelo a tarefas específicas com dataset menor |
| Avaliação | Medir desempenho e segurança com métricas e benchmarks |
| Implantação | Disponibilizar via API para aplicações |
| Feedback | Coletar dados de uso para melhorias futuras |

## Tabela 7 – Métricas e Hardware AWS

| Categoria | Detalhes |
|-----------|----------|
| Métricas | ROUGE (resumos), BLEU (tradução automática) |
| Hardware | AWS Trainium: treino rápido e barato de deep learning<br>AWS Inferentia: inferência rápida e baixa latência |
