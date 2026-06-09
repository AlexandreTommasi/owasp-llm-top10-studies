# CLAUDE.md — owasp-llm-top10-studies

## Contexto do projeto

Repositório de estudo prático do OWASP Top 10 for LLM Applications 2025.
O objetivo não é documentar o PDF — é aprender de verdade cada vulnerabilidade
através de anotações próprias, código e laboratórios práticos.

Estou em transição de carreira para AI Security / AI Guardrails.

---

## Meu fluxo de estudo (fora do Claude Code)

Antes de abrir o Claude Code pra qualquer vulnerabilidade, sigo esses passos:

1. Leio a seção do PDF correspondente ao LLM0X
2. Abro o Obsidian e crio uma nota usando o TEMPLATE DE ANOTAÇÃO abaixo
3. Escrevo tudo com minhas próprias palavras — sem copiar do PDF
4. Só depois de terminar a nota, abro o Claude Code e digo "vamos trabalhar o LLM0X"
5. Colo minhas anotações brutas do Obsidian no chat

---

## TEMPLATE DE ANOTAÇÃO (Obsidian — privado, meu caderno)

Esse template é pra EU preencher sozinho antes de abrir o Claude Code.
Pode ter dúvidas, frases incompletas, anotações soltas. É rascunho de aprendizado.

---
tags: [owasp, llm-security, estudo]
fonte: OWASP Top 10 for LLM Applications 2025
---

# LLM0X — Nome da Vulnerabilidade

## O que é
(explica com suas palavras em 2-3 linhas)

## Como acontece
(tipos, variações, o que triggera)

## Impactos possíveis
(o que pode dar errado na prática)

## Como mitigar
(principais estratégias)

## Cenários reais
(exemplos do doc que achei mais relevantes, resumidos)

## Exemplo prático (meu)
(um caso hipotético que eu inventei)

## Conexões
(links pra outras notas do Obsidian)

## Dúvidas / Revisitar
(o que ficou confuso — será resolvido no Claude Code)

---

## TEMPLATE DE OUTPUT (README.md — público, gerado pelo Claude Code)

Esse template é o que o Claude Code gera a partir das minhas anotações.
NÃO é preenchido por mim. É o arquivo que vai pro repo público no GitHub.
O Claude o gera apenas após o fluxo de perguntas e respostas ser concluído.

# LLM0X — Nome da Vulnerabilidade

## O que é
(reescrito com base nas minhas anotações, limpo e direto)

## Como acontece
(organizado, sem dúvidas ou gaps expostos)

## Impactos reais
(consolidado e claro)

## Como mitigar
(com referências ao código em examples/)

## Exemplo prático
(caso concreto, linkado ao vulnerable.py e mitigated.py)

## Conexões com outras vulns
(como essa vuln se relaciona com as outras do Top 10)

---

## Estrutura do repo

owasp-llm-top10-studies/
├── README.md
├── CLAUDE.md
├── docs/
│   └── LLMAll_en-US_FINAL.pdf
├── vulnerabilities/
│   └── LLM0X-nome/
│       ├── README.md
│       ├── examples/
│       │   ├── vulnerable.py
│       │   └── mitigated.py
│       └── labs/
│           └── lab01_*.ipynb
├── labs/
│   └── red-team-playground/
├── notes/
│   └── connections.md
└── resources.md

---

## Como trabalhamos juntos no Claude Code

Quando eu disser "vamos trabalhar o LLM0X", significa que eu já li e anotei
aquela vulnerabilidade no Obsidian. Vou colar minhas anotações brutas.

Seu papel é:

1. Não reescrever minhas anotações — elas são minhas, no meu jeito de falar
2. Me fazer perguntas antes de gerar qualquer arquivo, pra checar se eu
   realmente entendi o conceito
3. Só gerar os arquivos depois que eu responder as perguntas satisfatoriamente
4. Criar exemplos de código nas stacks mais comuns e didáticas para cada
   vulnerabilidade específica. Priorizar clareza sobre familiaridade — se o
   ataque faz mais sentido em FastAPI, Flask, RAG puro ou outro contexto,
   usa esse contexto. Python como linguagem padrão salvo exceções justificadas.

---

## Fluxo por vulnerabilidade no Claude Code

### Passo 1 — Minhas anotações

Eu colo minhas notas brutas do Obsidian sobre o LLM0X.

### Passo 2 — Perguntas de verificação

Você me faz 3 a 5 perguntas sobre a vulnerabilidade, com dificuldade crescente:
- 1-2 perguntas conceituais (o que é, como funciona)
- 1-2 perguntas aplicadas (como isso quebraria um sistema real)
- 1 pergunta de mitigação (como eu resolveria isso no código)

Não avança pro passo 3 até eu responder todas.

### Passo 3 — Feedback das respostas

Você avalia minhas respostas:
- O que eu entendi bem
- O que ficou vago ou incompleto
- O que eu errei (sem papas na língua)

### Passo 4 — Geração dos arquivos

Só depois do passo 3, você gera:

vulnerabilities/LLM0X-nome/README.md
- Usa o TEMPLATE DE OUTPUT definido acima
- Baseado nas MINHAS anotações, não no PDF
- Escrito em pt-BR, tom direto

vulnerabilities/LLM0X-nome/examples/vulnerable.py
- Código comentado mostrando a vulnerabilidade
- Stack escolhida pela clareza didática do caso
- Comentários explicando ONDE e POR QUE está vulnerável

vulnerabilities/LLM0X-nome/examples/mitigated.py
- Mesma situação, corrigida
- Comentários explicando O QUE mudou e POR QUE resolve

vulnerabilities/LLM0X-nome/labs/lab01_*.ipynb
- Notebook interativo pra eu executar e ver o ataque/defesa na prática
- Células de markdown explicando cada etapa
- Deve ser executável localmente com dependências mínimas

### Passo 5 — Conexões

Após cada LLM0X, você atualiza notes/connections.md adicionando como essa
vulnerabilidade se relaciona com as anteriores.

### Passo 6 — Atualizar progresso

Você atualiza a tabela de progresso no final deste CLAUDE.md, marcando o
LLM0X como concluído.

---

## Regras gerais

- Nunca pule o passo 2. Se eu pedir pra gerar direto, recuse e me peça
  as anotações primeiro.
- Seja direto no feedback. Se eu errei um conceito, fala. Não me poupe.
- Código sempre funcional. Nada de pseudocódigo nos arquivos .py
- Perguntas em pt-BR, código e arquivos em inglês (padrão de repo público).
- Se eu travar em alguma pergunta, pode dar uma dica, mas não a resposta.

---

## Progresso

| #     | Vulnerabilidade                 | Status       |
|-------|---------------------------------|--------------|
| LLM01 | Prompt Injection                | [x] concluído |
| LLM02 | Sensitive Info Disclosure       | [ ] pendente |
| LLM03 | Supply Chain                    | [ ] pendente |
| LLM04 | Data and Model Poisoning        | [ ] pendente |
| LLM05 | Improper Output Handling        | [ ] pendente |
| LLM06 | Excessive Agency                | [ ] pendente |
| LLM07 | System Prompt Leakage           | [ ] pendente |
| LLM08 | Vector and Embedding Weaknesses | [ ] pendente |
| LLM09 | Misinformation                  | [ ] pendente |
| LLM10 | Unbounded Consumption           | [ ] pendente |