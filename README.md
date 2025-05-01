# Stork-Auto-Bot
By Sabirusman 
Installation
Clone the repository:
git clone https://github.com/airdropinsiders/Stork-Auto-Bot.git
Navigate to the project directory:
cd Stork-Auto-Bot
Install dependencies:
npm install
Configure your credentials (see Configuration section below)
Configuration
Easy Setup with account.js
The bot now uses a account.js file for credentials.

Edit the generated accounts.js file with your credentials:
export const accounts = [
  { username: "email1", password: "pass1" },
  { username: "email2", password: "pass2" }
];
Replace username and password with your Stork Oracle account credentials. just add new line if you wanna run many accounts

Run the bot :

node index.js
Optional: Proxy Configuration
To use proxy servers for distribution of requests:

Create a proxies.txt file in the project root
Add one proxy per line in any of these formats:
HTTP proxies: http://user:pass@host:port
SOCKS proxies: socks5://user:pass@host:port
Usage
Start the bot with:

node index.js
The bot will:

Authenticate using your credentials from account.js
Fetch signed price data at regular intervals
Validate each data point
Submit validation results to Stork Oracle
Display your current statistics
Advanced Configuration Options
In your config.json file, you can adjust:

stork.intervalSeconds: How often the validation process runs in seconds (default: 5)
threads.maxWorkers: Number of concurrent validation workers (default: 1)
