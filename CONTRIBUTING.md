# Contributing

Thanks for your interest in improving the Family Meal Planner skill!

## How to Contribute

### Reporting Issues
Found a bug or have a suggestion? Open an issue and include:
- **What you were doing** (e.g., "asked for a meal plan for family of 3")
- **What happened** (e.g., "cost estimate was way off")
- **What you expected** (e.g., "accurate estimate within 5%")
- **Your context** (household size, budget, available stores, if relevant)

### Suggesting Improvements
Have an idea to make the skill better? Open an issue with:
- **The problem** (e.g., "batch cooking section doesn't cover instant pots")
- **Your suggestion** (e.g., "add instant pot meal patterns to batch-cooking-strategies.md")
- **Why it matters** (e.g., "instant pots are faster than crockpots for busy parents")

### Customizing for Your Region
If you've adapted the skill for your area, consider sharing:
- Updated store comparison data for your region
- Local pricing benchmarks
- Region-specific stores or grocery chains

Create a new branch or folder (e.g., `regional-variants/canada/` or `regional-variants/uk/`) and submit a PR.

### Improving Documentation
Spotted unclear wording or missing examples? PRs are welcome:
- Typo fixes
- Clearer explanations
- Additional examples
- Better formatting

## Guidelines

1. **Keep it practical.** The skill is designed for busy parents with tight budgets. Suggestions should solve real problems, not add complexity.

2. **Show your work.** If suggesting a new feature, include an example of how it would work in practice.

3. **Test in context.** If you update a reference file, test it with a realistic scenario first.

4. **Respect the philosophy.** The skill leads with constraints, asks before drafting, and pivots fast. Changes should reinforce (not undermine) this approach.

## Development Tips

### Testing Changes Locally
1. Copy the skill files to your Claude environment
2. Ask Claude to test the skill against your scenario
3. Share feedback on what worked/what didn't

### File Structure
- **SKILL.md** — Main workflow (keep under ~500 lines; reference files for deeper dives)
- **references/** — Detailed guidance on specific topics
- **README.md** — Getting started guide

If a reference file exceeds 300 lines, consider adding a table of contents.

### Updating References
When updating a reference file:
- Keep examples realistic and actionable
- Show the math for calculations (cost estimates, portion sizes)
- Include edge cases (e.g., "What if you don't have freezer space?")
- Link back to relevant sections in SKILL.md

## Code of Conduct

Be respectful. Assume good intent. We're all trying to make family budgeting easier.

---

Questions? Open an issue or start a discussion!
