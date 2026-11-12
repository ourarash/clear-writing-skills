# Clear Writing Skills

Two skills for AI assistants: explain ideas with enough context, then edit the prose so it sounds natural and reads easily.

| Skill | Use it for |
| --- | --- |
| [Plain English with Context](skills/plain-english-with-context/SKILL.md) | Explaining findings, technical concepts, plans, and recommendations so the reader understands the answer, its reason, and its practical effect. |
| [Humanize and Tighten](skills/humanize-and-tighten/SKILL.md) | Revising drafts to remove repetition, stiff phrasing, and unnecessary caveats while preserving facts and useful context. |

Use either skill independently. When using both, start with **Plain English with Context** to develop the explanation, then apply **Humanize and Tighten** as an editing pass. Neither requires the other.

Both skills consist of written instructions. They require no scripts, API keys, or external services.

## Examples

To explain a topic:

```text
Use $plain-english-with-context to explain this incident report to a product
manager. Explain what happened, why it matters, and what remains uncertain.

[Paste the report here.]
```

To edit an existing draft:

```text
Use $humanize-and-tighten to revise this draft. Keep the technical details,
numbers, and qualifications that affect how the reader should interpret it.

[Paste the draft here.]
```

To draft and edit in one request:

```text
Use $plain-english-with-context to draft an explanation from these notes.
Then use $humanize-and-tighten to edit it. The audience is an engineering
manager who does not know this system.

[Paste the notes here.]
```

## Install in Codex

Clone or download this repository. From the repository root, copy the folders for the skills you want into your personal skills directory:

```sh
mkdir -p "$HOME/.agents/skills"
cp -R skills/humanize-and-tighten "$HOME/.agents/skills/"
cp -R skills/plain-english-with-context "$HOME/.agents/skills/"
```

Run only the copy command for a skill you want to install. If you already have a copy of that skill, back it up before replacing it. Avoid keeping duplicate copies in different skills directories.

For a project-specific installation, copy the folders into that project's `.agents/skills/` directory instead. Codex detects skill changes automatically; restart it if a skill does not appear. See the [official skill documentation](https://learn.chatgpt.com/docs/build-skills) for discovery locations and configuration.

For another assistant that supports `SKILL.md` skills, follow that assistant's installation instructions and copy each complete skill folder.

## Repository layout

```text
skills/
├── humanize-and-tighten/
│   ├── SKILL.md
│   ├── LICENSE.txt
│   └── agents/openai.yaml
└── plain-english-with-context/
    ├── SKILL.md
    ├── LICENSE.txt
    └── agents/openai.yaml
```

Each `SKILL.md` contains the skill's instructions. The `agents/openai.yaml` files provide display names and example prompts for Codex.

## Attribution

Plain English with Context adapts selected ideas from ASD-STE100. It does not claim compliance with that standard; see the source link and explanation in the skill.

## License

[MIT](LICENSE). Each skill folder includes a copy of the license for independent distribution.
