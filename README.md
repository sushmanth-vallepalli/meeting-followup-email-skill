# Meeting Follow-up Email (AI skill)

Paste your rough meeting notes and this skill turns them into a ready-to-send follow-up email with decisions, action items (with owners and real due dates) and open questions. Use it right after any team sync, 1:1 or planning call.

It works even when the notes are messy: shorthand, typos, or English mixed with Telugu/Hindi.

## What it does that a plain "summarize this" doesn't

- Lists every action item as **Action – Owner – Due**, and writes **Owner needed** / **Date needed** instead of guessing.
- Turns "tmrw", "by friday", "next tuesday" into real dates when the meeting date is in the notes.
- Leaves out private details (health, salary, leave reasons) that shouldn't go to the whole team.
- Removes duplicate tasks and side chatter.
- Uses plain text instead of tables, so it pastes cleanly into Gmail or Outlook.
- Adds a short **Check before sending** list for you, under the email.

## Example

**Input** (messy notes from a team sync; names are made up):

```
team sync - 18 nov (wed)
ppl: ravi, priya, me (sush), kiran joined late

- login page bug inka undi, ravi fix chestha annadu by friday
- client demo next tuesday ki confirm ayyindi
- priya - UI mockups pampali client ki, tmrw EOD
- payment gateway razorpay or stripe?? decide cheyyaledu, kiran will check pricing
- kiran ki fever undi so thursday leave
- db backup weekly ga cheyyali - evaru chestharu??
- demo ki laptop + hdmi ready cheyyali
- ravi: login bug fix friday ki
- budget 45k approved for hosting (yearly)
```

**Output** (what the skill produced):

```
Subject: Follow-up: Team sync – Wed 18 Nov

Hi all,

Thanks for joining today's team sync on the login bug, the client demo and the payment setup.

Decisions
- The client demo is confirmed for Tue 24 Nov.
- A hosting budget of 45k (yearly) is approved.

Action items
1. Fix the login page bug – Ravi – Fri 20 Nov
2. Send the UI mockups to the client – Priya – Thu 19 Nov, end of day
3. Check pricing for Razorpay and Stripe – Kiran – Date needed
4. Set up weekly database backups – Owner needed – Date needed
5. Get the laptop and HDMI cable ready for the demo – Owner needed – Before the demo (Tue 24 Nov)

Open questions
- Payment gateway: Razorpay or Stripe? (Kiran is checking pricing)

Please reply if I've missed anything or got an owner or date wrong.

Thanks,
Sush

---
Check before sending:
- #4 and #5 have no owner, and #3 and #4 have no due date. Please fill these in.
- I turned "tmrw", "by friday" and "next tuesday" into Thu 19 Nov, Fri 20 Nov and Tue 24 Nov, counting from Wed 18 Nov.
- I left out the reason for Kiran's Thursday leave because it's a private health detail.
- The login bug was mentioned twice in the notes, so it's listed once.
```

## What I changed after testing

I tested the skill on three fresh sets of notes (a Telugu-English team sync, a 1:1 with a manager, and a brainstorm where nothing was decided) and fixed the instructions each time the output slipped:

1. **Duplicate tasks** – the login bug showed up twice → added "list a repeated task once".
2. **Private details** – a teammate's fever went into the team email → added a rule to leave out health, salary and leave reasons.
3. **Vague dates** – "by friday" means nothing a week later → relative days now become real dates when the meeting date is known (and stay as written when it isn't).
4. **Broken tables** – markdown tables showed as `| pipes |` in Gmail → switched to plain numbered lines.
5. **1:1 emails** – "Owner: Meena" reads oddly in an email to Meena → 1:1s now say "Me" and "You".
6. **Lost next meeting** – "meet again thursday" was dropped from the brainstorm → added a "Next meeting:" line.

## How to install

The skill is just the `meeting-followup-email` folder with its `SKILL.md` inside. Download this repo (green **Code** button → **Download ZIP**), unzip it, then add the folder to the AI tool you use:

- **ChatGPT:** add it from **Plugins → Skills**, then call it with `@meeting-followup-email`.
- **Codex:** copy the folder into `~/.codex/skills/`, then call it with `$meeting-followup-email`.
- **Claude Code:** copy the folder into `~/.claude/skills/` and restart, then call it with `/meeting-followup-email`.
- **Any other tool:** paste the contents of `SKILL.md` into a new chat, then paste your notes and ask it to follow the file exactly.

Once it's installed, you can also just paste your notes and ask for a follow-up email; the tool will pick the skill on its own.
