# DiscordLLM
Setup

1. Install Dependencies

Make sure you have Python installed, then run:

pip install discord.py aiohttp

2. Configure the Bot

Modify the following variables in the script before running it:
Discord Bot Token (from Discord Developer Portal)
Open Web UI API URL (default: http://localhost:8080/api/chat/completions)
Model Name (e.g., deepseek-r1:7b)
Authorization Token (JWT from Open Web UI)

3. Run the Bot

python bot.py


Usage

Send a message in your Discord server:

++ What is the capital of France?

The bot will process the message and return a response from the AI.

Troubleshooting

Bot is not responding?

Ensure you have enabled "Message Content" intent in the Discord Developer Portal.

Double-check your bot token and API authentication.

Verify that Open Web UI is running and accessible.

Check for API errors (401, 400, etc.).

Ensure your JWT Token is valid.

Check if your local API is accessible

Run:

curl -X POST http://localhost:8080/api/chat/completions \
  -H "Authorization: Bearer YOUR_TOKEN" \
  -H "Content-Type: application/json" \
  -d '{"model": "deepseek-r1:7b", "messages": [{"role": "user", "content": "Hello!"}]}'

If you receive a 401 Unauthorized error, ensure your API token is correct.
