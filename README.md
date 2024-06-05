# TelegramTemplate
A serverless telegram bot template

Prereqs

1. Telegram Bot Token from @botfather: https://t.me/botfather

2. Install Vercel CLI: https://vercel.com/docs/cli

3. Install NGROK https://ngrok.com/download

Local Development 

1. Clone Project

2. Set Environment Variable 
    Create a .env file in the root directory and add the following content.
TELEGRAM_BOT_TOKEN=<TELEGRAM_BOT_TOKEN>

Set the provided TOKEN from Telegram Bot.
Obtain External Domain
Enter the following content in the terminal.

vercel dev

> Vercel CLI 30.0.0
> Ready! Available at http://localhost:3000
Open ngrok to obtain a publicly accessible URL, then enter the following content in another terminal.

ngrok http 3000
Set Webhook
Finally, set up the webhook and copy the following URL

https://api.telegram.org/bot<TELEGRAM_BOT_TOKEN>/setWebhook?url=<Webhook_URL>
Replace the content with your own TOKEN and webhook URL.

TELEGRAM_BOT_TOKEN
Webhook_URL
Note that when setting the webhook URL, it should be DOMAIN name + '/api/webhook' to correspond to the path of the webhook. Once you have made the necessary modifications to the above content, open a blank page in your browser and paste it to submit.

Deployment
Deploy with Vercel CLI
Enter the following content in the terminal.

vercel
It will be automatically deployed to Vercel.

Environment Variable
Go to Vercel DashboardDashboard – Vercel

After locating the recently deployed project, configure the environment variables.

Set your own bot token inside.

KEY	VALUE
TELEGRAM_BOT_TOKEN	<TELEGRAM_BOT_TOKEN>
Webhook
After completing the deployment, you will obtain a URL provided by Vercel. Simply reconfigure the webhook.

https://api.telegram.org/bot<TELEGRAM_BOT_TOKEN>/setWebhook?url=<Webhook_URL>
<TELEGRAM_BOT_TOKEN> corresponds to the bot's TOKEN, and <Webhook_URL> corresponds to the Vercel URL + '/api/webhook'. Once you have made the necessary modifications to the above content, open a blank page in your browser, paste it, and submit.
