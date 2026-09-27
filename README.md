# DataFrame.fit for Cursor

Remote MCP connector for [DataFrame.fit](https://dataframe.fit) - review Garmin activities, recovery, nutrition, races, and the training plan from Cursor. With permission, rename sessions, edit the plan, log food, and push workouts to Garmin Connect.

## Install

### One-click

[![Add to Cursor](https://cursor.com/deeplink/mcp-install-dark.svg)](cursor://anysphere.cursor-deeplink/mcp/install?name=DataFrame.fit&config=eyJ1cmwiOiJodHRwczovL2RhdGFmcmFtZS5maXQvYXBpL21jcCJ9)

### Marketplace / plugin

Install this plugin from the Cursor Marketplace, or clone this repo into `~/.cursor/plugins/local/dataframe-fit` and reload Cursor.

### Manual `mcp.json`

```json
{
  "mcpServers": {
    "DataFrame.fit": {
      "url": "https://dataframe.fit/api/mcp"
    }
  }
}
```

## Sign in

1. Cursor opens DataFrame in the browser.
2. Sign in with Google if needed.
3. Choose what Cursor may view or change (View starts on; Create or update and Garmin push stay off until you tick them).
4. Return to Cursor. Do not paste an access token into chat.

Docs: [https://dataframe.fit/mcp](https://dataframe.fit/mcp) · [Connect AI assistants](https://dataframe.fit/support/connect-ai-mcp) · [Privacy](https://dataframe.fit/privacy)

## Reviewer test account

For marketplace review, use the seeded Google account (MFA disabled):

- Login: [https://dataframe.fit/login](https://dataframe.fit/login) → Sign in with Google
- Email: `dataframereview@gmail.com`
- Password: provided in the marketplace submission form (not stored in this repo)
- Account includes ~35 days of sample activities, recovery, plan, and nutrition (no live Garmin tokens)

## What the server can do

- Activities: list, detail, quality blocks, rename (if allowed)
- Training plan: read, create, update, delete, push to Garmin (if allowed)
- Wellness / recovery KPIs and home summary
- Nutrition read/write, races, calendar, gear, preferences

Each assistant connection is separate. Revoke Cursor under DataFrame **Settings → Connections** without affecting Claude or ChatGPT.
