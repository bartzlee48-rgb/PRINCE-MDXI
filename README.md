# PRINCE-MDXI WhatsApp Bot

A powerful WhatsApp bot built with Baileys for multi-device support.

## 🚀 Quick Start

### Prerequisites
- Node.js (v14 or higher)
- npm or yarn

### Installation

```bash
mkdir whatsapp-bot
cd whatsapp-bot
npm init -y
npm install @whiskeysockets/baileys @adiwajshing/keyed-db
```

### Running the Bot

```bash
npm start
```

The bot will display a QR code in the terminal. Scan it with your WhatsApp to authenticate.

## ✨ Features

- ✅ Multi-device support
- ✅ Automatic message echo
- ✅ Automatic reconnection
- ✅ Session persistence
- ✅ Message handling

## ⚙️ Configuration

Edit `bot.js` to customize:
- Message responses
- Bot commands
- Connection settings
- Event handlers

## 🌐 Deployment

The `Procfile` is configured for deployment:

```bash
git push heroku main
```

## 📝 License

MIT

---

**For more info, see the original PRINCE-MDXI repository**
