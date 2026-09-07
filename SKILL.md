---
name: winrate
description: Use this when it is Sunday and the founder wants to know what the week made. They say "run winrate", "/winrate", "what made money", "which video made money", or "my Sunday numbers". It reads the content log and the pipeline, asks for one number off YouTube Studio, and prints one screen: what shipped, the 7-day views, the asks with their sources, the money with its sources, the money with no source on its own line, and one move. On the founder's yes it writes the Sunday row into squad/content-log.md. It never sends and never estimates a number.
---

# Winrate

**Your work, in one line: read the files the squad already writes, count what the week
brought in and where each piece of it came from, print one screen, and write one row.**
The founder's part: one number off YouTube Studio, one Improve line, one yes.

This skill runs in ANY founder's repo. `.claude/squad-roots.md` is the per-repo instance
file every member-run skill reads first, and its values win over the `squad/` paths below,
which are worked examples. A row reading "(none yet)" is an unanswered field, not an
override: the worked-example path stands.

## The modes, and how they are called

| Mode | The founder says | Beats |
|---|---|---|
| sunday | "run winrate", `/winrate`, "what made money", "which video made money", "my Sunday numbers" | 0, 1, 2, 3 |

One mode. A run on any other day reads the same week; the row carries the date of the Sunday that ends it.

## The run map (where you run, where you STOP)

| Beat | Mode |
|---|---|
| 0 THE SOURCES | AUTO: the roots file, the content log, the pipeline, Stripe when this is Chris's copy |
| 1 THE VIEWS | HUMAN INPUT: the 7-day views of the newest piece 8 or more days old, read off YouTube Studio and pasted. **STOP** until it lands. No such piece yet: no stop, the brief prints `held`. |
| 2 THE BRIEF | AUTO: one screen printed, then **STOP · GATE: the Improve line, typed by the founder** |
| 3 THE ROW | HUMAN INPUT: the Improve line and the yes; then AUTO: one row under `## Sundays` in the content log |

The beat numbers ARE the step numbers below. Two stops, both real: a number only the
founder can see, and a line only the founder can decide.

**Resuming.** The rule keys on the OUTPUTS, never on a session's memory.

| Missing or incomplete | Resume at |
|---|---|
| no row dated this Sunday under `## Sundays` in `squad/content-log.md` | beat 0, the whole read again; it takes a minute |
| a row dated this Sunday is there | done. Print it. Never a second row for one Sunday |
| a row dated this Sunday is there and the founder gives a new Improve line | beat 3, that one field rewritten in place |

## The outputs

1. The brief, printed in chat. One screen, the shape in beat 2. It is not saved anywhere;
   the row is its memory.
2. `squad/content-log.md`: ONE row appended under `## Sundays`, the heading added the
   first time. Columns `date | shipped | 7-day views | asks | money | improve`.

Nothing else gets written. Never the pipeline, never the roots file.

## Beat 0 · The sources

Read these in this order. Paths come off the roots file; the ones here are the worked
example.

| # | Source | Where | What it gives |
|---|---|---|---|
| 1 | the content log | `squad/content-log.md` | one row per published piece (date, title, link, video id), plus the rows under `## Sundays` from earlier weeks |
| 2 | the pipeline | `squad/pipeline.md` | one row per person; the source field's second half names what brought them (a video, `cold, <list>`, `warm, <how>`); the money field; `the-close` writes this row after every reply and every call, so nothing here is typed by hand |
| 3 | the views | YouTube Studio, the founder's own eyes | beat 1 |
| 4 | Stripe, optional | the Stripe connector, Chris's copy only; skipped when absent, one line says so | sales cleared this week. The first payment is the sale; a renewal never is; a refund subtracts from the sale it refunds |

**The week** is Monday to this Sunday. The clock is the roots file's `timezone` row, else
the laptop's. "This week" means dated inside those seven days.

**Per-video tracing.** Every listing's booking link carries `utm_content=epNN`, and cal.com
shows that on the booking's details page, so a pipeline row whose source names `epNN`
traces to that episode. The episode's title is in the listing file under `squad/week/`
that carries that link; print the title, and the id off the content log. A source that
names a title traces to that title's row. A money field on a row whose source second half
is blank or reads `source unknown` is **money with no source written next to it.** It
prints on its own line. It is never guessed onto a piece.

**Counting once.** A money field counts the first Sunday it is seen. The earlier rows
under `## Sundays` say what was counted before; read them before adding.

## Beat 1 · The views

Only a piece past 7 days has a 7-day number. Name the newest row in the content log dated
8 or more days ago, then STOP on one line: "Open YouTube Studio, that video, Analytics,
last 7 days, and paste me the views." Take the number they paste. Never read it off a
connector, never estimate it, never round it.

No piece past 7 days yet: the brief prints `held` in that slot, and this beat ends.

## Beat 2 · The brief

One screen, this order, nothing added:

> WINRATE · 2026-09-13
> Shipped: ep03 "I Built a Cold Email Agent" (Tue)
> 7-day views, ep02: 1,240
> Asks this week: 3 · ep02 2 · cold, September list 1
> Money this week: $997 · ep02 $997
> Money with no source written next to it: $0
> The move: make 5 more like ep02, then 10

Laws of the screen:

- Counts only. A percent never prints without its count next to it.
- Money prints in whole dollars unless the cents are not zero. One currency; a foreign
  amount prints on its own line, labeled, never summed.
- An ask is a reply or a call that landed this week: a pipeline row dated this week whose
  third field is `interested`, `question`, `objection`, `signed, not paid` or `closed won`.
  Each source prints with its count; a source with nothing prints nothing.
- The money line prints the total first, then each source. The no-source line prints
  every time, `$0` when there is none.
- Two empty states: `nothing shipped, nothing in` when both files hold no row this week,
  and `asks in, no money yet` when there are asks and no money.

**The move**, one line, decided from the numbers and nothing else:

| The numbers say | The move |
|---|---|
| money came from one piece | make 5 more like <piece>, then 10 |
| replies landed, no calls | ask for the 20 minutes and nothing else |
| nothing moved | run the lane |
| money with no source | ask each of them where they found you and write it on the row |

More than one line true: money with no source first, then money from a piece.

Then STOP: "Type your Improve line, a change or a hold, and I write the row."

## Beat 3 · The row

The founder types the Improve line and says yes. Append ONE row under `## Sundays` in
`squad/content-log.md`, the heading added when it is not there:

> date | shipped | 7-day views | asks | money | improve
> 2026-09-13 | ep03 "I Built a Cold Email Agent" | ep02: 1,240 | 3 (ep02 2, cold September list 1) | $997 (ep02) | make 5 more like ep02, then 10

`held` in the views cell when beat 1 held. The improve cell is the founder's line, word for
word. One row per Sunday; a new Improve line rewrites that cell in place.

Then one line back: `/bip sunday` closes on this Improve line, and the plan's week N
Measure and Improve cells take the same two things.

## Rules

- **Never send.** No message, no email, no post.
- **Never write to the pipeline or the roots file.** This run touches one file, and one
  row in it.
- **Never estimate.** A number not in a source does not exist; the brief says so in its
  slot. The views come off the founder's paste, nothing else.
- **Never guess a source.** Money with no source prints on its own line and stays there
  until the founder writes the answer on the row.
- **Never rank pieces by views.** At one piece a week there is nothing to rank. The brief
  names the piece the money traced to and nothing more; the founder decides what to make.
- **Never a second row for one Sunday.**
- No em dashes anywhere. The brief and the row are read by the founder.
