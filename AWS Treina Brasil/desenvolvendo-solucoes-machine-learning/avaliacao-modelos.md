## Avaliação de Modelos

A avaliação de modelos acontece **após o treinamento**, com o objetivo de verificar se o modelo generaliza bem para dados que não foram vistos.

### Conjuntos de Dados de Avaliação
- **Treinamento**: usado para ajustar os parâmetros do modelo.  
- **Validação**: usado para avaliar o desempenho enquanto o modelo ainda está sendo ajustado.  
- **Teste**: usado após o ajuste final para verificar a qualidade preditiva do modelo antes da produção.  

### Ajuste do Modelo
- **Sobreajuste (overfitting)**: quando o modelo tem ótimo desempenho nos dados de treinamento, mas não generaliza bem para dados novos.  
- **Subajuste (underfitting)**: quando o modelo tem baixo desempenho até mesmo nos dados de treinamento, por não capturar relações importantes entre X (entradas) e Y (saídas).  
- **Balanceado**: quando o modelo não sofre de sobreajuste nem de subajuste.  

### Viés e Variância
- **Viés**: diferença entre o valor previsto e o valor real.  
- **Variância**: dispersão das previsões em diferentes conjuntos de dados.  
- Modelo ideal → baixo viés e baixa variância.  

---

## Métricas de Avaliação

A escolha das métricas depende do tipo de problema: **classificação** ou **regressão**.

### 1. Problemas de Classificação
Exemplo: classificar imagens como *“gato”* ou *“não gato”*.  

**Etapas de avaliação:**
1. Enviar observações com valores de destino conhecidos.  
2. Comparar previsões com valores reais.  
3. Calcular métricas que resumem a performance.  

#### Matriz de Confusão
Base da avaliação em classificação. Mostra os quatro cenários:
- **Verdadeiro Positivo (VP)**: previsto “gato”, real “gato”.  
- **Falso Positivo (FP)**: previsto “gato”, real “não gato”.  
- **Falso Negativo (FN)**: previsto “não gato”, real “gato”.  
- **Verdadeiro Negativo (VN)**: previsto “não gato”, real “não gato”.  

#### Principais Métricas
- **Acurácia**: (VP + VN) ÷ total de previsões.  
  - Boa para bases equilibradas.  
- **Precisão (Exatidão)**: VP ÷ (VP + FP).  
  - Indicada quando o custo de falsos positivos é alto.  
- **Recall (Sensibilidade)**: VP ÷ (VP + FN).  
  - Indicada quando é crítico reduzir falsos negativos.  
- **F1-Score**: média harmônica entre precisão e recall.  
  - Boa quando é necessário balancear FP e FN.  
- **AUC-ROC**: mede a separação entre classes em diferentes limiares.  
  - Útil em problemas de classificação binária como detecção de spam.  

---

### 2. Problemas de Regressão
Exemplo: prever preços de imóveis.  

#### Métricas mais usadas:
- **Erro Quadrático Médio (MSE)**:  
  \[
  MSE = \frac{1}{n} \sum (y_{real} - y_{previsto})^2
  \]  
  - Mede a média dos erros ao quadrado. Quanto menor, melhor.  

- **R² (Coeficiente de Determinação)**:  
  - Mede a proporção da variabilidade explicada pelo modelo (varia de 0 a 1).  
  - Próximo de 1 indica bom ajuste.  

---

## Métricas de Negócio

Além das métricas técnicas, é importante avaliar o modelo com base em **KPIs definidos pela empresa**, como:
- Aumento de vendas.  
- Redução de custos.  
- Retenção de clientes.  

**Exemplos:**
- Em manutenção preditiva → falsos positivos aumentam custos.  
- Em saúde → falsos negativos podem ser críticos.  

### Boas práticas:
- Desenvolver **métricas personalizadas** (funções de custo ligadas ao impacto econômico real).  
- Usar **testes A/B** ou **implantações canárias** para comparar diferentes versões de modelos em produção.  
