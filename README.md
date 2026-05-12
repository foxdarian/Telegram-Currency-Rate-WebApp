# Telegram Currency Rate WebApp

An asynchronous Telegram Mini App for real-time currency conversion. Users can select currencies and amounts through an interactive web interface, then get instant exchange rates. Built with modern Python async stack and external API integration.

![Python](https://img.shields.io/badge/Python-3.8%2B-blue?style=for-the-badge&logo=python)
![aiogram](https://img.shields.io/badge/aiogram-v3.0%2B-blue?style=for-the-badge&logo=telegram)
![httpx](https://img.shields.io/badge/httpx-async-blue?style=for-the-badge&logo=python)
![License](https://img.shields.io/badge/License-MIT-green?style=for-the-badge)

## 🛠️ Tech Stack

- **aiogram** — modern asynchronous framework for Telegram bots
- **httpx** — async HTTP client for API requests
- **python-dotenv** — environment variable management
- **ExchangeRate-API** — free currency conversion API

## 🚀 Installation

### 1. Clone the repository

```bash
git clone https://github.com/your-username/telegram-currency-rate-webapp.git
cd telegram-currency-rate-webapp
```

### 2. Create a virtual environment (recommended)

```bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```

### 3. Install dependencies

```bash
pip install -r requirements.txt
```

### 4. Configure environment variables

Create a `.env` file in the project root:

```env
TOKEN=your_telegram_token_from_botfather
WEB_APP_URL=https://your-webapp-url.com/index.html
```

> 💡 **How to get a token?**
> 1. Open Telegram and find the **@BotFather** bot
> 2. Send the `/newbot` command
> 3. Follow the instructions and copy your token

> 🌐 **How to host the WebApp?**
> - Upload `index.html` to a web server
> - Use free hosting like GitHub Pages or Vercel
> - Update `WEB_APP_URL` with your hosted URL

### 5. Run the bot

```bash
python main.py
```

## 📱 Usage

1. Open Telegram and find your bot
2. Send `/start` to get the WebApp button
3. Click "Open WebApp" to launch the currency converter
4. Select "From" and "To" currencies
5. Enter the amount to convert
6. Click "Get Exchange Rate" to send data back to the bot
7. Bot will reply with the converted amount

Example interaction:
```
/start
[Bot sends button: Open WebApp]
[User clicks button → WebApp opens]
[User selects USD to EUR, amount 100]
[User clicks Get Exchange Rate]
[Bot replies: 100 USD = 85.50 EUR]
```

## 🏗️ Project Structure

```
telegram-currency-rate-webapp/
├── main.py              # Main bot file
├── handlers/
│   └── routes.py        # Command handlers and WebApp data processing
├── middleware/
│   └── rate_limit.py    # Rate limiting middleware
├── index.html           # Telegram Mini App interface
├── README.md            # This file
├── requirements.txt     # Project dependencies
├── .env.example         # Example environment variables
└── .gitignore           # Git ignore rules
```

## 📖 Documentation

- [aiogram Documentation](https://docs.aiogram.dev/)
- [Telegram Bot API](https://core.telegram.org/bots/api)
- [Telegram Mini Apps](https://core.telegram.org/bots/webapps)
- [ExchangeRate-API](https://www.exchangerate-api.com/docs)
- [httpx Documentation](https://www.python-httpx.org/)

## 📄 License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
