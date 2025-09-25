# Inteligência Artificial Generativa

## O que é IA Generativa
A IA generativa é um subconjunto do aprendizado profundo. Pode adaptar os modelos criados usando o aprendizado profundo sem precisar treiná-los de novo ou ajustá-los. Ela consegue gerar novos dados com base nos padrões e estruturas aprendidos com os dados de treinamento.  
A IA generativa pode criar conteúdos, como conversas, histórias, imagens, vídeos, músicas e códigos.  

Referências gerais:  
- [O que é Inteligência Artificial](https://aws.amazon.com/what-is/artificial-intelligence/)  
- [O que é IA Generativa](https://aws.amazon.com/what-is/generative-ai/)  
- [O que é Machine Learning](https://aws.amazon.com/what-is/machine-learning/)  
- [Soluções da AWS](https://aws.amazon.com/pt/solutions/)  
- [Soluções de IA da AWS](https://aws.amazon.com/pt/solutions/ai/)  
- [Foundation Models](https://aws.amazon.com/what-is/foundation-models/)  

---

## Capacidades da IA Generativa
Se você está pensando em implementar a IA na organização, é importante entender seus recursos.  

- **Adaptabilidade**  
  Os modelos de IA generativa conseguem se adaptar a várias tarefas e domínios aprendendo com os dados e gerando conteúdo personalizado para contextos ou requisitos específicos.  

- **Responsividade**  
  Conseguem gerar conteúdo em tempo real, o que resulta em tempos de resposta rápidos e interações dinâmicas, especialmente úteis em chatbots e assistentes virtuais.  

- **Simplicidade**  
  Automatizam processos de criação de conteúdo, como a geração de texto semelhante ao humano, reduzindo tempo e esforço.  

- **Criatividade e exploração**  
  Podem gerar novas ideias, designs ou soluções combinando elementos de maneiras exclusivas, estimulando a inovação.  

- **Eficiência de dados**  
  Aprendem com pequenas quantidades de dados e geram novas amostras consistentes, úteis em cenários de dados escassos.  

- **Personalização**  
  Criam conteúdo adaptado a preferências individuais, aumentando engajamento e experiência do usuário.  

- **Escalabilidade**  
  Uma vez treinados, podem gerar grandes volumes de conteúdo rapidamente.  

---

## Desafios da IA Generativa

- **Violações regulatórias**  
  - *Risco*: exposição de dados pessoais sensíveis (PII).  
  - *Mitigação*: anonimização de dados, auditorias e conformidade regulatória.  

- **Riscos sociais**  
  - *Risco*: conteúdos indesejados que prejudiquem a reputação da organização.  
  - *Mitigação*: testes e avaliações antes da implantação.  

- **Preocupações com segurança e privacidade de dados**  
  - *Risco*: compartilhamento de informações pessoais.  
  - *Mitigação*: uso de criptografia, firewalls e práticas de segurança cibernética.  

- **Toxicidade**  
  - *Risco*: geração de conteúdo ofensivo ou impróprio.  
  - *Mitigação*: curadoria de dados de treinamento e uso de modelos de proteção.  

- **Alucinações**  
  - *Risco*: respostas imprecisas ou não baseadas em fatos.  
  - *Mitigação*: validação por fontes independentes e alertas de verificação.  

- **Interpretabilidade**  
  - *Risco*: más interpretações da saída do modelo.  
  - *Mitigação*: uso de conhecimento de domínio específico no desenvolvimento.  

- **Não determinismo**  
  - *Risco*: diferentes respostas para a mesma entrada.  
  - *Mitigação*: testes de consistência repetidos.  

---

## Fatores para Seleção de Modelos de IA Generativa

- Definição da tarefa (texto, imagem, código, multimodalidade).  
- Tipos de modelos disponíveis.  
- Requisitos de desempenho (acurácia, confiabilidade, tempo de resposta).  
- Restrições (computação, dados, ambiente de implantação).  
- Capacidades específicas exigidas.  
- Conformidade (justiça, transparência, rastreabilidade, regulamentos).  
- Custo de implantação, manutenção e recursos.  

---

## Modelos e Casos de Uso

### Laboratórios A121 — [Jurassic-2]
- **Tarefas**: geração de texto, resumo, parafrasear, bate-papo, extração de informações.  
- **Casos de uso**:  
  - Serviços financeiros — resumir documentos extensos.  
  - Varejo — gerar descrições de produtos.  

### Amazon — [Amazon Titan]
- **Tarefas**: resumo, classificação, perguntas e respostas, extração de informações, pesquisa.  
- **Casos de uso**:  
  - Publicidade — criar imagens com qualidade profissional.  
  - Atendimento ao cliente — gerar resumos em tempo real.  

### Anthropic — Claude
- **Tarefas**: geração de conteúdo, tradução, resposta a perguntas, resumo, explicação e geração de código.  
- **Casos de uso**:  
  - Desenvolvimento — geração e depuração de código.  
  - Jurídico — análise de documentos legais.  

### Stability AI — [Stable Diffusion]
- **Tarefas**: gerar imagens fotorrealistas, melhorar qualidade de imagens.  
- **Casos de uso**:  
  - Jogos e metaverso — criação de personagens e cenários.  
  - Marketing — campanhas e ativos de publicidade.  

### Cohere — Command
- **Tarefas**: geração de texto, extração de informações, perguntas e respostas, resumo.  
- **Casos de uso**:  
  - Atendimento ao cliente — chatbots.  
  - Saúde — resumos de textos técnicos.  

### Meta — Llama
- **Tarefas**: perguntas e respostas, bate-papo, resumo, análise de sentimentos.  
- **Casos de uso**:  
  - Atendimento ao cliente — chatbots de suporte.  

---

## Requisitos de Desempenho
Avaliar acurácia, confiabilidade e consistência em diferentes datasets. Monitorar desempenho ao longo do tempo.  

---

## Restrições
- Recursos computacionais disponíveis (CPU, GPU, memória).  
- Tamanho e qualidade dos dados.  
- Local de implantação (on-premises ou nuvem).  

---

## Capacidades
Avaliar se o modelo atende às demandas específicas (texto, imagem, multimodal).  

---

## Conformidade
Garantir alinhamento com regulamentos de privacidade, ética, justiça e transparência.  

---

## Custo
Considerar custos de treinamento, implantação, manutenção e escalabilidade.  

---

## Métricas de Negócio para IA Generativa

- **Satisfação do usuário**  
  Ex.: medir feedback em sites de e-commerce.  

- **Receita média por usuário (ARPU)**  
  Ex.: análise de monetização por base de clientes.  

- **Desempenho entre domínios**  
  Ex.: monitorar plataformas multissetoriais de e-commerce.  

- **Taxa de conversão**  
  Ex.: avaliar visitantes que se tornam clientes pagantes.  

- **Eficiência**  
  Ex.: otimizar linhas de produção ou fluxos de trabalho automatizados.  

---
# Cheat Sheet – IA Generativa

## O que é
- Subconjunto do aprendizado profundo.  
- Gera novos dados a partir de padrões aprendidos.  
- Produz: texto, imagens, vídeos, músicas, código.  

---

## Capacidades
- **Adaptabilidade**: se ajusta a diferentes tarefas e domínios.  
- **Responsividade**: gera conteúdo em tempo real.  
- **Simplicidade**: automatiza tarefas complexas.  
- **Criatividade**: gera novas ideias e soluções.  
- **Eficiência de dados**: aprende com poucos exemplos.  
- **Personalização**: conteúdo adaptado ao usuário.  
- **Escalabilidade**: produz grandes volumes rapidamente.  

---

## Desafios + Mitigação
- **Violações regulatórias** → anonimização e auditorias.  
- **Riscos sociais** → testes antes da produção.  
- **Privacidade de dados** → criptografia e segurança cibernética.  
- **Toxicidade** → curadoria + filtros de proteção.  
- **Alucinações** → validação por fontes externas.  
- **Interpretabilidade** → conhecimento de domínio aplicado.  
- **Não determinismo** → testes repetidos para consistência.  

---

## Seleção de Modelos
- **Defina a tarefa**: texto, imagem, multimodal.  
- **Avalie**: desempenho, restrições, capacidades, conformidade, custo.  

---

## Exemplos de Modelos
- **Jurassic-2 (AI21)** → geração de texto, resumos.  
- **Amazon Titan** → resumo, classificação, pesquisa.  
- **Claude (Anthropic)** → conteúdo, tradução, código.  
- **Stable Diffusion (Stability AI)** → imagens realistas.  
- **Cohere Command** → texto, perguntas e respostas.  
- **Llama (Meta)** → chatbots, análise de sentimentos.  

---

## Métricas de Negócio
- **Satisfação do usuário** → feedback e engajamento.  
- **ARPU** → receita média por usuário.  
- **Desempenho entre domínios** → adaptação em vários setores.  
- **Taxa de conversão** → visitantes virando clientes.  
- **Eficiência** → redução de custos e aumento de produtividade.  
