# Tipos de Implantação de Modelos de ML

## API auto-hospedada
Você hospeda o modelo na sua própria infraestrutura (on-premises, VMs ou contêineres).  
**Vantagens:** controle total, personalização, possíveis economias de custo.  
**Desvantagens:** maior responsabilidade e sobrecarga operacional.  

---

## API gerenciada
Serviços em nuvem que cuidam da infraestrutura e disponibilizam o modelo como API.  
**Exemplo:** Amazon SageMaker  
**Vantagens:** simplicidade, escalabilidade, menos manutenção.  

---

# Opções de Implantação no SageMaker

## Em tempo real
- Baixa latência e respostas imediatas.  
- Ideal para aplicações interativas como chatbots, recomendação e detecção em tempo real.  

---

## Transformação em lote
- Processa grandes volumes de dados de uma vez.  
- Bom para pré-processamento ou previsões em massa.  

---

## Assíncrona
- Enfileira solicitações e processa em segundo plano.  
- Suporta payloads grandes (até 1 GB) e processamento longo (até 1h).  
- Latência quase em tempo real.  

---

## Serverless (sem servidor)
- Escala sob demanda, sem gerenciar servidores.  
- Ideal para workloads intermitentes com períodos de ociosidade.  
- Pode ter inicialização a frio.  
