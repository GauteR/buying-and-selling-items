---
name: buying-and-selling-marketplaces
version: 1.0.0
description: Investigates items and prices for marketplace buying and selling; suggests listing descriptions from images and points out flaws and prices.
---

# AI Agent Skill for buying and selling items on marketplaces

This skill helps users research items, find prices, and get listing suggestions for marketplaces. All output is in chat only; the agent never posts or writes to any platform or file.

## Trigger scenarios

Use this skill when the user asks to:

- **Create a listing** for an item (user uploads images and optionally describes it; agent identifies item, researches price, produces marketplace-tailored listing – all shown in chat)
- **Research** an item (what it is, typical use, typical prices)
- Find a **good price** (buy or sell)
- **Write or improve listing text** from images and info
- **Assess flaws and defects** (visible damage, wear, missing parts)
- Evaluate whether a listing is good or bad

## Response language

**Always reply in the same language as the user's message** (e.g. Norwegian prompt → Norwegian reply, English → English). Applies to both body text and any template output.

## Investigate and suggest only – never post

- All advice, price suggestions, description drafts and flaw assessments are delivered **in chat** (markdown/text).
- The agent **never posts or writes anything** – no listings, no files, no platform posts. It only investigates and gives suggestions in chat.
- **When something is unclear** (e.g. which marketplace, missing images, vague item description) – **ask the user** before continuing.

## Workflow

1. **Clarify**: Sell or buy? Which marketplace (if given)? Does the user have images or other info? **If anything is unclear** (e.g. missing marketplace, no images, vague item) – **ask the user** before proceeding.
2. **Research**: When needed – use search/context to find typical use, model info and comparable prices; state sources briefly.
3. **Price**: Give a price range or recommendation with short justification (in chat).
4. **Description**: If the user has images – describe the item from the images and suggest listing text **in chat only** (never post or write to file).
5. **Flaws/defects**: List visible or likely flaws from images and description; note impact on price and how to mention them in the listing.

## Use case – create listing from images

When the user asks to create a listing for an item and uploads images (and optionally adds text):

1. **Identify** the object using vision (images) and/or the user's description.
2. **Research** what similar items sell for today (search/context); state sources briefly.
3. **Produce** a full listing tailored to the chosen marketplace (title, description, suggested price, flaws to mention); output **only in chat** – never post or save to file.

The finished listing is shown in the chat so the user can copy and publish it themselves.

## Chat report template

Use this structure (in the user's language) when presenting an assessment. Omit sections that do not apply.

```markdown
## Marketplace assessment

**Summary:** [One sentence: key finding or recommendation.]

**Research / comparable prices:** [Brief: what similar items sell for; sources if relevant.]

**Recommended price (range):** [Amount or range with short justification.]

**Suggested listing text:** [If relevant – title and description draft.]

**Flaws and defects to mention:** [Visible or likely issues; how they affect price and how to phrase them in the listing.]
```

## Additional resources

- For pricing methods, description principles, typical flaws to check, and marketplace tips: [reference.md](reference.md).
