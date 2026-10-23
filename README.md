# sarmad-writing-style

Sarmad Hanif's writing skills for GitHub Copilot (and other agents that read `SKILL.md`).

| Skill | Use it for |
|---|---|
| [sarmad-writing-style](skills/sarmad-writing-style/SKILL.md) | His voice for papers, reports, and course notes; how to port his Word edits; his slide preferences |
| [house-voice](skills/house-voice/SKILL.md) | Voice, format, and structure of lecture decks and explanatory prose: titles, slide anatomy, deck spine, banned vocabulary |
| [plain-language-technical-writing](skills/plain-language-technical-writing/SKILL.md) | Content discipline: define with units, show the numbers, separate observation from interpretation, state assumptions |

## Install on a new machine

Copilot reads user-scope skills from `~/.copilot/skills/<name>/SKILL.md`.

PowerShell:

```powershell
git clone https://github.com/hanifsarmad1/sarmad-writing-style.git "$env:USERPROFILE\code\sarmad-writing-style"
Copy-Item "$env:USERPROFILE\code\sarmad-writing-style\skills\*" "$env:USERPROFILE\.copilot\skills\" -Recurse -Force
```

bash:

```bash
git clone https://github.com/hanifsarmad1/sarmad-writing-style.git ~/code/sarmad-writing-style
mkdir -p ~/.copilot/skills && cp -R ~/code/sarmad-writing-style/skills/* ~/.copilot/skills/
```

To update later, `git pull` in the clone and run the copy line again.

