# Job hunt partner

A Claude skill that works as a job search partner for any profession, level and country.

It starts by asking you a few questions: what you do, which titles you want, where you can work, your pay floor and how you track applications. It asks only what the task in front of it needs. Then it helps with the whole search:

- **Finding and scoring roles.** Checks location, work rights, level and pay first, then scores the fit from 0 to 100. Flags ghost jobs and scams.
- **Resumes and CVs.** Reviews, adapts for one role, or rewrites. It follows the norms of the country you apply in and keeps every claim true to your own materials.
- **Portfolios and work samples.** Design case studies, GitHub, writing clips, campaign results, whatever your field uses.
- **Outreach.** LinkedIn connection notes, DMs, referral asks, informational interview invites and follow-ups, written to current LinkedIn limits.
- **Tracking.** Logs applications in Notion, Google Sheets, Excel or a plain table, sets a next action for every row, and runs a weekly review.

When the questions are done, it shows you a short profile and offers to save it, so the next session skips them.

## Install

**Claude apps (web, desktop, mobile):** [download job-hunt-partner.skill](https://github.com/mahdiverse/job-hunt-partner/raw/main/dist/job-hunt-partner.skill), open it in Claude and save it as a skill. You can also upload it in Claude's skills settings.

**Claude Code:** copy the `job-hunt-partner` folder into `~/.claude/skills/` (for all your projects) or into `.claude/skills/` inside one project.

Then just talk about your job search. For example:

- "Help me find senior data analyst roles I can do remotely from Lisbon."
- "Review my CV for a nursing to UX research switch." (attach the CV)
- "Fix this LinkedIn note to a recruiter at Stripe."
- "Set up a tracker for my applications in Google Sheets."

## What is inside

```
job-hunt-partner/
├── SKILL.md                      intake, routing and ground rules
└── references/
    ├── intake.md                 the questions and the profile block
    ├── evaluating-roles.md       gates, scoring, ghost jobs and scams
    ├── resume.md                 resumes, CVs and cover letters
    ├── portfolio.md              portfolio and work sample reviews
    ├── outreach.md               the message sequence, ask ladder and limits
    ├── outreach-examples.md      before and after examples from five fields
    ├── tracking.md               tracker fields, statuses and weekly review
    └── reading-pages.md          how to read job boards and LinkedIn safely
```

## Principles

- **Nothing invented.** Every claim about you comes from your resume, portfolio, LinkedIn or what you said. No made-up numbers, titles or skills.
- **Honest scores.** A short list of roles you can win beats a long list you cannot.
- **You stay in control.** It drafts and reads, but it never sends a message, clicks Connect or submits an application for you.

## Updating

LinkedIn limits and hiring norms change. The numbers in `references/outreach.md` and `references/evaluating-roles.md` name their sources and dates, so you can check them. Pull requests with newer data are welcome.

## License

MIT. See [LICENSE](LICENSE).
