# Operações de Machine Learning

O **MLOps** combina pessoas, tecnologia e processos para oferecer soluções colaborativas de machine learning (ML). Ele operacionaliza e simplifica o ciclo de vida de ML de ponta a ponta, desde o desenvolvimento e implantação do modelo até o monitoramento e manutenção.

É uma extensão dos princípios e práticas de DevOps aplicada a sistemas de ML, promovendo colaboração entre cientistas de dados, engenheiros de dados, desenvolvedores de software e operações de TI.

## Objetivos do MLOps

- Colocar cargas de trabalho de ML em produção e mantê-las operacionais.
- Aumentar o ritmo do ciclo de vida do modelo por meio da automação.
- Melhorar métricas de qualidade com testes e monitoramento.
- Promover colaboração entre equipes multidisciplinares.
- Garantir transparência, auditabilidade, explicabilidade e segurança dos modelos.

## Benefícios do MLOps

1. **Produtividade:** acesso rápido a dados confiáveis, reduzindo tempo perdido com dados ausentes ou inválidos.
2. **Auditabilidade:** rastreabilidade de experimentos, dados de origem e modelos treinados.
3. **Confiabilidade:** CI/CD garante implantações rápidas, consistentes e de alta qualidade.
4. **Qualidade de dados e modelos:** políticas para reduzir viés e monitoramento contínuo.
5. **Repetibilidade:** automação garante processos consistentes de treinamento, avaliação, versionamento e implantação.

## Princípios-chave do MLOps

- **Controle de versão:** rastreia alterações em dados, código e modelos, garantindo reprodutibilidade.
- **Automação:** automatiza ingestão de dados, pré-processamento, treinamento, validação e implantação.
- **CI/CD:**
  - **Integração contínua:** validação e teste de código, dados e modelos.
  - **Entrega contínua:** implantação automática de modelos treinados.
  - **Treinamento contínuo:** retreinamento automático dos modelos.
  - **Monitoramento contínuo:** monitora métricas relacionadas ao negócio e performance do modelo.
- **Governança de modelo:** garante documentação, comunicação, proteção de dados, compliance e revisão de modelos para verificar imparcialidade e ética.

## Ciclo de vida de ML e MLOps

O ciclo de vida de ML envolve o gerenciamento de código, dados e modelos:

- Processamento do código na preparação de dados
- Dados e código de treinamento na criação de modelos
- Modelos candidatos e dados de validação na avaliação de modelos
- Metadados na seleção do modelo
- Modelos prontos e código de inferência na implantação
- Código de produção, modelos e dados no monitoramento

O **MLOps** operacionaliza esses processos, garantindo eficiência, rastreabilidade, repetibilidade e qualidade em todas as etapas do ciclo de vida de ML.

# Implementando MLOps

O MLOps automatiza o ciclo de vida de Machine Learning de ponta a ponta. Um ciclo de vida produtivo de ML geralmente contém **pipelines de treinamento** e **pipelines de implantação** separados.

---

## Criação do modelo

O pipeline de construção de modelos cria novos modelos automaticamente, por exemplo, quando novos dados são disponibilizados.

---

## Avaliação do modelo

Após a criação do modelo, você aplica **medidas de controle de qualidade**, que podem ser:

- **Human-in-the-loop (manual)**: avaliação feita por pessoas.
- **Automatizada**: avaliação realizada por scripts ou algoritmos.

Se o modelo atender às métricas de desempenho estabelecidas, ele pode ser registrado em um **registro de modelos**.

---

## Aprovação do modelo

O registro de modelos permite **aprovar ou rejeitar versões de modelos**. A aprovação inicia o pipeline de implantação do modelo.

---

## Implantação do modelo

O pipeline de implantação segue um fluxo semelhante ao **CI/CD tradicional**, incluindo etapas como:

1. Origem
2. Criação
3. Implantação no ambiente de preparação
4. Testes
5. Promoção no ambiente de produção

---

## Modelo em produção

Após a implantação, é necessário **monitorar o modelo em produção**, incluindo:

- Infraestrutura de hospedagem
- Qualidade dos dados
- Desempenho do modelo

---

# Serviços da AWS para MLOps

A AWS fornece diversos serviços para implementar um pipeline completo de MLOps. A seguir, estão as principais etapas e os serviços correspondentes:

---

## Preparar dados

- **SageMaker Data Wrangler**: ferramenta LCNC (baixo código / sem código) que permite importar, preparar, transformar, destacar e analisar dados por meio de uma interface web.
- **API de processamento do SageMaker**: permite executar scripts e cadernos para processar, transformar e analisar conjuntos de dados de várias frameworks de ML, como scikit-learn, MXNet ou PyTorch, utilizando ambientes totalmente gerenciados.

---

## Armazenar atributos

- **SageMaker Feature Store**: ajuda cientistas de dados, engenheiros de ML e profissionais clínicos a criar, compartilhar e gerenciar atributos para desenvolvimento de modelos.

---

## Treinar

- **Trabalhos de treinamento do SageMaker**: permitem treinar modelos usando algoritmos integrados ou personalizados.

---

## Experimentos

- **SageMaker Experiments**: possibilita testar várias combinações de dados, algoritmos e parâmetros, observando o impacto das mudanças incrementais na acurácia do modelo.

---

## Trabalho de processamento

- Permite executar tarefas de **pré-processamento e pós-processamento de dados**, engenharia de atributos e avaliação de modelos na infraestrutura totalmente gerenciada do SageMaker.

---

## Pipelines

- **SageMaker Model Building Pipelines**: cria fluxos de trabalho completos para gerenciar e implantar trabalhos do SageMaker.

---

## Registro

- **SageMaker Model Registry**: possibilita catalogar modelos, gerenciar versões, controlar status de aprovação e implantar modelos em produção.

---

## Implantações

- **SageMaker Deployment**: oferece diversas opções de infraestrutura e implantação para fazer previsões (inferência) com modelos de ML.

---

## Modelo de monitoramento

- **SageMaker Model Monitor**: monitora a qualidade dos modelos de ML em produção, garantindo desempenho consistente e detecção de problemas.
