web: npm start
git clone https://github.com/bartzlee48-rgb/repository-name.git
cd repository-name
https://github.com/bartzlee48-rgb/repository-name.git
npm start
const { default: makeWASocket, useMultiFileAuthState } = require('@whiskeysockets/baileys');
const fs = require('fs');
const path = require('path');

async function startBot() {
  const { state, saveCreds } = await useMultiFileAuthState('auth_info_baileys');
  
  const sock = makeWASocket({
    auth: state,
    printQRInTerminal: true
  });

  sock.ev.on('connection.update', (update) => {
    const { connection, lastDisconnect } = update;
    if (connection === 'close') {
      const shouldReconnect = (lastDisconnect?.error)?.output?.statusCode !== 401;
      if (shouldReconnect) {
        startBot();
      }
    } else if (connection === 'open') {
      console.log('✅ Bot connected successfully!');
    }
  });

  sock.ev.on('creds.update', saveCreds);

  sock.ev.on('messages.upsert', async (m) => {
    console.log(JSON.stringify(m, undefined, 2));
    
    const msg = m.messages[0];
    if (!msg.message) return;
    
    // Echo bot example
    await sock.sendMessage(msg.key.remoteJid, { text: 'Echo: ' + msg.message.conversation });
  });
}

startBot().catch(err => console.error('Bot error:', err));
npm install @whiskeysockets/baileys @adiwajshing/keyed-db
Node.js
node_modules/
auth_info_baileys/
*.log
.env
.DS_Store
msg.message.conversation
