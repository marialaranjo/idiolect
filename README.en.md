# idiolect

🇵🇹 [Ler em português](README.md)

> **idiolect** *(noun, linguistics)*: the speech and writing pattern
> unique to one person — the vocabulary, syntax, and tone only they have.

A skill for Claude (and any agent compatible with the [Agent
Skills](https://agentskills.io) format) that produces text that genuinely
sounds like [NAME] in any professional context: emails, cover letters,
job/programme applications, CVs, and reports or technical documents.

This template was built from the architecture of a system already
validated over months of real use, but with the voice and identity
content left blank — it's ready to fill in, not ready to use as-is.
**Start with `PREENCHER_PRIMEIRO.md`** (the fill-in guide; currently
Portuguese-only — see the note below).

## Structure

```
idiolect/
├── PREENCHER_PRIMEIRO.md  ← fill-in guide, read first (PT only for now)
├── SKILL.md                ← entry point; the first thing the agent reads
├── core/                    identity, tone, rules — always relevant
├── domains/                 rules per document type
├── contexts/                project-specific facts (empty at the start)
├── templates/                ready-to-fill structures
└── examples/                 before/after + folder for real writing samples
```

See `SKILL.md` for the full map and the routing table.

## Why this architecture

It uses **progressive disclosure**: `SKILL.md` is small and works as an
index; the agent only loads the files in `core/`, `domains/`, `contexts/`,
`templates/`, or `examples/` that the specific task requires, instead of
loading everything at once. This keeps the system easy to extend (just
add a new file under `contexts/` for a new project) without bloating the
agent's context on every request.

## How to fill it in

See `PREENCHER_PRIMEIRO.md` for the full guide. Summary:
1. Facts in `core/PROFESSIONAL_IDENTITY_TEMPLATE.md` (5 min)
2. Real writing samples in `examples/writing-samples/`, then ask the
   agent to update `core/VOICE_DNA_TEMPLATE.md` based on them
3. A profession-specific domain file, if it's needed (optional)

No renaming needed — the project name (`idiolect`) stays fixed in the
`SKILL.md` `name:` field and in the folder name; only the internal content
gets personalized.

## A note on language

`PREENCHER_PRIMEIRO.md` and the deeper guide files are currently
Portuguese-only, since that's the language the original system was built
and validated in. The templates in `templates/` and the greeting/closing
examples are also written in Portuguese. If you're writing in another
language, adjust those conventions when filling in
`core/WRITING_RULES.md` and the files under `templates/` — the
architecture itself (progressive disclosure, the evidence methodology,
the pipeline) is language-independent. If there's interest, the
supporting docs can be translated too.

## Privacy, if the repository is public

Once filled in, this system holds personal data — and possibly data about
third parties, if the writing samples mention them. The included
`.gitignore` already protects `contexts/` and `examples/` (except each
folder's `README.md`) — but the safest approach is still to keep your
filled-in version with real data in a **private** repository, separate
from this public template. See `PREENCHER_PRIMEIRO.md` §"Antes de
publicar num repositório público" ("Before publishing to a public
repository").

## Installation

**Claude.ai:** `Settings → Capabilities` (enable "Code execution and file
creation") → `Customize → Skills` → upload this folder's `.zip`.

**Claude Code:** extract to `~/.claude/skills/idiolect/` (personal) or
`.claude/skills/idiolect/` inside a specific project.

## Credits

Architecture adapted, with permission, from a personal writing system
already validated in real use. `core/HUMANIZER.md` is a specialization of
[**blader/humanizer**](https://github.com/blader/humanizer) (MIT) — the
generic "remove signs of AI writing" skill, with 30k+ stars on GitHub.
All credit for the underlying pattern detection goes to the original
project; see that repository for the current count and version.

## License

MIT — see `LICENSE`.
