---
name: family-meal-planner
description: Generate cost-optimized weekly meal plans for families with tight budgets. Use this skill whenever a user asks for a meal plan, wants to reduce grocery spending, is planning meals for toddlers or young children, needs batch-cooking strategies, or mentions budget constraints. Includes grocery list generation, store-specific shopping recommendations, cost estimation, and budget monitoring against actuals.
tags:
  - meal-planning
  - budget-management
  - grocery-optimization
  - family-finance
  - batch-cooking
compatibility: None (works standalone)
---

# Family Meal Planner

A practical skill for generating realistic, cost-optimized weekly meal plans and monitoring grocery spending against budget targets.

---

## OVERVIEW

This skill helps families plan meals that fit their budget, honor their constraints (dietary restrictions, available time, household size), and actually work for busy parents. It includes:

- **Setup questionnaire** to capture household constraints upfront
- **7-day meal plan generation** optimized for batch cooking
- **Consolidated grocery list** organized by store
- **Cost estimation** with transparent pricing and inflation buffering
- **Budget monitoring** against actuals (YNAB exports, receipt data)
- **Pragmatism-first philosophy** — lead with constraints, pivot immediately when they change

---

## CAPTURE INTENT: THE SETUP QUESTIONNAIRE

**CRITICAL: Never draft a meal plan without asking these questions first.** Answers prevent wasted iterations.

### Household & Appetite
1. How many people? What are their ages? (This determines portion sizes and cooking strategy)
2. Any dietary restrictions, allergies, or strong preferences?
3. Who does the cooking? How much time per week for meal prep? (This determines batch-cooking feasibility)
4. Past meal plan pain points? (e.g., "previous plans made too much food," "toddler won't eat leftovers," "we got bored of repetition")

### Budget & Spending
5. Weekly or monthly grocery budget? (e.g., "$150/week" or "$600/month")
6. Current spending (if available)? (YNAB export, rough estimate, or last month's receipts)
7. Other food spending to monitor? (restaurants, coffee, snacks) — what's the target?

### Stores & Shopping
8. Which stores are available? Which do you prefer? (e.g., Trader Joe's, Publix, Costco, Walmart, local chains)
9. Any store constraints? (e.g., "Costco portions are too large," "Whole Foods is too expensive," "I only shop at one store")
10. Do you have freezer space for batch cooking? Crockpot? Food processor?

---

## MAIN WORKFLOW

### STEP 1: VALIDATE CONSTRAINTS & ASK CLARIFYING QUESTIONS

Before generating anything, review the answers to the setup questionnaire. If any are missing or vague, ask:

- **Household size unclear?** → "I need ages to plan portion sizes. A 2-year-old eats differently than a 6-year-old."
- **Budget missing?** → "What's a comfortable weekly or monthly grocery budget for your household?"
- **Cooking time unclear?** → "How many hours per week can you dedicate to cooking/prep? This determines if crockpot meals are realistic."
- **Stores not specified?** → "Which stores are near you and do you shop at?"

**Do not proceed to Step 2 until you have clear answers.**

---

### STEP 2: IDENTIFY CONSTRAINTS & TRADE-OFFS

Document the top 3–5 constraints that will shape the plan:

**Examples:**
- "Household of 4 (ages 2, 5, adult, adult) → need toddler-friendly proteins and soft textures"
- "Working parent with 4 hours/week for prep → crockpot meals are essential, batch-cooked proteins only"
- "$600/month budget ($150/week) → no specialty products, focus on bulk proteins + seasonal produce"
- "Only Walmart available → optimize for Walmart's strengths (Great Value brand, bulk meat)" 
- "Costco portions too large → need portion-size alternatives for 3-person household"

**Frame constraints neutrally.** Don't say "this is hard." Say "this shapes the plan this way."

---

### STEP 3: GENERATE 7-DAY MEAL PLAN

Create a weekly meal plan that:

1. **Yields 2–3 servings per cook session** — a crockpot chicken recipe feeds dinner tonight + tacos tomorrow + chicken salad on day 3
2. **Prioritizes batch cooking** — Sunday prep yields 3+ dinner components for the week
3. **Reuses ingredients** — if you buy a rotisserie chicken, it appears in 3 meals
4. **Includes toddler adaptations** (if applicable) — soft textures, no added salt, finger-friendly sizes
5. **Builds lunches from dinner leftovers** — don't plan lunches separately; they're built from dinner prep
6. **Flags "boring" repetition** — if the same protein appears twice, space them out or vary the flavor profile

**Format:**
```
SUNDAY PREP (4 hours)
- Crockpot: Chicken thighs (→ dinner Mon, tacos Tue, salad Wed)
- Sheet pan: Roasted vegetables (→ side all week)
- Batch: Rice/grains (→ 3+ dinners)

MONDAY
- Dinner: Chicken + roasted veg + rice
- Lunch (Tue): Leftovers

TUESDAY
- Dinner: Chicken tacos (leftover chicken + fresh toppings)
- Lunch (Wed): Leftover tacos or chicken salad

... etc
```

---

### STEP 4: BUILD CONSOLIDATED GROCERY LIST

**Organize by store section, not by meal.** This prevents duplicate trips and makes shopping faster.

**Format:**
```
TRADER JOE'S
Produce
- Carrots (2 lbs) — $0.89
- Spinach (1 bag) — $1.99
Proteins
- Ground beef (2 lbs) — $7.98
Dairy
- Cheddar cheese (1 block) — $3.49

WALMART
Proteins
- Chicken thighs (3 lbs) — $8.97
Pantry
- Rice (2 lb bag) — $2.18
- Olive oil (large) — $6.47
```

---

### STEP 5: ESTIMATE COSTS & FLAG VARIANCES

1. **Calculate per-ingredient cost** based on store pricing
2. **Apply 10% inflation buffer** to account for price changes (see `references/cost-estimation.md` for methodology)
3. **Sum per store, then total**
4. **Compare to budget target**

**Format:**
```
ESTIMATED TOTAL: $145
- Trader Joe's: $52
- Walmart: $93

BUDGET TARGET: $150/week
VARIANCE: -$5 (under budget ✓)
```

**If over budget:** See `references/cost-estimation.md` for adjustment workflows (swap ingredients, reduce portions, use cheaper stores).

---

### STEP 6: FLAG REUSABLE COMPONENTS & SHOPPING SHORTCUTS

Call out:
- "Rotisserie chicken (Costco) → use for: tacos, salad, quesadillas"
- "Frozen vegetables (cheaper than fresh, same nutrition) → can substitute for fresh"
- "Buy store-brand pasta instead of name brand (saves ~$0.30/box)"

---

### STEP 7: MONITOR ACTUALS VS. BUDGET (If Applicable)

If the user provides YNAB exports or spending data:

1. **Compare category-level actuals** (groceries, restaurants, etc.) against targets
2. **Flag any trending over** in high-risk categories (restaurants, specialty foods, bulk snacks)
3. **Suggest adjustments** (e.g., "Restaurants spending is $80 over budget; next week, batch-cook 2 extra meals")

See `references/budget-monitoring.md` for tracking methodology.

---

## CONSTRAINTS-FIRST FRAMEWORK

**This framework prevents wasted iterations. Follow it religiously.**

### Lead with Constraints, Then Recommend

Always surface the top 3 constraints upfront before showing the meal plan:

❌ **Wrong:** "Here's your meal plan! I picked recipes that are family-friendly and budget-conscious."

✅ **Right:** "Based on your constraints (household of 3, $600/month budget, only Walmart available, 4 hours/week for prep), here's the plan. The main trade-off: you'll see more repetition in proteins to hit the budget."

### Ask About Appetite Capacity Before Suggesting Recipes

❌ **Wrong:** Suggest Costco bulk chicken packages for a family of 2 without confirming portion sizes.

✅ **Right:** "Before I suggest recipes, how much chicken does your household actually eat per week? Costco sells 5-lb packs—is that realistic?"

### Validate Batch-Cooking Time Availability

❌ **Wrong:** Recommend 5 crockpot meals when the user only has 2 hours/week for prep.

✅ **Right:** "You have 3 hours/week. That supports 2–3 batch-cooked proteins and 1 sheet-pan meal. Does that feel realistic?"

### Check Past Plan Failures Upfront

❌ **Wrong:** Suggest a new meal plan without asking why the last one failed.

✅ **Right:** "Your last plan made too much food. Before I draft this one, confirm: are we reducing portion sizes, or would you rather plan for 2 dinners per recipe instead of 3?"

### Pivot Immediately If a Constraint Changes

If the user flags a new constraint mid-planning:
- **Don't rationalize the original suggestion**
- **Don't offer to "make it work anyway"**
- **Pivot immediately and reframe the plan around the new constraint**

❌ **Wrong:** "Costco portions are too large, but you could freeze half..." (rationalizing)

✅ **Right:** "Understood. Costco is off the table. Walmart and Trader Joe's have better-sized packages for you. Let me revise the plan."

---

## PRAGMATISM CHECKLIST

Before presenting any meal plan, confirm:

- ✅ Household size and ages verified
- ✅ Appetite capacity (portion sizes) confirmed
- ✅ Batch-cooking time available and realistic
- ✅ Store selection confirmed (not assumed)
- ✅ Dietary restrictions and preferences checked
- ✅ Budget target clear (weekly or monthly)
- ✅ Cost estimates shown with source and buffer explained
- ✅ Reusable components flagged
- ✅ Toddler/child-specific meals addressed (if applicable)
- ✅ Past plan failures understood and addressed

**If any item is unchecked, ask the clarifying question before proceeding.**

---

## REFERENCE FILES

This skill includes bundled references for deeper dives:

- **`references/cost-estimation.md`** — How inflation buffering works, pricing sources, cost adjustment workflows, budget variance analysis
- **`references/store-comparison.md`** — How to evaluate stores by ingredient category, template for users, cost-per-item comparison logic
- **`references/batch-cooking-strategies.md`** — Crockpot meal patterns, freezer-friendly recipes, time budgets, ingredient reusability, portion planning for toddlers

Read these when:
- A user wants to customize store logic for their area
- Cost estimates are trending over budget
- They need crockpot or freezer strategies
- They want to understand the pricing methodology

---

## TONE & STYLE

- **Be direct.** No fluff. Show your math.
- **Skip flattery.** Users are busy. They want pragmatic solutions.
- **Lead with constraints.** Frame trade-offs honestly upfront.
- **Pivot fast.** If a constraint changes, reframe immediately. Don't defend the original suggestion.
- **Ask before drafting.** Review suggestions with the user first; never assume context.
- **Show work.** When estimating costs or flagging budget variances, show the calculation.

---

## COMMON SCENARIOS

### "Make me a meal plan for $600/month"
→ Ask: Household size? Ages? Cooking time available? Stores near you? Past failures?

### "This plan made too much food last time"
→ Ask: How many days of leftovers felt excessive? Should we target 2 meals per recipe instead of 3? What portion sizes are realistic?

### "I don't have time to batch cook"
→ Ask: How much time do you have? If it's <2 hours/week, batch cooking isn't realistic. Pivot to simpler 30-min meals instead.

### "Costco is too expensive / portions are too big"
→ Don't defend Costco. Immediately offer store alternatives. Flag which ingredients work better at Walmart/Trader Joe's.

### "We went over budget on restaurants last month"
→ Review the YNAB data. Identify patterns (weeknight eating out? Weekend brunch?). Suggest meal-prep solutions that address the specific pain point.

---

## SUCCESS CRITERIA

A meal plan is successful when:

1. ✅ **It fits the budget** (within 5% variance)
2. ✅ **Batch cooking is realistic** given available time
3. ✅ **Household actually eats the food** (no surprises about preferences)
4. ✅ **Portions align with actual appetite capacity** (not too much leftovers, not too little)
5. ✅ **Shopping is simplified** (organized by store, no duplicate trips)
6. ✅ **Ingredients are reused** (not buying 6 different proteins for variety)
7. ✅ **Toddlers/kids are fed well** (appropriate textures, nutrition, appeal)
