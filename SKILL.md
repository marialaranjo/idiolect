---
name: "idiolect"
description: |
  Perfil de escrita de [NOME] ([PROFISSÃO]). Usar sempre que se produza ou
  reveja texto em nome dele/a: emails, cartas de motivação, candidaturas,
  relatórios/documentos técnicos, ou qualquer pedido de "escrever como
  eu"/"com a minha voz". Não aplicar com rigor a escrita pessoal/lúdica não
  profissional — aí o registo é mais livre.
license: MIT
---

# idiolect — sistema de escrita de [NOME]

> ⚠️ **Este é um template genérico, ainda por preencher.** Foi construído a
> partir da arquitetura de um sistema de escrita pessoal já validado ao
> longo de meses de uso real, mas o conteúdo de voz/identidade abaixo está
> vazio ou com marcadores de exemplo. Ver `PREENCHER_PRIMEIRO.md` antes de
> usar pela primeira vez.

Sistema de escrita para produzir texto que soa genuinamente a [NOME], não a
IA genérica. Usa disclosure progressivo: este ficheiro é o mapa — a maior
parte do conteúdo real vive nas pastas abaixo e só deve ser lido quando a
tarefa o justificar.

## Antes de escrever uma única frase

1. **Identificar o registo** — ler `core/VOICE_DNA_TEMPLATE.md` (Registo A
   formal, B funcional, C nota interna — nunca reproduzir C em texto final)
2. **Identificar o domínio** — qual ficheiro de `domains/` se aplica (ver
   tabela abaixo)
3. **Identificar o contexto** — se o pedido envolve um projeto/tema
   específico já documentado, ler o ficheiro correspondente em `contexts/`
4. **Escrever**, aplicando `core/WRITING_RULES.md` transversalmente
5. **Humanizar** — passar por `core/HUMANIZER.md` antes de considerar o
   texto pronto
6. Se o texto envolve dados sensíveis, factos verificáveis ou risco
   profissional: passar por `domains/FACT_CHECK_ETHICS.md` como última
   verificação, **sempre por último**

```
Pedido → VOICE_DNA + domain + context → rascunho → HUMANIZER → FACT_CHECK_ETHICS → entrega
```

## Mapa da árvore

```
idiolect/
├── PREENCHER_PRIMEIRO.md    guia de arranque — ler antes de tudo
│
├── core/            sempre relevante — ler para qualquer tarefa de escrita
│   ├── VOICE_DNA_TEMPLATE.md    tom, registos, vocabulário — por preencher
│   ├── THINKING_STYLE.md        como interpretar pedidos fragmentados/
│   │                             associativos — tem nota opcional sobre
│   │                             PHDA/outras particularidades cognitivas
│   ├── WRITING_RULES.md         regras operacionais sempre/nunca, pipeline
│   ├── HUMANIZER.md             remover "cheiro a IA" sem perder rigor
│   └── PROFESSIONAL_IDENTITY_TEMPLATE.md  credenciais para assinaturas —
│                                            por preencher
│
├── domains/         ler o que corresponder ao tipo de documento
│   ├── INSTITUTIONAL_WRITING.md   cartas de motivação, candidaturas, CV
│   ├── FACT_CHECK_ETHICS.md       verificação final: factos, ética, dados
│   └── README_DOMINIO_ESPECIFICO.md  guia para criar um domínio próprio
│                                       da profissão (ex. jurídico, técnico,
│                                       académico, comercial)
│
├── contexts/        ler só se o pedido mencionar um projeto/tema específico
│   └── README.md     vazio de propósito — ver guia para adicionar factos
│
├── templates/       estruturas prontas a preencher
│   ├── email-template.md
│   ├── motivation-letter-template.md
│   ├── cv-template.md
│   └── report-template.md
│
└── examples/        calibração e amostras
    ├── before-after/          exemplos de reescrita (vazio no início)
    └── writing-samples/       amostras reais para calibrar a voz — ver README
```

## Tabela de routing rápido

| Pedido típico | Ler |
|---|---|
| "Escreve um email a [alguém]" | `core/VOICE_DNA_TEMPLATE.md` §Registo B + `templates/email-template.md` |
| "Escreve uma carta de motivação para [vaga/formação]" | `domains/INSTITUTIONAL_WRITING.md` + `templates/motivation-letter-template.md` + `core/PROFESSIONAL_IDENTITY_TEMPLATE.md` |
| "Ajuda-me a organizar/atualizar o CV" | `templates/cv-template.md` + `core/PROFESSIONAL_IDENTITY_TEMPLATE.md` |
| "Ajuda com este relatório/documento técnico" | `templates/report-template.md` + `domains/README_DOMINIO_ESPECIFICO.md` (se já existir um domínio próprio criado) |
| "Revê este texto" | `domains/FACT_CHECK_ETHICS.md` (se envolver factos/dados sensíveis) |
| "Tira o cheiro a IA disto" / "humaniza isto" | `core/HUMANIZER.md` |
| Pedido fragmentado, várias ideias na mesma mensagem | `core/THINKING_STYLE.md` antes de responder |

## Regra de fecho

Nunca entregar um texto profissional sem passar pelo teste final de
`core/VOICE_DNA_TEMPLATE.md` §6 e, se aplicável, pela checklist de
`domains/FACT_CHECK_ETHICS.md`. Em caso de dúvida sobre um facto, uma data,
ou uma citação: marcar ⚠️ e perguntar — nunca preencher com suposição
plausível (ver `core/WRITING_RULES.md`).
