# README_DOMINIO_ESPECIFICO.md

> Guia para criar um ficheiro de domínio próprio da profissão de [NOME],
> se as convenções desse campo forem fortes o suficiente para justificar
> (ex. linguagem jurídica, normas técnicas de engenharia, formato
> académico, relatórios comerciais). Opcional — os domínios genéricos já
> incluídos (`INSTITUTIONAL_WRITING.md`, `FACT_CHECK_ETHICS.md`) chegam
> para a maioria dos casos.

---

## Quando vale a pena criar um domínio novo

- Há um tipo de documento que a pessoa escreve com frequência e que tem
  regras próprias fortes (formato, vocabulário, estrutura obrigatória)
- Essas regras não estão cobertas pelos ficheiros genéricos já existentes

## Como construir, passo a passo

1. **Nomear o ficheiro** por tema: `domains/[TEMA]_WRITING.md` (ex.
   `LEGAL_WRITING.md`, `TECHNICAL_WRITING.md`, `ACADEMIC_STYLE.md`,
   `SALES_WRITING.md`)
2. **Copiar a estrutura** de `INSTITUTIONAL_WRITING.md` como esqueleto:
   estrutura obrigatória do documento típico, padrão de argumentação, o que
   nunca fazer
3. **Preencher com exemplos reais**, não regras abstratas — se possível,
   colar um documento real já escrito pela pessoa e anotar o que o torna
   característico daquele campo
4. **Ligar ao `SKILL.md`** — adicionar uma linha na tabela de routing a
   apontar para o novo ficheiro

## Perguntas para orientar o preenchimento

- Qual é a estrutura obrigatória de um documento típico deste campo
  (secções, ordem, formato de citação)?
- Que vocabulário técnico é esperado e não deve ser "simplificado" pela IA?
- Que erros são especialmente graves neste campo (ex. um erro de formato
  legal, uma norma técnica incorreta)?
- Há um código de conduta ou norma profissional a respeitar? Se sim,
  acrescentar essa checklist a `domains/FACT_CHECK_ETHICS.md` §5

## Exemplo de estrutura mínima para um novo domínio

```md
# [TEMA]_WRITING.md

> Regras para [tipo de documento] em [campo]. Registo [A/B], ver
> `core/VOICE_DNA_TEMPLATE.md`.

## Estrutura obrigatória
1. ...
2. ...

## Vocabulário técnico a preservar
- ...

## O que nunca fazer neste domínio
- ...
```
