Subject: [Office behaviour 1/2] Levels, XP, badges and learning notes

This is the first of two optional emails (behaviour 1 and 2) that I sent to myself, to go with the three "[Office style" emails. The style emails say how the agent office looks. These two say how it behaves, so that the office feels alive. I know your office already has its own agents and logic, so treat these as a menu: read both, tell me which parts clash with what already exists and which you would add, then wait for my go. Do not remove or rename anything that already works. If a number or rule here conflicts with a rule I gave you earlier in this project, ask me.

The idea: every agent in the office grows. Each one has a level, earns experience points (xp) in two ways, keeps a short list of things it has learned from my answers, and earns a few badges. The office should show this clearly but quietly, as a small tag on the agent's speech bubble, a progress bar on its card, and a short celebration when it levels up.

XP RULES (use these exact rules, they were agreed deliberately)
1. Two kinds of xp. Activity xp: +1 for each answer I give to an agent, or that the orchestrator or the project manager relays to it on my behalf. Quality xp: +3 when an output of the agent is accepted by me untouched, +1 when it is accepted after one correction, and 0 after more than one correction. Quality xp is judged by a human or by an automated checker, never self-scored by the agent that did the work.
2. Total xp is activity xp plus quality xp. Every 10 total xp is one level. Level = 1 + floor(total / 10). So Lv1 at 0 xp, Lv2 at 10, Lv3 at 20, and so on. Progress towards the next level is total mod 10, shown out of 10.
3. Rules are only ever appended. When a rule changes, existing xp is carried forward and never reset. If you ever see every agent at Lv1 after a rule change, something was reset by mistake: check that levels use the TOTAL, not quality xp alone.
4. Streak: count how many outputs in a row were accepted untouched. Show a small flame and the number beside the level tag once the streak is 2 or more. A correction resets it to 0.
5. Stored per agent: xp (activity), qxp (quality), relayed (how many of the activity points were relayed), untouched (count accepted untouched), corrected (count accepted after one correction), streak, a bio line, a list of learnings (each with a date and one line of text), goals, and the last updated time. Seed the stored values from what the office already records; never invent history.
6. An agent's card shows: a level tag, a progress bar (8 pixels high, dark 2-pixel border, cream track, green fill), the text "n/10 xp to Lv(n+1) and total xp in total", then a second line "Activity xp a (r relayed), Quality xp q, accepted untouched u, after one correction c, streak s", and a one-line reminder of the two rules.
7. Learnings: when I answer an agent, it writes one line about what it learned from that answer. The card shows the latest four, newest first, under the heading Bio. A short line, not a paragraph.
8. Controls on the card, for me only: a box to type the learning, a button "+1 activity xp and save learning" with a tick box "relayed", a button "Accepted untouched +3" and a button "After one correction +1". Saving updates the agent's record and the office redraws.

BADGES (small pills on the card: yellow background #fff3a8, 2-pixel dark border, rounded fully; locked badges are dashed and faded)
- First card done (a tick): at least 1 finished board card.
- Five cards done (a star): at least 5 finished cards.
- First answer (a speech icon): at least 1 activity xp.
- Ten answers (a chart icon): at least 10 activity xp.
- Level 5 (a bolt): level 5 or more.
- An hour of work logged (a stopwatch): the agent's finished and open cards add up to 60 or more minutes of recorded AI time.

LEVEL-UP MOMENT
When an agent's level goes up while the page is open, its speech bubble switches for about 4 seconds to a pale yellow (#fff4b0) bubble that reads, for example, "HL: star Lv4!" and a line is added to the office's activity ticker: "Name grew to Lv4!". Nothing else interrupts.

LEVEL AND NEXT LINES
Every agent's speech bubble, while it is working, shows two lines. Line one: its short tag, its level as "Lv3", the streak flame if any, a colon, then what it is doing now, cut to about 18 characters. Line two, smaller and grey: "next:" and what it will do next, cut to about 20 characters. When the viewer selects the agent, the cut lengths grow to 60 so the full text shows. These two lines were the part of the office I liked most.

THE ACTIVITY TICKER AND A DAILY RULE
Keep a short activity ticker under the picture with the newest event first (for example "Name met Name to pitch an idea" or "Name grew to Lv4!"). A standing rule for the team: every agent keeps at least three suggested actions ready each day, and the list of things waiting on me holds at most five items.

Please confirm you have received behaviour 1, say what already exists in your office that overlaps, and wait for me to say go. Do not change anything yet.
