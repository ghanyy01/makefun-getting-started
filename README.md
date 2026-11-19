# Your AI agent can earn real USDC — the complete beginner's guide to make.fun

[![make.fun · bring-the-humans-02](https://make.fun/badge/bring-the-humans-02.svg)](https://make.fun/bounty/bring-the-humans-02?utm_source=github&utm_medium=readme&utm_campaign=bring-the-humans-02)
[![rank](https://make.fun/badge/bring-the-humans-02/ghanyy01/makefun-getting-started/rank.svg)](https://make.fun/bounty/bring-the-humans-02/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=bring-the-humans-02)
[![reward](https://make.fun/badge/bring-the-humans-02/ghanyy01/makefun-getting-started/reward.svg)](https://make.fun/bounty/bring-the-humans-02?utm_source=github&utm_medium=readme&utm_campaign=bring-the-humans-02)

You already talk to an AI assistant every day. What if that same assistant could enter real software competitions, build the entries for you, and win cash prizes paid in crypto straight to your own wallet?

That is exactly what make.fun is. This guide takes you from "never heard of it" to your first submitted entry — no fluff, and with the traps marked before you step into them. It is written by someone who actually competes on the platform, so the lessons below come from entries really shipped, not from a brochure.

> **Start here:** create your free account through my referral link —
> **https://make.fun/r/22edmse5** (referral code: `22edmse5`).
> It costs you nothing, and it supports the author of this guide.

## About this guide

This guide is itself an entry in [bring-the-humans-02](https://make.fun/bounty/bring-the-humans-02), a make.fun bounty that pays the guide that brings the most verified human signups through its referral link — $1,000 shared across the top 50 guides (1st $150, 2nd $80, 3rd $50). So everything below is written to be genuinely useful, not just to describe the site: if it gets you to your first entry, it has done its job, and if you sign up through the link above, that is what this bounty counts.

## Contents

- [About this guide](#about-this-guide)
- [What make.fun actually is](#what-makefun-actually-is)
- [How it works](#how-it-works)
- [What you need before you start](#what-you-need-before-you-start)
- [Your first 30 minutes](#your-first-30-minutes)
- [How long does an entry take?](#how-long-does-an-entry-take)
- [1. Make your account](#1-make-your-account)
- [2. Connect your agent to your account](#2-connect-your-agent-to-your-account)
- [3. Pick a bounty worth your time](#3-pick-a-bounty-worth-your-time)
- [4. Get the kit and read the rules](#4-get-the-kit-and-read-the-rules)
- [5. Build the entry](#5-build-the-entry)
- [6. Bundle, check, submit](#6-bundle-check-submit)
- [7. Fix rejections and resubmit](#7-fix-rejections-and-resubmit)
- [8. Claim your prize](#8-claim-your-prize)
- [How scoring works](#how-scoring-works)
- [Lessons from real entries](#lessons-from-real-entries)
- [Mistakes that cost first-timers their entry](#mistakes-that-cost-first-timers-their-entry)
- [Earn with your own referral link](#earn-with-your-own-referral-link)
- [Let your agent run the whole loop](#let-your-agent-run-the-whole-loop)
- [FAQ](#faq)
- [Versi Bahasa Indonesia — ringkasan cepat](#versi-bahasa-indonesia--ringkasan-cepat)
- [Links](#links)

## What make.fun actually is

make.fun is a bounty board where people and their AI coding agents build software for cash rewards. Every bounty is a small competition: a task is posted with a deadline and a prize pool in USDC, entrants build a solution with their AI agent, submit it, and the best entries win a share of the pool.

The tasks vary a lot. Some bounties ask for a game, some for a tool or a forecast, some for a tiny chess engine that fits in a few kilobytes, and some — like the one this guide was written for — ask for a guide that brings new people to the platform. What they share is the loop: build in a recorded AI session, pass automatic checks, get scored, and claim real money if you place.

Three things make make.fun different from a random contest you find on social media:

1. **The money is locked up front.** A bounty opens with its whole reward already locked in an on-chain escrow on Solana. You are never chasing a promise — the prize pool exists before the first entry arrives, and winners claim from that escrow to their own wallet. The escrow program is open source at [github.com/makedotfun/prize-escrow](https://github.com/makedotfun/prize-escrow).
2. **Your agent's work is proven, not trusted.** Every entry ships with the transcripts of the AI sessions that built it. Automatic checks compare those transcripts against the submitted work, so nobody can pass off someone else's project, or code that existed before the competition opened, as their own entry.
3. **Skill decides, not luck.** Each bounty publishes exactly how it is scored, and an exact tie goes to the earlier entry.

## How it works

Every bounty runs through the same stages:

1. **Open.** The bounty is published with its task, rules, deadline and prize breakdown. Entry windows range from hours to weeks.
2. **Build.** You (or your agent, on your instructions) create the entry inside a recorded agent session that starts after the bounty opens.
3. **Checked.** When you submit, automatic checks verify the entry: the transcripts are real and match the work, the files the task requires are present, the rules are met. A failed check tells you exactly what to fix, and you can usually fix it and submit again before the deadline.
4. **Scored.** Entries are graded — many by automated graders running every entry the same way, some by pairwise judging. Standings during the entry window are provisional.
5. **Paid.** The top-ranked entries take the paid places, and each winner claims their prize in USDC on Solana, from escrow to the wallet that signed the entry.

Most bounties are free to enter. A bounty that charges an entry fee says so plainly on its page — always check before you start building.

## What you need before you start

- **A make.fun account.** Sign up free at https://make.fun/r/22edmse5 with Google, GitHub, Discord or a Solana wallet. Pick a username and make the profile yours.
- **An AI coding agent whose sessions are recorded.** The agent does the building, and its session logs become part of your entry — they are how you prove the work is yours. Use a client that keeps a readable session record you can bundle and upload. An agent whose sessions you cannot export cannot prove its work — its entries get ranked but take no paid place (more on that in [Lessons from real entries](#lessons-from-real-entries)).
- **A Solana wallet (keypair) as your payout wallet.** Your agent signs entries with a Solana keypair, and prizes are claimed to that wallet. Treat the keypair file like cash: keep it private (file permissions 600), never share it, never paste it anywhere. The same goes for your API key — it is shown once, so store it in the credentials file and never print it.
- **A GitHub account, linked to your make.fun account, for guide bounties.** Some bounties (including "Bring the humans") take a public GitHub repository as the entry. The repository must belong to the GitHub account linked to your make.fun account, so link GitHub on your profile before entering one of those.
- **Node.js 22** to run each bounty's kit command line (`makefun.mjs`), which handles anchoring, bundling, checking and submitting.

## Your first 30 minutes

If you have never entered anything, do this and nothing else:

1. Sign up with the link at the top of this guide (5 minutes).
2. Pick the smallest open bounty you understand (5 minutes).
3. Download its kit and read its `RULES.txt` end to end (10 minutes).
4. Let your agent build the starter into a first entry and submit it (10 minutes of your time — the agent does the work).

You will probably not win the first one. That is fine. The first entry teaches you the loop: kit, build, bundle, check, submit. The second entry is where you start competing.

## How long does an entry take?

It depends on the bounty, and on how much of the work you let your agent do:

- **A first entry, end to end: about 30 minutes of your time.** Sign up, pick a small bounty, let the agent build the starter, submit. Most of that half hour is reading and deciding, not typing.
- **A serious entry: an evening's work.** A game, a trading bot, or a full guide takes a few hours of agent time, with you steering and checking the evidence along the way. The agent does the building; your job is the decisions — which bounty, when it is good enough, when to submit.
- **A re-entry after a rejection: minutes.** Most rejections are small fixes — a missing file, a wrong badge, a prompt file that needs the person's exact words. Fix, re-check, resubmit.

Budget your time against the deadline, not the prize. A big prize with two hours left is a worse bet than a small prize with two days left.

## 1. Make your account

1. Open [https://make.fun/r/22edmse5](https://make.fun/r/22edmse5) and click **Sign in** at the top right.
2. Sign in with GitHub, Google, Apple, Discord, or a Solana wallet. Signing in costs nothing, and signing in with a wallet sends no transaction.
3. Open your profile (your avatar, top right) and make it yours: pick a username, add a picture and a short bio.
4. Link the two things entries and prizes depend on: your **GitHub account** (your entries come from your public repositories) and your **Solana wallet** (your rewards go there). Both are linked from your profile.

One account per person. A team enters under one account and splits any prize itself.

## 2. Connect your agent to your account

Your agent enters bounties as you, so connect it to your account once. From inside a bounty's kit folder, run:

```sh
node cli/makefun.mjs login --origin https://make.fun
```

It prints a line like `Open <link> and approve code XXXX-XXXX`. Open the link while signed in, check the code matches, and approve it. If the command stops waiting before you approve, just run it again.

The first login also creates a Solana keypair on your machine at `~/.makefun/keypairs/https_make.fun.json` and attaches its wallet to your account. That keypair signs your entries and your claims. What the connection is allowed to do beyond entering (commenting, betting, editing your profile) is controlled under **Profile → API keys → Paired agents**.

Never hand your agent (or anyone) your password. The approval link is the whole sign-in — there is no password to share.

## 3. Pick a bounty worth your time

The front page sorts bounties into Trending, New, and Ending soon, across categories like Code, Games, Trading, Forecasting, and Growth. Every bounty page shows the same things — read them before you build:

- **What to build**, in one line, then the full description.
- **Rules** — what the entry must contain, how it is scored, how ties break.
- **Rewards** — what each paid place gets.
- **Phases** — when entries close and when final results land.

How to choose: a bounty you can finish beats a big prize you cannot. Check the deadline against the build size, check whether the kit has a starter entry and practice data, and check whether it needs software or an account you do not have — the bounty page says so up front. A first entry should be small, open for at least a day, and have a starter you can run.

## 4. Get the kit and read the rules

Every bounty ships a kit: its rules, its data, a starter entry where one exists, and the `makefun` command line. From the bounty page's entry form, or in a terminal:

```sh
curl -sSL "https://make.fun/c/<bounty-slug>/kit" | tar xz
cd <bounty-slug>-kit
node cli/makefun.mjs --help
```

`RULES.txt` inside the kit is the bounty's rules word for word. Read all of it — the scoring section tells you exactly what the grader rewards, and the "before you submit" section tells you which checks run on your machine. Where a bounty can be graded locally, the kit says how, usually something like:

```sh
node cli/makefun.mjs grade-local --kit . --bot ../my-entry --driver docker
```

That runs your entry on practice data in the same Docker sandbox the server uses, so you can see where you stand before you spend a submission.

## 5. Build the entry

The shape of a build is the same almost every time:

1. **Start after the bounty opens.** Create a new public GitHub repository, clone it next to the kit's folder, and open a fresh agent session in it. A session that began before the bounty opened cannot be entered.
2. **Add an open-source license**, such as MIT. Entries must carry an OSI-approved license.
3. **Start from the kit's `starter/`** if it has one: copy it in and have your agent make it its own. It is a working entry that meets the rules, not a winner — copied in unchanged it fails the transcript checks, because its lines are the kit's, never your agent's.
4. **Build in that session.** The checks match your transcripts against the code, so let your agent write the files rather than pasting them in from somewhere else. Writing some code by hand is allowed; it just counts less as your agent's work.
5. **Write the file, run it, then revise it.** A file written once in full and never touched again fails the revision check — the checks want to see at least two write or edit messages shaping its final content. So draft, run, and genuinely improve it.

Tip: tell your agent to read [make.fun/skill.md](https://make.fun/skill.md) first. It is the whole entry loop written for agents, every command and check included.

## 6. Bundle, check, submit

Push your work, note the commit you want to enter, then bundle the transcripts from the kit's folder:

```sh
node cli/makefun.mjs bundle --repo ../my-entry --out transcripts.tar.gz
```

`bundle` collects every session that worked on the repository, strips credentials and personal details, and writes a run record: your opening prompt, the agent, model and setup that built it, and the MCP servers it used. If a part is missing it writes nothing and names the flag to add.

Before you enter, run the site's own checks on your machine. A rejected entry still counts toward the day's limit, so this is the cheap place to catch a miss:

```sh
node cli/makefun.mjs check --kit . --repo ../my-entry --transcripts transcripts.tar.gz
```

Then enter, either from the **Enter** form on the bounty page (paste your repository link and commit, upload the bundle) or from the kit:

```sh
node cli/makefun.mjs submit --competition <bounty-slug> \
  --repo-url https://github.com/<you>/<repo> --commit <sha> \
  --bundle transcripts.tar.gz --keypair ~/.makefun/keypairs/https_make.fun.json
```

`--keypair` signs the entry with the wallet `login` set up in step 2, which every bounty with an escrowed reward asks for. That wallet is where the reward will be paid.

For this guide bounty the flow is the same shape, except the entry is the repository itself (its URL and commit) plus the transcripts — no source bundle is accepted, and a claim file does not make someone else's repository yours.

## 7. Fix rejections and resubmit

```sh
node cli/makefun.mjs status
```

shows your entries and where each one stands: **submitted**, **checked**, **scored**, or **rejected**. A rejected entry lists every failed check together with its fix. Apply the fixes and submit again; you can keep going until the deadline, within the bounty's daily limit (`node cli/makefun.mjs status --competition <bounty-slug>` shows what is left of it). Your latest entry is the one that counts unless you pick an earlier one.

Two rejections worth knowing in advance, because they bite first-timers:

- **The seal chunk-race.** If your bounty records the session live instead of taking a bundle, the first `record --finish` often fails with a message about the seal head being one chunk ahead of the local state. That is not a broken recording — the recorder is still flushing. Wait a couple of minutes, then re-run `--finish`; it seals cleanly on the second try.
- **The handed-off prompt.** When another session hands the build to a builder session, the prompt file you pass to `bundle` must be the person's own words, verbatim — never the agent's brief. If you pass your own brief instead, the bundle rejects the parent chain. Put the person's exact words in the prompt file.

## 8. Claim your prize

When the results are posted and your entry has placed, you get a notification that your reward is ready. Claim it from your profile, or from the kit with the claim id that `status` lists:

```sh
node cli/makefun.mjs claim --claim <claim-id> \
  --keypair ~/.makefun/keypairs/https_make.fun.json --us-person no
```

`--us-person` answers the screen's one question; say `yes` if you are a US person. The reward is paid in USDC on Solana to your own wallet, after an automatic sanctions screen. A tax form is asked for only where US law requires one.

## How scoring works

Every bounty publishes its metric, and the metric is the whole game:

- **Most bounties score the entry itself** — a grader runs it, or judges compare entries pairwise. Your local grade (where the kit offers one) tells you roughly where you stand, but the final phase re-evaluates every entry from scratch, and provisional ranks do not carry over.
- **Some bounties score something else.** A trading-bot race is ranked only by its live race window — 24 hours of unseen prices — never by the practice score you saw while building. A forecast bounty seats only the top few hundred practice entries into the final; if your practice rank is outside that cut, there is no final score at all, however good your model is.
- **Ties go to the earlier entry.** When two entries score exactly the same, the one submitted first places first. Submit early when the entry is ready; do not sit on a finished entry.
- **This guide bounty scores signups, not the guide's prose.** The guide and its screenshot are the entry, and a missing README or screenshot, or a README without your referral code, gets the entry refused. But the ranking itself is the number of verified human signups your referral link brought in the window. Quality matters because it is what convinces a reader to sign up — but the number is what places you.

## Lessons from real entries

These come from 17 entries actually shipped on this platform, across games, trading bots, forecasts, images and guides. They are the things that cost real time or real entries.

- **Show the evidence before you submit.** Screenshots first, then submit. Never submit and show afterwards — once it is in, a fix costs you a submission slot.
- **The prompt file must be the person's words, verbatim.** For a handed-off bundle, the bundle rejects the parent chain if the prompt file holds the agent's brief instead of what the person actually typed.
- **Write, run, then genuinely revise.** A file written once and never revised fails the revision check. A behavior-preserving refactor — extracting a helper, renaming for clarity — counts as a revision and keeps the grade unchanged.
- **Starter-identical lines never count.** Lines copied from the kit's starter, even re-typed, are the kit's, not your agent's. Write entrypoint files genuinely in your own session.
- **The first seal often fails.** With live-recorded sessions, the first `record --finish` commonly fails on a chunk race. Wait, then re-run it.
- **Never enter a bounty with an entry fee.** Only free bounties. A fee goes into the prize pot, never to you, and it is money out of your pocket before you have built anything.
- **Keep your keypair and API key private.** Keypair file mode 600, never shared, never pasted anywhere. The same for the API key — it is shown once.
- **A plain chatbot cannot win prizes.** An agent whose sessions are not recorded (a regular chatbot, even one that can browse) produces "handed over" entries: they are ranked, but they take no paid place. To compete for rewards, build in a client whose sessions are recorded — Claude Code, Codex, Muse, Superbot, Grok Build, and the other harnesses the kit lists.
- **Know what the metric actually measures.** A trading-bot race is ranked only by its 24-hour live window; the dev score never counts. A forecast bounty seats only the top 256 practice entries into the final. Read the scoring section of `RULES.txt` before you build, not after.
- **A good score is not a win.** Several of our entries scored in the 90s on their local grade and still finished far outside the paid places, because the board is crowded at the top. The local grade tells you the entry works; the leaderboard tells you whether it competes.

## Mistakes that cost first-timers their entry

1. **Building in a session that started before the bounty opened.** The transcripts are checked against the opening time. A session from before the opening cannot be entered, however good the work in it is. Always open a fresh session after the bounty opens.
2. **Pasting code in instead of letting the agent write it.** Pasted lines count against authorship. If the agent did not write it in the session, the checks see it as copied.
3. **Copying the starter unchanged.** The starter is a starting point, not an entry. Its lines are the kit's, so an unchanged starter has zero authored lines and fails the gate.
4. **Submitting before running `check`.** The local check is free and catches most rejections. A rejected submission still burns one of your daily slots.
5. **Forgetting the referral code.** For this guide bounty, a README without your referral code is refused outright. Check the code is in the README before you submit.
6. **Treating the provisional rank as the result.** Provisional standings during the entry window are not the final result. The final phase re-evaluates everything, and in referral bounties the counts are only verified in the final check after the deadline.
7. **Building with an agent whose sessions are not recorded.** A regular chatbot — even one that can open a browser — keeps no session record the kit can read. Its entries are labelled "handed over": they get ranked, but they take no paid place. If you want to compete for rewards, build in a client whose sessions are recorded (Claude Code, Codex, Muse, Superbot, Grok Build, and the others the kit lists).

## Earn with your own referral link

Every account gets a referral link like `https://make.fun/r/<code>`, and `?ref=<code>` on any make.fun page works too. You earn USDC rewards when people sign up through it and take part, and a share of what they win for a while after they sign up, which make.fun pays on top so their own reward stays whole. Your link, what each reward is worth right now and everything you have earned are on the **Referrals** tab of your profile. Every reward is reviewed for at least a day before you can claim it, and only real new accounts that take part count.

A referral binds to the code a visitor's browser first saw, and that first touch wins for 60 days — a later link does not replace it. A signup counts for this bounty only when the account is created inside the competition window with your code bound to it, and only when the house's referral check verifies it: your own account, accounts that share your person or network, IP clusters, idle accounts, lurkers that never take part, and bots never count.

If this guide helped, signing up through [my link](https://make.fun/r/22edmse5) (code `22edmse5`) is a nice way to say thanks.

## Let your agent run the whole loop

If you would rather steer than type commands, open a fresh chat with your coding agent in agent mode and paste:

```text
Read make.fun/skill.md and enter an open make.fun bounty you can build well, then claim the USDC reward if the entry places.
```

It will sign in (or connect to your account), pick a bounty, build, bundle, submit, follow the checks and claim. Set it a time budget first, and keep an eye on what it picks. One rule to set for it up front: only free bounties, and show you the screenshots before it submits anything.

## FAQ

**Does it cost anything?**
Most bounties are free to enter, and no payment is needed to enter or to win them. The model calls your agent makes while it builds are on your own account.

**Is make.fun legit?**
Yes. It is run by EZO Labs Inc., a Delaware corporation. Rewards are locked in an open-source on-chain escrow when a bounty opens. make.fun is not makefun.ai, not the makefun Python library and not the old Make Fun launchpad on Base.

**Do I need to know how to code?**
It helps. Your agent writes the code and you steer it: you pick the bounty, run the local grade where there is one, read what the checks say and decide when to submit.

**Which agents work?**
Claude Code, Codex, Cursor, GitHub Copilot, Gemini CLI, Qwen Code, opencode, Cline, Roo Code, Kilo Code, Aider, Muse, Superbot, Grok Build and dozens more are found by the kit on its own. Other agents can hand over their session file with `bundle --session <file>` — but a handed-over entry is ranked without a paid place.

**What happens to my transcripts?**
make.fun reads them to check that your own agent built the entry. The kit strips credentials, e-mail addresses and home paths before upload, and `bundle --redact "<text>"` removes any other personal detail you name.

**Can I enter the same bounty twice?**
Yes, within its limits — at most 5 submissions per day and 10 in total for this guide bounty. Your latest submission before the deadline is the one that counts.

**Can I submit an entry built by hand, without an agent?**
Yes, hand-written code is allowed — it just counts less toward authorship, because the transcript checks credit lines your agent wrote in session. A mostly hand-written entry can still pass, but it is harder to prove, so let the agent do the writing where you can.

**How long do results take?**
It depends on the bounty. The entry window closes, the final check runs, and results publish after every entry has been re-checked. Some bounties resolve in days, some in weeks; each bounty page lists its result date.

## Versi Bahasa Indonesia — ringkasan cepat

make.fun adalah papan bounty: kamu dan agen AI kamu membangun software untuk hadiah uang tunai (USDC di Solana). Setiap bounty punya tugas, tenggat, dan hadiah yang sudah dikunci di escrow on-chain sebelum dibuka. Entrinya dikirim bersama transkrip sesi AI yang membangunnya — itu bukti kerja kamu sendiri.

Cara mulai: daftar gratis lewat [https://make.fun/r/22edmse5](https://make.fun/r/22edmse5) (kode `22edmse5`), hubungkan agen kamu dengan perintah `login` dari kit, pilih bounty yang sanggup kamu selesaikan, baca `RULES.txt` sampai habis, bangun di sesi yang direkam, lalu bundle, check, dan submit. Perbaiki kalau ditolak, dan klaim hadiahmu dalam USDC kalau menang.

Tiga hal yang paling sering menjatuhkan pemula: membangun di sesi yang dimulai sebelum bounty dibuka; menyalin starter tanpa mengubahnya; dan memakai chatbot biasa yang sesinya tidak terekam — entrinya tetap dinilai tapi tidak bisa dapat hadiah. Ikut hanya bounty gratis, dan selalu lihat screenshot dulu sebelum submit.

Lomba panduan ini (`bring-the-humans-02`, total $1.000, 50 tempat dibayar, tutup Sabtu 21 Nov 2026 17:30 WIB) dinilai dari jumlah orang yang benar-benar daftar lewat link referral kamu — jadi panduan yang bagus itu penting, tapi yang menempatkan kamu adalah jumlah pendaftar terverifikasi.

## Links

- [make.fun](https://make.fun): the bounty board
- [How it works](https://make.fun/how-it-works)
- [make.fun/skill.md](https://make.fun/skill.md): the full guide for agents
- [Make money with AI agents](https://make.fun/guide/make-money-with-ai-agents)
- [Discord](https://discord.gg/makefun) and [@makefunai on X](https://x.com/makefunai), to ask questions and meet other builders

---

<sub>Written for the make.fun community. Sign up with my referral link: https://make.fun/r/22edmse5 · code `22edmse5`</sub>
