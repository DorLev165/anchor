# Anchor — Binding Product/Clinical Spec (v3)

Authored by the product owner (Dor's aunt), 2026-08-18, translated from Hebrew.
**If anything elsewhere contradicts this document, this document wins.**
Rule for AI/devs: choose and adapt only from the routes and content approved here.
**Never invent new therapeutic content or principles. If content or logic is missing — ask her.**

## 1. Core principle

The goal is NOT to make anxiety disappear, and NOT to teach the user they must calm down first.
First understanding: **"This is anxiety. My body and my thoughts are reacting to anxiety right now."**
It does not mean every thought is a fact, that I'm losing control, or that something dangerous is necessarily happening.
From there: understand what's happening → identify what's in my control → take one small real-world step despite the anxiety.

## 2. Main flow

RECOGNIZE → IDENTIFY → INTERVENE → ACTION → LEARN

Breathing is never a mandatory stage. Inside Recognize you may offer:
"Take one slow breath in through your nose and slowly out through your mouth, if you want."
Never imply you must calm down before you can cope.

## 3. Situation picker (MY ANXIETY IS RISING)

Social situation · Test / school · Presentation / performance · Dating / relationship ·
Work / interview · Flying / travel · Being alone · Health / medical · Difficult conversation ·
Something else · I'm not sure / it came out of nowhere.
Situations chosen in onboarding are shown first.

## 4. RECOGNIZE (keep this message)

"Your anxiety is up right now. That can affect what you feel in your body and what your mind is telling you."

## 5. IDENTIFY — route selection

"What's happening most right now?"
- I'm afraid of what might happen → LOOK AT IT STRAIGHT / WORST CASE
- I keep thinking about something again and again → SPOT THE LOOP
- I'm stuck on something I can't control → CONTROL
- I want to avoid, leave or cancel → AVOIDANCE / ACTION
- I'm not sure → one short clarifying question. The AI must not invent a new therapeutic route.

## 6. LOOK AT IT STRAIGHT / WORST CASE

"What are you afraid will happen?" → "If that actually happened — what could you do next?"
No reassurance ("It won't happen" / "Everything will be fine").
Land on: **"Even if something I don't want happens — I can handle what comes next."**
Coping answers must not automatically reinforce escape or avoidance.

## 7. SPOT THE LOOP

Already thought about this more than once? Any NEW information?
If no new info: "This is the anxiety loop — not a new problem to solve." Don't keep re-analyzing.
Message is not "get the thought out of your head" but:
**"A thought can be there without deciding what you do next."**

## 8. CONTROL

Keep the existing exercise, the gentle "Take another look" correction on wrong sorts, and "Here's the split."
Show ~6 cards per use (3 In My Control + 3 Not In My Control) sampled from a larger
situation-specific pool so the exercise varies between uses.

Content pools (Control / Not in control / One Small Step) — as implemented in `index.html` `SIT`:
SOCIAL, TEST, PERFORMANCE, FLIGHT, DATE, BEING ALONE, RELATIONSHIP/BREAKUP, JOB INTERVIEW,
DIFFICULT CONVERSATION — using her exact lists from the v3 message.
Note e.g. "Feeling completely calm" belongs in **Not** in my control (test, performance).

## 9. AVOIDANCE

"If anxiety wasn't making this decision for you, what would you want to do?" → break it into a small step
(Go to the party → Walk through the door; Complete the test → Read the first question;
Give the presentation → Say the first line; Take the flight → Walk to the gate).
The system must never learn that avoidance is a good solution just because it lowered anxiety short-term.

## 10. ONE SMALL STEP

Nearly every route ends at: "What's one small thing you can do now that's in your control?"
The step must be **specific + immediate + healthy + in the user's control**.
Not reassurance, not repeated checking, not avoidance.

## 11. FOLLOW-UP (must really happen)

Save the step and later ask: **"Did you do your one step?"**
- YES → "You did it — even with the anxiety there. That's what counts." Then:
  "How did it go?" — Easier than I expected / About what I expected / Harder than I expected.
- NOT YET → "Want to make the step smaller?" and offer a smaller version of the same step
  (e.g. Walk in → Walk to the entrance; Stay 10 minutes → Stay 2 more minutes).

## 12. LEARNING / PERSONALIZATION

Per use, store as relevant: situation, anxiety before, main fear/pattern, route used, one small step,
anxiety after, did the user take the step, how it went.
Learn over time which route helps THIS user in THIS situation move forward —
not only what lowered the anxiety number. Anxiety 8 → 7 + went into the date = **success**.

## 13. Rules the system never bypasses

- Thought ≠ fact.
- Never promise the feared thing won't happen.
- Never reinforce reassurance seeking, repeated checking, or avoidance (even if they lower anxiety).
- Never try to make the user "erase" thoughts.
- Calm is not a precondition for acting.
- The AI may pick and adapt from approved routes/content only — never invent new therapeutic principles.

## 14. The one-line product

Recognize "this is anxiety" → understand what anxiety is doing → stop treating every thought as a fact
or every uncertainty as a problem to solve → identify what's in my control → take one small real-world step.
**The goal isn't to make anxiety disappear. The goal is to stop anxiety from choosing your next move.**

---

# v3 completions (2026-08-22) — all previously open content questions answered

## 15. HEALTH / MEDICAL

Work on the anxiety and the uncertainty. **Never tell the user "It's just anxiety" and never state that a
symptom is not medical.** (Implemented: this route overrides the RECOGNIZE second sentence with
"Anxiety can make sensations louder and harder to read. That doesn't settle what any sensation means —
it means anxiety is part of what you're feeling right now.")

- **In my control:** Describing what I'm feeling clearly / Following medical advice I've already received /
  Making an appropriate medical appointment if needed / Choosing whether to keep checking / What I do next.
- **Not in my control:** Knowing with 100% certainty what every sensation means / How quickly a sensation
  goes away / Every sensation my body produces / What a test result will be / What might happen in the future.
- **Afraid will happen:** Something is seriously wrong with me / This feeling means something dangerous /
  The symptom will get worse / A test will show something bad / I won't be able to cope if something is wrong.
- **One Small Step:** Stop checking for the next 10 minutes / Write down my concern once, then return to what
  I was doing / Follow the medical plan I already have / If appropriate, make one appointment instead of
  repeatedly searching or checking / Do one normal activity for the next few minutes.

## 16. Missing fear lists (now provided)

- **BEING ALONE:** Something bad will happen while I'm alone / I'll panic and no one will be here /
  I won't be able to handle how I feel / A sound means someone or something is there / I'll lose control /
  I won't be able to get help if I need it.
- **RELATIONSHIP / BREAKUP:** They won't reply / They're losing interest in me / They'll leave me /
  I said or did something wrong / They're upset with me / The relationship is over /
  I won't be able to handle the breakup or rejection.

## 17. Dating / relationship split — CONFIRMED

After choosing Dating / relationship: **"What is this about right now?"**
→ "A date / meeting someone" | "A relationship / message / breakup" — each leads to its own pool.

## 18. Smaller-step ladders

Principle: **the step gets smaller but stays in the same direction**
(Walk into the party → Walk to the entrance, never → Go home). If there is no good match,
the user writes their own step.

- SOCIAL: Walk in → Walk to the entrance → Stay nearby for 2 minutes · Say hello → Move closer to one person → Make eye contact
- TEST: Start answering → Read the first question → Look at the first question · Work on the next question → Write one thing I know → Read it once
- PERFORMANCE: Start → Get into position → Prepare to begin · Say the first line → Look at the first line → Get ready to say it
- FLIGHT: Board → Walk to the gate → Stay at the gate · Sit and buckle up → Enter the plane → Stand in the boarding line
- DATE: Walk in → Walk to the entrance → Arrive and stay there for a moment · Say hello → Approach → Make eye contact and smile
- BEING ALONE: Stay 5 more minutes → 2 minutes → 1 minute · Continue a normal activity → Start it for 2 minutes → Begin the activity
- RELATIONSHIP: Put the phone down for 10 → 5 → 2 minutes · Don't send another message right now → Wait 10 minutes → Write it without sending
- INTERVIEW: Enter/join the interview → Go to the entrance/join the call → Stay ready to enter · Answer the first question → Listen to it → Say the first sentence
- DIFFICULT CONVERSATION: Start the conversation → Say the first sentence → Prepare/approach · Say what I need to say → Say one part → Write down the first sentence
- HEALTH: Stop checking for 10 → 5 → 2 minutes · Return to a normal activity → Do it for 2 minutes → Start it

Implementation note: a step with no authored rung reduces only by lowering its own minute count
(10 → 5 → 2 → 1); it is never swapped for a different action, and never suggests a bigger step.

**Per the product owner, route content for the MVP is now closed — no further content additions for now.**

## 19. CHECK THE STORY (added 2026-08-24)

Closes a gap from the original idea: whether an anxious thought rests on what is actually happening,
or on an existing belief the person holds about themselves.

**Offered, never automatic**, and only for self-belief / interpretation thoughts —
"People don't like me", "I'm weird", "I'm not good enough",
"Everyone notices something wrong with me", "I always mess things up".

Flow: *"Is this thought based on something that happened right now — or could an old belief about
yourself be shaping how you see it?"* → **What facts seem to support this thought?** →
**What facts don't fit this thought?** → *"A belief can feel true without being the whole picture.
Your mind is giving you one interpretation. The facts may tell a more complete story."*
→ then straight to One Small Step. No further analysis.

Rules:
- **Never tell the user their belief is untrue** — we don't know that. The goal is to separate
  fact, interpretation, and existing belief.
- **It must not become repeated reassurance.** Same thought already checked and no new information
  → back to the loop principle: *"No new information — not a new problem to solve."*
- Not a route every user must pass through — a tool inside the existing engine.
- Stores the chosen belief and the result of the check per session, and counts recurrences
  (`anchor.beliefs`) so recurring self-belief patterns can be surfaced later.
