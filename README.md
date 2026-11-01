# Whiskers

Whiskers plans your family's meals with you. It keeps a cookbook you share, builds a week's meal plan from it, turns the plan into a shopping list with an estimated cost, and keeps each person's food diary against their calorie and macro targets. Plans, recipes and shopping lists show up as interactive views in the chat.

## What this plugin contains

- **The Whiskers connector** (`.mcp.json`): the remote MCP server at `https://whiskers.fogx.dev/mcp`. You sign in with a fogx account (OAuth).
- **The `whiskers` skill** (`skills/whiskers/SKILL.md`): how to plan a week, save and import recipes, log food, share with your family, show views, and how to file a bug report when something fails.

The plugin runs no code on your computer, has no hooks and no commands.

## What it sends and fetches

Everything goes to the Whiskers server at `https://whiskers.fogx.dev` over the connector, and only when a tool is called:

- What you ask Whiskers to store: recipes, meal plans, shopping lists, food diary entries, nutrition targets, who you share with and invites, food preferences, and bug reports you agree to file.
- Links you ask it to import a recipe from: the Whiskers server fetches that page or video.
- Food searches go from the Whiskers server to Open Food Facts and USDA FoodData Central. Shopping-list prices come from the Whiskers server's own lookups at a supermarket (Knuspr), made with no data of yours. Some features (reading food descriptions and photos, importing recipes, translating list items) send the text or image to an AI model provider on the server's side.

Whiskers does not read your chat history, memory or files. Privacy policy: https://whiskers.fogx.dev/legal/privacy. Terms: https://whiskers.fogx.dev/legal/terms.

## Try it

- "Plan dinners for next week from my cookbook and make the shopping list."
- "Import this recipe into our cookbook: https://www.chefkoch.de/rezepte/..."
- "Import this Instagram video: https://www.instagram.com/reel/..."
- "I had two eggs and a slice of rye bread for breakfast. How am I doing today?"
- "Show me this week's meal plan."

## Support

Email fogxdev@gmail.com, or ask Claude to file a bug report through Whiskers (`feedback_submit`).
