Laptop Finder Automation (n8n + Telegram)
This project is an automated workflow built with n8n that identifies laptops under a specific budget (e.g., 99k) based on a custom prompt, organizes the data into a spreadsheet, and delivers the results directly to a Telegram bot.

🚀 How It Works
The workflow follows a 4-step logic:

Trigger/Prompt: Initiates the search based on a specific criteria (e.g., "Find laptops under 99k").

Data Processing: Uses JavaScript (Code Node) to filter and format the laptop data.

Sheet Generation: Organizes the filtered results into a structured format (Google Sheets or Excel).

Telegram Delivery: Sends the final data/file to a Telegram chat using a bot created via BotFather.

🛠️ Tech Stack
Automation: n8n.io

Messaging: Telegram Bot API

Logic: JavaScript (Node.js)

Bot Management: BotFather (for API Token) & User Info Bot (for Chat ID)

📋 Prerequisites
Before importing the workflow, ensure you have:

An active n8n instance.

A Telegram Bot Token from @BotFather.

Your Chat ID (obtained via @userinfobot).

⚙️ Setup Instructions
1. Telegram Bot Setup
Message @BotFather on Telegram and create a new bot using /newbot.

Copy the API Token provided.

Message your new bot and then check @userinfobot to get your Chat ID.

2. n8n Configuration
Add a Telegram Node to your n8n canvas.

Create new Credentials using your API Token.

In the Chat ID field of the node, enter your unique ID.

3. JavaScript Logic
The custom JS node processes the search query to ensure only laptops fitting the "99k" criteria are included in the final sheet.