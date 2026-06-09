# Connections between vulnerabilities

Mapa de como as vulnerabilidades do OWASP LLM Top 10 se relacionam entre si.
Atualizado a cada vulnerabilidade estudada.

---

## LLM01 — Prompt Injection

| Relacionada com | Tipo de relação | Descrição |
|----------------|----------------|-----------|
| LLM07 — System Prompt Leakage | **Vetor → Impacto** | Prompt injection é o vetor mais comum pra forçar o modelo a revelar o system prompt. LLM01 frequentemente *causa* LLM07. |
| LLM06 — Excessive Agency | **Amplificador** | Um agente com muitas ferramentas e permissões amplifica exponencialmente o impacto de uma injeção. LLM01 + LLM06 é a combinação mais perigosa do Top 10. |
| LLM08 — Vector and Embedding Weaknesses | **Subtipo** | Injeção indireta via RAG pressupõe que o documento malicioso foi indexado no banco vetorial — caso específico de envenenamento do pipeline de embeddings. |
