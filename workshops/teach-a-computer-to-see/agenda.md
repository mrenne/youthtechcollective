# Teach a Computer to See — Workshop Agenda

**Format:** 90-minute hands-on workshop
**Ages:** 12–17 (see the facilitator guide for adjusting between 12–13 and 14–17)
**Group size:** 8–16 participants, working in pairs
**Devices:** 1 laptop or Chromebook with a webcam per pair, plus 1 for the facilitator connected to a projector
**Tool:** [Google Teachable Machine](https://teachablemachine.withgoogle.com/) (free, browser-based, no account or install)

## Learning goals

By the end, participants can:

1. Explain that machine learning means a computer learns patterns from **examples** (training data), not from rules someone wrote.
2. Train, test and improve their own image classifier.
3. Show how bad or unbalanced training data makes an AI fail, and connect it to real-world AI bias.
4. Design a model that solves a real problem, and judge whether it is reliable enough to use.

## Run of show

| Time | Segment | What happens |
|---|---|---|
| 0:00–0:10 | **Welcome and hook** | Name tags and pairs. Facilitator demos a pre-trained "thumbs up / thumbs down / nothing" model on the projector, then breaks it live (for example, it calls a coffee mug "thumbs up"). Ask: *"Nobody wrote rules for this. So how does it decide, and why did it just fail?"* |
| 0:10–0:20 | **How machines learn (unplugged)** | "Spot the rule" game: show 6 made-up creatures labeled A or B. Teens work out the hidden rule, then find that a second pattern fits too (a shortcut the data accidentally taught). Introduce **classes**, **training data**, **predictions**, **confidence** and **shortcut learning**. |
| 0:20–0:40 | **Build 1: Rock–Paper–Scissors** | Guided step by step on the projector. Each pair builds a 3-class model (rock, paper, scissors) with about 30 webcam images per class, trains it and tests it. |
| 0:40–0:50 | **Break the model** | Pairs try to fool their model: swap hands, change the background, change the lighting, use the other partner. Then they record an "accuracy score" out of 10 tries. Debrief connects to real cases of AI bias. |
| 0:50–0:55 | **Break** | Facilitator hands out challenge briefs. |
| 0:55–1:15 | **Build 2: Solve a problem** | Each pair picks a challenge brief (or pitches their own) aimed at a real user, then builds a 2–4 class model. Required: a "nothing / background" class, a test on another pair, and an accuracy score. |
| 1:15–1:25 | **Showcase** | Gallery walk: half the pairs demo while the other half visit, then swap. Visitors try to fool each model and judge whether it's reliable enough for its intended user. |
| 1:25–1:30 | **Wrap-up** | Three takeaways (below), a 3-question exit survey and the take-home sheet. |

## Three takeaways to say out loud at the end

1. **AI learns from examples.** What you show it is what it learns, including shortcuts you didn't mean to teach.
2. **Bad data makes bad AI.** If the examples are missing people, places or situations, the AI gets those wrong, and in the real world that affects real people.
3. **You can build this.** You just trained an AI in 20 minutes. The people who decide what data goes in are the ones who shape how AI behaves, and that can be you.

## Related files

- [materials.md](materials.md): what to buy and what the partner provides
- [facilitator-guide.md](facilitator-guide.md): setup, script, troubleshooting
- [handouts.md](handouts.md): challenge briefs, take-home sheet, survey
