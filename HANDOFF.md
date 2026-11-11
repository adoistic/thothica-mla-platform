# Handoff: the Thothica MLA constituency system

Prepared by Adnan (Thothica) for Mr. Siraj, 11 November 2026.

This file is meant to be read two ways:

1. **By you, Mr. Siraj**, to understand what this project is, what exists today and what does not.
2. **By your own Claude.** You can give Claude this whole repository (or just this file) and ask it
   questions in plain language, such as "explain the fund router to me" or "what would it take to
   add a feature for X". Part 9 at the end is written for Claude and tells it how to help you.

---

## 1. The one-paragraph version

After meetings in Kerala, one MLA's office asked Thothica whether we could build an online,
AI-powered platform that helps the member stay connected to constituents and serve them easily,
fairly and efficiently. We answered with a **proposal**: a "constituency operations system" for
Kerala MLAs. It works over WhatsApp (no app to download), in Malayalam and English, and it is built
around the work an MLA's front office already does every day. The proposal is a web page with
three clickable demos, plus the same material as a PDF deck.

## 2. Where things stand (please read this first)

| | Status |
|---|---|
| The idea and the design | **Done.** Written up in full in the web page and the PDF. |
| Clickable demos | **Done, but they are demonstrations.** The three "See it working" screens run in the browser on invented names and data. They show how the product would feel. They are not connected to WhatsApp, a database or any AI. |
| The actual working system | **Not built yet.** No server, no database, no WhatsApp connection, no live AI. |
| Feedback from the MLA office | **Waiting.** The proposal ends with six questions for the office (see part 7). |

So this is a **concept for discussion**, dated August 2026. It is the right moment for new ideas,
because nothing has been built that would need to be undone.

## 3. How to look at it

- **The web page (best way):** https://adoistic.github.io/thothica-mla-platform/
  Open it on a phone or a laptop. Scroll down to "See it working" and tap through the three demos.
- **The PDF deck:** `Thothica-MLA-constituency-operations.pdf` in this repository. This is the
  version to forward or print.

Everything in the demos is shown in English so each word can be checked. The real product would
run in Malayalam and English. All names, wards and amounts in the demos are invented.

## 4. The problem it solves

What an MLA's front office runs on today, as described in the proposal:

- **A WhatsApp group and a paper register.** Requests come by voice note, phone call, folded paper
  and word of mouth, and live in a staffer's memory.
- **Silence as the default reply.** Most people who write to a member never hear back. That silence
  is what they remember.
- **No memory across time.** A promise made at a house visit in March is forgotten by August. When
  staff change, the history leaves with them.
- **Money that lapses quietly.** Development fund allocations expire unspent because nobody sees
  the position until March.
- **Two jobs that never meet.** Constituency casework and Assembly work sit in separate diaries.
- **Only the loud are heard.** Whole wards go quiet and nobody notices.

## 5. The core idea

**Model the constituency, not the complaint.** Most grievance systems are like a post office: a
complaint comes in, a ticket opens, it is sent somewhere. This system instead keeps a map of the
constituency itself: its households, wards, roads, transformers, water schemes, schools, the
authority responsible for each, and the funds that can pay for repairs.

Example: forty complaints about water from one ward stop being forty separate tickets. They become
one fact about one water line, owned by a named authority, possibly already covered by a sanctioned
work. The office solves one thing instead of forty, and each person who complained is told their
complaint is part of a known case (the demo says "you and 39 others").

## 6. What the system would do (the features)

The work of an MLA's office is split into three separate "rails", because each needs different
handling.

### Rail A: Obligations (things the state owes)

Roads, transformers, street lights, water connections, drainage, school and anganwadi repairs.

- **Civic issues, ward by ward.** Every report is placed on a ward map and joined to the asset it
  is about.
- **The fund router.** For each request, the system works out which fund could pay for it (for
  example, too small for the Asset Development Fund but right for the Special Development Fund) or
  whether it needs no fund at all (a transformer goes to KSEB). It drafts the proposal.
- **Closing the loop.** Months later, the person who reported the problem is told it became a
  sanctioned work with a number.
- **Lapse alarms.** Unspent money that is about to expire is flagged in December and January, not
  discovered in March.

### Rail B: Presence (requests for the member's time, name or signature)

This rail has never been built anywhere and is where an office wins or loses its reputation.

- **Referral letters, with care.** Three grades of letter, the weakest by default. A background
  check ("diligence file") before any letter. Every letter numbered and retrievable years later.
  Repeat requests are detected.
- **Invitations and greetings.** The promise is a warm, specific reply within 48 hours, never a
  promise to attend. The reply is one of: attend, send a representative, or send a message.
  Malayalam wording is written and approved by a person, not freely generated. Deaths and illness
  go on a separate, faster path. Print-ready cards.
- **Appointments and inaugurations.** The office controls the member's time. People see their
  place in the queue. Requests are grouped by panchayat into each trip.

### Rail C: Outbound (the office telling people things)

- Scheme alerts to people who are eligible.
- Updates on works to the ward affected.
- Monsoon and disaster warnings.
- A one-page monthly constituency report.

### The three demo screens

1. **The constituent's phone.** A person sends a WhatsApp voice note. Within a minute it is
   transcribed, classified, placed in a ward, matched to the asset, checked for duplicates, sent
   to the right authority and given a tracking number. There are three cases to try: a complaint,
   an invitation and a scheme alert.
2. **The member's phone.** What the MLA sees in the car between programmes: letters waiting for
   signature, matters stuck too long with a department, invitations needing a decision, money at
   risk of lapsing, and a **visit brief** before arriving somewhere. The brief lists who is
   waiting, what was promised to each of them, and what is pending in that ward.
3. **The office desk.** The staff's daily screen: today's queue, invitations, referral letters, a
   ward map and works and funds. Every item must have a next date and a named owner, and items
   that go quiet escalate on their own. The map also flags wards that have gone silent.

### What the office produces without retyping

Letters to departments and collectorates; draft Assembly questions when casework has failed; cards
for blessings, congratulations, condolences and regrets; the monthly report; the visit brief.
Everything in both Malayalam and English.

### Safeguards built into the design

- Caste, community and similar data is collected **only** to find people the schemes they are
  owed, with consent naming the scheme. The system can answer "who qualifies for this scheme" but
  can never list, filter or export people by community or religion.
- **There is no party affiliation field anywhere, and there never will be.**
- Every look at sensitive data is logged.
- Whoever funds the system sees nothing of the constituents' messages.
- The data belongs to the office, not the person, with a handover if the member changes.
- Built to India's Digital Personal Data Protection Act, 2023. Outbound messages freeze
  automatically during election periods.

## 7. The plan and the open questions

**How the first constituency would start:**

1. Two to three weeks on the ground building the register of every school, anganwadi, health
   centre, road, transformer, water scheme and local organisation.
2. A working demonstrator on invented data, before any commitment.
3. Then the office runs on it.

**Versions:**

- **V1:** bilingual intake with visible status, ward map, civic issues and the fund router,
  invitations and appointments with the reply window, referral letters with the diligence file,
  the monthly report.
- **V2:** sending each matter to the right authority with drafted documents, a ledger of promises,
  turning failed casework into Assembly questions, targeted outbound messages.
- **V3:** the visit brief, a public dashboard, an annual record.

**Six questions we asked the MLA office** (still open):

1. Is a 48-hour reply to every invitation realistic for an office of that size?
2. Are three grades of referral letter, defaulting to the weakest, too strict?
3. How many staff sit at the desk, and should the screens default to Malayalam or English?
4. Which constituency first: rural, urban or mixed?
5. Is there a fourth kind of work we have missed?
6. Should the pitch open with the constituent's phone or with the fund router?

**Two items Thothica is handling:** checking the fund rules against current government orders before
building the fund router, and a legal opinion before building referral letters that involve
foreign funders.

## 8. What is in this repository

| File | What it is |
|---|---|
| `HANDOFF.md` | This file. |
| `README.md` | A short pointer to this file and the live page. |
| `index.html` | The whole proposal web page, including the three demos. One file. |
| `Thothica-MLA-constituency-operations.pdf` | The same proposal as a shareable PDF deck. |
| `ideas/` | A folder for your ideas. See `ideas/README.md`. |
| `.claude/launch.json` | A setting that lets Claude open the page on a computer for preview. You can ignore it. |

Two things that are **not** in here, to avoid confusion:

- The "track record" section of the page describes other Thothica projects (for example a
  development-funds portal for another state). That work lives elsewhere and is confidential.
- A Kerala flood project (the Pamba river film) was once worked on in the same folder. It is a
  separate project and was deliberately kept out of this repository.

## 9. For Claude: how to help Mr. Siraj

You are helping Mr. Siraj, who is not a programmer, understand this proposal and contribute ideas.
Adnan at Thothica owns the repository and will build whatever is agreed.

- **Explain in plain language.** No jargon without a one-line explanation. Use examples from the
  demos (the ward 12 transformer, Lalitha's housing application, the ₹41 lakh lapse alarm).
- **Be honest about status.** Nothing in this repository is a working system. The demos are
  browser mockups on invented data. Do not describe any feature as live.
- **The source of truth is `index.html`.** The PDF repeats it. If this file and `index.html`
  disagree, `index.html` wins; say so.
- **When Mr. Siraj has an idea**, help him turn it into a short note in `ideas/`, following the
  template in `ideas/README.md`. Say which rail (A, B or C) it belongs to, or whether it is a new
  rail. Check it against the safeguards in part 6. If an idea would need data about caste,
  religion or party, or would let anyone see who complained about what, point that out plainly.
- **Do not edit `index.html` or the PDF.** Those are the proposal as sent. Changes go through
  Adnan. Add new files in `ideas/` instead.
- **Saving and sharing an idea:** save the note in `ideas/`, then commit it on a new branch and
  open a pull request to `main` on GitHub, so Adnan can see it and reply. If Mr. Siraj prefers,
  he can simply send the note to Adnan instead.
