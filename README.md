# 🔰 Multi Platform Downloader by Rerezz

Modul Node.js serbaguna untuk mendownload konten dari berbagai platform seperti **TikTok**, **YouTube (MP3/MP4)**, **Instagram**, **Facebook**, **CapCut**, **MediaFire**, **Google Drive**, hingga **GitHub Repo (ZIP)**.

Semua endpoint menggunakan REST API dari:  
🔗 [https://www.decode.im-rerezz.xyz](https://www.decode.im-rerezz.xyz)

---

## 📦 Instalasi

```bash
npm install axios
```

```bash
npm install decode-imrerezz
```

```
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
} = require('decode-imrerezz');

const apikey = 'YOUR APIKEY';
/* 
    AMBIL APIKEY MWLALUI WEBSITE BRIKUT 
    https://www.decode.im-rerezz.xyz
*/

tiktokdl('https://vt.tiktok.com/ZSMFgV7RB/', apikey)
.then(data => {
    console.log(data);
})
.catch(err => {
    console.error('Terjadi kesalahan:', err);
});

ytmp3('https://youtube.com/watch?v=MApD55xTFJE', apikey)
.then(data => {
    console.log(data);
})
.catch(err => {
    console.error('Terjadi kesalahan:', err);
});

ytmp4('https://youtube.com/watch?v=MApD55xTFJE', apikey)
.then(data => {
    console.log(data);
})
.catch(err => {
    console.error('Terjadi kesalahan:', err);
});
```

