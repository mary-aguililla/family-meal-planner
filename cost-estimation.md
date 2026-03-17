# Cost Estimation Reference

How to estimate meal plan costs, apply inflation buffering, adjust for budget overages, and monitor actuals against targets.

---

## INFLATION BUFFERING METHODOLOGY

Grocery prices fluctuate weekly. To avoid under-budgeting, apply a 10% buffer on top of estimated ingredient costs.

### Why 10%?
- **Real-world variance:** Prices vary by location, store, brand, and week
- **Seasonal swings:** Produce costs spike in winter; proteins fluctuate with commodity prices
- **Store differences:** Walmart's eggs cost different from Trader Joe's (even accounting for quality)
- **Conservative baseline:** 10% is a practical safety margin that prevents budget shocks

### How to Apply It

**Step 1: Get ingredient prices**
From store websites, apps (Instacart, Amazon Fresh), or recent receipts. Document the source and date.

```
Chicken thighs (3 lbs) — Walmart — $8.97 — (Jan 15, 2026)
Spinach (1 bag) — Trader Joe's — $1.99 — (Jan 15, 2026)
```

**Step 2: Sum ingredient costs**
```
Subtotal: $145.60
```

**Step 3: Apply 10% buffer**
```
Buffer (10%): $14.56
ESTIMATED TOTAL: $160.16
```

**Step 4: Show the buffer explicitly**
When presenting costs to the user, always show:
- Subtotal (without buffer)
- Buffer amount and percentage
- Final estimate

This transparency prevents "how did we exceed budget?" surprises.

---

## PRICING SOURCES & DATING

Always document where prices come from. Store prices change weekly.

### Best Sources (In Order)
1. **Store website/app** (most current) — Instacart, Amazon Fresh, store apps
2. **Recent receipts** (personal actuals) — most reliable for user's location
3. **Price comparison sites** (secondary) — grocery comparison websites
4. **YNAB/personal spending data** (historical baseline) — for trend analysis

### Dating Prices
Always include the date you pulled prices. If you cite prices from Jan 15, note it:

```
Estimated costs based on prices pulled Jan 15, 2026 from Walmart.com and TJ.com.
Prices updated weekly. Your actual costs may vary by location.
```

If the user comes back a month later, pull fresh prices. Don't reuse month-old estimates.

---

## COST ADJUSTMENT WORKFLOWS

If the plan exceeds budget, don't just say "swap X for Y." Use this workflow:

### Workflow: Over-Budget Plan

**Scenario:** Estimated plan is $165, but budget is $150.

**Step 1: Identify the variance**
```
Budget: $150/week
Estimated: $165/week
Overage: $15 (+10%)
```

**Step 2: Break down costs by category**
```
Proteins: $75 (45% of budget)
Produce: $40 (24%)
Pantry (grains, oils, pasta): $25 (15%)
Dairy/eggs: $15 (9%)
Frozen/other: $10 (6%)
```

**Step 3: Identify adjustment levers (in priority order)**

1. **Protein swaps** (biggest impact, usually 40–50% of budget)
   - Chicken thighs → Ground chicken (same yield, often cheaper)
   - Ground beef → Eggs or beans (1–2 meals/week)
   - Salmon → Canned tuna (same omega-3s, 1/3 the cost)

2. **Reduce protein quantity** (modest impact)
   - Instead of 3 lbs chicken, use 2.5 lbs + add beans to one meal
   - Trade one meat meal for a vegetarian meal (beans, lentils, eggs)

3. **Swap produce** (modest impact)
   - Fresh spinach → Frozen spinach (often cheaper, same nutrition)
   - In-season produce → Out-of-season (cost varies; check current prices)
   - Premium vegetables → Budget staples (carrots, cabbage, celery are cheap year-round)

4. **Buy store-brand pantry items** (small but cumulative impact)
   - Name-brand pasta → Store-brand (save ~$0.30–0.50 per box)
   - Name-brand rice → Store-brand (save ~$0.20 per lb)

**Step 4: Propose specific swaps**

❌ **Wrong:** "You could reduce costs by swapping cheaper proteins."

✅ **Right:** "To hit your $150 budget, swap 1.5 lbs of chicken thighs ($9) for 2 lbs ground chicken ($7). That saves $2. For the other $13, use frozen spinach instead of fresh ($1 savings), and buy store-brand pasta ($0.50 savings across 4 boxes). That brings you to $148 total."

**Step 5: Confirm the swaps with the user**

"Does ground chicken + frozen spinach + store-brand pasta work for you? Or do you want to adjust differently (e.g., add a vegetarian meal instead)?"

### Workflow: Under-Budget Plan

If the plan is under budget, **don't automatically expand it.** Instead:

1. **Show the variance:** "This comes in at $138 (your budget: $150). You have $12 flexibility."
2. **Ask the user:** "Want to add premium items (organic, higher-quality proteins), or keep the savings?"
3. **Offer specific upgrades (if they want them):**
   - Swap conventional vegetables for organic (adds ~$1–2)
   - Upgrade ground beef to grass-fed (adds ~$3)
   - Add a treat food (specialty pasta, good cheese, etc.)

---

## PER-INGREDIENT COST TRACKING

When building a grocery list, show cost per ingredient so users understand where money goes.

### Format

```
PROTEINS (45% of budget)
- Chicken thighs (3 lbs @ $2.99/lb) — $8.97
- Ground chicken (2 lbs @ $3.49/lb) — $6.98
- Eggs (18 count @ $2.50/dozen) — $3.75

PRODUCE (24% of budget)
- Carrots (2 lbs @ $0.89/lb) — $1.78
- Spinach (frozen, 1 bag) — $2.49
- Bell peppers (3 @ $1.50 ea) — $4.50

SUBTOTAL: $145.60
BUFFER (10%): $14.56
ESTIMATED TOTAL: $160.16
```

### Why Show Per-Ingredient Costs?
- Users see where their money goes
- Easy to spot "that's expensive" and adjust (e.g., "pepper is $1.50 each?")
- Transparent; prevents mistrust

---

## BUDGET VARIANCE ANALYSIS

If a user provides actuals (YNAB, receipts), compare against the estimated plan and identify patterns.

### Workflow: Actuals vs. Estimate

**Scenario:** User estimated $150/week, but actuals are $167.

**Step 1: Calculate variance**
```
Estimate: $150
Actual: $167
Variance: +$17 (+11%)
```

**Step 2: Break down actuals by category (if available)**

If you have detailed YNAB data:
```
Estimated vs. Actual (weekly average):

                   ESTIMATE  ACTUAL  VARIANCE
Proteins          $75       $82     +$7 (+9%)
Produce           $40       $45     +$5 (+12%)
Pantry            $25       $26     +$1 (+4%)
Dairy/eggs        $15       $14     -$1 (-7%)
SUBTOTAL          $155      $167    +$12
```

**Step 3: Identify patterns**

- **One-time spikes:** "You bought organic spinach once ($4 extra). That's not recurring."
- **Category overages:** "Produce is consistently over. Either prices spiked, or you bought premium items (organic, local)."
- **Waste:** "You bought 3 chickens but only used 2. That's wasted money."

**Step 4: Suggest adjustments**

❌ **Wrong:** "You went over budget."

✅ **Right:** "You went over by $17. Here's what I see: proteins cost $7 more (likely commodity price movement), and produce cost $5 more (produce was pricier that week, or you bought organic). One-time: specialty cheese (+$3). To get back to $150, either (a) accept the $167 as the new reality and adjust budget, (b) swap proteins next week, or (c) buy less produce variety. What feels right?"

---

## GROCERY INFLATION TRENDS

If a user tracks spending over months, help them spot inflation patterns.

### Workflow: Monthly Trend Analysis

**Scenario:** User provides 3 months of spending data.

```
Month 1 (Jan): $640/month ($160/week)
Month 2 (Feb): $665/month ($166/week)
Month 3 (Mar): $680/month ($170/week)

Trend: +$40/month year-over-year (+6.25%)
Trajectory: $680/month × 12 = $8,160/year
```

**Report:**
"Your grocery spending is trending up ~$1.50/week month-over-month. This could be:
- Commodity price inflation (typical 2–5%/year for groceries)
- Seasonal produce (winter produce costs more)
- Gradual shopping habit change (slightly higher quality items, more variety)

If this continues, plan to increase budget by $10–20/month by Q2. Or, lock in the cheaper proteins/produce before prices climb further."

---

## HANDLING SPECIAL CASES

### Bulk Buying (Costco, Sam's Club)
- Costs are lower per unit, but require upfront commitment and storage
- Only recommend if household size and appetite can consume the bulk before spoilage
- Always ask: "Does your household have freezer space? Can you use 5 lbs of chicken in a week?"
- Compare cost-per-serving, not absolute cost

### Pantry Staples (Oil, Rice, Pasta)
- Buy these in bulk (they don't spoil and take up little space)
- Show the per-serving cost to illustrate savings
- "Bulk olive oil ($15 bottle) costs $0.06/tablespoon vs. $0.15 from a smaller bottle. Worth it if you cook regularly."

### Seasonal Price Swings
- Summer produce is cheap (local, abundant)
- Winter produce is expensive (shipped, stored)
- Canned/frozen vegetables are cheaper and stable year-round
- Show user: "In winter, use frozen vegetables to cut costs. Same nutrition, half the price."

### Organic/Premium Items
- Only recommend if budget explicitly allows
- Show the trade-off: "Organic chicken is $2/lb more. That's $6 extra per week for the 3-lb plan."
- Let user decide if the premium is worth it

---

## COST DOCUMENTATION CHECKLIST

When estimating costs, always show:

- ✅ Source of prices (store name, website, date)
- ✅ Per-ingredient costs (transparency)
- ✅ Subtotal before buffer
- ✅ 10% buffer amount
- ✅ Final estimated total
- ✅ Comparison to budget target
- ✅ Variance explanation (over/under, and why)
- ✅ Store breakdown (if multiple stores)
- ✅ Reusable ingredients flagged (e.g., "bulk chicken → 3 meals")

This checklist ensures transparency and prevents surprises.
