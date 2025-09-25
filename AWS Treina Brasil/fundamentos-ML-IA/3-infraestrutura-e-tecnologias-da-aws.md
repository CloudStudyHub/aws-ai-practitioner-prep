# Infraestrutura e Tecnologias da AWS

A AWS oferece um conjunto abrangente de serviços de ML e IA generativa que podem ajudar você a liberar todo o potencial dessas tecnologias transformadoras.

Nesta lição, você aprenderá sobre os vários serviços de IA e ML disponíveis na AWS, desde a compreensão de texto com o **Amazon Comprehend** até a geração de código com o **Amazon Q Developer**.  

Você também explorará as vantagens de usar os serviços de IA generativa da AWS e os benefícios da infraestrutura da AWS ao desenvolver aplicações de IA generativa.  
Por fim, conhecerá as vantagens e desvantagens de custos e as considerações ao usar essas ferramentas poderosas.

---

## Pilha de Serviços de IA/ML da AWS

Neste vídeo, você conhecerá a infraestrutura de IA/ML da AWS e as diferentes camadas e domínios para criar aplicações usando essas tecnologias.

### Estruturas de ML
No centro dessa camada está o **Amazon SageMaker**, um serviço de machine learning totalmente gerenciado que você pode usar para criar, treinar e implantar seus próprios modelos personalizados.  
Ele fornece ferramentas e infraestrutura para acelerar o ciclo de vida de desenvolvimento e implantação de ML.

### Serviços de IA/ML
Nessa camada, a AWS oferece serviços especializados para diferentes casos de uso:

- **Textos e Documentos**:  
  - Amazon Comprehend (PLN)  
  - Amazon Translate (tradução de idiomas)  
  - Amazon Textract (extração de dados de documentos)  

- **Chatbots**:  
  - Amazon Lex (interfaces de conversação, tecnologia do Alexa)  

- **Fala**:  
  - Amazon Polly (texto em fala)  
  - Amazon Transcribe (reconhecimento de voz)  

- **Visão**:  
  - Amazon Rekognition (análise de imagens e vídeos)  

- **Pesquisa**:  
  - Amazon Kendra (pesquisa corporativa inteligente)  

- **Recomendações**:  
  - Amazon Personalize (recomendações em tempo real)  

- **Diversos**:  
  - AWS DeepRacer (aprendizado por reforço em prática com carro autônomo)

### IA Generativa
A AWS oferece serviços e ferramentas baseados em **modelos de base (FMs)**:

- **Amazon SageMaker JumpStart** → soluções para casos de uso comuns.  
- **Amazon Bedrock** → FMs da Amazon e startups, acessíveis via API.  
- **PartyRock** → Playground prático para criação de aplicações com Bedrock.  
- **Amazon Q** → Assistente corporativo baseado em IA generativa.  
- **Amazon Q Developer** → Recomendações de código baseadas em ML.  

---

## Frameworks de ML

A camada de **frameworks de ML** é crucial no desenvolvimento e implantação de modelos.  

No centro está o **Amazon SageMaker**, que oferece as ferramentas necessárias para criar, treinar e executar **LLMs** e outros **FMs** de forma eficiente e econômica.

### Amazon SageMaker
- Criação, treinamento e implantação de modelos para qualquer caso de uso.  
- Infraestrutura e fluxos de trabalho totalmente gerenciados.  
- Reduz custos e esforço, acelerando a chegada dos modelos à produção.  

---

## Serviços de IA/ML

Além da infraestrutura, a AWS disponibiliza serviços prontos para uso:

### [Amazon Comprehend](https://aws.amazon.com/pt/comprehend/)
Usa PLN e ML para extrair informações de dados não estruturados:  
- Identificação de idioma  
- Extração de frases-chave, pessoas, lugares, marcas ou eventos  
- Análise de sentimentos (positivo/negativo)  
- Tokenização e partes do discurso  
- Organização automática de arquivos por tópicos  

### [Amazon Translate](https://aws.amazon.com/pt/translate/)
Serviço de tradução neural com aprendizado profundo, oferecendo:  
- Traduções rápidas e de alta qualidade  
- Localização de conteúdo (sites, apps etc.)  
- Tradução de grandes volumes de texto  
- Comunicação multilíngue eficiente  

### [Amazon Textract](https://aws.amazon.com/pt/textract/)
Extrai texto e dados de documentos digitalizados, indo além do OCR, pois:  
- Identifica campos em formulários  
- Extrai informações armazenadas em tabelas  

### [Amazon Lex](https://aws.amazon.com/pt/lex/)
Permite criar bots de voz e texto, com:  
- Reconhecimento automático de fala (ASR)  
- Compreensão de linguagem natural (NLU)  
- Construção de sistemas IVR e chatbots realistas  

### [Amazon Polly](https://aws.amazon.com/pt/polly/)
Transforma texto em fala realista, com:  
- Ampla variedade de vozes e idiomas  
- Aplicações habilitadas para fala em escala global  

### [Amazon Transcribe](https://aws.amazon.com/pt/transcribe/)
Reconhecimento de fala em texto:  
- Suporte a formatos WAV, MP3 e streaming em tempo real  
- Marcações de tempo por palavra  
- Uso em transcrição de chamadas, legendas e análises de conteúdo  

### [Amazon Rekognition](https://aws.amazon.com/pt/rekognition/)
Analisa imagens e vídeos com ML:  
- Identificação de objetos, cenas, atividades  
- Detecção de conteúdo impróprio  
- Recursos avançados de análise e comparação facial  

### [Amazon Kendra](https://aws.amazon.com/pt/kendra/)
Reinventa a pesquisa corporativa com ML, permitindo buscas inteligentes em sites e aplicações.

### [Amazon Personalize](https://aws.amazon.com/pt/personalize/)
Cria recomendações personalizadas em tempo real a partir de dados de usuários, itens e interações.

### [AWS DeepRacer](https://aws.amazon.com/pt/deepracer/)
Carro autônomo em escala 1/18 para aprendizado por reforço (RL):  
- Aprende comportamentos sem dados rotulados  
- Otimiza decisões de curto prazo para atingir objetivos de longo prazo  

---

## Serviços de IA Generativa

A camada de **IA generativa** inclui ferramentas para acelerar o desenvolvimento e integração de modelos:

### [Amazon SageMaker JumpStart](https://docs.aws.amazon.com/sagemaker/latest/dg/studio-jumpstart.html)
- Soluções pré-construídas para casos comuns  
- Suporte ao ajuste fino de +150 modelos open source  

### [Amazon Bedrock](https://aws.amazon.com/pt/bedrock/)
- FMs da Amazon e startups em API  
- Experiência serverless  
- Personalização privada com seus dados  

### [Amazon Q](https://aws.amazon.com/pt/q/)
- Assistente corporativo para responder perguntas, gerar conteúdo e simplificar decisões  

### [Amazon Q Developer](https://aws.amazon.com/pt/q/developer/)
- Recomendações de código com ML  
- Suporte a linguagens como C#, Java, JS, Python e TS  
- Integração com IDEs  
- Geração de blocos inteiros de código (10–15+ linhas)  


# Vantagens e Benefícios das Soluções de IA da AWS

De pequenas startups a grandes empresas, as organizações confiam na AWS para inovar com poderosas ferramentas de IA.  
A AWS oferece recursos de segurança e privacidade de alto nível para manter seus dados seguros e acesso aos modelos de IA mais avançados disponíveis.

Com a AWS, você pode criar e desenvolver suas próprias aplicações de IA personalizadas que usam IA generativa.  
Essas aplicações podem ser adaptadas de acordo com suas necessidades específicas, aproveitando a tecnologia de IA generativa para criar soluções verdadeiramente únicas e personalizadas.

A AWS fornece uma infraestrutura segura e compatível para criar aplicações de IA, utilizando:  
- Recursos de segurança robustos  
- Atributos de conformidade específicos do setor  
- Modelo de responsabilidade compartilhada  
- Serviços e ferramentas que apoiam o desenvolvimento e a implantação responsáveis e seguros de soluções de IA tradicionais e generativas  

---

## Considerações sobre Custos

Ao trabalhar com serviços de IA e ML na AWS, é essencial entender as várias considerações de custo envolvidas.  
Esses fatores podem afetar capacidade de resposta, disponibilidade, redundância, desempenho, cobertura regional, modelos de preços, throughput e uso de modelos personalizados.

### Capacidade de Resposta e Disponibilidade
Os serviços de IA generativa da AWS são projetados para serem altamente responsivos e disponíveis.  
Níveis mais altos de capacidade de resposta e disponibilidade geralmente têm custos maiores.  
Por exemplo, serviços com menor latência e implantação em várias regiões costumam ser mais caros.

### Redundância e Cobertura Regional
Para garantir alta disponibilidade, os serviços podem ser implantados em múltiplas **Zonas de Disponibilidade** ou **Regiões AWS**.  
Essa redundância gera custos adicionais devido ao provisionamento de recursos e replicação de dados.

### Desempenho
A AWS oferece opções de computação como **CPU, GPU e aceleradores de hardware personalizados**.  
Instâncias de GPU, embora mais caras, proporcionam melhorias significativas em workloads específicas.

### Preços Baseados em Tokens
Serviços como **Amazon Q Developer** e **Amazon Bedrock** usam modelo de preços baseado em **tokens**.  
O custo é proporcional à quantidade de tokens processados ou gerados.

### Throughput Provisionado
Serviços como **Amazon Polly** e **Amazon Transcribe** permitem provisionar throughput com antecedência.  
Níveis mais altos têm custos maiores, mas garantem desempenho previsível em workloads críticas.

### Modelos Personalizados
Além de modelos pré-treinados, a AWS permite:  
- Ajuste fino (fine-tuning) de modelos existentes  
- Uso de modelos personalizados próprios  

Essas opções podem gerar custos adicionais, dependendo do tamanho do modelo, dados de treinamento e recursos computacionais necessários.

---

## Conclusão

Ao entender essas considerações de custo, você pode tomar decisões informadas e otimizar implantações de IA na AWS, equilibrando **custo, desempenho e requisitos de negócio** de forma eficaz.
