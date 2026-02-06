# Decision Ledger — FG Holdings

O Decision Ledger é o sistema de memória estratégica da FG Holdings.

Aqui não se registram apenas ações.
Aqui se registram decisões, contextos, impactos e aprendizados.

Sem Decision Ledger:
- não há governança real
- não há aprendizado contínuo
- não há inteligência estratégica

---

## 1. Princípio do Registro de Decisão

Toda decisão relevante deve:
- ser registrada
- ter contexto explícito
- ter responsável identificado
- ter impacto estimado
- gerar histórico comparável

Decisão não registrada é decisão perdida.

---

## 2. O que É uma Decisão Relevante

Devem gerar registro no Decision Ledger:

- aprovar ou pausar um projeto
- alocar ou cortar orçamento
- lançar ou cancelar produto
- mudar preço, fluxo ou regra
- aceitar ou rejeitar parceria
- exceções à regra padrão
- qualquer decisão com impacto financeiro, operacional ou estratégico

Se gera impacto → é decisão → deve ser registrada.

---

## 3. Estrutura Obrigatória de um Registro

Toda decisão deve conter:

| Campo | Descrição |
|-----|----------|
| `decision_id` | Identificador único |
| `timestamp_utc` | Data e hora |
| `decision_maker` | Pessoa ou instância responsável |
| `context` | Por que a decisão foi tomada |
| `options_considered` | Alternativas avaliadas |
| `chosen_option` | Opção escolhida |
| `affected_entities` | Marcas, projetos, dados afetados |
| `expected_impact` | Financeiro, operacional, estratégico |
| `confidence_level` | Grau de confiança (0–1) |
| `review_date` | Data sugerida para reavaliação |

Campos ausentes tornam o registro inválido.

---

## 4. Linha do Tempo Estratégica

O sistema deve permitir visualizar decisões por:

- marca
- projeto
- pessoa
- período
- tipo de impacto

Isso cria:
- rastreabilidade
- análise histórica
- base real para aprendizado

---

## 5. Relação com Dados e Importações

Decisões podem ser disparadas por:
- dados importados
- alertas financeiros
- padrões operacionais
- análises manuais

O Decision Ledger conecta:
**dado → decisão → impacto**

---

## 6. Aprendizado e Revisão

Decisões devem poder ser:
- revisadas
- comparadas com resultado real
- marcadas como:
  - sucesso
  - neutra
  - falha

Falhas não são erro.
Falhas são dado estratégico.

---

## 7. Auditoria e Governança

- Nenhum registro é apagado
- Alterações geram versão
- Justificativas são opcionais, mas incentivadas
- Acesso é controlado por permissão

Governança não é controle — é clareza.

---

## 8. Regra Final

Não se governa o que não se lembra.
Não se aprende com o que não se registra.
Não se escala o que não se entende.

Se não vira Decision Ledger, não vira sistema.

Frase-guia:
"Aqui nada se perde, mas só avança o que vira sistema."
