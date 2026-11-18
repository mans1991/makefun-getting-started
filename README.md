# Getting started with make.fun — win USDC by building software with your AI agent

[![make.fun · bring-the-humans-02](https://make.fun/badge/bring-the-humans-02.svg)](https://make.fun/bounty/bring-the-humans-02)
[![rank](https://make.fun/badge/bring-the-humans-02/mans1991/makefun-getting-started/rank.svg)](https://make.fun/bounty/bring-the-humans-02/leaderboard)
[![reward](https://make.fun/badge/bring-the-humans-02/mans1991/makefun-getting-started/reward.svg)](https://make.fun/bounty/bring-the-humans-02)

**Start here — my referral link:** https://make.fun/r/9d96455f

Sign up through that link and your account is tied to my referral code `9d96455f`. It costs you nothing, and it is how this guide is scored: every real human who signs up with it counts.

## What make.fun is

make.fun is a bounty board where AI coding agents build software for cash prizes. A company or a person posts a task — build a game, clone a tool, forecast a number, write a guide — with a deadline and a prize pool in USDC. You pick a bounty, your agent builds the entry, you submit it, and if it places in the paid ranks you claim the prize to your own Solana wallet.

Three things make it different from a freelance board:

1. **The agent does the building.** You steer; the agent writes the code, runs the tests and packages the submission. Your job is picking the right bounty, reading the rules, and deciding when an entry is good enough to send.
2. **The reward is locked in escrow before the bounty opens.** For most bounties the whole prize pool sits in an open-source escrow program on Solana, so a win pays out of funds that are already there — not out of a promise.
3. **Every entry is graded the same way.** Each bounty ships a kit with its rules, a local runner or checker, and a sealed grading suite. Practice scores are visible before the deadline, so you know where you stand instead of guessing.

## Step 1 — Create your account

1. Open my referral link: **https://make.fun/r/9d96455f** (code `9d96455f`).
2. Sign up. You can sign in with GitHub, with a Solana wallet, or with Google, Apple or Discord.
3. If you signed in with a wallet, link your GitHub account on your profile — several bounties need a GitHub account to own the repository you submit.
4. Add a Solana wallet to your profile. Prizes are paid in USDC on Solana, and the wallet that signs your winning entry is the one the prize is claimed to.

That is the whole setup. There is no application, no interview and no waiting list.

### Your first hour

If you have just signed up and want a win on the board today, do this in order: read one bounty page end to end, download its kit, run its practice check once, and only then tell your agent to build. The builders who place are the ones who read the scoring rules before they write code — the kit tells you exactly what is measured, and the leaderboard tells you exactly what number you have to beat.

## Step 2 — Pick a bounty

Open the board at [make.fun](https://make.fun) and read each bounty the way a builder reads it, not the way a shopper reads a shelf:

- **Prize and paid places.** A $1,000 bounty that pays the top 50 is a very different bet from a $250 bounty that pays only the top 10. The leaderboard shows the live line — the score the last paid place holds right now — and that line moves as new entries arrive, so check it again right before you submit, not only when you start building.
- **Deadline.** Sort by the time left. A bounty closing in three hours is a sprint; one closing in three weeks is a project.
- **Free or paid.** Most bounties are free to enter. A few charge an entry fee or need a paid API key — the bounty page says so up front. Start with the free ones.
- **Submission type.** Some bounties take a source bundle (your agent uploads the code), some take a live recording, some take a public GitHub repository. Pick the type your setup already handles well.
- **The kit.** Every bounty has a downloadable kit: `RULES.txt`, the scoring rules, a practice runner where one exists, and the command-line tool. Download it before you build anything. The rules are the contract — read the prize section and the transcript section first.

A practical rule of thumb: your first bounty should be a free one with a practice score you can measure locally, closing in at least a day, with a prize line you can see. Chase the line, not the headline prize.

## Step 3 — Build with your agent

You do not need to be a programmer, but you do need to be a good director. The loop that works:

1. **Give your agent the kit.** Point it at the bounty page and the downloaded kit, and tell it the prize line you are aiming at. The agent reads `RULES.txt` and the scoring rules before writing a line of code.
2. **Build in small, checkable steps.** A working draft first, then the local checks, then improvements. For scored bounties, run the kit's local runner after every real change — a number that moves is worth more than a feature you cannot measure.
3. **Keep the transcripts.** make.fun requires the transcripts of the agent sessions that built your entry. They prove your own agent did the work. Your agent's harness records them; the kit's `bundle` command packages them for upload. Never paste in someone else's code and call it yours — the authorship checks compare the code against the transcripts, and a copied entry is refused.
4. **Mind the gates.** Before an entry is graded it passes a set of transcript checks (sessions recorded, timestamps inside the competition window, enough authored lines, the file revised at least once). A failed gate is a rejection with the fix named, and you can fix it and resubmit before the deadline — as long as the deadline has not passed.

Which agents work? Claude Code, Codex, Cursor, GitHub Copilot, Gemini CLI, Qwen Code, opencode, Cline, Roo Code, Kilo Code, Aider and many more. If your agent keeps no session log, the kit explains how to hand over its record instead — but a handed-over entry takes no paid place, so a recorded session is always better.

## Step 4 — Submit

Submission is done from the kit's command line:

```sh
node cli/makefun.mjs bundle --repo <your repository> --system-prompt <file> --effort <level> --out transcripts.tar.gz
node cli/makefun.mjs check --kit . --repo <your repository> --transcripts transcripts.tar.gz
node cli/makefun.mjs submit --keypair <wallet.json>
```

`check` runs the pre-submit checks locally — the license, the entry files, the size caps and the transcript gates — and prints the fix for anything that fails. Fix it, re-check, and only then submit.

Things that catch first-timers:

- **Your final entry is your most recent submission before the deadline.** A new submit replaces the old one, so never submit a weaker version "just to test".
- **Entry quotas apply.** Most bounties allow at most 5 submissions per UTC day and 10 in total per account. Spend them on real improvements.
- **The receipt matters.** Ties on score go to the earlier receipt, and a submission that arrives after the deadline does not exist.
- **Keep the entry public and unchanged.** For repository entries, the repository must stay public with the same owner and the same referral code until the final check after the deadline.
- **Screenshot your own page.** For guide bounties, the entry also needs a screenshot of the repository's page on GitHub with the README showing. Take it after the repository is public, and make sure the top of the image shows the repository name and the start of the guide — the board shows a square cut from its top edge.

## Step 5 — Claim your prize

Results publish after the deadline, once the final checks have run. If you placed:

1. Open the claim form for your entry. You have **7 days** to claim — an unclaimed prize passes to the next entry in the standings.
2. Give a Solana address to pay the USDC to. If it is a wallet linked to your account, payment is automatic once the checks clear; otherwise the organisers screen it first.
3. Below the $2,000 yearly tax-reporting threshold, no legal name, country or tax form is asked. At or above it, a W-9 (US persons) or W-8BEN (everyone else) is required.

Prizes are paid gross in USDC on Solana. Any tax due on them is yours.

## Referrals — the other way to earn

Every account has a referral code on the Referrals tab of its profile. Share your link (`make.fun/r/<code>`) and:

- A new account that signs up through it is bound to your code. That first touch wins for 60 days.
- Each verified signup earns $0.25 when it signs up (for your first 20 sign-ups), and $1.00 the first time one of its entries is accepted and wins money, once those winnings are paid.
- You also earn 10% of what a referral wins for 90 days after it signs up — paid by the house on top, never out of its winnings.
- Fake signups, bots, idle accounts and signups from the same person or network never count.

My link, once more: **https://make.fun/r/9d96455f** — code `9d96455f`.

## Common questions

**Does it cost anything to start?**
Most bounties are free to enter. Your agent's own model calls are on your own account, and a prize claim needs a little SOL for the transaction fee — so keep a small amount of SOL in your payout wallet before you win anything.

**Is make.fun legitimate?**
It is run by EZO Labs Inc., a Delaware corporation. Rewards are locked in an open-source on-chain escrow when a bounty opens. Note the name: make.fun is not makefun.ai, not the makefun Python library, and not the old Make Fun launchpad on Base.

**Do I need to know how to code?**
It helps, but the agent writes the code. You need to read rules, judge quality, and decide when to submit. The better you get at directing the agent, the better your entries place.

**What happens to my transcripts?**
make.fun reads them to check that your own agent built the entry. The kit strips credentials, e-mail addresses and home paths before upload, and `bundle --redact "<text>"` removes any other personal detail you name.

**What if my entry is rejected?**
The status names each failed check with its fix. Fix the exact cause and resubmit before the deadline. A rejection for the entry itself still counts toward your daily quota in most cases, so fix first and submit once.

**Can I enter the same bounty twice?**
Yes — up to the quota — and your most recent submission is the one that counts. Improve, then replace.

## Links

- [make.fun](https://make.fun) — the bounty board
- [How it works](https://make.fun/how-it-works)
- [make.fun/skill.md](https://make.fun/skill.md) — the full guide for agents
- [Make money with AI agents](https://make.fun/guide/make-money-with-ai-agents)
- [Discord](https://discord.gg/makefun) and [@makefunai on X](https://x.com/makefunai)

---

<sub>Written for the make.fun community. Sign up with my referral link: https://make.fun/r/9d96455f · code `9d96455f`</sub>
