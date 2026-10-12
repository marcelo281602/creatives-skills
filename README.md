# CREATIVES agent skills

Skills for AI agents on making, growing and running an AI creator account. Each skill is a folder in the
[Agent Skills](https://agentskills.io) format: a `SKILL.md` with plain instructions, plus templates, references and
worked examples. Read a skill before you turn it on.

New skills are added in batches. Each batch is published as a release, with one zip per skill and one zip of everything.

## Skills

| Skill | Category | Level | Status |
|---|---|---|---|
| [Character bible](skills/character-bible/SKILL.md) | Create | Beginner | Ready |

More Create, Grow and Build skills are on the way.

## Install

Every zip holds a single skill folder, so it unzips straight into your agent's skills directory. Replace `<slug>` with
the skill's folder name, e.g. `character-bible`.

**Claude Code** — personal skills live in `~/.claude/skills`, project skills in `.claude/skills`.

```sh
mkdir -p ~/.claude/skills && curl -fsSLo /tmp/<slug>.zip https://github.com/marcelo281602/creatives-skills/releases/latest/download/<slug>.zip && unzip -oq /tmp/<slug>.zip -d ~/.claude/skills
```

**Codex** — user skills live in `~/.agents/skills`, repository skills in `.agents/skills`.

```sh
mkdir -p ~/.agents/skills && curl -fsSLo /tmp/<slug>.zip https://github.com/marcelo281602/creatives-skills/releases/latest/download/<slug>.zip && unzip -oq /tmp/<slug>.zip -d ~/.agents/skills
```

**Cursor** — reads `~/.cursor/skills` and `~/.agents/skills` (or `.cursor/skills` and `.agents/skills` in a project).

```sh
mkdir -p ~/.cursor/skills && curl -fsSLo /tmp/<slug>.zip https://github.com/marcelo281602/creatives-skills/releases/latest/download/<slug>.zip && unzip -oq /tmp/<slug>.zip -d ~/.cursor/skills
```

**Claude apps** — download the zip and keep it zipped. In Claude, open Customize → Skills, press +, then Create skill →
Upload a skill, and choose the zip. Code execution must be on (Settings → Capabilities).

**Any agent** — the open-source [skills CLI](https://github.com/vercel-labs/skills) knows where most agents keep skills:

```sh
npx skills add marcelo281602/creatives-skills --skill <slug>
```

**Everything at once:** download
[creatives-skills-all.zip](https://github.com/marcelo281602/creatives-skills/releases/latest/download/creatives-skills-all.zip),
which unzips into one folder per skill, or clone this repository.

## Safety

Skills are instructions your agent will follow. None of them asks you to paste keys into a chat; keep your keys in your
own environment. Anything that publishes or spends money should wait for your approval.

The example character, Juno, is fictional and exists only to teach. Build your own character with the Character bible
template rather than publishing as Juno.

## License

MIT — see [LICENSE](LICENSE).
