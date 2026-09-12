---
name: winrate
description: Use this when it is Sunday and the founder asks what the week made. They say "run winrate", "/winrate", "what made money", "which video made money", or "my Sunday numbers". It asks for one number off YouTube Studio and prints one screen, money with no source on its own line. On the founder's yes it writes the Sunday row into squad/content-log.md. It never sends and never estimates a number.
---

# Winrate

**Your work, in one line: read the files the squad already writes, count what the week
brought in and where each piece of it came from, print one screen, and write one row.**
The founder's part: one number off YouTube Studio, one Improve line, one yes.
A run on any other day reads the same week, and the row carries the Sunday's date.

Your first message on a fresh run carries this line, once:

> This skill is a base. Once you have done it your way, tell your squad "update the skill to do it like this."

This skill runs in ANY founder's repo. `.claude/squad-roots.md` is the per-repo instance
file every member-run skill reads first, and its values win over the `squad/` paths below,
which are worked examples.

## The rules

- **Never send.** No message, no email, no post.
- **Never write to the pipeline or the roots file.** One file, one row in it.
- **Never estimate.** A number not in a source does not exist; the brief says so in its
  slot. The views come off the founder's paste, nothing else.
- **Never guess a source.** Money with no source prints on its own line and stays there
  until the founder writes the answer on the row.
- **Never rank pieces by views.** The brief names the piece the money traced to and
  nothing more; the founder decides what to make.
- **Never a second row for one Sunday.**
- No em dashes anywhere.

## 1. The sources

- `squad/content-log.md`: one row per published piece (date, title, link, video id), plus
  the rows under `## Sundays` from earlier weeks.
- `squad/pipeline.md`: one row per person; the source field's second half names what
  brought them (a video, `cold, <list>`, `warm, <how>`); the money field.
- Stripe, Chris's copy only: sales cleared this week. The first payment is the sale; a
  renewal never is; a refund subtracts from the sale it refunds.

**The week** is Monday to this Sunday, dated inside those 7 days. The clock is the roots
file's `timezone` row, else the laptop's.

**Per-video tracing.** Every listing's booking link carries `utm_content=epNN`, and cal.com
shows that on the booking's details page, so a pipeline row whose source names `epNN`
traces to that episode. Its title is in the listing file under `squad/week/` carrying that
link; print the title, and the id off the content log. A money field on a row whose source
second half is blank or reads `source unknown` is **money with no source written next to
it.** It prints on its own line. It is never guessed onto a piece.

**Counting once.** A money field counts the first Sunday it is seen. The earlier rows
under `## Sundays` say what was counted before; read them before adding.

## 2. The views

Only a piece past 7 days has a 7-day number. Name the newest row in the content log dated
8 or more days ago, then stop on one line: "Open YouTube Studio, that video, Analytics,
last 7 days, and paste me the views." Take the number they paste. Never read it off a
connector, never estimate it, never round it.

No piece past 7 days yet: no stop, the brief prints `held` in that slot.

## 3. The brief

One screen, this order, nothing added:

> WINRATE · 2026-09-13
> Shipped: ep03 "I Built a Cold Email Agent" (Tue)
> 7-day views, ep02: 1,240
> Asks this week: 3 · ep02 2 · cold, September list 1
> Money this week: $997 · ep02 $997
> Money with no source written next to it: $0
> The move: make 5 more like ep02, then 10

- Counts only. A percent never prints without its count. Both files empty this week:
  `nothing shipped, nothing in`.
- An ask is a reply or a call that landed this week: a pipeline row dated this week whose
  third field is `interested`, `question`, `objection`, `signed, not paid` or `closed won`.
  Each source prints with its count; a source with nothing prints nothing.
- The money line prints the total first, then each source. The no-source line prints every
  time, `$0` when there is none.

**The move**, one line, decided from the numbers and nothing else:

| The numbers say | The move |
|---|---|
| money with no source | ask each of them where they found you and write it on the row |
| money came from one piece | make 5 more like <piece>, then 10 |
| replies landed, no calls | ask for the 20 minutes and nothing else |
| nothing moved | run the lane |

Then stop: "Type your Improve line, a change or a hold, and I write the row."

## 4. The row

The founder types the Improve line and says yes. Append ONE row under `## Sundays` in
`squad/content-log.md`, the heading added when it is not there:

> date | shipped | 7-day views | asks | money | improve
> 2026-09-13 | ep03 "I Built a Cold Email Agent" | ep02: 1,240 | 3 (ep02 2, cold September list 1) | $997 (ep02) | make 5 more like ep02, then 10

`held` in the views cell when the views held. The improve cell is the founder's line, word
for word. Then one line back: `/bip sunday` closes on this Improve line, and the plan's
week N Measure and Improve cells take the same 2 things.

**Resuming.** No row dated this Sunday under `## Sundays`: run the whole read again, it
takes a minute. A row already there: print it, never a second one, and a new Improve line
rewrites that cell in place. The rule keys on the file, never on what a session remembers.
