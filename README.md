# Family Meal Planner Skill

A practical Claude skill for generating cost-optimized weekly meal plans and monitoring grocery spending for families with tight budgets.

Built for busy parents who want realistic meal planning without the fluff.

---

## What This Skill Does

When you ask for a meal plan, this skill will:

1. **Ask clarifying questions** about your household, budget, stores, and constraints
2. **Generate a realistic 7-day meal plan** optimized for batch cooking
3. **Build a consolidated grocery list** organized by store section
4. **Estimate costs transparently** with pricing sources and inflation buffering
5. **Monitor spending** against your budget (if you provide actuals)
6. **Suggest adjustments** if costs drift or constraints change—without rationalizing

---

## Quick Start

### Using in Claude.ai

1. **Download this repository** (Code → Download ZIP, or clone it)
2. **Reference the skill** when chatting with Claude: "I have this meal planner skill—let me use it to plan meals"
3. **Ask for a meal plan:** "I need a meal plan for a household of 3 with a $600/month budget"
4. Claude will ask setup questions → You answer → You get a meal plan with grocery list and cost estimates

### Using with Claude API

1. **Clone this repo:**
   ```bash
   git clone https://github.com/[your-username]/family-meal-planner.git
   cd family-meal-planner
   ```

2. **Load the skill in your Claude session** by copying `SKILL.md` and the `references/` folder into your project

3. **Call Claude with the skill context:**
   ```python
   # Example: Read SKILL.md and pass as system context when calling Claude API
   with open('SKILL.md', 'r') as f:
       skill_context = f.read()
   
   # Include in your Claude API prompt
   messages = [
       {
           "role": "user",
           "content": f"{skill_context}\n\nCreate a meal plan for a family of 4 with a $800/month budget."
       }
   ]
   ```

---

## File Structure

```
family-meal-planner/
├── README.md                         (This file)
├── SKILL.md                          (Main workflow & core logic)

├── CONTRIBUTING.md                   (How to contribute)
├── .gitignore
└── references/
    ├── cost-estimation.md            (Pricing, inflation, budget monitoring)
    ├── store-comparison.md           (Store selection & cost optimization)
    └── batch-cooking-strategies.md   (Crockpot, freezing, portions)
```

### Core Files

**SKILL.md** (~350 lines)
- Setup questionnaire (10 key questions to capture constraints)
- 7-step meal planning workflow
- Constraints-first framework
- Pragmatism checklist

Read this first. It's complete on its own and references the other files as needed.

**references/cost-estimation.md**
- How the 10% inflation buffer works
- Pricing sources and dating best practices
- Cost adjustment workflows (if over budget)
- Budget variance analysis for actuals tracking

Read if: You want to customize cost calculations, understand pricing methodology, or track spending over time.

**references/store-comparison.md**
- Store evaluation framework (Walmart vs. Trader Joe's vs. Costco, etc.)
- Cost-per-item comparison logic
- Multi-store shopping strategies
- Store-strength mapping template

Read if: You have multiple stores available and want to optimize which to shop at.

**references/batch-cooking-strategies.md**
- Crockpot meal patterns (shredded protein, stew, pulled meat, ground meat)
- Sunday prep workflow with time budgets
- Freezer-friendly recipes
- Portion planning for toddlers (ages 1–4)
- Time-saving shortcuts

Read if: You want batch cooking guidance or have young children.

---

## Core Philosophy

This skill is built on five principles:

1. **Lead with constraints.** Before recommending anything, understand the household limits (time, money, appetite, available stores, dietary needs).

2. **Ask before drafting.** Don't assume context. The setup questionnaire prevents wasted iterations and creates better plans.

3. **Pivot fast.** If a constraint changes mid-planning ("Costco is too expensive"), immediately reframe the plan. Don't defend the original suggestion.

4. **Show your math.** Costs, variances, adjustments, and portion sizes should be transparent and traceable.

5. **Pragmatism over perfection.** If batch cooking requires 4 hours and you only have 2 hours available, that's OK—shift to simpler meals or buy shortcuts.

---

## Customization & Regional Variants

The skill is designed to be customized for your location and preferences.

### For Your Region

1. **Store names:** Edit `references/store-comparison.md` to list stores in your area (replace Walmart, Trader Joe's, etc.)
2. **Pricing sources:** Update store websites/apps you use for price research
3. **Local chains:** Add grocery chains specific to your region (e.g., Tesco for UK, IGA for Australia)

### For Your Household

1. **Batch cooking:** If you prefer 30-min meals, the skill will adapt when you indicate limited prep time in the setup
2. **Dietary needs:** Provide specific restrictions in setup (allergies, vegetarian, keto, etc.)
3. **Budget:** Any budget works; the skill scales to your targets
4. **Toddler ages:** Portion and texture recommendations adjust by age

### Contributing Variants

If you customize this skill for your region (e.g., Canada, UK, Australia), consider contributing:
- Regional store comparisons
- Local pricing benchmarks
- Regional grocery chains

Create a new folder (e.g., `regional-variants/canada/`) and submit a PR. See [CONTRIBUTING.md](CONTRIBUTING.md).

---

## Example Scenarios

### Scenario 1: Busy Parent, One Stop
**Constraints:** Household of 3, $600/month budget, Walmart only, 3 hours/week for prep

**What the skill does:**
- Optimizes recipes for Walmart's strengths
- Suggests batch-cooking meals that fit 3 hours
- Builds a Walmart-only grocery list
- Estimates costs using Walmart pricing

**Result:** One-stop shopping, realistic for your time, fits your budget.

---

### Scenario 2: Budget-Conscious Multi-Store Shopper
**Constraints:** Household of 4, $800/month budget, Costco + Trader Joe's + Walmart available, 4 hours/week for prep

**What the skill does:**
- Identifies cheapest store for each ingredient (Costco for proteins, TJ for produce)
- Suggests 2-store shopping strategy (saves 15% vs. one-stop)
- Builds separate lists per store
- Adjusts for Costco bulk sizes and membership fee

**Result:** Optimized shopping across stores, maximum savings.

---

### Scenario 3: Parent with Toddler
**Constraints:** Household of 3 (including 18-month-old), $500/month budget, batch cooking, need toddler-friendly meals

**What the skill does:**
- Plans batch-cooked proteins (shredded chicken, ground beef)
- Sets aside plain portions for toddler before seasoning
- Adjusts textures and portions by age
- Flags safe finger foods vs. choking hazards

**Result:** One batch of cooking feeds whole family with appropriate adaptations.

---

## FAQ

**Q: Do I need YNAB or expense tracking to use this?**
A: No. The skill works great without actuals. If you track spending (YNAB, spreadsheet, etc.), the skill can compare actuals to estimates and flag variances.

**Q: What if I don't have time for batch cooking?**
A: The skill will pivot to quicker meal options. Just indicate your available prep time in the setup questionnaire.

**Q: Can I use this for dietary restrictions (vegetarian, keto, allergies)?**
A: Yes. The setup questionnaire specifically asks about restrictions, and the skill adapts all recommendations.

**Q: What if my stores aren't Walmart/Trader Joe's/Costco?**
A: The skill is flexible. Just tell it which stores you have access to. Customize `references/store-comparison.md` for your region if you want.

**Q: How often should I use this?**
A: Weekly (to plan the upcoming week) or monthly (to batch plan and freeze). The skill handles both.

---

## Contributing

Found a bug? Have a suggestion? Want to add regional variants?

See [CONTRIBUTING.md](CONTRIBUTING.md) for guidelines.

---

## Use This Skill

Feel free to use, modify, and share this skill however you like.

---

## Support

- **Questions about using the skill?** Open an issue.
- **Want to improve the skill?** Fork it, customize it, and submit a PR.
- **Having trouble?** Check the reference files (`references/`) for deeper dives on specific topics.

---

**Last updated:** March 2026
