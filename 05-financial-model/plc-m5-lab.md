# Master Product Financials & Strategic Bets, Module 5 Lab

## Make your evaluation and funding decision
- **What assumption is doing the most work? If this number is 20-30% off, what changes?:** Individual-to-team conversion. a 25% relative miss on this one number is the entire distance between "funded initiative on track" and "kill criterion triggered."
- **What is the structural problem in this case? Look past the headline numbers for something that does not hold up on closer inspection.:** The CAC and payback figures don't reconcile, and once you try to make them reconcile, the unit economics get meaningfully worse than presented.
- **Is the kill criterion complete and actionable? Does it name the consequence, or hand the decision back to the room?:** No, it correctly names a threshold but not a consequence, which means it leaves the decision to the room rather than making one.
- **Your verdict: FUND / FUND WITH ONE CONDITION / DO NOT FUND. If a condition, name it; otherwise explain in one sentence.:** Fund with one condition. Before any capital is released, the kill criterion must be rewritten to name a specific, binding action, not "reassessed.

## Write your business case
- **The strategic bet. What specific outcome are you backing, who does it serve, and what is the mechanism that connects the product decision to a financial result?:** An 18-percentage-point increase in Day 90–180 return rate (KR1, 22% → 40%) for users who were highly engaged in their first 90 days and have since gone quiet, achieved by making the product demonstrably "remember" what helped that specific person, rather than prompting them on a fixed schedule. It serves the maintenance-phase user defined in the strategy, who is someone who already resolved their acute crisis, isn't in an active mental-health episode, and is quietly deciding whether Fable still has a place in their life. 

Personalized, contextually triggered check-in → user perceives it as relevant/remembered rather than generic or intrusive → voluntary re-engagement increases without notification fatigue (KR1 moves without the notification-volume cost) → a meaningful share of returners stay engaged through the 6-month mark → premium subscriptions that would have lapsed are retained (KR2) → retained premium ARR that would otherwise have churned off the books.
- **The assumptions. List the assumptions your case rests on, then rank them: which one, if wrong, most changes your conclusion?:** 1. Personalization based on historical usage reads as "remembered," not "recycled" or stale. The user has to feel understood, not just re-shown old content.	This is the one that, if wrong, collapses the entire bet to zero not a smaller win, a null result. Every other assumption is about execution quality; this one is about whether the core mechanism works at all. Nothing downstream of it survives if it's false.
2. Contextual/need-triggered timing is technically achievable without defaulting to a fixed cadence. This is the caveat named directly in the rock.	If this fails, the build doesn't go to zero; it goes to the wrong shape. Engineering under time pressure reverts to "daily" or fixed-interval prompting because it's easier to ship, which is exactly the streak mechanic already ruled out. This is the most dangerous assumption to get wrong precisely because failure here can look like success on KR1 while quietly violating KR3 and the hard no.
3. The clinical veto approves the mechanism without materially narrowing what can be personalized. A clinical-safety-driven restriction on how much history can be surfaced, or how directly it can reference a user's past distress, could blunt the "remembered" effect enough to undercut assumption #1 not kill it, but weaken it below a useful threshold.
4. Lapsed users are receptive to any contact at all, even well-designed contact. Some fraction of the cohort has mentally "closed the loop" on Fable and will treat any prompt as unwanted regardless of quality. Caps the realistic ceiling on conversion even if the mechanism works perfectly on the receptive portion of the cohort; this bounds the size of the win, not whether it exists.
5. Enough usage history exists per user to personalize meaningfully. Users with sparse or short acute-phase engagement may not have a clean enough signal. Limits the addressable share of the cohort, similar to #4: a scope/scale constraint, not a mechanism-validity constraint.
- **The expected return. What does the bet generate and when? Express it at unit level (per customer) and at scale (what volume hits target).:** There is no dollar figure anywhere in this rock, only percentage-point KR movements.
Value per successfully retained user = Premium ARPU/month x incremental months retained
- **The kill criterion. Name the specific metric, threshold, timeline, and financial consequence that tells the team to stop. Actionable, not a conversation.:** Early / Leading Indicator (Week 8, before a full KR1 read is even possible)

Metric: Opt-out rate and negative-sentiment flags on the check-in prompts themselves, measured directly, not inferred from downstream return behavior.
Threshold: If opt-out/complaint rate exceeds a defined ceiling e.g., 2x the baseline notification opt-out rate or if the clinical veto has not approved a shipped version by week 8.
Consequence: The trigger-timing mechanism is stopped and rebuilt before any further rollout and engineering does not proceed to wider release on the current cadence logic. This tier exists specifically to catch Assumption #2 failing silently the "became the streak mechanic we ruled out" risk before it has a chance to contaminate the KR1 data six months later.

## Stress-test and finalize
- **Paste your finalized business case here.:** Rock #6: AI-Generated Check-In Prompts
Business Case One-Pager:  v2, post CFO stress test
$388.8K
ARR Protected
Base case, Yr 1
10.5 mo
Payback
vs. 12-mo hurdle
18 pts
KR1 Target Lift
22% → 40%
2 Gates
Kill Criteria
Wk 8 + Wk 26

THE BET
Increase Day 90–180 return rate (KR1: 22% → 40%) for high-engagement users who have gone quiet, by making the product demonstrably "remember" what helped them, not prompting on a fixed schedule. This is a retention save-play against an already-monetized cohort, not an acquisition play: value comes from ARR protected, not ARR created.
RETURN MODEL
Target cohort
40,000 high-engagement, now-lapsed users / yr
Premium ARPU
$15/month
Baseline → target 6-mo retention
48% → 65% (KR2)
Project cost (eng + design + clinical)
$340,000
ARR protected, base case
$388,800  →  10.5-month payback

LOAD-BEARING ASSUMPTION
Personalization must read as "remembered," not "recycled." This is binary if false, the bet is null, not smaller,  so it cannot be sensitized by percentage. It is tested directly by the Week 8 gate below, not modeled financially.
SENSITIVITY: CLINICAL NARROWING (THE CORRECT 20–30% TEST)
Scenario
ARR Protected
Payback
vs. 12-mo Hurdle
Base case
$388,800
10.5 mo
Clears
Clinical narrows 20%
$311,040
13.1 mo
Modest miss
Clinical narrows 30%
$272,160
15.0 mo
Fails hurdle

Even at 30% degradation, ARR protected stays positive; the 12-month payback hurdle is what actually breaks, not the return itself.
KILL CRITERIA
Tier 1:  Week 8
Opt-out/complaint rate > 2× confirmed baseline, or clinical veto not approved. → Trigger mechanism stopped & rebuilt. One re-attempt cycle only.
Tier 2:  Week 26
Incremental lift vs. control < 8 pts, or ARR protected < $200K. → Trigger-system expansion paused; differentiator claim formally downgraded pending re-justification.
