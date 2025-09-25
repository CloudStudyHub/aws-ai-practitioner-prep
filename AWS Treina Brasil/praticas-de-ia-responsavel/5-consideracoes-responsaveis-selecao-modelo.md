# Considerações Responsáveis para Selecionar um Modelo

Selecionar um modelo é uma das primeiras e mais críticas etapas para o desenvolvimento de um sistema de IA. A seleção de modelos tem implicações estratégicas sobre o desempenho do sistema de IA, experiência do usuário, entrada no mercado, contratação e lucratividade.

> Dica: Você pode usar a avaliação de modelos no Amazon Bedrock ou no SageMaker Clarify para métricas como precisão, robustez, toxicidade ou critérios que exijam julgamento humano.

---

## Defina o Caso de Uso da Aplicação de Forma Restrita

Ao selecionar um modelo, defina seu caso de uso específico. Isso permite ajustar o modelo para otimizar resultados para aquele objetivo.

### Exemplo: IA Tradicional

| Aplicação                  | Ajuste do Modelo                     |
|-----------------------------|------------------------------------|
| Recuperação de galeria      | Favorecer recall ou precisão       |
| Reconhecimento de celebridades | Favorecer precisão               |
| Supervisão virtual          | Favorecer precisão                 |

> Nota: Uma aplicação de recuperação de galeria para encontrar pessoas desaparecidas deve favorecer recall, enquanto reconhecimento de celebridades favorece precisão.

### Exemplo: IA Generativa

| Recurso                     | Catalogar Produto | Persuadir a Comprar |
|-----------------------------|-----------------|------------------|
| Público-alvo                | Demografia ampla | Demografia restrita |
| Possíveis problemas         | Veracidade       | Veracidade, viés, toxicidade |
| Consequências               | Danos à marca, vendas perdidas | Danos à marca, vendas perdidas |
| Ajuste                       | Neutralidade, clareza, integridade | Foco no benefício para o grupo específico |

> Nota: IA para catalogar produtos tem público amplo; IA para persuadir compra deve focar em público restrito.

---

## Seleção de Modelo com Base no Desempenho

O desempenho do modelo depende de:

- Nível de personalização (prompts, retreinamento)
- Tamanho do modelo (quantidade de parâmetros)
- Opções de inferência (API, autogerenciado)
- Contratos de licenciamento
- Janelas de contexto
- Latência

### Avaliação com Conjuntos de Dados de Teste

O desempenho de um modelo depende do **modelo + conjunto de dados de teste**. Por exemplo:

- Conjunto A → bom desempenho  
- Conjunto B → ótimo desempenho  
- Conjunto C → desempenho degradado

> Lembre-se de que conjuntos de dados podem evoluir ao longo do tempo.

---

## Seleção com Base em Sustentabilidade

Sustentabilidade significa desenvolver e implantar IA de forma social, ambiental e economicamente responsável.

---

## Considerações sobre Agência Responsável

A agência responsável refere-se à capacidade da IA de agir de forma ética e socialmente responsável.

- **Alinhamento de valores:** Decisões baseadas em princípios morais, alinhadas aos valores humanos.
- **Habilidades de raciocínio responsável:** Capacidade de refletir sobre dilemas morais e aplicar princípios éticos.
- **Nível adequado de autonomia:** Limites claros e supervisão humana em domínios sensíveis.
- **Transparência e responsabilidade:** Supervisão externa, justificativa de decisões e prestação de contas.

> Capacidade de agir responsável exige inteligência próxima à cognição humana.

---

## Considerações Ambientais

| Desafio                        | Solução                                                      |
|--------------------------------|-------------------------------------------------------------|
| Consumo de energia              | Otimizar eficiência, usar energia renovável, considerar pegada de carbono |
| Utilização de recursos          | Maximizar eficiência, reutilizar hardware, minimizar desperdício eletrônico |
| Avaliação de impacto ambiental  | Avaliar impactos diretos e indiretos, implementar estratégias de mitigação |

---

## Considerações Econômicas

- Benefícios: Automação, aumento da eficiência
- Riscos: Perda de empregos, desigualdade, concentração de poder
- Considerar impactos econômicos e sociais antes da seleção do modelo
