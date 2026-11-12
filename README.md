# Clear Writing Skills

Two reusable instruction sets for AI assistants: one helps explain ideas clearly; the other edits drafts into natural, concise prose.

| Skill | Use it for |
| --- | --- |
| [Plain English with Context](skills/plain-english-with-context/SKILL.md) | Explaining findings, concepts, and recommendations with the context readers need to understand them. |
| [Humanize and Tighten](skills/humanize-and-tighten/SKILL.md) | Removing repetition, stiff phrasing, and unnecessary caveats while preserving facts and useful context. |

Use either skill on its own. When using both, draft with **Plain English with Context**, then edit with **Humanize and Tighten**.

## Install in Codex

Clone this repository and copy one or both skill folders into your personal skills directory:

```sh
git clone https://github.com/ourarash/clear-writing-skills.git
cd clear-writing-skills
mkdir -p "$HOME/.agents/skills"
cp -R skills/humanize-and-tighten "$HOME/.agents/skills/"
cp -R skills/plain-english-with-context "$HOME/.agents/skills/"
```

Skip the copy command for any skill you do not want. Back up an existing installation before replacing it. For use in a single project, copy the folders into that project's `.agents/skills/` directory instead.

Restart Codex if the skills do not appear. See the [official skill documentation](https://learn.chatgpt.com/docs/build-skills) for details.

## Use

Ask Codex to use either skill by name, or combine them:

```text
Use $plain-english-with-context to explain these notes to a product manager.
Then use $humanize-and-tighten to edit the draft. Preserve the facts and any
qualifications that affect the reader's understanding.

[Paste your notes here.]
```

For other assistants that support `SKILL.md`, follow their installation instructions and copy each complete skill folder.

## License

[MIT](LICENSE). Each skill folder includes a copy.

Plain English with Context adapts selected ASD-STE100 ideas without claiming compliance; the skill includes the source link.
