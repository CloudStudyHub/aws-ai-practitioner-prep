# Machine Learning (ML)

Machine Learning (ML) é um subconjunto da Inteligência Artificial (IA) que se concentra no desenvolvimento de algoritmos e modelos estatísticos para que os sistemas de computador possam **aprender com os dados** e fazer previsões ou decisões **sem serem programados de maneira explícita**.  

Os modelos de ML aprendem padrões e relacionamentos com base nos dados em vez de depender de regras codificadas. Eles são treinados em grandes conjuntos de dados, e a **acurácia e o desempenho melhoram com o tempo** à medida que mais dados são processados.

Nesta seção, você aprenderá sobre **quando o ML é uma solução adequada** e as técnicas utilizadas para casos de uso específicos.

---

## Quando a IA e o ML são soluções adequadas

Para determinar a solução adequada de IA, é preciso entender quando usar a IA para resolver um problema de negócios. A IA é uma boa opção para os seguintes casos:

### Codificação de regras complexas

Muitas tarefas humanas não podem ser resolvidas de maneira eficaz com soluções simples baseadas em regras. Por exemplo, a **filtragem de spam**:

- Determinar se um e-mail é legítimo ou spam é complexo, pois envolve muitas variáveis e sobreposições.  
- O ML pode ser usado para resolver esse tipo de problema de forma eficiente.

### Escalabilidade

Escalar certas tarefas humanas para grandes volumes de dados é desafiador:

- Um humano pode revisar algumas centenas de e-mails, mas milhões de e-mails exigem soluções automáticas.  
- Soluções de ML são adequadas para problemas em grande escala, mantendo eficiência e precisão.

---

## Abordagem alternativa para IA e ML

Nem sempre é necessário usar ML. Avalie todas as abordagens e selecione a mais adequada com base nos **requisitos e limitações** da tarefa:

- Se um valor-alvo pode ser determinado por regras simples, cálculos ou etapas predeterminadas, o ML não é necessário.  
- O ML é mais indicado quando não é viável codificar manualmente todas as regras ou padrões.

---

## Técnicas e casos de uso de Machine Learning

Escolher uma solução de ML envolve **entender as técnicas apropriadas** para casos de uso específicos. As principais técnicas são:

1. **Aprendizado Supervisionado**  
2. **Aprendizado Não Supervisionado**  
3. **Aprendizado por Reforço**

### Aprendizado Supervisionado

- Algoritmos são treinados em **dados rotulados**.  
- Objetivo: aprender uma função de mapeamento para prever saídas para novos dados.  

#### Tipos de aprendizado supervisionado

**1. Classificação**  
- Atribui rótulos ou categorias a novas instâncias de dados com base em um modelo treinado.  
- Exemplos de casos de uso:
  - Detecção de fraudes  
  - Classificação de imagens  
  - Retenção de clientes  
  - Diagnóstico médico  

**2. Regressão**  
- Prediz valores contínuos ou numéricos com base em variáveis de entrada.  
- Exemplos de casos de uso:
  - Previsão de popularidade de anúncios  
  - Previsão do tempo  
  - Estimativa da expectativa de vida  
  - Previsão do crescimento populacional  

---

### Aprendizado Não Supervisionado

- Algoritmos aprendem com **dados não rotulados**.  
- Objetivo: descobrir padrões, estruturas ou relacionamentos ocultos.  
- O modelo cria seus próprios rótulos e detecta propriedades emergentes nos dados.

#### Tipos de aprendizado não supervisionado

**1. Agrupamento em clusters (Clustering)**  
- Agrupa dados em clusters com base em semelhanças.  
- Casos de uso:
  - Segmentação de clientes  
  - Marketing direcionado  
  - Sistemas recomendados  

**2. Redução de dimensionalidade**  
- Reduz o número de atributos mantendo as informações mais importantes.  
- Casos de uso:
  - Visualização de Big Data  
  - Compactação significativa  
  - Descoberta de estruturas  
  - Elicitação de atributos  

---

### Aprendizado por Reforço

- O agente aprende com **tentativa e erro**, usando **recompensas e penalidades** para melhorar decisões ao longo do tempo.  
- Útil quando o resultado desejado é conhecido, mas o caminho para alcançá-lo não é.  

**Exemplo: AWS DeepRacer**
- Agente: carro virtual  
- Ambiente: pista de corrida virtual  
- Ações: aceleração e direção  
- Objetivo: completar a pista rapidamente sem sair dela  
- O agente aprende o comportamento desejado através de recompensas.

---

## Resumo das técnicas de Machine Learning

| Técnica | Subcategoria | Objetivo | Casos de Uso |
|---------|-------------|----------|--------------|
| Supervisionado | Classificação | Atribuir rótulos a novos dados | Detecção de fraudes, Diagnóstico, Classificação de imagens |
| Supervisionado | Regressão | Prever valores contínuos | Previsão do tempo, Previsão de mercado, Expectativa de vida |
| Não Supervisionado | Agrupamento em clusters | Descobrir grupos naturais | Segmentação de clientes, Marketing direcionado |
| Não Supervisionado | Redução de dimensionalidade | Reduzir atributos mantendo padrões | Visualização, Compactação de dados |
| Reforço | - | Aprender por tentativa e erro | Simuladores, Robótica, Jogos |

---

## Diagrama ilustrativo 

```text
Machine Learning
├── Supervisionado
│   ├── Classificação
│   └── Regressão
├── Não Supervisionado
│   ├── Agrupamento em clusters
│   └── Redução de dimensionalidade
└── Aprendizado por Reforço
