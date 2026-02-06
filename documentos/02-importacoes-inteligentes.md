# Importações Inteligentes — FG Holdings

Este documento define como QUALQUER dado entra na FG Holdings.
Importar dados não é upload técnico — é um ato estratégico.

Nenhum dado entra sem ser compreendido.
Nenhum dado entra sem destino claro.
Nenhum dado entra sem aprendizado.

---

## 1. Princípio da Importação Inteligente

Toda importação deve:
- reduzir ambiguidade
- gerar dado reutilizável
- alimentar decisões futuras
- respeitar o Contrato de Dados da FG

Importar ≠ armazenar  
Importar = classificar + vincular + aprender

---

## 2. Pipeline Obrigatório de 3 Etapas

Toda importação segue EXATAMENTE estas etapas.

---

### ETAPA 1 — DETECÇÃO AUTOMÁTICA

O sistema deve identificar automaticamente:

**Tipo do dado**
- PDF
- CSV
- planilha
- imagem / print
- payload de API
- texto manual

**Origem provável**
- banco
- plataforma de anúncios
- fornecedor
- parceiro
- equipe interna
- sistema externo

**Sugestões automáticas**
- entidade de destino
- classificação
- marca relacionada
- campos obrigatórios

Toda sugestão deve ter:
- explicação
- confidence_score (0–1)

---

### ETAPA 2 — CONFIRMAÇÃO HUMANA

Antes de salvar, o sistema deve perguntar:

> “Detectamos que este dado parece ser **X**  
> e deve ser salvo em **Y**, na marca **Z**.  
> Confirmar?”

O usuário pode:
- confirmar
- ajustar classificação
- alterar entidade
- alterar marca
- cancelar a importação

Nenhum dado é salvo sem confirmação explícita.

---

### ETAPA 3 — APRENDIZADO ASSISTIDO

Após a confirmação:

O sistema deve registrar:
- o que foi sugerido
- o que foi confirmado
- o que foi corrigido

Essas correções alimentam:
- melhoria do classificador
- redução de fricção futura
- histórico de decisões semelhantes

---

## 3. Histórico de Importações

Cada importação gera um registro contendo:
- data e hora
- responsável
- tipo de dado
- origem
- entidade destino
- marca
- resultado (aceito / ajustado / rejeitado)
- confidence_score

Este histórico não pode ser apagado.

---

## 4. Relação com o Contrato de Dados

Se qualquer campo obrigatório do contrato estiver ausente:
- a importação deve ser bloqueada
- o sistema deve solicitar correção

Importação não corrige contrato.
Contrato governa importação.

---

## 5. Integrações

Integrações automáticas (APIs, syncs, webhooks):
- seguem o mesmo pipeline
- são tratadas como “atores”
- possuem responsible_actor próprio

Integração não tem privilégio.
Integração segue regra.

---

## 6. Falhas e Rejeições

Quando um dado é rejeitado:
- o motivo deve ser registrado
- o dado não é descartado
- o histórico permanece acessível

Erro vira aprendizado.

---

## 7. Regra Final

Não existe:
- upload rápido
- importação temporária
- dado “só para olhar”

Se não puder ser classificado, vinculado e aprendido:
→ não entra.

Frase-guia:
"Aqui nada se perde, mas só avança o que vira sistema."
