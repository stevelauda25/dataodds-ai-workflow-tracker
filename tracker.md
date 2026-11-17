# DataOdds AI workflow

<!--
This file is the tracker's only data. The page reads it on every load.
- One row per item. Status must be Live, Partly live or Planned.
- A "## Heading" starts a new area. Keep "## Open questions" last.
-->

## Building

| Item | Status | Notes |
| --- | --- | --- |
| Frontend tasks in Amp threads | Live | One thread per task, since Nov 11. Threads run on the Mac or on Amp's cloud machines. |
| Shared rules every agent reads | Live | AGENTS.md, `docs/conventions.md`, `docs/team-context.md` and folder guides: code rules, product decisions and how changes ship. |
| Shared instructions for Daffa and Naufal | Live | One set of personal Amp instructions: where to branch, the checks to run, what each PR must carry. |
| Unfinished work behind feature flags | Live | Vercel Flags. |
| Audits run by agents | Live | Amp audits the codebase for a class of bug. Its findings become small fix PRs (Nov 13 audit: 20 bugs fixed, 19 risks being worked through). |

## Review and merge

| Item | Status | Notes |
| --- | --- | --- |
| One small PR per change | Live | Each PR carries its Amp thread link and a one-line changelog. Daffa reviews and merges, Naufal's PRs included. |
| Agent review on every PR | Partly live | An agent session reviews each PR before Daffa merges it. CodeRabbit reviews PRs into main by itself; on the small PRs into the daily branch it runs only when asked (`@coderabbitai review`). |
| One ready PR into main a day | Live | Since Nov 17 (Evan's Nov 16 ask): small PRs go into a daily branch, and one PR from it into main each evening, never a draft. Evan reviews one PR, with no merge order. |
| Checks we can trust | Live | CI (typecheck, lint, tests, Storybook) is green since Nov 12 and runs on every PR, the small ones included. |
| A person reviews risky changes | Live | Billing, sign-in and user-data changes get a careful human review. |

## Shipping and reporting

| Item | Status | Notes |
| --- | --- | --- |
| Release notes written from the PRs | Live | Each day's version and changelog are drafted by an agent from the PRs' changelog lines. |
| Daily checkpoint in Slack | Live | Drafted by an agent from the day's work. |
| Narrated presentation of the day's PR | Planned | Evan asked on Nov 16: the daily update includes an AI-made, narrated visual walkthrough of the changes in the day's PR. First one tonight. |
| Notes, checkpoint and presentation start by themselves | Planned | Today someone starts them by hand at the end of the day. |

## Feedback and bugs

| Item | Status | Notes |
| --- | --- | --- |
| Triage agent on user feedback | Planned | In-app feedback lands in Slack `#dataodds-bugs-feat-requests`. An agent would turn each one into a Linear ticket with steps to reproduce. |
| Small bugs arrive with a fix PR | Planned | The same agent opens a fix PR for small, clear bugs. |
| Amp started from Slack or Linear | Partly live | Evan added Amp to the Slack channels on Nov 12. We still start threads ourselves. |

## Testing and production

| Item | Status | Notes |
| --- | --- | --- |
| QA agent on every preview | Planned | An agent clicks through each PR's preview before it merges. |
| Errors and usage sent to agents | Planned | No error tracker yet; usage is in PostHog. Needs webhooks into Amp. |
| Agents can load real odds | Partly live | Backend PR #13 (Nov 12) opens the dev backend to previews and Amp's cloud machines. Check whether it merged. |

## Working with the backend and design

| Item | Status | Notes |
| --- | --- | --- |
| Backend work in Amp | Live | William runs a Player Props space in Amp. |
| Frontend and backend in the same thread | Planned | A shared space for features that need both sides. Today the asks still go through Slack. |
| Frontend threads read the backend docs | Partly live | The contract is in the backend repo and in Notion. The backend repo should be attached to the frontend project; to be confirmed from a thread. |
| Product decisions agents can look up | Partly live | `docs/team-context.md` records each product decision, so agents check it before asking Evan. |
| Design in Amp | Partly live | Evan made a Design space for Frank on Nov 12. |

## Open questions

| Question | Who |
| --- | --- |
| Do we keep Amp after the trial, and who pays for it? | Evan, Steve |
| Did backend PR #13 merge? | William |
| When do frontend and backend start sharing threads? | William, Evan |
| How do we measure speed now (request to users, report to fix)? | Steve |
