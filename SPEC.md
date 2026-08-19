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

## Open questions for the product owner (content she has not provided yet)

1. **HEALTH / MEDICAL** — no Control/Not/Steps/Fears pool was provided. Currently wired to the generic pool.
2. **Fears lists** ("What are you afraid will happen?") for **BEING ALONE** and **RELATIONSHIP/BREAKUP** —
   currently free-text only (alone) / minimal reuse of her earlier date items (relationship).
3. **Dating / relationship** is one picker row per §3, but the pools separate DATE from RELATIONSHIP/BREAKUP —
   implemented as one extra tap ("A date / meeting someone" vs "A relationship — a message, a reply, a breakup"). Confirm.
4. **Smaller steps** — only her authored reductions plus "the previous step on the same ladder" are offered;
   otherwise the user writes their own smaller version. Does she want a full smaller-step table per situation?
