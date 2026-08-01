# HUMANIZER.md

> Remove sinais de escrita gerada por IA de texto profissional, **sem
> sacrificar rigor e sem inflacionar resultados**. Especialização da skill
> genérica [`humanizer`](https://github.com/blader/humanizer) (blader, MIT
> — atualmente 33 padrões, baseada no guia "Signs of AI writing" da
> Wikipedia, mantida por WikiProject AI Cleanup) para [NOME]. Usar sempre
> depois de gerar ou rever um relatório, candidatura, ou email, antes de
> entregar como final.
>
> **Manter atualizado:** a skill original é ativamente mantida — o número
> de padrões e o comando de instalação podem mudar. Consultar o
> repositório para o comando de sincronização atual (à data de escrita:
> `npx skills update humanizer --global`) e reaplicar manualmente as
> regras abaixo, que não existem no original.

---

## Regra de ouro: em texto formal, "neutro" é a voz humana

Em relatórios, candidaturas e correspondência formal: **não injetar
opinião, humor ou primeira pessoa emotiva** — isso não é humanizar, é
desalinhar do Registo A (`core/VOICE_DNA_TEMPLATE.md`). A "personalidade"
num texto formal vem de **precisão específica** (datas, factos, nomes
concretos), não de opinião ou informalidade.

## Processo (draft → auditoria → final)

1. Ler o texto e identificar ocorrências dos padrões abaixo
2. Escrever um **rascunho** que mantém todos os factos/números tal como no
   original (nunca inflacionar nem inventar), varia o comprimento de frase
   sem sacrificar o registo
3. Perguntar: **"O que torna isto obviamente escrito por IA?"** — responder
   em bullets curtos
4. Rever para uma **reescrita final** sem travessões (—) nem meia-risca (–)
   a fazer de vírgula/parênteses
5. Se o texto envolve dados sensíveis ou risco profissional, passar por
   `domains/FACT_CHECK_ETHICS.md` antes da entrega

## Padrões a corrigir

**A. Inflação de significância — o erro mais perigoso aqui.** Nunca
transformar "resultados positivos" em "impacto incrível"; "contribuiu para"
em "revolucionou". Cortar linguagem de significância não sustentada por
dado concreto.

**B. Linguagem promocional.** Vigiar: *rico, profundo, notável, de
excelência, compromisso com, pioneiro* (quando não verificável), *de
referência* (sem fonte).

**C. Atribuições vagas.** Nunca "estudos mostram", "é consensual que" sem
citar fonte concreta. Se não houver fonte confirmada, marcar ⚠️ e não
escrever a afirmação.

**D. Vocabulário de IA em português.** Vigiar (em excesso): *essencial,
crucial, fundamental, aprofundar, evidenciar, destacar, robusto, panorama,
tecido* (metafórico), *sublinhar, valioso, vibrante, ecossistema* (fora de
biologia), *jornada* (fora do literal).

**E. Regra de três forçada.** Não agrupar artificialmente em conjuntos de
três para parecer exaustivo — só manter se forem genuinamente as categorias
certas.

**F. Travessões/meia-risca como regra de estilo.** A versão final não deve
conter — nem – a substituir vírgula, ponto ou parênteses.

**G. Voz passiva sem sujeito quando o ator é conhecido.** Preferir "A
equipa implementou..." em vez de "Foi implementado..." exceto quando o
sujeito é genuinamente indiferente ou desconhecido.

**H. Secções formulaicas "Desafios e Perspetivas Futuras".** Não forçar por
convenção — só incluir com conteúdo real e específico.

**I. Negrito, emojis e headers decorativos em documentos formais.** Sem
emojis; negrito só para termos técnicos ou nomes próprios, nunca frases
inteiras.

**J. Hedging.** Algum hedging é correto e necessário quando reflete
incerteza real ("os dados sugerem"). Cortar apenas hedging redundante
empilhado.

**K. Fórmulas de aforismo / aberturas teatrais.** Evitar "X é o Y de Z" ou
"Sinceramente? A resposta é...". Raramente apropriado em texto formal.

**L. Comunicação de chatbot colada como conteúdo.** Verificar que não
sobrou "Espero que isto ajude", "Aqui está uma visão geral", "Queres que
continue?".

## O que NÃO corrigir (falsos positivos)

- Gramática perfeita e registo consistente, se for legitimamente o padrão
  desta pessoa
- Vocabulário erudito/técnico genuíno do campo dela
- Frases longas com subordinação, se for o padrão confirmado do Registo A
- Hedging cientificamente/factualmente justificado

## Teste final

1. Nenhum resultado foi inflacionado além do que os dados/factos sustentam?
2. Toda a terminologia técnica está correta?
3. Nenhuma afirmação tem atribuição vaga sem fonte?
4. O registo de `VOICE_DNA_TEMPLATE.md` foi respeitado?
5. Passa o teste de leitura em voz alta como algo que [NOME] escreveria?

Se a resposta a qualquer um destes for "não", voltar ao passo 2. Para texto
puramente pessoal/lúdico fora do âmbito profissional, os padrões gerais de
"Signs of AI writing" continuam a aplicar-se com menos peso nas regras I e
K — nesses casos, mais personalidade e opinião são bem-vindas.
