<h1 align="center">mock-interview</h1>

<p align="center"><strong>A realistic mock job interview for any job, in your terminal or chat.<br>
Then an honest report: a score out of 10, what worked, what hurt you, what to fix.</strong></p>

<p align="center">
  <img src="https://img.shields.io/badge/agent%20skill-SKILL.md-8a63d2" alt="Agent skill">
  <img src="https://img.shields.io/badge/works%20with-Claude%20Code%20·%20Codex%20·%20Cursor%20·%20Gemini%20CLI%20·%20Copilot-555" alt="Works with Claude Code, Codex, Cursor, Gemini CLI, Copilot">
  <a href="./LICENSE"><img src="https://img.shields.io/badge/license-MIT-blue" alt="MIT license"></a>
</p>

Most "AI interview coaches" tell you every answer was great. This one doesn't.
It researches the job, plays a real interviewer, digs into vague answers, and grades you
the way a hiring manager would in the debrief.

Works for any job title: product manager, nurse, sales executive, accountant, teacher, developer…
For DevOps, SRE and platform roles, use the specialized
[**devops-mock-interview**](https://github.com/georgesmomo/devops-mock-interview).

## How it works

| Step | What happens |
|---|---|
| **1. Intake** | One message, 3 required answers: job title, level, interview type. Company, job posting and CV are optional. |
| **2. Research** | The agent reads the posting, researches the company and benchmarks the role. You see each step as it happens. |
| **3. Briefing** | You meet your interviewer: a name, a role, a style. |
| **4. Interview** | One question at a time. Follow-ups when you're vague. No hints, no feedback, like the real thing. |
| **5. Report** | Score /10, hire or no-hire verdict, evidence from your own answers, your two weakest answers rewritten, 3 priorities. |

## What it looks like

```text
🔎 Reading the job posting…
   ✓ 7 requirements found. Key ones: roadmap ownership, SQL, stakeholder management.
🏢 Researching Northwind Logistics…
   ✓ B2B freight platform, ~600 people, opening 3 new warehouses this year.
📄 Reading your CV…
   ✓ 4 years in e-commerce. Gap to probe: no pricing experience.
🎯 Building the interview plan…
   ✓ 5 competencies, 8 questions, about 30 minutes.

Your interviewer is Claire Martin, Head of Product. Direct, polite, digs into details.

Claire: [1/8] Thanks for your time today. To start, can you introduce yourself?

You:    I've been a PM for 4 years, we launched a lot of features at my company…

Claire: Okay. You said "we launched". Which one did you own, end to end?
```

And at the end: [see a full sample report](examples/sample-report.md).

```text
## Verdict: 5.7/10 — Borderline

You know the PM vocabulary and your motivation is clear. But you never gave
a number for anything you shipped, and that is what the hiring manager will remember.
```

## Install

**Any agent** (Claude Code, Codex, Cursor, Gemini CLI, GitHub Copilot, OpenCode and more),
with the [skills CLI](https://github.com/vercel-labs/skills):

```bash
npx skills add georgesmomo/mock-interview
```

**Claude Code plugin:**

```text
/plugin marketplace add georgesmomo/mock-interview
/plugin install mock-interview@mock-interview
```

**Manual:** copy `skills/mock-interview/` into your agent's skills folder
(for Claude Code: `~/.claude/skills/mock-interview/`).

## Use

Just ask:

```text
Interview me for a senior sales executive role at Salesforce.
```

```text
Prepare me for my nurse interview on Monday. Here is the job posting: https://…
```

In Claude Code you can also type `/mock-interview`.

During the interview: `pause` to pause, `stop` to end early and get your report.

Tip: give it your CV and the real job posting. The questions get much sharper.

## Why this one

- **Real conditions.** One question at a time, follow-ups, a pressure question, no feedback until the end.
- **No flattery.** Calibrated scoring: 5 means "maybe", 8+ means "I'd defend this hire".
- **Evidence-based.** Every strength and weakness quotes what you actually said.
- **Short report.** One screen and a half. Plain sentences. No corporate filler.
- **Any language.** It interviews you in the language you write in.
- **Any agent.** A plain `SKILL.md`, no code, no API key.

## Files

```text
skills/mock-interview/
├── SKILL.md                       # the 5-phase flow
└── references/
    ├── interview-types.md         # question patterns by interview type and level
    ├── scoring.md                 # calibrated rubric and verdict rules
    └── report-template.md         # exact report structure
```

## 🇫🇷 En français

Un entretien d'embauche simulé et réaliste, pour n'importe quel métier, avec Claude Code,
Codex, Cursor, Gemini CLI ou Copilot. L'agent étudie l'offre et l'entreprise, joue un vrai
recruteur, vous relance quand vous êtes flou, puis vous rend un rapport sans langue de bois :
note sur 10, verdict, points forts, points faibles, vos deux pires réponses réécrites et
trois priorités.

```bash
npx skills add georgesmomo/mock-interview
```

Puis écrivez simplement : « Prépare-moi à mon entretien de chef de projet chez Decathlon. »
L'entretien se déroule en français.

## Contributing

Issues and pull requests are welcome, especially new interview patterns for specific jobs.
If it helped you land a job, a ⭐ helps others find it.

## License

[MIT](./LICENSE) © Georges MOMO
