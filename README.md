# Surf Location Research

A portable Markdown skill for researching surf destinations and date-specific conditions using forecasts, timestamped observations, guides, video evidence and satellite geography.

## Single-file skill: Claude Code and other agents

Download [SKILL.md](https://raw.githubusercontent.com/felixzcheng/surf-location-research/main/SKILL.md). It includes the complete workflow and report template; no supporting files are required for this version.

### Claude Code

Save the file as `~/.claude/skills/surf-location-research/SKILL.md` for personal use, or `.claude/skills/surf-location-research/SKILL.md` inside a project. Invoke it with `/surf-location-research Da Nang tomorrow`.

See the [official Claude Code skill documentation](https://code.claude.com/docs/en/skills). These installation instructions have been checked against the documentation; the workflow has not been end-to-end tested in Claude.

### Other agents and chat interfaces

If your agent supports SKILL.md skills, put the file in its documented skill directory. Otherwise, attach or paste the Markdown and say:

> Follow the attached Surf Location Research workflow. Begin by asking for my own surfing profile and preferences, then research [destination] for [dates].

The agent needs web research access for current conditions. Video and satellite inspection depend on its tools. Markdown instructions do not grant tools or permissions, and automatic skill discovery varies by product. Without web access, it must disclose that current conditions cannot be verified.

## Original multi-file bundle: Codex

1. Download [surf-location-research.zip](surf-location-research.zip).
2. Unzip it and copy the entire `surf-location-research` folder into `$CODEX_HOME/skills` (or `~/.codex/skills` when unset).
3. Keep `SKILL.md`, `references/`, and `agents/` together. Back up an existing skill of the same name before replacing it.
4. In a new turn, ask: `Use $surf-location-research to research Da Nang tomorrow.`

## First-use setup

Before research, the skill asks for your own surfing level, board, stance, goals, comfortable breaking-wave face size, wave preferences, limitations and report language. Unknown and no preference are valid answers. If you decline setup, it provides a general report with personal suitability unverified.

No author's personal surfing profile is included. Your answers are used within the conversation and are not written into this shared skill.

## Evidence and limitations

Web research access is required. Browser/video and satellite access improve coverage. The skill distinguishes observations, forecasts, historical data and seasonal guidance, and discloses missing or inaccessible evidence. It does not continuously monitor conditions.

The archive includes the skill instructions, report template, UI metadata and installation instructions.
