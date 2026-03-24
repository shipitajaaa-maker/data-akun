fetch('https://jsonplaceholder.typicode.com/users')
.then(response => response.json())
.then(data => console.log(JSON.stringify(data, null, 2)))
.catch(error => console.error(error));

["access_token","cdn_override"]

https://github.com/shipitajaaa-maker/data-akun

https://github.com/shipitajaaa-maker/data-akun/blob/main/README.md

fetch('https://api.example.com/data', {
  headers: {
    'Authorization': 'Bearer TOKEN_KAMU'
  }
})

fetch('https://jsonplaceholder.typicode.com/users')
API_KEY=xxxxxxx
ACCESS_TOKEN=xxxxxxx
id_rsa.pub
id_rsa
. 
const fs = require('fs');
const path = require('path');

const filePath = './messages/inbox/chat/message_1.json';

// cek file ada atau tidak
if (!fs.existsSync(filePath)) {
  console.error('❌ File tidak ditemukan:', filePath);
  process.exit(1);
}

// baca & parse JSON
let data;
try {
  data = JSON.parse(fs.readFileSync(filePath, 'utf8'));
} catch (err) {
  console.error('❌ Gagal parse JSON:', err.message);
  process.exit(1);
}

// cek struktur data
if (!data.messages) {
  console.error('❌ Format JSON tidak valid');
  process.exit(1);
}

// tampilkan pesan
data.messages
  .sort((a, b) => a.timestamp_ms - b.timestamp_ms)
  .forEach(msg => {
    const sender = msg.sender_name || 'Unknown';
    const text = msg.content || '[Pesan non-teks]';
    const date = new Date(msg.timestamp_ms).toLocaleString();

    console.log(`${date} - ${sender}: ${text}`);
  });












const fs = require('fs');
const path = require('path');

// 🔥 GANTI ini sesuai folder kamu
const folder = './messages/inbox';

// ambil semua folder chat
fs.readdirSync(folder).forEach(chatFolder => {
  const chatPath = path.join(folder, chatFolder);

  // cek apakah folder
  if (fs.lstatSync(chatPath).isDirectory()) {

    // baca semua file JSON di dalamnya
    fs.readdirSync(chatPath).forEach(file => {
      if (file.endsWith('.json')) {

        const filePath = path.join(chatPath, file);
        const data = JSON.parse(fs.readFileSync(filePath, 'utf8'));

        if (!data.messages) return;

        data.messages
          .sort((a, b) => a.timestamp_ms - b.timestamp_ms)
          .forEach(msg => {
            const sender = msg.sender_name || 'Unknown';
            const text = msg.content || '[Non-text]';
            const date = new Date(msg.timestamp_ms).toLocaleString();

            console.log(`${date} - ${sender}: ${text}`);
          });
      }
    });

  }
});
