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
ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAABAQC... user@V2025
ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAABAQC... user@vivoy21d
-----BEGIN OPENSSH PRIVATE KEY-----
b3BlbnNzaC1rZXktdjEAAAAABG5vbmUAAAAE...
... (panjang banget)
-----END OPENSSH PRIVATE KEY-----
cat ~/.ssh/id_rsa.pub

data.messages
  .sort((a, b) => a.timestamp_ms - b.timestamp_ms)
  .forEach(msg => {
    const sender = msg.sender_name || 'Unknown';
    const text = msg.content || '[Non-text]';
    const date = new Date(msg.timestamp_ms).toLocaleString();

    console.log(`${date} - ${sender}: ${text}`);
  });

const fs = require('fs');

// baca file JSON
const data = JSON.parse(
  fs.readFileSync('./messages/inbox/chat/message_1.json', 'utf8')
);

// urutkan dari lama ke baru + tampilkan
data.messages
  .sort((a, b) => a.timestamp_ms - b.timestamp_ms)
  .forEach(msg => {
    const sender = msg.sender_name || 'Unknown';
    const text = msg.content || '[Pesan non-teks]';
    const date = new Date(msg.timestamp_ms).toLocaleString();

    console.log(`${date} - ${sender}: ${text}`);
  });
console.log(data.messages.length);
console.log(`${date} - ${sender}: ${text}`);

