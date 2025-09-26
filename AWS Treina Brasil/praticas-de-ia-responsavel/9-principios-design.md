# Princípios do Design Centrado no Ser Humano para uma IA Explicável

O **Design Centrado no Ser Humano (HCD)** é uma abordagem para criar produtos e serviços que sejam intuitivos, fáceis de usar e que atendam às necessidades das pessoas que os utilizarão.  
Quando aplicado à **IA explicável**, o HCD ajuda a garantir que as explicações e interfaces fornecidas sejam claras, compreensíveis e úteis para os usuários, incluindo precisão e justiça.

---

## Princípios-Chave do Design Centrado no Ser Humano para uma IA Explicável

Os princípios-chave do HCD para uma IA explicável incluem:

1. Design para Tomada de Decisão Ampliada  
2. Design para Tomada de Decisão Não Enviesada  
3. Design para Aprendizado Humano e de IA

---

## Design para Tomada de Decisão Ampliada

O objetivo é apoiar os tomadores de decisão em situações de alto risco, maximizando os benefícios do uso da tecnologia e minimizando riscos e erros potenciais, especialmente sob estresse ou ambientes de alta pressão.

### Aspectos-chave

| Aspecto       | Descrição                                                                 |
|---------------|---------------------------------------------------------------------------|
| Clareza       | Apresentar informações de forma compreensível, sem vieses ou mal-entendidos. |
| Simplicidade  | Minimizar a quantidade de informações necessárias, mantendo o essencial.  |
| Usabilidade   | Garantir facilidade de uso e navegação, independentemente do nível técnico. |
| Reflexividade | Incentivar os usuários a refletirem sobre suas decisões.                  |
| Responsabilidade | Atribuir consequências às decisões tomadas usando tecnologia amplificada. |

---

## Design para Tomada de Decisão Não Enviesada

Visa criar processos, sistemas e ferramentas de tomada de decisão **livres de vieses**, promovendo imparcialidade e eficiência.

### Etapas do Design

1. Identificar e avaliar possíveis vieses.  
2. Criar processos e ferramentas transparentes e justos.  
3. Treinar tomadores de decisão para reconhecer e mitigar vieses.

### Aspectos-chave

| Aspecto        | Descrição                                                                 |
|----------------|---------------------------------------------------------------------------|
| Transparência  | Processos claros, acessíveis e auditáveis, facilitando a identificação de vieses. |
| Imparcialidade | Minimizar parcialidade e discriminação, incluindo diversas perspectivas. |
| Treinamento    | Capacitar tomadores de decisão a reconhecer e mitigar vieses.             |

---

## Design para Aprendizado Humano e de IA

Cria ambientes e ferramentas de aprendizado eficazes tanto para humanos quanto para IA, considerando pontos fortes, limitações e metas da experiência de aprendizado.

### Aspectos-chave

- **Aprendizagem Cognitiva:** Humanos e IA aprendem observando, interagindo ou experienciando cenários simulados ou reais.  
- **Personalização:** Experiências e ferramentas adaptadas às necessidades específicas do usuário, utilizando algoritmos de análise de dados e ML.  
- **Design Centrado no Usuário:** Ambientes intuitivos e acessíveis, priorizando experiência e usabilidade.

---

## Aprendizado por Reforço a partir do Feedback Humano (RLHF)

Técnica de ML que utiliza **feedback humano** para otimizar modelos.  
- Incorpora feedback na função de recompensas para alinhar o modelo às metas, necessidades e desejos humanos.  
- Aplicável em IA tradicional e generativa.

### Benefícios do RLHF

- Melhoria no desempenho da IA.  
- Fornecimento de parâmetros de treinamento complexos.  
- Aumento da satisfação do usuário.

---

## Amazon SageMaker Ground Truth

O **SageMaker Ground Truth** fornece recursos para incorporar feedback humano no ciclo de vida do ML:

- Anotação de dados para RLHF.  
- Permite feedback direto e orientação sobre resultados de modelos (ordenar, classificar ou ambos).  
- Dados resultantes (comparação e classificação) são usados para criar uma função de recompensa, que treina ou ajusta o modelo.
