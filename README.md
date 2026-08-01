# idiolect

🇬🇧 [Read this in English](README.en.md)

> **idiolect** *(substantivo, linguística)*: o padrão de fala e escrita
> único de uma pessoa — vocabulário, sintaxe, tom que só ela tem.

Skill para o Claude (e qualquer agente compatível com o formato [Agent
Skills](https://agentskills.io)) que produz texto a soar genuinamente a
[NOME] em qualquer contexto profissional: emails, cartas de motivação,
candidaturas, CV e relatórios/documentos técnicos.

Este template foi construído a partir da arquitetura de um sistema já
validado ao longo de meses de uso real, mas com o conteúdo de voz e
identidade em branco — está pronto a preencher, não pronto a usar tal como
está. **Começar por `PREENCHER_PRIMEIRO.md`.**

## Estrutura

```
idiolect/
├── PREENCHER_PRIMEIRO.md  ← ler primeiro
├── SKILL.md                ← ponto de entrada; lido primeiro pelo agente
├── core/                    identidade, tom, regras — sempre relevante
├── domains/                 regras por tipo de documento
├── contexts/                factos específicos de projetos (vazio no início)
├── templates/                estruturas prontas a preencher
└── examples/                 antes/depois + pasta para amostras reais
```

Ver `SKILL.md` para o mapa completo e a tabela de routing.

## Porque esta arquitetura

Usa **disclosure progressivo**: o `SKILL.md` é pequeno e funciona como
índice; o agente só carrega os ficheiros de `core/`, `domains/`,
`contexts/`, `templates/` ou `examples/` que a tarefa concreta exigir, em
vez de carregar tudo de uma vez. Isto mantém o sistema fácil de expandir
(basta adicionar um novo ficheiro em `contexts/` para um novo projeto) sem
sobrecarregar o contexto do agente em cada pedido.

## Como preencher

Ver `PREENCHER_PRIMEIRO.md` — resumo:
1. Factos em `core/PROFESSIONAL_IDENTITY_TEMPLATE.md` (5 min)
2. Amostras reais de escrita em `examples/writing-samples/`, e pedir para
   atualizar `core/VOICE_DNA_TEMPLATE.md` com base nelas
3. Domínio próprio da profissão, se fizer falta (opcional)

Não é preciso renomear nada — o nome do projeto (`idiolect`) fica fixo no
`name:` do `SKILL.md` e no nome da pasta; só o conteúdo interno é
personalizado.

## Privacidade, se o repositório for público

Depois de preenchido, este sistema passa a conter dados pessoais (e
possivelmente de terceiros, se as amostras de escrita os mencionarem). O
`.gitignore` incluído já protege `contexts/` e `examples/` (exceto os
`README.md` de cada pasta) — mas o mais seguro continua a ser manter a
versão preenchida com dados reais num repositório **privado**, separado
deste template público. Ver `PREENCHER_PRIMEIRO.md` §"Antes de publicar
num repositório público".

## Nota sobre a língua

Os templates em `templates/` e os exemplos de saudação/fecho estão em
português. A escrever noutra língua, ajustar essas convenções ao preencher
`core/WRITING_RULES.md` e os ficheiros de `templates/` — a arquitetura em
si (disclosure progressivo, metodologia de evidência, pipeline) é
independente da língua.

## Como instalar

**Claude.ai:** `Definições → Capacidades` (ativar "Execução de código e
criação de ficheiros") → `Personalizar → Skills` → carregar o `.zip` desta
pasta.

**Claude Code:** extrair para `~/.claude/skills/idiolect/` (pessoal) ou
`.claude/skills/idiolect/` dentro de um projeto específico.

## Créditos

Arquitetura adaptada, com permissão, a partir de um sistema de escrita
pessoal já validado. `core/HUMANIZER.md` é uma especialização de
[**blader/humanizer**](https://github.com/blader/humanizer) (MIT) — a
skill genérica "remove sinais de escrita de IA", com 30k+ estrelas no
GitHub. Todo o crédito da deteção dos padrões-base é do projeto original;
ver o repositório para o número e a versão atuais.

## Licença

MIT — ver `LICENSE`.
