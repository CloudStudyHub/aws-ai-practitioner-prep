# Modelos Transparentes e Explicáveis

Para promover a confiança e a responsabilidade em um sistema de IA, os modelos devem ser **transparentes** e **explicáveis**.

---

## Transparência e Explicabilidade

Sistemas de IA impactam áreas como finanças, saúde e segurança, exigindo **confiança e responsabilidade**.

- **Transparência**: responde à pergunta **COMO** o modelo toma decisões.
- **Explicabilidade**: responde à pergunta **POR QUE** o modelo tomou determinada decisão.

### Transparência
- Facilita auditoria e responsabilidade.
- Ajuda a criar confiança no sistema.

### Explicabilidade
- Explica por que uma decisão foi tomada.
- Auxilia desenvolvedores a depurar modelos.
- Permite que usuários tomem decisões informadas.

---

## Modelos Transparentes vs. Modelos de Caixa Preta

Modelos de caixa preta são complexos e não revelam seu funcionamento interno.  
Modelos transparentes e explicáveis oferecem:

### Maior Confiança
- Usuários compreendem melhor as decisões.
- Importante em aplicações de alto risco.

### Mais Fácil de Depurar e Otimizar
- Permite identificar problemas internos.
- Facilita melhorias específicas.
- Modelos de caixa preta dificultam esse processo.

### Melhor Compreensão dos Dados e Processos
- Fornece visão ampla do comportamento do modelo.
- Crucial em áreas onde explicabilidade é prioritária, como saúde.

---

## Soluções para Modelos Transparentes e Explicáveis

- **Estruturas de explicabilidade**: SHAP, LIME, explicações contrafactuais.
- **Documentação transparente**: arquitetura, fontes de dados, processos de treinamento.
- **Monitoramento e auditoria**: supervisão humana, ferramentas automatizadas.
- **Supervisão humana**: validação das decisões em situações críticas.
- **Explicações contrafactuais**: mostram como a saída mudaria com diferentes entradas.
- **Explicações na interface do usuário**: tornam o modelo compreensível aos usuários finais.

---

## Riscos de Modelos Transparentes e Explicáveis

- Maior complexidade e custos de desenvolvimento.
- Possibilidade de vulnerabilidades exploráveis.
- Expectativas irreais de total transparência.
- Excesso de informações pode comprometer privacidade ou vantagem competitiva.

---

## Ferramentas da AWS para Transparência e Explicabilidade

### Transparência

#### AWS AI Service Cards
> Documentação única sobre serviços de IA da AWS, incluindo casos de uso, limitações, design responsável e práticas recomendadas.

#### Amazon SageMaker Model Cards
> Documenta detalhes essenciais de modelos de ML, incluindo uso pretendido, métricas de treinamento, resultados e considerações adicionais.

### Explicabilidade

#### SageMaker Clarify
- Fornece pontuações detalhadas sobre quais atributos influenciam as previsões.
- Suporta modelos tabulares, de PLN e visão computacional.
- Gera gráficos agregados para compreensão geral do modelo.

#### SageMaker Autopilot
- Usa ferramentas do SageMaker Clarify para explicar decisões.
- Ajuda engenheiros, gerentes e stakeholders a interpretar previsões.
- Permite explicações por instância durante a inferência.
