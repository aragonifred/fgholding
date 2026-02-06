# Contrato de Dados — FG Holdings

Este documento define o CONTRATO OBRIGATÓRIO para entrada, uso e circulação de dados
em qualquer sistema, produto, integração ou processo da FG Holdings.

Nenhum dado existe sem contrato.
Nenhuma decisão acontece sem dado válido.
Nenhuma exceção é permitida.

---

## 1. Princípio Fundamental

Todo dado que entra na FG Holdings deve:
- ter origem clara
- ser rastreável no tempo
- ter responsável identificado
- estar vinculado a uma entidade válida
- servir a uma decisão ou métrica real

Se não cumprir todos os critérios abaixo, o dado é BLOQUEADO.

---

## 2. Metadados Obrigatórios (SEM EXCEÇÃO)

Todo registro deve conter:

| Campo | Descrição |
|-----|----------|
| `source` | Origem do dado (humano, integração, sistema, arquivo) |
| `source_detail` | Detalhe da origem (ex: Google, Stripe, Banco, CSV) |
| `timestamp_utc` | Data e hora em UTC |
| `responsible_actor` | Pessoa ou integração responsável |
| `classification` | financeiro, usuário, operação, marketing, impacto, governança |
| `brand_scope` | holding ou marca relacionada |
| `entity_destination` | Entidade onde o dado será salvo |
| `confidence_score` | Grau de confiança (0–1) quando detectado automaticamente |
| `raw_reference` | Link ou ID do dado bruto, quando existir |

Se QUALQUER campo estiver ausente → o sistema deve exigir correção antes de salvar.

---

## 3. Classificação Obrigatória

Todo dado deve ser classificado em pelo menos uma categoria:

- **financeiro**
- **usuário**
- **operação**
- **marketing**
- **impacto**
- **governança**

Classificações incorretas devem ser corrigidas manualmente.
O sistema deve aprender com as correções.

---

## 4. Entidades Válidas

Nenhum dado pode existir solto.

Todo dado deve estar ligado a uma entidade reconhecida, como:
- transação
- projeto
- marca
- usuário
- parceiro
- decisão
- ativo

Se a entidade não existir:
- o sistema deve sugerir criação
- ou bloquear a importação

---

## 5. Data Map (Rastreabilidade)

Para cada tipo de dado, o sistema deve saber:
- de onde ele vem
- onde é armazenado
- onde é usado
- que decisões ele alimenta
- quem é o dono do dado

Este mapa é patrimônio da FG Holdings.

---

## 6. Aprendizado Assistido

Quando um humano:
- corrige classificação
- altera destino
- rejeita um dado

O sistema deve:
- registrar a correção
- usar isso como treinamento
- reduzir perguntas em casos semelhantes

---

## 7. Segurança e Governança

- Dados não podem ser apagados
- Alterações geram histórico
- Decisões relevantes geram registro auditável
- Acesso deve respeitar nível de permissão

---

## 8. Regra Final

Nenhum dado entra “só para ver”.
Nenhum dado entra “depois a gente organiza”.
Nenhum dado entra fora do contrato.

Se não virar sistema, não entra.

Frase-guia:
"Aqui nada se perde, mas só avança o que vira sistema."
