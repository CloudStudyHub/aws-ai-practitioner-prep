# Preparação Responsável de Conjuntos de Dados

Um requisito essencial da IA responsável é preparar seus conjuntos de dados de forma responsável. Isso inclui garantir que os dados sejam **balanceados**, **inclusivos** e **diversos**, permitindo que os modelos não exibam vieses indesejados.

> Ferramentas úteis: SageMaker Clarify e SageMaker Data Wrangler para ajudar a balancear conjuntos de dados.

---

## Balanceamento de Conjuntos de Dados

Conjuntos de dados balanceados são essenciais para criar modelos que não discriminem injustamente.

- Devem representar todos os grupos ou tópicos de dados.
- Garantem que cada grupo tenha exemplos suficientes.
- São críticos em áreas como contratação, empréstimos ou justiça criminal.

### Estratégias para balanceamento

1. **Coleta de dados inclusivos e diversos**
   - Reflete perspectivas, experiências e dados demográficos variados.
   - Previne vieses relacionados a idade, gênero, etnia, etc.
   - Exemplo: um modelo treinado apenas com pessoas de meia idade pode falhar em prever dados de jovens e idosos.

2. **Curadoria de dados**
   - Rotular, organizar e pré-processar dados para treinamento eficaz.
   - Garante representatividade e qualidade.

---

## Coleta de Dados Inclusivos e Diversos

- Reflete com precisão diferentes perspectivas.
- Evita vieses sociais e legais.
- Deve ser aplicada a **qualquer tópico**, não apenas dados sobre pessoas (ex.: produtos, clima, geografia).

> Benefícios: promove imparcialidade, transparência e responsabilidade na IA.

---

## Curadoria de Dados

A curadoria envolve preparar os dados para que funcionem corretamente no modelo.

### Etapas da curadoria

1. **Pré-processamento de dados**
   - Limpeza, normalização e seleção de recursos.
   - Elimina vieses e melhora a qualidade do conjunto de dados.

2. **Aumento de dados**
   - Gera novas instâncias para grupos sub-representados.
   - Ajuda a balancear o conjunto de dados.

3. **Auditoria regular**
   - Verifica se o conjunto de dados permanece balanceado.
   - Adota medidas corretivas se vieses forem identificados.

---

## Equilibrar Dados para o Caso de Uso Pretendido

O **caso de uso** define como os dados devem ser balanceados.

- Exemplo: sistema de IA para câncer em crianças deve priorizar dados pediátricos, não adultos.
- Ajuste os conjuntos de dados de acordo com a população ou tópico específico do modelo.

> A preparação responsável garante modelos mais justos, precisos e confiáveis.
