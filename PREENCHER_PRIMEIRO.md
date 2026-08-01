# Guia de arranque — ler antes da primeira utilização

Este sistema nasceu de um já validado ao longo de muitos meses e dezenas de
conversas reais. Não é possível copiar a "voz" de uma pessoa para outra —
por isso este ficheiro-base vem vazio, com uma arquitetura pronta, à espera
de ser preenchida com factos e amostras reais.

Funciona mesmo sem estar 100% preenchido — a IA usa bom senso e regras
genéricas de escrita profissional nos campos em falta. Mas quanto mais
completo estiver, mais o texto gerado soa à pessoa real e não a texto
genérico.

## Passo 1 — Factos (5 minutos, faz-se uma vez)

Abrir `core/PROFESSIONAL_IDENTITY_TEMPLATE.md` e preencher: nome, formação,
credenciais/cédulas profissionais, instituição(ões), áreas de atuação,
formatos de assinatura. São factos, não estilo — não precisa de reflexão
longa.

## Passo 2 — Registos de voz (feito aos poucos, ao longo do tempo)

Abrir `core/VOICE_DNA_TEMPLATE.md`. Não precisa de estar completo já.
Cada vez que a pessoa usar o sistema para escrever um email, uma carta, um
relatório — e corrigir o que a IA propôs — essa correção é sinal a
incorporar aqui. Ver a metodologia de evidência (🟢🔵) explicada no próprio
ficheiro.

**Atalho mais rápido:** colar 2–3 emails ou textos reais já escritos pela
pessoa (sem edição) em `examples/writing-samples/`, e pedir:
> "Lê os ficheiros em examples/writing-samples/ e atualiza o VOICE_DNA_TEMPLATE com o que encontrares."

## Passo 3 — Domínio da profissão (opcional, quando fizer falta)

`domains/INSTITUTIONAL_WRITING.md` e `domains/FACT_CHECK_ETHICS.md` já
vêm genéricos e prontos a usar. Se a profissão tiver convenções próprias
fortes (ex. linguagem jurídica, normas técnicas, formato académico), ver
`domains/README_DOMINIO_ESPECIFICO.md` para criar um ficheiro de domínio
dedicado.

## Passo 4 — Contexto de projetos (opcional)

Se houver um projeto, empresa ou instituição que apareça repetidamente nos
textos (nomes, datas, factos que não quer ter de repetir sempre), criar um
ficheiro em `contexts/` — ver `contexts/README.md`.

## Nota sobre particularidades cognitivas (opcional)

`core/THINKING_STYLE.md` vem vazio por defeito, tal como o resto do
sistema — não assume nenhum perfil cognitivo específico até ser preenchido
com padrões reais. Se a pessoa tiver PHDA, dislexia, ou outra
particularidade que mude claramente como estrutura e comunica pedidos (ex.
pedidos fragmentados, vários ramos na mesma mensagem), esse ficheiro tem
uma secção opcional já preparada com padrões de partida plausíveis — basta
que se aplique, não precisa de configuração extra para a "ativar". Se não
se aplicar, ignorar essa secção; o resto do ficheiro funciona à parte
dela.

## Depois de preencher

1. Substituir `[NOME]` (nome normal, com maiúsculas e acentos — ex. "João
   Silva") e `[PROFISSÃO]` em todos os ficheiros pelos valores reais.
   Pedir à IA:
   > "Substitui [NOME] por 'X' e [PROFISSÃO] por 'Y' em todos os ficheiros
   > da skill."
2. Não é preciso renomear a pasta nem mexer no `name:` do `SKILL.md` —
   ambos ficam `idiolect`, o nome fixo do projeto, tal como o repositório
   `blader/humanizer` mantém o nome `humanizer` independentemente de quem
   o instala
3. Apagar este ficheiro ou mantê-lo — não interfere com o funcionamento

## Antes de publicar num repositório público

Depois de preencher `core/PROFESSIONAL_IDENTITY_TEMPLATE.md`,
`core/VOICE_DNA_TEMPLATE.md` e `core/THINKING_STYLE.md` com dados reais, e
depois de colocar amostras reais em `examples/` ou factos em `contexts/`:
isto passa a conter informação pessoal (e possivelmente de terceiros, se
os textos de exemplo mencionarem clientes, colegas ou parceiros). Se o
repositório for público no GitHub, **não** fazer commit dessas versões
preenchidas — ver `.gitignore` incluído (já protege `contexts/` e
`examples/`, exceto os `README.md` de cada pasta) e considerar manter o
fork com os dados reais num repositório privado, separado do template
público.
