# Cisco Router Scraper Telegram Bot 🤖🕷️

A Telegram bot powered by **Puppeteer** and **Node-Telegram-Bot-API** that automates the collection of Cisco router specifications. Users can trigger the scraper via simple chat commands, and the bot will dynamically gather product listings, crawl for data sheets, and stream PDFs straight into the personal chat.

## 🚀 Features
- **On-Demand Scraping**: Initiated directly from Telegram using the `/start` command.
- **Live Document Streaming**: Automatically generates and streams product logs (`.txt`) and technical specification sheets (`.pdf`) right into your chat bubble.
- **Safe Execution & Stop Flag**: Built-in state control via `/stop` to immediately interrupt running scraper routines if needed.
- **Zero Disk Bloat**: Documents are cleanly generated on-the-fly and fully erased from the host server right after being dispatched to the user.
- **Pre-Render Cleanup**: Removes distracting cookie walls and live chat pop-ups via Puppeteer style injections for pristine PDF printing.

## 🛠️ Tech Stack
- **Node.js** (Runtime environment)
- **node-telegram-bot-api** (Telegram Bot interaction)
- **Puppeteer** (Headless browser automation)
- **dotenv** (Secure environment configuration)

## 📋 Prerequisites
- **Node.js** (v16.0.0 or higher)
- A Telegram Bot Token (generated via [@BotFather](https://t.me))

## 🔧 Installation & Setup

1. **Clone the repository:**
   ```bash
   git clone https://github.com
   cd cisco-router-telegram-bot
   ```

2. **Install project dependencies:**
   ```bash
   npm install
   ```

3. **Configure Environment Variables:**
   Copy the example configuration file and fill in your actual Telegram bot token:
   ```bash
   cp .env.example .env
   ```
   Open the newly created `.env` file and replace `your_bot_token_here` with the token from `@BotFather`.

4. **Launch the bot:**
   ```bash
   npm start
   ```

## 🤖 Available Commands
- `/start` — Initializes a new scraping worker thread, collects live information from Cisco, and delivers files sequentially.
- `/stop` — Gracefully halts an active scraping worker cycle.

## 📝 License
This project is open-source and available under the [MIT License](LICENSE).
