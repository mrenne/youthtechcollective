# Teach a Computer to See — Facilitator Guide

Everything you need to run the workshop: prep, a segment-by-segment script, troubleshooting and follow-up. Pair it with [agenda.md](agenda.md), [materials.md](materials.md) and [handouts.md](handouts.md).

---

## 1. Two weeks before

- [ ] **Do a device test at the partner site.** This is the most important step. On one of *their* devices, on *their* Wi-Fi, open https://teachablemachine.withgoogle.com/, start an Image Project, turn on the webcam and train a 2-class model. If the camera is blocked or the site is filtered, ask the partner's IT person to allow it, or plan to bring the backup webcams and your own laptop.
- [ ] Confirm the headcount, the age range and how many devices are available. Plan for 1 device per pair.
- [ ] Confirm that a staff member will be in the room the whole time. You should never be alone with participants.
- [ ] Ask whether the partner has its own photo/media release. Use theirs if so.
- [ ] Ask the partner to print the handouts, or print them yourself.
- [ ] Ask them to share the event on their calendar, newsletter and social media. Send them a 2-sentence description and a photo.

## 2. Day before

- [ ] Build and save your **demo model** (thumbs up / thumbs down / nothing) on your own laptop. You can save it to your Google Drive from the menu, or export it to get a shareable link. Use only *your own* face and hands in demo models.
- [ ] Pack the kit bin: backup webcams, demo objects, challenge briefs, name tags, markers, sticky notes, handouts, an HDMI adapter for your laptop and a power strip.
- [ ] Prepare the 6 "spot the rule" creature pictures and 2 test pictures (see section 4, segment 2). Hand-drawn or a slide is fine.

## 3. Setup (arrive 30–45 minutes early)

1. Connect your laptop to the projector and open your demo model.
2. On each participant device, open Chrome to https://teachablemachine.withgoogle.com/train/image (the image project page) so pairs can start right away.
3. Check that each device has power and that the room is well lit. Light from the front is best, and teens should sit with their backs away from bright windows.
4. Put out name tags and markers, and pair up teens as they arrive. Try to pair a 12–13-year-old with a 14–17-year-old, and an experienced coder with a beginner.

---

## 4. Segment-by-segment script

Text in *italics* is suggested wording. Put it in your own words.

### Segment 1: Welcome and hook (0:00–0:10)

- Introduce yourself in one sentence and explain what you'll build today.
- Live demo: show thumbs up, thumbs down and nothing to the camera while the bars on screen change. Then hold up a mug or a phone and let it misclassify confidently.
- *"I didn't write a single rule for this. I showed it about 30 pictures of each. So why does it think my mug is a thumbs up?"* Take a couple of guesses. Don't resolve it yet.
- Quick round: *"Where does AI make decisions about you?"* Teens usually name face unlock, social media feeds, content moderation, school proctoring software and photo tagging.

### Segment 2: How machines learn, unplugged (0:10–0:20)

- Show 6 made-up creatures labeled **A** or **B**. All the A's have spots, and *also* all happen to be blue. The B's have no spots and come in other colors.
- Ask pairs to write down the rule. Most will say "spots." Then show a **blue creature with no spots** and a **red creature with spots**, and ask them to classify both.
- Reveal: the data supports *two* rules, so a model can't tell which one you meant. This is **shortcut learning**, and it's exactly why the mug fooled the demo model.
- Name the vocabulary and write it on the board: **training data**, **classes**, **prediction**, **confidence**, **shortcut learning**.

### Segment 3: Build 1, Rock–Paper–Scissors (0:20–0:40)

Go step by step on the projector and wait until every pair is done before moving to the next step.

1. Click **Image Project**, then **Standard image model**.
2. Rename "Class 1" to **Rock**, "Class 2" to **Paper**, and click **Add a class** for **Scissors**.
3. Under Rock, click **Webcam**. Hold up a fist and **hold the record button** to collect about 30 images while moving your hand around a little (closer, farther, tilted).
4. Repeat for Paper and Scissors.
5. Click **Train Model**. *Keep this browser tab open and in front while it trains.* Switching tabs can pause training.
6. Test it in the **Preview** panel and watch the confidence bars.

Tip: one partner holds up hands while the other clicks. They swap roles in Build 2.

### Segment 4: Break the model (0:40–0:50)

Challenge: *"You have 5 minutes. Try to fool your AI."* Suggestions:

- Let the *other* partner test it
- Use the other hand
- Change the background, or stand in front of a busy wall
- Hold your hand far away
- Show it nothing, or your face

Then each pair runs a quick **accuracy test**: 10 tries by the partner who *didn't* train it, counting how many are correct.

Debrief (5 minutes):

- *"What made it fail?"* The usual answer: it only learned from one hand, one background and one light setting.
- *"How would you fix it?"* More variety in the training data, plus a "nothing" class.
- Real-world link: research audits such as MIT's *Gender Shades* project (2018) found that commercial face-analysis systems had much higher error rates for darker-skinned women than for lighter-skinned men. The cause was largely who was and wasn't in the training data. Ask: *"Your rock-paper-scissors model failing is funny. When is a model failing not funny?"* Good examples are hiring tools, medical imaging, policing and school proctoring.

### Segment 5: Break (0:50–0:55)

Hand out the challenge briefs (see [handouts.md](handouts.md)).

### Segment 6: Build 2, solve a problem (0:55–1:15)

- Each pair picks a brief or pitches their own idea. Their idea needs your OK: no classifying people by appearance (see the safety notes below).
- Requirements: 2–4 classes, **always** a "nothing / background" class, a test by another pair, and a 10-try accuracy score.
- Ask them to name who the model is *for* and what would happen if it got something wrong.
- Coaching questions to ask instead of giving fixes:
  - *"What does it predict when nothing is there?"*
  - *"Which two classes get confused? What's the shortcut it might be using?"*
  - *"Would you trust this if it were for a real person? What accuracy would you need?"*
- **Fast finishers (any of these):**
  - Build an audio or pose version of the same idea.
  - Export the model (**Export Model → Upload**) to get a shareable link, then open the provided p5.js or JavaScript sample code and change what happens on each prediction. Only do this with models trained on objects or gestures, never faces.
  - **micro:bit level-up:** hand them a micro:bit V2 and point them to https://createai.microbit.org/. They train a *motion* model with the accelerometer and run it on the board. It makes a good bridge to a follow-up physical-computing workshop.

### Segment 7: Showcase (1:15–1:25)

- Split the room: half the pairs stay at their devices to demo while the others visit, then swap after 4 minutes.
- Visitors try to fool each model. Celebrate the clever failures as much as the successes.

### Segment 8: Wrap-up (1:25–1:30)

- Say the three takeaways (see [agenda.md](agenda.md)).
- Hand out the exit survey and take-home sheet, plus certificates if you're using them.
- **Privacy close-out:** *"Before you go, close your browser tab. Your pictures disappear when the tab closes, and that's on purpose."* Then do a quick check of each device yourself.

---

## 5. Troubleshooting

| Problem | Fix |
|---|---|
| "Allow camera" pop-up never appeared, or camera is blocked | Click the camera icon in the address bar and choose Allow. On managed Chromebooks, the partner's IT person may need to allow it. Fall back to backup webcams or upload images instead. |
| Camera is in use by another app | Close video-call apps and other tabs that use the camera. |
| Training seems frozen | Keep the tab in front and wait 1–2 minutes. On slow devices, reduce to about 20 images per class. |
| Model always predicts the same class | Unbalanced data. Make the image counts for each class roughly equal, and add a "nothing" class. |
| Model works for one teen but not the other | That's a teachable moment. Have both partners add images. |
| Page crashed or tab closed | Unsaved work is lost. Rebuilding takes about 3 minutes, so treat it as a speed-run challenge. |
| Wi-Fi drops | Once the page is loaded, training and testing keep working. Just don't refresh the page. |
| Fewer devices than expected | Make groups of 3 with rotating roles: camera operator, clicker and tester. |

## 6. Adapting by age

The 12–17 range covers a big developmental spread, so plan to differentiate inside the room rather than running separate sessions.

- **Ages 12–13:** Keep Build 1 fully guided. Offer the more concrete challenge briefs (Recycling Sorter, Doodle Reader). In the bias debrief, focus on "who's missing from the data?"
- **Ages 14–17:** Speed up Build 1 by giving the steps once, then letting them go. Push the briefs that have a real user and real stakes. In the debrief, introduce *overfitting*, *dataset balance* and *false positives vs false negatives* (for example, which mistake is worse for a smoke-alarm detector?). Offer the export/code and micro:bit level-ups.
- **Experienced coders:** Go straight to the export/code level-up after Build 1, and ask them to help a neighboring pair during Build 2.
- **Mixed groups:** Pair younger teens with older ones, and have them swap the trainer and tester roles between builds.
- **Teen dynamics:** Let pairs pick their own partners when they already know each other. Keep the showcase low-stakes, with no forced presenting. Recognize good testing ("you found a great failure") as much as good models.

## 7. Safety, privacy and inclusion

- **A partner staff member stays in the room the whole time.** You are never alone with a participant.
- **Images stay in the browser.** In the default flow, Teachable Machine trains on the device and doesn't upload images. Don't save participants' models to Drive or export them with their faces in the data. Close all tabs at the end.
- **No appearance-based classes.** Don't allow models that sort people by looks, skin, gender, body or "who's cool." Steer teens toward objects, gestures, pets in photos, recycling and so on. If it comes up, use it as a short teaching moment about why that's a harmful use of AI.
- **Teens who don't want to be on camera** can use objects and drawings for everything. Offer this option to everyone up front so nobody is singled out.
- **Photos for promotion:** take them only of teens with a signed release, and favor shots of hands and screens over faces.
- **Accessibility:** if a participant has limited hand mobility, gestures can be replaced by objects, head tilts or sounds (audio project).

## 8. After the workshop (same day)

- [ ] Write down the attendance count and the age range.
- [ ] Collect the exit surveys or check the Google Form responses.
- [ ] Write 3 notes: what worked, what dragged and what you'll change next time.
- [ ] Ask the partner staff member for a 1–2 sentence quote. These are useful for grant applications and new partners.
- [ ] Send a thank-you email to the partner within 48 hours and propose the next date.
