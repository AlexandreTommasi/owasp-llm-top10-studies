# OWASP LLM Top 10 — Study & Labs

Repositório de estudo prático do [OWASP Top 10 for LLM Applications 2025](https://genai.owasp.org).

Cada vulnerabilidade tem teoria resumida nas minhas palavras, exemplos de código
comentados e laboratórios práticos pra executar localmente.

> Parte do meu roadmap de transição para AI Security / AI Guardrails.

---

## Por que esse repo existe

Não é um resumo do PDF. É um repositório de aprendizado ativo — cada seção foi
estudada, anotada no Obsidian e depois consolidada aqui com código funcional.

---

## Vulnerabilidades

| #     | Vulnerabilidade                 | Status       |
|-------|---------------------------------|--------------|
| [LLM01](./vulnerabilities/LLM01-prompt-injection/) | Prompt Injection | [ ] pendente |
| [LLM02](./vulnerabilities/LLM02-sensitive-info-disclosure/) | Sensitive Info Disclosure | [ ] pendente |
| [LLM03](./vulnerabilities/LLM03-supply-chain/) | Supply Chain | [ ] pendente |
| [LLM04](./vulnerabilities/LLM04-data-model-poisoning/) | Data and Model Poisoning | [ ] pendente |
| [LLM05](./vulnerabilities/LLM05-improper-output-handling/) | Improper Output Handling | [ ] pendente |
| [LLM06](./vulnerabilities/LLM06-excessive-agency/) | Excessive Agency | [ ] pendente |
| [LLM07](./vulnerabilities/LLM07-system-prompt-leakage/) | System Prompt Leakage | [ ] pendente |
| [LLM08](./vulnerabilities/LLM08-vector-embedding-weaknesses/) | Vector and Embedding Weaknesses | [ ] pendente |
| [LLM09](./vulnerabilities/LLM09-misinformation/) | Misinformation | [ ] pendente |
| [LLM10](./vulnerabilities/LLM10-unbounded-consumption/) | Unbounded Consumption | [ ] pendente |

---

## Estrutura

owasp-llm-top10-studies/
├── vulnerabilities/
│   └── LLM0X-nome/
│       ├── README.md        # Teoria nas minhas palavras
│       ├── examples/
│       │   ├── vulnerable.py    # Código vulnerável comentado
│       │   └── mitigated.py     # Versão corrigida comentada
│       └── labs/
│           └── lab01_*.ipynb    # Laboratório prático executável
├── notes/
│   └── connections.md       # Como as vulns se conectam entre si
└── resources.md             # Links, cursos e referências

---

## Referência

- [OWASP Top 10 for LLM Applications 2025](https://genai.owasp.org)
- PDF original em `docs/LLMAll_en-US_FINAL.pdf`