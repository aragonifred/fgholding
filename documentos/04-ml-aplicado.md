# Machine Learning Aplicado — FG Holdings

ML na FG Holdings NÃO é estética.
ML é uma camada prática para detectar padrões, antecipar riscos e sugerir decisões melhores.

Regras:
- ML nunca executa sozinho
- ML sempre explica o porquê
- ML sempre permite override humano
- ML é incremental: começa simples e cresce por necessidade real

---

## 1. Pré-requisitos (Bloqueio de execução)

ML só pode operar se:
- Contrato de Dados estiver sendo respeitado
- Importações estiverem registradas em histórico
- Decision Ledger estiver ativo (decisão → impacto)

Se qualquer pré-requisito falhar:
→ ML é bloqueado e o sistema deve sugerir correção estrutural.

---

## 2. Tipos de Inteligência Permitidos

O ML na FG deve operar em 4 modos:

1) **Detecção de Anomalias**
- custos fora do padrão
- queda abrupta de margem
- picos inesperados de demanda

2) **Tendências e Projeções Simples**
- previsão de caixa
- projeção de burn rate
- projeção de receita/custo (média móvel, sazonalidade simples)

3) **Recomendações Assistidas**
- sugerir pausar ou investir
- sugerir ajustes de pricing
- sugerir foco operacional

4) **Classificação e Roteamento (Importações)**
- aprender destino correto
- reduzir perguntas
- aumentar taxa de acerto

---

## 3. Princípios de Explicabilidade (Anti-caixa-preta)

Toda sugestão do ML deve conter:
- o que foi detectado
- quais sinais foram usados (features)
- qual histórico comparativo foi usado
- qual nível de confiança (0–1)
- qual ação sugerida
- qual risco se ignorar

Exemplo obrigatório de retorno:
“Custo do fornecedor X aumentou 27% vs média 90 dias.
Confiança: 0,78. Sugestão: revisar contrato ou trocar fornecedor.
Risco: margem da marca Y entra em zona amarela em 30–45 dias.”

---

## 4. ML por Domínio (Implementação Gradual)

### 4.1 Financeiro (Prioridade Máxima)
Objetivo:
- alertar antes do problema estourar

Sinais típicos:
- variação de custos por categoria
- margem por marca
- burn rate
- fluxo de caixa

Saídas:
- alertas
- projeções
- sugestões de cortes/reinvestimentos

---

### 4.2 Submarcas (Eficiência e ROI)
Objetivo:
- entender consumo de recurso vs retorno

Sinais típicos:
- tempo investido vs receita
- custo de aquisição vs LTV (se houver)
- custo fixo por marca
- churn / retenção (se aplicável)

Saídas:
- ranking de eficiência
- sugestão: pausar / manter / acelerar
- sugestões de novos ciclos de teste

---

### 4.3 Conexa (Produto Core)
Objetivo:
- otimizar funil e operação real

Sinais típicos:
- conversão por etapa do funil
- tempo de resposta operacional
- drop-off por etapa
- uso de créditos / consultas

Saídas:
- gargalo mais provável
- sugestão de ajuste de fluxo
- sugestão de pricing de créditos (testes controlados)

---

### 4.4 Impacto Social (Score Explicável)
Objetivo:
- criar um Score de Impacto que faça sentido

Sinais típicos:
- investimento em ações de impacto
- engajamento indireto
- percepção de marca (quando houver)
- resultados mensuráveis (quando houver)

Saídas:
- score de impacto por projeto
- comparativos históricos
- sugestão de melhor alocação

---

## 5. Governança do ML (Controle e Segurança)

Regras:
- ML não executa alterações
- ML não altera regras fixas
- ML sugere e pede confirmação

Toda sugestão que virar ação deve:
- gerar Decision Ledger
- registrar antes/depois
- registrar impacto real futuramente (sucesso/neutro/falha)

---

## 6. Mínimo Viável de ML (MVP)

Para começar simples e com valor mensurável:

MVP 1: Financeiro
- alerta de custo anormal
- alerta de burn rate
- projeção simples de caixa

MVP 2: Importações
- classificador de destino
- taxa de acerto registrada

MVP 3: Conexa
- funil real com gargalos
- sugestão de melhoria por etapa

---

## 7. Métricas de Qualidade do ML

O ML precisa ser auditado.

Métricas obrigatórias:
- taxa de acerto (classificações/importações)
- taxa de falso positivo (alertas)
- taxa de adoção (quantas sugestões viram decisão)
- impacto real pós-decisão (resultado)

---

## 8. Regra Final

ML na FG é ferramenta de decisão.
Se não for explicável, não entra.
Se não for auditável, não entra.
Se não gerar valor real, não entra.

Frase-guia:
"Aqui nada se perde, mas só avança o que vira sistema."
