# Whiskers

Whiskers plans a household's meals. It keeps the household's shared cookbook, builds a week's meal plan from it, turns the plan into a shopping list (and, with a connected Knuspr account, a grocery cart), and keeps each person's food diary against their calorie and macro targets. Plans, recipes and shopping lists show up as interactive views in the chat.

## What this plugin contains

- **The Whiskers connector** (`.mcp.json`): the remote MCP server at `https://whiskers.fogx.dev/mcp`. You sign in with a fogx account (OAuth); the first sign-in creates a household for you.
- **The `whiskers` skill** (`skills/whiskers/SKILL.md`): how to plan a week, save and import recipes, log food, manage a household, show views, and how to file a bug report when something fails.

The plugin runs no code on your computer, has no hooks and no commands.

## What it sends and fetches

Everything goes to the Whiskers server at `https://whiskers.fogx.dev` over the connector, and only when a tool is called:

- What you ask Whiskers to store: recipes, meal plans, shopping lists, food diary entries, nutrition targets, household names and invites, preferences, and bug reports you agree to file.
- Links you ask it to import a recipe from: the Whiskers server fetches that page or video.
- Food searches go from the Whiskers server to Open Food Facts and USDA FoodData Central; with a Knuspr account connected, product searches and the cart go to Knuspr. Some features (reading food descriptions and photos, importing recipes, translating list items) send the text or image to an AI model provider on the server's side.

Whiskers does not read your chat history, memory or files. Privacy policy: https://whiskers.fogx.dev/legal/privacy. Terms: https://whiskers.fogx.dev/legal/terms.

## Try it

- "Plan dinners for next week from my cookbook and make the shopping list."
- "Import this recipe: https://www.chefkoch.de/rezepte/..."
- "I had two eggs and a slice of rye bread for breakfast. How am I doing today?"
- "Show me this week's meal plan."

## Support

Email fogxdev@gmail.com, or ask Claude to file a bug report through Whiskers (`feedback_submit`).
