# PlateWeek: Spec

**Plan the week's meals, and the shop writes itself** · #8 of 16 · Wave 1: Daily keepers · Used: Weekly · Medium · Revenue potential: Medium · Home & Household · Source: New (Claude) + ChatGPT (absorbs BasketBuddy)

## One-liner

Drag meals onto days, reuse your own meal library, and get the week's shopping list built automatically (and sent straight to BasketBuddy). Set a weekly food budget and see the estimated cost.

## Problem / audience

- **Who it's for:** Households trying to cut food waste, save money and end the 'what's for dinner?' question.
- **The problem it solves:** Deciding meals every day is draining and leads to waste and takeaways.
- **Example:** On Sunday a user plans five dinners from their library and gets one shopping list grouped by aisle.

## MVP features (ship with only these)

1. Weekly planner: drag meals to days
2. Personal meal library with ingredients
3. Auto-generated shopping list
4. Weekly food budget estimate
5. Shared shopping list with running total and aisle order (from BasketBuddy)

## Not in MVP

- Share the plan with a household (sync)
- Leftovers mode
- Send the list to BasketBuddy

## Monetisation

| Model | Detail |
|---|---|
| Free | One week ahead and 20 meals, with ads |
| Premium | £2.99/month: unlimited meals, plan further ahead, sharing, budgets |

Prices are starting points; test before committing. **Portfolio premium promise:** free has ads; the moment you pay you get no ads, cloud backup and storage, and sync across your devices, plus this app's extras.

## Retention: The Progression Loop

| Stage | Design |
|---|---|
| Cue | Sunday planning reminder |
| Tiny win | Fill the week |
| Progress | Weeks planned; money and waste saved |
| Share | Weekly meal plan images |
| Next step | Copy last week's plan |
| Cadence | Weekly |

Follow the portfolio guardrails: no guilt-trip notifications, no fake urgency, progress is
never wiped, at most one notification a day by default.

## Animation and tone: five signature animations

**Playful.** Celebrations, confetti, cute characters, satisfying sounds and mild comic reactions. Nothing tragic.

- Meal planned: the plate slides onto Tuesday with a clink
- Full week planned: chef's kiss
- List made: the shopping list unrolls itself
- Under budget: the trolley pops a wheelie
- Leftovers: the lunchbox does a happy dance

**Line we don't cross:** No diet culture or calorie shaming.

## AI

**Light.** Paste a recipe and get its ingredient list. Cheap model, one call per recipe, result saved. (Portfolio rule: plain code first, code does the maths,
cheapest model, shared budget cap, premium-gated.)

## Platform & data

- **Platform:** Expo app; household sharing needs Supabase.
- **Data:** On the device; sync for sharing.
- **Backend:** AI proxy for recipe parsing; shared data once household sharing is added. Premium backup and sync use the shared portfolio backend (see the master repo's HOSTING.md).
- **Stack:** shared portfolio foundation (Expo, PostHog, RevenueCat, AdMob, shared Progression Loop module).

## Growth engine

- **Content pillars:** Cheap meal plans; Batch cooking; Food waste
- **Shareable output:** Weekly meal plan images

## Risks

Combining ingredients and units across recipes takes care. Avoid nutrition or health claims.

## Launch checklist

- [ ] Name checked on the App Store, Play Store and a trademark search
- [ ] MVP features done and tested
- [ ] Progression Loop wired (cue, tiny win, progress, milestone, next step)
- [ ] Privacy policy and terms
- [ ] Landing page
- [ ] Analytics wired (D1/D7/D30 retention)
- [ ] Payments / ads wired
- [ ] Added to the Growth & Maintenance Engine as an app config
