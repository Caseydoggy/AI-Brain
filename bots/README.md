# Bots

Every bot works for the one broker who owns this brain, on the broker's own Grok account. Each bot
has a folder here with three files:

- `job.md`: what the bot is for, which tools and skills it uses, where its onboarding stands, and
  how the broker likes working with it.
- `onboarding.md`: how the bot gets ready to work on its first run.
- `routines.md`: the routines it can offer, and the ones that are set up.

| Name in Grok | Brain name | What it does |
|---|---|---|
| Inbox Manager | `inbox-manager` | Keeps the inbox under control: what needs the broker, replies in their voice, flags |
| Daily Brief | `daily-brief` | A short rundown in the chat: the day ahead, the end of the day, the week ahead |
| Calendar Watch | `calendar-watch` | Watches the calendar, preps client meetings, books and moves meetings |
| Boss Lady | `chief-of-staff` | Coordinates the other bots, reads their logs, hands them work, and helps with priorities and projects |

Each bot keeps its own name in Grok up to date here: when the broker renames it, it changes its
row. A bot the broker makes later adds its own row ("A new bot" in [[brain/joining]]). If the broker
asks you to make one, see "Making a bot for the broker" in the same file.

## Where two jobs meet

- **An email asks for a meeting:** the Inbox Manager offers only free times it read in the
  connected calendar. No calendar connected: it asks the broker for times instead (in a routine
  run, it flags the email). Once a time is agreed, it passes it to Calendar Watch to book.
- **Rundowns of the day and the week** are the Daily Brief's. It reads the other bots' logs, so
  every bot logs as it goes.
- **A meeting or a call worth remembering:** whichever bot has the notes writes the summary, after
  checking that no other bot already did ([[skills/meeting-summary]], [[skills/call-summary]]).
- **Boss Lady coordinates the other bots:** it reads their logs and messages them by their
  name in Grok. Inbox work goes to the Inbox Manager, calendar work to Calendar Watch, and
  rundowns of the day and the week to the Daily Brief. Boss Lady never does those jobs itself
  and never changes the other bots' files.
- **Before you offer a routine,** check the other bots' `routines.md`, so the broker never pays
  twice for the same thing.

To hand work to another bot, message it by its name in Grok, in one message with everything it
needs. You can only reach bots on the broker's own account. If the broker has no bot for that job,
tell the broker what needs doing instead. The bot that gets the message handles it as a hand-off
("Routine runs and hand-offs" in `AGENTS.md`).

## What gets saved

Replies, prep notes, lists and briefs are shown in the chat or written in the broker's own tools,
not saved in the brain. The brain keeps your log line, and the summaries of meetings and calls.
