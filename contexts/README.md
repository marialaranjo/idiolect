# contexts/

Esta pasta está vazia de propósito. Serve para guardar **factos fixos de um
projeto, empresa ou tema específico** que apareça repetidamente nos textos
de [NOME], para não ter de os repetir em cada pedido.

## Quando criar um ficheiro aqui

Quando a pessoa escrever repetidamente sobre o mesmo projeto/entidade e
houver factos que se mantêm estáveis: nomes de instituições, datas,
siglas, histórico de um projeto, dados de equipa.

## Como criar

1. Nomear por tema: `contexts/[NOME_DO_PROJETO].md`
2. Listar apenas factos verificados — nunca suposições
3. Marcar campos incertos com ⚠️ em vez de preencher
4. Referenciar o ficheiro no `SKILL.md`, tabela de routing, se for um tema
   frequente

## Exemplo de estrutura mínima

```md
# NOME_DO_PROJETO.md

> Factos de referência sobre [projeto/entidade]. Consultar sempre antes de
> escrever sobre este tema — nunca reconstruir de memória.

## Factos-chave
- [facto 1]
- [facto 2]

## Histórico/datas relevantes
| Período | Situação |
|---|---|
```
