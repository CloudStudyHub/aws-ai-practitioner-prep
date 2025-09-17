# 🔹 Domínio 3 – Aplicação de Modelos de Base: Questões

### Tarefa 3.1: Design de Aplicações e Critérios de Seleção

1. Qual critério avalia o custo por token, de hospedagem e ajuste fino de um modelo de base?
- [ ] Modalidade
- [ ] Custo e Complexidade
- [ ] Latência
- [ ] Janela de Contexto

2. Um modelo que processa texto e imagem simultaneamente é considerado:
- [ ] Unimodal
- [ ] Multimodal
- [ ] Apenas texto
- [ ] Apenas imagem

3. A velocidade de resposta de um modelo é avaliada pelo critério:
- [ ] Capacidade de Personalização
- [ ] Latência
- [ ] Tamanho da Janela de Contexto
- [ ] Suporte a Idiomas

4. O parâmetro que define a quantidade máxima de tokens processados em uma chamada é:
- [ ] Temperatura
- [ ] Max Tokens
- [ ] Janela de Contexto
- [ ] Modalidade

5. Qual critério verifica se um modelo permite fine-tuning para domínios específicos?
- [ ] Suporte a Idiomas
- [ ] Capacidade de Personalização
- [ ] Custo e Complexidade
- [ ] Latência

6. Qual critério avalia se o modelo suporta os idiomas necessários para a aplicação?
- [ ] Suporte a Idiomas
- [ ] Modalidade
- [ ] Janela de Contexto
- [ ] Temperatura

---

### Parâmetros de Inferência e Geração de Respostas

7. O que a temperatura (temperature) controla em um modelo de IA?
- [ ] Quantidade de tokens processados
- [ ] Aleatoriedade da resposta
- [ ] Velocidade de inferência
- [ ] Tipo de dado processado

8. Uma temperatura baixa (ex: 0.1) gera respostas:
- [ ] Criativas e inesperadas
- [ ] Previsíveis e consistentes
- [ ] Sempre curtas
- [ ] Focadas apenas em texto

9. Qual parâmetro define o comprimento máximo da resposta gerada pelo modelo?
- [ ] Temperature
- [ ] Max Tokens
- [ ] Janela de Contexto
- [ ] Modalidade

---

### Tarefa 3.1: Geração Aumentada de Recuperação (RAG)

10. O principal objetivo da técnica RAG é:
- [ ] Reduzir custo de treinamento
- [ ] Acessar conhecimento externo atualizado
- [ ] Evitar o uso de embeddings
- [ ] Substituir o ajuste fino

11. Qual serviço AWS simplifica a implementação de RAG?
- [ ] Amazon SageMaker
- [ ] Knowledge Bases for Amazon Bedrock
- [ ] Amazon Neptune
- [ ] AWS Lambda

12. Em RAG, qual tipo de banco é usado para armazenar embeddings dos documentos?
- [ ] Banco de dados relacional ou vetorial
- [ ] Banco de dados em cache
- [ ] Banco de dados NoSQL sem vetores
- [ ] Apenas arquivos CSV

13. Qual é o principal benefício de RAG para respostas de IA?
- [ ] Reduz a latência do modelo
- [ ] Evita alucinações usando dados confiáveis
- [ ] Substitui totalmente o modelo pré-treinado
- [ ] Aumenta a temperatura automaticamente

---

### Tarefa 3.1: Agentes (Agents)

14. Um agente é diferente de um LLM porque:
- [ ] Apenas responde perguntas
- [ ] Pode executar ações e orquestrar tarefas externas
- [ ] Não precisa de prompts
- [ ] Funciona sem dados

15. Qual serviço AWS permite criar e gerenciar agentes?
- [ ] Amazon Bedrock
- [ ] Agents for Amazon Bedrock
- [ ] Amazon Q
- [ ] Amazon SageMaker

16. Qual seria um exemplo de ação que um agente pode realizar?
- [ ] Responder perguntas triviais
- [ ] Planejar férias buscando voos e hotéis
- [ ] Apenas resumir texto
- [ ] Treinar outro modelo

---

### Tarefa 3.2: Engenharia de Prompts

17. Qual técnica de prompt pede ao modelo realizar uma tarefa sem fornecer exemplos?
- [ ] Zero-shot Prompting
- [ ] Few-shot Prompting
- [ ] Chain-of-Thought
- [ ] Prompts Negativos

18. Qual técnica inclui exemplos de entrada e saída para guiar o modelo?
- [ ] Zero-shot Prompting
- [ ] Few-shot Prompting
- [ ] Chain-of-Thought
- [ ] Prompts Negativos

19. Chain-of-Thought (CoT) instrui o modelo a:
- [ ] Ignorar os exemplos no prompt
- [ ] Decompor seu raciocínio passo a passo
- [ ] Aumentar a temperatura
- [ ] Reduzir tokens de saída

20. Prompts Negativos são usados para:
- [ ] Aumentar criatividade
- [ ] Indicar o que o modelo deve evitar gerar
- [ ] Ajustar a temperatura
- [ ] Escolher a modalidade do modelo

21. Qual risco envolve um usuário mal-intencionado inserindo instruções no prompt para desviar o comportamento do modelo?
- [ ] Prompt Hijacking
- [ ] Jailbreaking
- [ ] Exposição de Dados
- [ ] Prompt Injection

22. Qual ameaça busca contornar filtros de segurança do modelo para gerar conteúdo proibido?
- [ ] Prompt Hijacking
- [ ] Jailbreaking
- [ ] Exposição de Dados
- [ ] Prompt Injection

23. Qual risco envolve vazar informações sensíveis incluídas no prompt enviado a uma API?
- [ ] Prompt Hijacking
- [ ] Jailbreaking
- [ ] Exposição de Dados
- [ ] Prompt Injection

24. Ataques que manipulam entradas não confiáveis para gerar respostas maliciosas são chamados de:
- [ ] Prompt Hijacking
- [ ] Jailbreaking
- [ ] Exposição de Dados
- [ ] Prompt Injection

---

### Tarefa 3.3: Treinamento e Ajuste Fino

25. Qual fase inicial de treinamento massivo faz o modelo aprender padrões de linguagem e fatos gerais?
- [ ] Fine-Tuning
- [ ] Pré-treinamento
- [ ] In-context Learning
- [ ] RAG

26. Qual técnica adapta um modelo pré-treinado a um conjunto de dados específico de uma tarefa?
- [ ] Fine-Tuning
- [ ] Pré-treinamento
- [ ] Zero-shot Prompting
- [ ] Few-shot Prompting

27. O que é Catastrophic Forgetting (Esquecimento Catastrófico)?
- [ ] Perda de dados no banco
- [ ] Ajuste fino que degrada desempenho em tarefas antigas
- [ ] Erro de inferência do modelo
- [ ] Problema de embeddings

28. PEFT (Parameter-Efficient Fine-Tuning) tem como objetivo:
- [ ] Treinar todos os pesos do modelo
- [ ] Treinar apenas pequenos parâmetros para reduzir custo e memória
- [ ] Substituir embeddings
- [ ] Aumentar a temperatura

29. LORA é uma técnica de:
- [ ] Engenharia de prompts
- [ ] PEFT (Ajuste Fino Eficiente de Parâmetros)
- [ ] RAG
- [ ] Agentes

30. RLHF (Reinforcement Learning from Human Feedback) é usado para:
- [ ] Ajustar modelo de acordo com preferências humanas
- [ ] Substituir o pré-treinamento
- [ ] Treinar embeddings
- [ ] Medir latência
