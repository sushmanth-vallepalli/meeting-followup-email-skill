---
name: meeting-followup-email
description: Turns rough meeting notes into a ready-to-send follow-up email with decisions, action items (owner + real due date) and open questions. Use when someone pastes meeting notes, call notes, a standup summary or a transcript and asks for a follow-up email, recap mail, "mail the action items" or "send this to the team", even if the notes are messy shorthand or mixed with Telugu/Hindi words.
---

# Meeting follow-up email

Turn messy meeting notes into a short, clear follow-up email that the sender can paste into Gmail or Outlook and send with almost no edits.

## Step 1: Read the notes and pull out four things

- **Meeting facts:** topic, date, who attended, and who is sending (the note-taker, often written as "me").
- **Decisions:** only things the notes show were agreed or confirmed ("final", "confirmed", "approved", "going with", "ok ayyindi"). Ideas that were only discussed are NOT decisions.
- **Action items:** a task, who owns it, and when it is due.
- **Open questions:** things raised but not settled, or waiting on someone.

## Step 2: Action item rules

- One task per line. Start with a verb: "Send…", "Fix…", "Check…".
- If the same task appears more than once in the notes, list it once.
- **Owner:** use the name as written in the notes, with a capital first letter. If nobody is named, write **Owner needed**. Never guess an owner.
- **1:1 meetings:** when the email goes to the one other person who was in the meeting, write the sender's tasks as "Me" and the reader's tasks as "You".
- **Due date:**
  - If the notes give a date, use it.
  - If they give a relative day ("tmrw", "by friday", "next tuesday", "EOD") and the meeting date is in the notes, turn it into a real date, like "Thu 19 Nov". "Next <day>" means the first such day after the meeting.
  - If the meeting date is NOT in the notes, keep the words as written ("by Monday"). Do not invent a date.
  - If a task is tied to an event ("for the demo"), write "Before <event> (<date if known>)".
  - Otherwise write **Date needed**.

## Step 3: Clean the language

- Notes may mix English with Telugu or Hindi, use shorthand (tmrw, EOD, w/, pls, ppl) or have typos. Write the email in plain, polite, professional English.
- Copy names, product names, ticket numbers, amounts and numbers exactly. Don't round, convert or add currency symbols that aren't in the notes.
- Leave out personal details that are not the team's business: health, leave reasons, salary, family matters, personal phone numbers. If someone is unavailable, at most say "Kiran is out on Thursday", without the reason.
- Leave out side chatter, jokes, and status updates that need nothing from anyone (like "already raised a ticket").

## Step 4: Write the email in exactly this format

Use plain text with simple bullets and numbers, not a markdown table (tables break when pasted into email).

```
Subject: Follow-up: <topic> – <meeting date, if known>

Hi <"all" for a group, or the person's first name for a 1:1>,

<One sentence: thanks + what the meeting was about.>

Decisions
- <decision>

Action items
1. <Action> – <Owner> – <Due>
2. ...

Open questions
- <question> (<who is checking, if named>)

Next meeting: <day/date, only if the notes mention one>

Please reply if I've missed anything or got an owner or date wrong.

Thanks,
<sender's name from the notes, otherwise [Your name]>
```

- Skip any section or line that has nothing in it. Never write "None".
- If nothing was decided, add one line after the opening sentence: "We didn't finalise anything yet; next steps are below."
- Keep the email under 200 words. No filler like "I hope this email finds you well".
- Never add tasks, decisions, people or dates that are not in the notes.

## Step 5: Add a short note for the sender (below the email)

After the email, add a line `---` and then **Check before sending:** with a bullet for every "Owner needed" or "Date needed" item, every date you converted from a relative day, and anything you left out on purpose (like a private detail). If there is nothing to check, skip this part.
