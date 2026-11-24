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
| UI changes follow one procedure | Live | Since Nov 23, every new or changed screen loads the `ui-change` skill: it picks the screen to copy, measures it and captures dark, light and phone screenshots and a motion check for the PR. |
| Fixes go in, changes wait for Evan | Live | Since Nov 17, a fix goes straight in. A change to how something looks or behaves needs Evan's OK first, with a before and after in `#pod-blissful-team`. |
| Unfinished work behind feature flags | Live | Vercel Flags, switched in the Vercel dashboard. Merging to main deploys, so anything not ready stays behind a flag. |
| Audits run by agents | Live | Amp audits the codebase for a class of bug. Its findings become small fix PRs (Nov 13 audit: 20 bugs fixed, 19 risks being worked through). Skills for an end-of-day quality audit and an over-engineering audit. |

## Review and merge

| Item | Status | Notes |
| --- | --- | --- |
| One small PR per change | Live | Each PR follows the PR template: its Amp thread link, what changed, UI evidence, checks run and a one-line changelog. Daffa reviews and merges, Naufal's PRs included. |
| Agent review on every PR | Partly live | Each PR is reviewed by an agent session before Daffa merges it, and since Nov 23 also reviewed for what to delete (`ponytail-review`). CodeRabbit reviews the day's PR into main by itself; on the small PRs into the daily branch it still skips unless asked (`@coderabbitai review`). |
| One ready PR into main a day | Live | Since Nov 17: small PRs go into a daily branch, and one ready PR from it into main each evening, with the fixes listed apart from the changes Evan approved. Evan merges it with a merge commit, so each small PR stays in the history. |
| Checks we can trust | Live | CI (typecheck, lint, unit tests, Storybook) runs on every PR, the small ones included. Before a PR the agent also runs format, knip and the related tests and stories. |
| A person reviews risky changes | Live | Billing, sign-in and user-data changes get a careful human review. |

## Shipping and reporting

| Item | Status | Notes |
| --- | --- | --- |
| Release notes written from the PRs | Live | Each evening an agent adds one release-notes commit to the daily branch: the version bump and an entry written from the PRs' changelog lines. |
| Daily checkpoint in Slack | Live | Drafted by an agent from the day's work and posted in `#pod-blissful-team`, linking the day's PR. |
| Presentation of the day's PR | Live | A slide deck with a caption per slide, sent to Evan as a PDF and attached to the day's Slack update. Not narrated. |
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
| QA agent on every preview | Planned | An agent clicks through each PR's preview before it merges. Previews sit behind Vercel's login, so the agent needs a way in. |
| Errors and usage sent to agents | Planned | No error tracker yet; usage is in PostHog. Needs webhooks into Amp. |
| Agents can load real odds | Partly live | Backend PR #13 merged Nov 11: the dev backend can admit preview origins. Our docs still say it accepts only `localhost:3000`, so odds reach a dev server on that port only. |

## Working with the backend and design

| Item | Status | Notes |
| --- | --- | --- |
| Backend work in Amp | Live | William runs a Player Props space in Amp. |
| Frontend and backend in the same thread | Planned | A shared space for features that need both sides. Today the asks still go through Slack. |
| Frontend threads read the backend docs | Partly live | Agents read the Backend For Frontend page in Notion each time, which mirrors the backend repo's docs. Whether the backend repo is attached to the frontend project is still to be confirmed. |
| Product decisions agents can look up | Live | `docs/team-context.md` records each product decision with who and when, and agents add new ones as they're made (Evan's Nov 23 decisions went in the same day). |
| Design in Amp | Partly live | Evan made a Design space for Frank on Nov 12. |

## Open questions

| Question | Who |
| --- | --- |
| Do we keep Amp after the trial, and who pays for it? | Evan, Steve |
| Is the dev backend set to admit preview origins, so previews and agents get real odds? | William |
| When do frontend and backend start sharing threads? | William, Evan |
| How do we measure speed now (request to users, report to fix)? | Steve |
