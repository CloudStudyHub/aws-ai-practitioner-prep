# 🔹 Domínio 5 - Segurança, Conformidade e Governança para Soluções de IA

Este domínio aborda as práticas e ferramentas necessárias para proteger sistemas de **Inteligência Artificial (IA)**, garantir a **conformidade com regulamentações** e estabelecer uma **governança de dados e modelos** robusta.

---

## Tarefa 5.1: Métodos para proteger sistemas de IA

Foco nos riscos de segurança específicos para sistemas de IA e nos serviços da AWS para mitigá-los, começando pelos **fundamentos de segurança na nuvem**.

### Modelo de Responsabilidade Compartilhada da AWS (Shared Responsibility Model)

Conceito fundamental que define claramente **as responsabilidades de segurança entre a AWS e o cliente**:

- **Responsabilidade da AWS (Segurança da Nuvem):**  
  A AWS protege a **infraestrutura física**, incluindo hardware, software, rede e instalações que executam os serviços da nuvem.

- **Responsabilidade do Cliente (Segurança na Nuvem):**  
  O cliente gerencia a **segurança dos dados, aplicações, sistemas operacionais e rede**. Isso inclui:  
  - Gerenciamento de permissões e acessos  
  - Criptografia de dados  
  - Conformidade e políticas internas

---

### Gerenciamento de Identidade e Acesso (IAM)

- **AWS IAM (Identity and Access Management):** Serviço central para gerenciar usuários, grupos e permissões na AWS.  
  - **Princípio do menor privilégio:** conceda apenas as permissões estritamente necessárias para cada tarefa.

- **Usuário Raiz (Root User):**  
  - Primeira identidade criada na conta AWS.  
  - Possui **acesso completo**.  
  - Melhor prática: **não usar para tarefas diárias** e proteger com **MFA (Multi-Factor Authentication / Autenticação Multifator)**.

- **Usuários, Grupos e Funções (Roles):**  
  - Criar usuários IAM individuais para cada pessoa  
  - Organizar em grupos por função  
  - Usar **Roles** para acesso temporário a recursos com credenciais que expiram automaticamente

- **AWS IAM Identity Center:**  
  - Serviço recomendado para ambientes com **múltiplas contas AWS**  
  - Permite uso de **provedor de identidade externo**  
  - Centraliza gerenciamento de permissões

---

### Proteção de Dados e Infraestrutura

#### Criptografia
- **Criptografia em Repouso (At Rest):** Protege dados armazenados (ex.: Amazon S3, Amazon RDS).  
- **Criptografia em Trânsito (In Transit):** Protege dados enquanto se movem pela rede.  
- **AWS KMS (Key Management Service):** Serviço gerenciado para criar e controlar chaves de criptografia usadas na proteção de dados.

#### Segurança de Rede
- **Amazon VPC (Virtual Private Cloud):** Configura redes privadas isoladas na AWS, controlando tráfego de entrada e saída.  
- **AWS PrivateLink:** Conexões privadas entre VPCs e serviços AWS, evitando internet pública.  
- **Amazon Macie:** Serviço baseado em **Machine Learning** que identifica, classifica e protege **dados sensíveis**, como **PII (Personally Identifiable Information / Informações de Identificação Pessoal)**, armazenados no Amazon S3.

---

### Vulnerabilidades Específicas de IA e Estratégias de Mitigação

Sistemas de IA possuem vetores de ataque únicos:

- **Envenenamento de Dados (Data Poisoning):**  
  Inserção de dados corrompidos ou maliciosos no conjunto de treinamento para manipular previsões futuras do modelo.

- **Entradas Adversárias (Adversarial Inputs):**  
  Pequenas alterações nos dados de entrada que podem enganar o modelo e gerar previsões incorretas.

- **Inversão de Modelo (Model Inversion):**  
  Um invasor consegue inferir informações sensíveis do conjunto de treinamento ao consultar repetidamente o modelo e analisar suas respostas.

- **Injeção de Prompt (Prompt Injection):**  
  Ataque específico em **IA Generativa**, em que instruções maliciosas são inseridas em um prompt, fazendo o modelo ignorar suas instruções originais.

---

### Governança e Rastreabilidade de Modelos

Monitoramento e rastreabilidade de **dados, código e configurações** são essenciais para auditoria, depuração e reprodutibilidade.

- **Amazon SageMaker Model Monitor:** Monitora modelos em produção, detectando desvios (**drifts**) na qualidade dos dados e previsões, que podem indicar problemas ou vieses.  
- **Amazon SageMaker Model Registry:** Repositório central para catalogar, versionar e controlar o ciclo de vida de modelos treinados (status: pendente, aprovado, rejeitado).  
- **Amazon SageMaker ML Lineage Tracking:** Representação gráfica completa do fluxo de trabalho de ML, da origem dos dados ao modelo implantado.  
- **Amazon SageMaker Feature Store:** Repositório centralizado de **features** (características) usadas em modelos, facilitando descoberta, compartilhamento e reutilização.

---

## Tarefa 5.2: Regulamentos de Governança e Conformidade

### Padrões e Regulamentações

- **ISO (International Organization for Standardization):** Padrões internacionais para gestão de **segurança da informação** (ex.: ISO 27001) e gerenciamento de riscos em sistemas de IA (ISO 42001).  
- **SOC (System and Organization Controls):** Relatórios de auditoria que validam os controles de segurança de uma organização.  
- **EU AI Act:** Regulamentação da União Europeia que classifica aplicações de IA por risco (inaceitável, alto risco, baixo risco) e define requisitos rigorosos para sistemas de alto risco.  
- **NIST AI RMF (AI Risk Management Framework):** Framework do Instituto Nacional de Padrões e Tecnologia dos EUA para desenvolvimento e uso responsável de IA.

---

### Serviços da AWS para Governança e Conformidade

- **AWS Artifact:** Portal para acessar relatórios de conformidade da AWS (ISO, SOC, etc.)  
- **AWS Audit Manager:** Automatiza coleta de evidências para auditorias, mapeando uso da AWS para requisitos de conformidade  
- **AWS Config:** Monitora e avalia continuamente configurações de recursos para garantir conformidade com políticas internas e regulatórias  
- **AWS CloudTrail:** Registra todas as chamadas de API na conta, fornecendo trilha de auditoria completa  
- **Amazon Inspector:** Analisa cargas de trabalho continuamente em busca de vulnerabilidades e desvios das melhores práticas  
- **AWS Trusted Advisor:** Fornece recomendações em tempo real para melhores práticas em custo, desempenho, segurança e tolerância a falhas

---

### Estratégias de Governança de Dados

Gerenciar **disponibilidade, integridade, segurança e usabilidade dos dados**:

- **Ciclos de Vida de Dados:** Políticas para gerenciar dados desde criação até descarte seguro, incluindo residência (geolocalização) e retenção.  
- **Catálogo de Dados:** Repositório centralizado de metadados que ajuda usuários a descobrir e entender os dados disponíveis.  
  - **AWS Glue Data Catalog:** Armazena metadados sobre fontes de dados.  
- **Controle de Acesso Refinado:**  
  - **AWS Lake Formation:** Permite controle detalhado de acesso (linha, coluna e célula) em data lakes no Amazon S3.

---

# 🗂️ Tabelas de Resumo: Domínio 5 – Segurança, Conformidade e Governança

---

## Tabela 1: Modelo de Responsabilidade Compartilhada da AWS

| Responsabilidade da AWS (Segurança **DA** Nuvem) | Responsabilidade do Cliente (Segurança **NA** Nuvem) |
|--------------------------------------------------|------------------------------------------------------|
| Proteger a infraestrutura global que executa os serviços. Isso inclui data centers, hardware e software que sustentam a nuvem. | Configurar de forma segura os serviços utilizados. |
| A segurança física da infraestrutura. | Proteger os dados, incluindo a aplicação de criptografia. |
| Manutenção da rede e da computação dos serviços da AWS. | Gerenciar o acesso de usuários e permissões usando o AWS IAM. |

---

## Tabela 2: Vulnerabilidades Específicas de Sistemas de IA

| Vulnerabilidade | Descrição |
|-----------------|-----------|
| **Envenenamento de Dados (Data Poisoning)** | Um ator malicioso introduz dados corrompidos ou maliciosos no conjunto de treinamento para manipular as previsões futuras do modelo. |
| **Entradas Adversárias (Adversarial Inputs)** | Um invasor faz pequenas e muitas vezes imperceptíveis manipulações nos dados de entrada para enganar o modelo e gerar uma previsão incorreta. |
| **Inversão de Modelo (Model Inversion)** | Um invasor consegue inferir informações sensíveis sobre os dados de treinamento originais ao consultar repetidamente o modelo e analisar suas saídas. |
| **Injeção de Prompt (Prompt Injection)** | Ataque específico de IA Generativa onde um usuário insere instruções maliciosas em um prompt para sequestrar a funcionalidade do modelo. |

---

## Tabela 3: Principais Serviços de Segurança da AWS

| Serviço AWS | Função Principal |
|------------|-----------------|
| **AWS IAM (Identity and Access Management)** | Controla quem pode acessar o quê na sua conta AWS. Seguir o princípio do menor privilégio. |
| **AWS KMS (Key Management Service)** | Permite criar, gerenciar e usar chaves de criptografia para proteger dados em repouso e em trânsito. |
| **Amazon VPC (Virtual Private Cloud)** | Configura redes privadas e isoladas, controlando o tráfego de entrada e saída. |
| **Amazon Macie** | Usa Machine Learning para descobrir, classificar e proteger dados sensíveis, como **PII (Personally Identifiable Information / Informações de Identificação Pessoal)**, armazenados no Amazon S3. |

---

## Tabela 4: Principais Serviços de Conformidade e Auditoria da AWS

| Serviço AWS | Função Principal |
|------------|-----------------|
| **AWS Artifact** | Portal central para acessar relatórios de conformidade da AWS (ISO, SOC, etc.) de auditores terceirizados. |
| **AWS Audit Manager** | Automatiza a coleta de evidências para auditorias, mapeando o uso da AWS aos requisitos de conformidade. |
| **AWS Config** | Monitora e avalia continuamente as configurações dos recursos AWS para garantir conformidade com políticas internas e regulatórias. |
| **AWS CloudTrail** | Registra todas as chamadas de API na conta AWS, fornecendo trilha de auditoria completa de quem fez o quê e quando. |
| **Amazon Inspector** | Analisa cargas de trabalho continuamente em busca de vulnerabilidades de software e desvios das melhores práticas de segurança. |

---

## Tabela 5: Ferramentas de Governança de Modelos no Amazon SageMaker

| Ferramenta SageMaker | Função Principal |
|---------------------|-----------------|
| **Model Monitor** | Monitora continuamente os modelos em produção para detectar desvios (**drifts**) na qualidade dos dados e das previsões. |
| **Model Registry** | Repositório centralizado para catalogar, versionar e gerenciar o ciclo de vida de modelos treinados, controlando status (ex.: pendente, aprovado). |
| **ML Lineage Tracking** | Cria representação gráfica do fluxo de trabalho de ML, desde a origem dos dados até o modelo, permitindo auditoria e reprodutibilidade. |
| **Model Cards** | Documenta informações cruciais sobre o modelo, como dados de treinamento, desempenho, usos e limitações. |
