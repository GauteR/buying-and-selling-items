# Buying and selling (marketplaces) skill

Agent skill for researching items and prices, suggesting listing text from images, and pointing out flaws when buying or selling on marketplaces (e.g. Finn, eBay, Facebook Marketplace, Blocket).

- **Investigate and suggest only**: All output is in chat; the agent never posts or writes to any platform or file.
- **Response language** follows the user's message.
- **When unclear**: The agent asks the user (e.g. marketplace, images, item description) before continuing.

Install as a personal or project skill and use when the user asks about selling, buying, pricing, listing text, or evaluating items for marketplaces.

## Installation

Install with [Skills CLI](https://skills.sh/) (requires Node.js):

```bash
npx skills add gauter/buying-and-selling-skill
```

To install globally (into `~/.cursor/skills/`) without confirmation:

```bash
npx skills add gauter/buying-and-selling-skill -g -y
```

**Alternative (without Skills CLI):** Clone the repo and place it in Cursor's skills directory, e.g. `~/.cursor/skills/buying-and-selling-skill/` (global) or `.cursor/skills/buying-and-selling-skill/` (project).

## Files

- **SKILL.md** – Main instructions (trigger, workflow, template, link to reference).
- **reference.md** – Pricing, description principles, flaws and defects, marketplace tips.

## License

[MIT](LICENSE)
