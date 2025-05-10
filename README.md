# 📥 Multi Downloader Module by Rerezz

Modul downloader Node.js untuk berbagai platform populer seperti TikTok, YouTube (mp3/mp4), Instagram, Facebook, CapCut, Mediafire, Google Drive, dan GitHub. Semua data diambil dari endpoint API pribadi milik Rerezz.

## 🚀 Instalasi

```bash
npm install axios
```
Lalu import modul ini ke project kamu:

javascript
Salin
Edit
const {
  tiktokdl,
  ytmp3,
  ytmp4,
  igdl,
  fbdl,
  capcutdl,
  mfdl,
  gdrive,
  gitclone
} = require('./downloader'); // Ganti sesuai path file kamu
🔐 API Key
Semua endpoint membutuhkan API key yang valid. Tambahkan sebagai parameter kedua pada setiap fungsi.

📦 Fungsi dan Contoh Penggunaan
1. tiktokdl(url, apikey)
Download video TikTok tanpa watermark.

js
Salin
Edit
const data = await tiktokdl('https://vt.tiktok.com/xxxx', 'your-api-key');
console.log(data);
2. ytmp3(url, apikey)
Download audio dari YouTube.

js
Salin
Edit
const data = await ytmp3('https://www.youtube.com/watch?v=xxxx', 'your-api-key');
console.log(data);
3. ytmp4(url, qual, apikey)
Download video dari YouTube.

qual: kualitas video (contoh: 360, 720, dll)

js
Salin
Edit
const data = await ytmp4('https://www.youtube.com/watch?v=xxxx', '360', 'your-api-key');
console.log(data);
4. igdl(url, apikey)
Download media dari Instagram (feed, reels, story).

js
Salin
Edit
const data = await igdl('https://www.instagram.com/reel/xxxx', 'your-api-key');
console.log(data);
5. fbdl(url, apikey)
Download video dari Facebook.

js
Salin
Edit
const data = await fbdl('https://www.facebook.com/watch/?v=xxxx', 'your-api-key');
console.log(data);
6. capcutdl(url, apikey)
Ambil informasi dan video dari CapCut Template.

js
Salin
Edit
const data = await capcutdl('https://www.capcut.com/t/Zxxxx', 'your-api-key');
console.log(data);
7. mfdl(url, apikey)
Download file dari Mediafire.

js
Salin
Edit
const data = await mfdl('https://www.mediafire.com/file/xxxx/file', 'your-api-key');
console.log(data);
8. gdrive(url, apikey)
Ambil file dari Google Drive (public sharing only).

js
Salin
Edit
const data = await gdrive('https://drive.google.com/file/d/xxxx/view', 'your-api-key');
console.log(data);
9. gitclone(url, apikey)
Ambil link ZIP dari repo GitHub.

js
Salin
Edit
const data = await gitclone('https://github.com/user/repo', 'your-api-key');
console.log(data);
⚠️ Error Handling
Setiap fungsi akan throw Error jika ada masalah seperti:

Invalid URL atau API key

Format URL tidak didukung

Response dari API tidak sesuai

Gunakan try-catch:

js
Salin
Edit
try {
  const data = await tiktokdl(url, apikey);
  console.log(data);
} catch (err) {
  console.error(err.message);
}
📬 Kontak
Dikembangkan oleh Rerezz Official
📫 Telegram: @rerezzdev
🌐 API: https://www.decode.im-rerezz.xyz

📄 Lisensi
