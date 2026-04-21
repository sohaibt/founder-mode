# Contributing to founder-mode

Thanks for your interest in contributing! founder-mode is an open source Claude Code plugin that encodes Brian Chesky's founder mode operating system into structured slash commands.

## Ways to contribute

### Add a new slash command

Have a founder-mode practice or framework that should be a command? Open an issue with:
- The command name and what it does
- What inputs it needs from the user
- What the output should look like
- The source material it's grounded in (transcript, essay, talk, book)

We strongly prefer commands grounded in **primary sources** — not generic startup advice. If Brian Chesky, Paul Graham, Steve Jobs, or another founder-mode practitioner described the practice specifically, it belongs here.

Label: `new-command`

### Add a research source

Found a transcript, interview, essay, or talk that surfaces new founder-mode practices? Open an issue or PR with:
- The source (URL, transcript, or summary)
- What new practices or principles it adds
- Which existing commands it could strengthen

Label: `research`

### Improve an existing command

If a command gives shallow analysis, misses nuance, or doesn't match the source material:
- Better scoring frameworks
- More specific Chesky/PG quotes and references
- Sharper pressure-test questions
- Edge case handling (different company sizes, stages, industries)

Label: `enhancement`

### Fix bad advice

If a command gives advice that's wrong, misleading, or harmful — that's a bug. Founder-mode tools should be opinionated but grounded. Report it.

Label: `bug`

## How the plugin works

Each slash command is a `SKILL.md` file in the `skills/` directory. The file contains:
1. **YAML frontmatter** — name, description, argument hint
2. **Framework instructions** — the structured analysis Claude follows
3. **Output format** — what the response should look like
4. **Important notes** — edge cases and guardrails

There's no code to run. The "logic" is the framework itself — encoded as expert instructions that Claude follows when the user invokes the command.

## Adding a new command

1. **Create a directory** in `skills/` with your command name (lowercase, hyphens):
   ```
   skills/your-command-name/SKILL.md
   ```

2. **Write the SKILL.md** following this structure:
   ```yaml
   ---
   name: your-command-name
   description: One sentence explaining when to use this command.
   argument-hint: [what the user should provide]
   ---

   # Command Title

   You are a strategic advisor who...

   ## Context From the User

   $ARGUMENTS

   ## Your Analysis Framework

   [The structured framework Claude follows]

   ## Output Format

   [What the response should look like]

   ## Important Notes

   [Edge cases, guardrails, when NOT to use this]
   ```

3. **Every command must include:**
   - A structured scoring or assessment framework
   - Specific references to Chesky, PG, or other primary sources
   - Actionable next steps (not generic advice)
   - Pressure-test questions that challenge the analysis
   - Honest acknowledgment of when the framework doesn't apply

4. **Test it locally:**
   ```bash
   claude --plugin-dir ./founder-mode
   /founder-mode:your-command-name [test input]
   ```

5. **Submit a PR** with:
   - The SKILL.md file
   - A brief description of the source material it's grounded in
   - An example of what the output looks like

## Quality standards

- **Grounded in sources.** Every recommendation should trace back to a specific practice, quote, or principle from primary material. No generic startup advice.
- **Opinionated but honest.** Founder mode has failure modes. Every command should acknowledge when the framework doesn't apply.
- **Structured output.** Scoring tables, clear frameworks, specific next steps. Not essays.
- **Pressure-test questions.** Every command should challenge the user's assumptions, not just validate them.
- **Company-size aware.** What works at 10 people ≠ 500 people. Commands should adapt.

## Pull request guidelines

- Open an issue first for new commands so we can discuss the approach
- Keep PRs focused — one command per PR
- Include the source material reference
- Test the command locally before submitting
- Show an example output in the PR description

## What we don't want

- Generic productivity advice not grounded in founder-mode sources
- Commands that are just "ask Claude to do X" without a structured framework
- Advice that applies equally to managers and founders (the whole point is the distinction)
- Low-confidence recommendations without acknowledging uncertainty

## Questions?

Open an issue or reach out to [Sohaib Thiab](https://sohaibthiab.me).
