# Compensações de Modelos

## Compensações de Interpretabilidade

A **interpretabilidade** é um recurso da transparência do modelo.  
Ela indica o grau em que um ser humano pode entender a causa de uma decisão, diferente da **explicabilidade**, que visa traduzir o comportamento do modelo para termos humanos.

### Interpretabilidade
- Acesso direto ao sistema para interpretar a saída do modelo com base nos pesos e recursos.
- Exemplo: compreender exatamente **como** o modelo gera previsões.

### Explicabilidade
- Explica o comportamento do modelo para humanos.
- Utiliza métodos independentes de modelo (gráficos de dependência parcial, SHAP, modelos substitutos) para relacionar atributos de entrada às saídas.
- Permite explicar a natureza e o comportamento do modelo sem precisar acessar completamente a mecânica interna.

---

### Exemplos

> **Exemplo de Interpretabilidade**  
> Um economista cria um modelo de regressão multivariada para prever a inflação. Ele visualiza os parâmetros estimados para medir a saída esperada com diferentes dados, entendendo exatamente o **porquê** e o **como** do comportamento do modelo.

> **Exemplo de Explicabilidade**  
> Um veículo de mídia usa uma rede neural para categorizar artigos. Não é possível interpretar o modelo em profundidade, mas métodos independentes revelam que artigos de negócios que mencionam organizações esportivas são categorizados como esportes. Isso fornece uma explicação compreensível do modelo sem interpretabilidade total.

---

*Diagrama sugerido*: relação entre **interpretabilidade** e **desempenho**.  
- Alta interpretabilidade: mais transparência, mas desempenho pode ser menor.  
- Alta explicabilidade: permite compreensão geral e bom desempenho.

---

## Compensações de Proteção e Transparência

### Proteção do Modelo
- Capacidade de evitar danos sociais, vieses, violações de privacidade ou segurança.
- Garante uso responsável do modelo em benefício da sociedade.

### Compensações
- **Precisão:** Modelos complexos → mais precisos, menos interpretáveis.  
- **Privacidade:** Técnicas como privacidade diferencial → maior proteção, menor transparência.  
- **Proteção:** Filtragem de saídas → reduz transparência do raciocínio.  
- **Segurança:** Treinamento isolado → limita auditoria externa.

---

## Controlabilidade do Modelo

### Controle do Modelo
- Possibilidade de influenciar previsões alterando dados de treinamento.
- Modelos controláveis: mais transparentes, corrigem vieses e saídas indesejadas.

- Avaliação da controlabilidade: manipulação de dados (adição ou remoção de exemplos) deve gerar mudanças esperadas.
- Modelos lineares → mais controláveis que redes neurais complexas.
- Técnicas para aumentar controlabilidade: aumento de dados e restrições no treinamento.
